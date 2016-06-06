---
layout: chapter
title: Bubble Art
slides:

  - title: title-page
    class: title-slide

    notes: |

      In this section we will make randomised bubble artwork.

    content: |

      # Bubble Art
      _Creating piles of random bubbles_


  ##########


  - title: demo
    class: centered-slide

    notes: |

      Here's an example of something you might create.

    content: |

      ## Bubble Art Demo

      <iframe height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/PPPPaN/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/PPPPaN/'>Randomised Bubble Art</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      You can create something like this but with your own theme


  ##########


  - title: startercode
    class: centered-slide

    notes: |

      Open up `bubbleart.html` in your code editor.

    content: |

      ## Code Your Own

      Create a new file called `bubbleart.html` and paste in this code:
      
      <iframe height='450' scrolling='no' src='//codepen.io/gatherworkshops/embed/OybELP/?height=450&theme-id=19418&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/OybELP/'>Bubble Art Starter Code</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      You will need to click and drag to scroll and get it all!


  ##########


  - title: containercss
    class: centered-slide

    notes: |

      We have already added a little bit of CSS to make it easier to get started.

    content: |

      ## Bubble Box

      In your HTML there is already a container:

      ```html
      <div id="bubbleBox">
      </div>
      ```

      And some CSS for it:

      ```css
      #bubbleBox {
        height: 100vh;
        width: 100vw;
        position: relative;
        overflow: hidden;
        background-color: lightblue;
      }

      ```

      You should already see this code in bubbleart.html
      {:.checkpoint}


  ##########


  - title: bubblecss
    class: centered-slide

    notes: |

      We have already added a little bit of CSS to make it easier to get started.

    content: |

      ## Designing a Bubble

      In your CSS, create a class called `bubble`:

      ```css
      .bubble {
        width: 50px;
        height: 50px;
        border-style: solid;
        border-width: 2px;
        border-radius: 50%; 
        border-color: black;
        background-color: white;
      }

      ```

      In your HTML, inside your `bubbleBox`, add a bubble:

      ```html
      <div id="bubbleBox">
      <div class="bubble"></div>
      </div>
      ```

      You should see a white circle with a black border.
      {:.checkpoint}


  ##########


  - title: bubblecolours
    class: centered-slide

    notes: |

      We can also change the colour of our bubble by changing the
      background and border colours.

    content: |

      ## Designing A Bubble

      You can also make the background and border colours see-through:

      ```css
      .bubble {
        width: 50px;
        height: 50px;
        border-style: solid;
        border-width: 2px;
        border-radius: 50%; 
        border-color: rgba( 255, 255, 255, 0.2);
        background-color: rgba( 255, 255, 255, 0.2);
      }
      ```
      {:data-line="7-8"}

      Remix to make any colour you like.


  ##########


  #- title: rgbacolours
  #  class: centered-slide
  #
  #  notes: |
  #
  #    See-through colours are made by mixing together red, green and blue.
  #
  #    Once we have a colour we can also change how see-through that colour is.
  #
  #  content: |
  #
  #    ## See-through Colours
  #
  #    <iframe height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/ojjexg/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/ojjexg/'>RGBA Colour Picker</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
  #    </iframe>


  ##########


  - title: creatingbubbleswithjquery
    class: centered-slide

    notes: |

      Once you are happy with your bubble design, delete the hard-coded one from your HTML.

    content: |

      ## Delete your bubble HTML

      Once you are happy with how your bubble looks,<br>
      delete it from your bubbleBox:

      ```html
      <div id="bubbleBox">
      </div>
      ```

      We will make it again, but using jQuery.

      Your bubble box should be empty again.
      {:.checkpoint}    


  ##########


  - title: createbubblefunction
    class: centered-slide

    notes: |

      All our code for creating a bubble will be grouped together.

      It will be grouped inside a function.

      This helps us to easily find the code we are looking for,
      know what it does, and use it over and over without copying
      and pasting.

    content: |

      ## CreateBubble Function

      Make a new function which will create a bubble:

      ```javascript
      function createBubble() {

        // code to create a bubble goes here

      }
      ```


  ##########


  - title: createbubble
    class: centered-slide

    notes: |

      Create a bubble and put it on the screen.

    content: |

      ## Create A Bubble

      Inside your createBubble function:

      ```javascript
      function createBubble() {
      var bubble = $('<div>');
      bubble.addClass('bubble');
      bubble.appendTo('#bubbleBox');
      }
      ```
      {:data-line="2-4"}


  ##########


  - title: runbubblefunction
    class: centered-slide

    notes: |

      :)

    content: |

      ## Run the Function

      Run the `createBubble` function:

      ```javascript
      function createBubble() {
      var bubble = $('<div>');
      bubble.addClass('bubble');
      bubble.appendTo('#bubbleBox');
      }

      createBubble();
      ```
      {:data-line="7"}

      You should see your bubble in the box again.
      {:.checkpoint}


  ##########


  - title: swarming
    class: centered-slide

    notes: |

      Now, we can create a whole swarm by repeating the same
      piece of code over and over.

    content: |

      ## Create a Swarm

      Now that we've got code to make one bubble,<br>
      we can easily make more using a loop:

      ```javascript
      var numberOfBubbles = 0;
      while( numberOfBubbles < 20 ) {
        createBubble();
        numberOfBubbles = numberOfBubbles + 1;
      }

      ```
      {:data-line="1-2,4-5"}



  ##########


  - title: identicalbubbles
    class: centered-slide

    notes: |

      Where are all the bubbles?

    content: |

      ## Where are all the bubbles?

      We made 20 bubbles, but we can still only see one.

      **They are all identical!** They are the same size and they are in the same place, stacked on top of each other.

      We need to move them so they don't overlap.


  ##########


  - title: bubbleposition
    class: centered-slide

    notes: |

      We can also change the position of our bubble

    content: |

      ## Bubble Position

      We can also change the position of our bubbles:

      ```javascript
      function createBubble() {
      var bubble = $('<div>');
      bubble.addClass('bubble');

      var leftSpace = 300;
      bubble.css('left', leftSpace);
    
      var topSpace = 300;
      bubble.css('top', topSpace);

      bubble.appendTo('#bubbleBox');
      }
      ```
      {:data-line="5-9"}

      Your bubbles should now be stacked in a different place.
      {:.checkpoint}


  ##########


  - title: randomnumbers
    class: centered-slide

    notes: |

      Generating a random number always follows the same format.

    content: |

      ## Random Numbers

      ```javascript
      var randomNumber = Math.random() * howMany;

      ```

      **var randomNumber** : The variable to store the random number
      **Math.random()** : Creates a random number between 0 and 1
      **howMany** : How many numbers to choose between.


  ##########


  - title: randomposition
    class: centered-slide

    notes: |

      We can use a random number creator to make our bubble show up
      in a different place each time we refresh the page.

    content: |

      ## Random Bubble Position

      Randomly position your bubbles:

      ```javascript
      var leftSpace = Math.random() * 300;
      bubble.css('left', leftSpace);
    
      var topSpace = Math.random() * 300;
      bubble.css('top', topSpace);
      ```
      {:data-line="1, 4"}

      Your bubbles should now be all in different places.
      {:.checkpoint}


  ##########


  - title: smartpositioning
    class: centered-slide

    notes: |

      We can also change the position of our bubble

    content: |

      ## Smarter Positioning

      We could even make our random numbers<br>
      based on the size of the bubble box:

      ```javascript
      var leftSpace = Math.random() * $('#bubbleBox').width();
      bubble.css('left', leftSpace);
    
      var topSpace = Math.random() * $('#bubbleBox').height();
      bubble.css('top', topSpace);
      ```
      {:data-line="1, 4"}

      Your bubbles should now be all around the box.
      {:.checkpoint}


  ##########


  - title: bubblesize
    class: centered-slide

    notes: |

      The default bubble size is set in the CSS, but we can also
      change it using jQuery.

    content: |

      ## Bubble Size

      Change the size of your bubbles using jQuery:

      ```javascript
      var leftSpace = Math.random() * $('#bubbleBox').width();
      bubble.css('left', leftSpace);
    
      var topSpace = Math.random() * $('#bubbleBox').height();
      bubble.css('top', topSpace);

      var size = 200;
      bubble.css('width', size);
      bubble.css('height', size);
      ```
      {:data-line="7-10"}

      Your bubbles should now be bigger.
      {:.checkpoint}


  ##########


  - title: randomsize
    class: centered-slide

    notes: |

      We can also randomise the size of our bubble.

    content: |

      ## Random Sizing

      We can use the same random number trick as before<br>
      to make our bubbles all different sizes:

      ```javascript
      var size = Math.random() * 200;
      bubble.css('width', size);
      bubble.css('height', size);

      ```
      {:data-line="1"}

      Your bubbles should now be all different sizes.
      {:.checkpoint}


  ##########


  - title: challenge
    class: centered-slide

    notes: |

      See if you can theme your bubble art in a unique and interesting way.

    content: |

      ## Challenge: Themed Bubble Art

      Give your bubble art a unique and creative theme.


  ##########


  - title: summary
    class: centered-slide

    notes: |

      Congratulations! You've made another jQuery app!

      Through this chapter you have learned about:

      - Creating elements using jQuery
      - Using functions to group code together
      - Running code over and over using loops
      - Generating random numbers
      - Changing an element's CSS using jQuery

      Well done :)

    content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){:height="200"}

      ## Bubble Art: Complete

      Fabulous! Now let's make those bubbles dance...

      [Take me to the next chapter!](animation.html)

---







