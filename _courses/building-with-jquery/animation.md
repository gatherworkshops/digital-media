---
layout: chapter
title: Animation
slides:

  - title: title-page
    class: title-slide

    notes: |

      :)

    content: |

      # Animation
      _Moving stuff with jQuery_


  ##########


  - title: demo
    class: centered-slide

    notes: |

      Here's an example of something you might create.

    content: |

      ## Animation Demo

      <iframe height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/KdNmLe/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/KdNmLe/'>Animated Bubble Art</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      You can create something like this but with your own theme


  ##########


  - title: startingmovement
    class: centered-slide

    notes: |

      When the page loads we want the bubbles
      to move.

      To move the bubbles, we need a reference to all the bubbles.

      Once we have all the bubbles, we can run the function on them.

    content: |

      ## Make The Bubbles Move

      You'll need a function that knows how to move one bubble:

      ```javascript
      function moveBubble() {

        // code to move a single bubble goes here

      }

      ```

      And you'll also need to run the function for every bubble:


      ```javascript
      var allBubbles = $('.bubble');
      allBubbles.each( moveBubble );
      ```


  ##########


  - title: movebubble
    class: centered-slide

    notes: |

      We said that each bubble should be run with the moveBubble function.

      When we have a whole set of things and we run 
      a function on each one individually, inside the
      function we can get the bubble using the keyword
      "this".

      Inside the function "this" means "this bubble".

    content: |

      ## Identifying a Single Bubble

      ```javascript
      function moveBubble() {

        var bubble = $(this);

      }
      ```
      {:data-line="3"}


  ##########


  - title: newposition
    class: centered-slide

    notes: |

      Inside this function, we need to decide on some new
      CSS values for our bubble.

      Once we have new values, we can animate a slow change
      from the old values to the new values.

    content: |

      ## New Bubble Position

      ```javascript
      function moveBubble() {

      var bubble = $(this);

      var leftSpace = Math.random() * container.width();
      var topSpace = Math.random() * container.height();

      }
      ```
      {:data-line="5-6"}

      
  ##########


  - title: animatingposition
    class: centered-slide

    notes: |

      Inside this function, we need to decide on some new
      CSS values for our bubble.

      Once we have new values, we can animate a slow change
      from the old values to the new values.

    content: |

      ## New Bubble CSS


      ```javascript
      function moveBubble() {

      var bubble = $(this);

      var leftSpace = Math.random() * container.width();
      var topSpace = Math.random() * container.height();
    
      var newCSS = {
        'left': leftSpace,
        'top': topSpace
      }

      bubble.animate( newCSS, 5000 );

      }
      ```
      {:data-line="8-13"}

      Your bubbles should now move when you refresh.
      {:.checkpoint}


  ##########


  - title: animatingsize
    class: centered-slide

    notes: |

      You can also change the size.

      Create another variable to calculate the new width and height,
      then add that to the animation set.

    content: |

      ## Animating Size

      Add a new size to your animation:

      ```javascript
      var leftSpace = Math.random() * container.width();
      var topSpace = Math.random() * container.height();
      var size = Math.random() * 200;
    
      var newCSS = {
        'left': leftSpace,
        'top': topSpace,
        'width': size,
        'height': size
      }
      ```
      {:data-line="3, 8-9"}
   

      Your bubbles should now move and change size.
      {:.checkpoint}


  - title: randomanimationlength
    class: centered-slide

    notes: |

      At the moment, all our bubbles take 5 seconds to
      animate from their old CSS values to their new
      values.

      We can use a random number generator to have each
      bubble take a different amount of time to animate.

    content: |

      ## Animation time

      ```javascript
      var animationTime = Math.random() * 10000 + 5000;
      bubble.animate( newCSS, animationTime );

      ```



  - title: moveforever
    class: centered-slide

    notes: |

      We can also make our bubbles animate forever.

      We do this by waiting until the end of the animation,
      and then running the bubble through `moveBubble` all
      over again.

    content: |

      ## Floating forever

      ```javascript
      bubble.animate( newCSS, animationTime, moveBubble );

      ```


  ##########


  - title: challenge
    class: centered-slide

    notes: |

      See if you can change your animations to match your theme.

    content: |

      ## Challenge: Themed Animations

      Give your animations a personal twist.


  ##########


  - title: summary
    class: centered-slide

    notes: |

      Great, now you can do animations too!

      Through this chapter you have learned about:

      - Getting a group of elements by their class
      - Running a function on every element in a group
      - Storing CSS values in JavaScript Objects
      - Animating CSS from old to new values
      - Looping CSS animations

      Well done :)

    content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){:height="200"}
      
      ## Animations: Complete

      Woohoo, animations! But what about interactions...

      [Take me to the next chapter!](interaction.html)


---
