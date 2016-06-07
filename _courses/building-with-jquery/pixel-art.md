---
layout: default
title: Pixel Art
slides:

  - title: title-page
    section: pixelart
    class: title-slide

    notes: |

      In this section we will make a pixel art drawing board.

    content: |

      # Pixel Art
      _Clicking elements and changing their classes_


  ##########


  - title: pixels
    class: centered-slide

    notes: |

      All digital images are made up of pixels.

      We talk about cameras having a certain number of "megapixels". A megapixel is a _million_ pixels!

    content: |

      ## All Digital Images Are Made Of Pixels

      ![Close-up of the pixels in a photograph](assets/images/photo-pixels.jpg)

      Most images contain millions of pixels


  ##########


  - title: aboutpixelart
    class: centered-slide

    notes: |

      Although all images are made up of pixels, when we talk about "pixel art" 
      we mean images where the artist has drawn each pixel.

      In pixel art, there is usually a limited number of colours and sometimes
      the image is displayed bigger, so that each "pixel" block is plainly visible.

      Pixel art can be scaled down very small and still be recognisable. 

    content: |

      ## Pixel Art

      ![Pixel Art: Mario, Luigi, Peach and Toad by Hama-Girl](assets/images/mario-pixel-art.png){:height="350"}

      In "pixel art" the artist draws each individual pixel

      
  ##########


  - title: paperpixels
    class: centered-slide

    notes: |

      Design a picture or pattern by colouring in whole squares in only black.

    content: |

      ## Black and White Pixel Art

      ![Black and white pixel art](assets/images/black-and-white-examples.gif)

      What can you create using only a hundred pixels?


  ##########


  - title: blackandwhitedemo
    section: pixelart
    class: centered-slide

    notes: |

      Here is an example of the pixel art drawing board we will be creating.

    content: |

      ## Pixel Art Demo

      <iframe width='500' height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/qOOBmL/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/qOOBmL/'>Black and White Pixel Art Demo</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.</iframe>

      Click a pixel to change it between black and white.


  ##########


  - title: codeyourown
    class: centered-slide

    notes: |

      Let's get started building our own!

    content: |

      ## Code Your Own

      Create a new file called `pixelart.html` and paste in this code:
      
      <iframe height='520' scrolling='no' src='//codepen.io/gatherworkshops/embed/epBrwG/?height=520&theme-id=19418&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/epBrwG/'>Pixel Art Starter HTML</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>


  ##########


  - title: drawingboard
    class: centered-slide

    notes: |

      The first thing we need is the drawing board.

      Our drawing board will be a white box with a solid border.

    content: |

      ## Create the Drawing Board

      Between your `style` tags, describe how the board should look:

      ```css
      .drawingBoard {
        width: 300px;
        height: 300px;
        border-style: solid;
      }
      ```

      Between your `body` tags, add the drawing board div:

      ```html
      <div class="drawingBoard">
      </div>
      ```

      You should see an empty box on your page.
      {:.checkpoint}


  ##########


  - title: boardposition 
    class: centered-slide

    notes: |

      We can also put the board in the middle of the page.

      Because our drawing board is a div, it is a "block" element.

      Block elements can be horizontally positioned using their margins.

      By setting the left margin and right margin to both be `auto`,
      the board will automatically use the same amount of spacing on
      both the left and the right sides.

      Unfortunately this doesn't work for vertical positioning!

    content: |

      ## Drawing Board Positioning

      Modify your `drawingBoard` style to center the board:

      ```css
      .drawingBoard {
        width: 300px;
        height: 300px;
        border-style: solid;
        margin-left: auto;
        margin-right: auto;
      }
      ```
      {: data-line="5-6" }

      Your box should now be in the middle of the page.
      {:.checkpoint}


  ##########


  - title: pixelboxes
    class: centered-slide

    notes: |

      Next we need to create our pixels.

      Each "pixel" will be an empty box with a subtle border.

      For this particular drawing board, we will have a 10x10
      grid, making up a total of 100 pixels.

      To fit 10 boxes across, the width of each pixel will need
      to be 10% of the drawing board's width.

      To fit 10 boxes down, the pixel height will also need to
      be 10% of the board's height.

    content: |

      ## Creating the Pixels

      Between your `style` tags, describe how each pixel should look:

      ```css
      .pixel {
        width: 10%;
        height: 10%;
        border-style: solid;
        border-width: 1px;
        border-color: rgba(0,0,0,0.1);
      }
      ```

      Between your `drawingBoard` tags, create 100 pixel divs:

      ```html
      <div class="pixel"></div>
      ```

      You should have pixels going off the bottom of your page :/
      {:.checkpoint}


  ##########


  - title: stackingpixels
    class: centered-slide

    notes: |

      We've now got all the pixels we need, but they go for miles off
      the bottom of the page.

      This is because each pixel is a `block` element, and block elements
      take up a whole line of their own by default, forcing anything after
      them to go to the next line.

      We can fix this by using a `flex` layout. Boxes with `flex` enabled
      can have other boxes inside which easily stack against each other.

    content: |

      ## Stacking Pixels

      Modify your `drawingBoard` to use a flex layout:

      ```css
      .drawingBoard {
        width: 300px;
        height: 300px;
        border-style: solid;
        margin-left: auto;
        margin-right: auto;
        display: flex;
        flex-wrap: wrap;
      }
      ```
      {:data-line="7-8"}

      Your pixels should now be stacked in your board.
      {:.checkpoint}


  ##########


  - title: smallerborders
    class: centered-slide

    notes: |

      We now have borders between our pixels which are 2px wide, when we
      only wanted 1px.

      This is because each pixel box has a 1px border, so putting them right next
      to each other makes 2px between each box in total.

      We can selectively hide the border for two sides of each pixel box,
      to make the dividers appear as only 1px wide.

    content: |

      ## Smaller Borders

      Modify your `pixel` class to only use bottom and right borders:

      ```css
      .pixel {
        width: 10%;
        height: 10%;
        border-style: solid;
        border-width: 1px;
        border-color: rgba(0,0,0,0.1);
        border-top: 0;
        border-left: 0;
      }
      ```
      {:data-line="7-8"}

      You should now have thinner borders on each pixel box.
      {:.checkpoint}


  ##########


  - title: getpixels
    class: centered-slide

    notes: |

      The objects on the page we want to be working with are 
      the pixels, so our first step is to use jQuery to identify
      all of the pixels in our box.

    content: |

      ## Get Those Pixels

      Between your `script` tags, get all the pixels:

      ```javascript
      var allPixels = $('.pixel');
      alert( allPixels.length );
      ```

      Refresh, and you should see a pop-up which says "100".
      {:.checkpoint}


  ##########


  - title: whitepixels
    class: centered-slide

    notes: |

      When we first load the page, we want all the pixel to be white.

    content: |

      ## White Pixels

      Create a new CSS class called `white`:

      ```css
      .white {
        background-color: white;
      }
      ```

      Instead of the alert, add the class `white` to every pixel:
      ```javascript
      var allPixels = $('.pixel');
      allPixels.addClass('white');
      ```
      {:data-line="2"}


  ##########


  - title: clicklistener
    class: centered-slide

    notes: |

      Using jQuery, we can quickly and easily tell our code to
      look out for someone clicking an object on the page.

      Because we already have a variable containing all the pixels,
      we can add a "click listener" to the variable, and that will
      apply to all the pixel objects stored in the variable.

      Inside the brackets we tell the code what it is we want to
      happen when a click occurs.

      The words inside the bracket are a function name. We need to
      write some code which runs under that function name.

      To check our clicks work, we'll make our clicks show a test
      message on the screen.

      Create a function called `changeColor` and put the code to
      run between the function's curly brackets.

    content: |

      ## Wait For Clicks

      After making all pixels white, also add a click watcher:

      ```javascript
      var allPixels = $('.pixel');
      allPixels.addClass('white');
      allPixels.click(changeColor);
      ```
      {:data-line="3"}

      Leave a blank line then create the `changeColor` function:

      ```javascript
      function changeColor() {
        alert("Change the color!");
      }
      ```

      When you click pixels, you should see a popup message.
      {:.checkpoint}


  ##########


  - title: blackpixels
    class: centered-slide

    notes: |

      When we click a pixel, we want it to turn black.

      To do this, we will need to use CSS to change the background colour
      of the pixel box.

      There are a few different ways to do this, but today we'll create 
      a new class called `black` which will set the background colour 
      to black.

      When we apply the class "black" to a pixel, it will turn black.

    content: |

      ## Black Pixels

      Create a new CSS class called `black`:

      ```css
      .black {
        background-color: black;
      }
      ```

      When a pixel is clicked, remove `white` and add `black`:

      ```javascript
      function changeColor() {
        var pixel = $(this);

        pixel.removeClass('white');
        pixel.addClass('black');
      }
      ```
      {:data-line="2-5"}


  ##########


  - title: blackandwhitepixels
    class: centered-slide

    notes: |

      You can now change the colour of pixels, but what if you 
      make a mistake?

      We need a way to also change the color from black back to
      white again if you click a second time.

      Use an `if - else` statement to change the color class.

      You should then be able to change between black and white
      by clicking a pixel more than once.

    content: |

      ## Black and White Pixels

      Modify your `changeColor` function to handle both colours:

      ```javascript
      function changeColor() {
        var pixel = $(this);

        if( pixel.hasClass('white') ) {
        pixel.removeClass('white');
        pixel.addClass('black');
        }

        else if( pixel.hasClass('black') ) {
        pixel.removeClass('black');
        pixel.addClass('white');
        }
      }
      ```
      {:data-line="4-12"}

      Pixels should now change between black and white.
      {:.checkpoint}


  ##########


  - title: blackandwhitedemo2
    section: pixelart
    class: centered-slide

    notes: |

      Your pixel art drawing board should now work just like this one.

    content: |

      ## All Done!

      ![Basic Pixel Art Complete](assets/images/basic-pixel-art-complete.png){:height="400"}

      Your drawing board should now work!

      Recreate your paper-based picture and take a screenshot.
      {:.checkpoint}


  ##########


  - title: colouredpaperpixels
    class: centered-slide

    notes: |

      Design a picture or pattern by colouring in whole squares in any colour.

    content: |

      ## Colourful Pixel Art

      ![Gather Workshops Logo](assets/images/colour-examples.gif)

      What could you create with more colours?


  ##########


  - title: colourdemo
    section: pixelart
    class: centered-slide

    notes: |

      Here is an example of the pixel art drawing board we will be creating.

    content: |

      ## Coloured Pixel Art Demo

      <iframe width='500' height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/QjbVrz/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/QjbVrz/'>Coloured Pixel Art Demo</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      Click a pixel to cycle through the colour options


  ##########


  - title: addingcolours
    class: centered-slide

    notes: |

      Now how might we add more colours to our tile clicking
      options?

      The CSS has support for lots more colours, and you could
      add more if you want to.

      Adding more colours is done by adding more `else if`
      options to the `if` code we already have.


    content: |

      ## Going Full-Spectrum

      ![Gather Workshops Logo](assets/images/colour-flow.svg){:width="100%"}

      We want pixels to change to the next colour when clicked.


  #########


  - title: addingcolourscode
    class: centered-slide

    notes: |

      Add `else if` options to the `if` code you already have.


    content: |

      ## Going Full-Spectrum

      Modify your `changeColor` function to use more colours:

      ```javascript
        if( pixel.hasClass('white') ) {
        pixel.removeClass('white');
        pixel.addClass('black');
        }

        else if( pixel.hasClass('black') ) {
        pixel.removeClass('black');
        pixel.addClass('red');
        }

        else if( pixel.hasClass('red') ) {
        pixel.removeClass('red');
        pixel.addClass('white');
        }
      ```
      {: data-line="8, 11-14"}

      Your pixels should now change through more colours.
      {:.checkpoint}


  ##########


  - title: democode
    class: centered-slide

    notes: |

      Here's a demo of the final product, in case you 
      get lost and can't figure out what's going wrong!

      You can look at the HTML, CSS or JavaScript 

    content: |

      ## Demo Code

      <iframe height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/QjbVrz/?height=500&theme-id=18720&default-tab=js' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/QjbVrz/'>Coloured Pixel Art Demo</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      Change tabs between HTML, CSS and JS to look at the final code


  ##########


  - title: colourcomplete
    class: centered-slide

    notes: |

      Your pixel art drawing board should now work.

    content: |

      ## All Done!

      ![Coloured Pixel Art Complete](assets/images/basic-pixel-art-complete.png)
      {:height="400"}

      Your drawing board should now work!

      Create a colourful picture and take a screenshot.
      {:.checkpoint}


  ##########


  - title: challenge
    class: centered-slide

    notes: |

      See if you can make a higher-definition version of the grid.

    content: |

      ## High Definition Pixel Art

      ![Comparing low, medium and high resolution images](assets/images/pixel-resolution.gif)

      **Challenge:** <br>
      Make your pixel artboard able to draw 
      more detailed images.


  ##########


  - title: summary
    class: centered-slide

    notes: |

      Congratulations! You've made your first jQuery app!

      Through this chapter you have learned about:

      - Getting a group of elements in a page
      - Functions
      - Running a function when a click happens
      - Adding and removing classes

      Well done :)

    content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){:height="200"}

      ## Pixel Art: Complete

      Well done! Now let's play with some bubbles...

      [Take me to the next chapter!](bubble-art.html)


---





