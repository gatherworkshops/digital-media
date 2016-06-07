---
layout: default
title: Interaction
slides:


  - title: title-page
    class: title-slide

    notes: |

      In this section we will make stuff happen by looking out for events.

    content: |

      # Interaction
      _Reacting to clicks and key presses_


  ##########


  - title: demo
    class: centered-slide

    notes: |

      Here's an example of something you might create.

    content: |

      ## Animation Demo

      <iframe height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/KdNmLe/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/KdNmLe/'>Animated Bubble Art</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      Try clicking a bubble or pressing spacebar


  ##########


  - title: poppingbubbles
    class: centered-slide

    notes: |

      :)

    content: |

      ## Click to Pop Bubbles

      Here's a function to pop a bubble:

      ```javascript
      function popBubble() {
        var bubble = $(this);
        bubble.remove();
      }
      ```

      And how to look for a click on any bubble:
      ```javascript
      var allBubbles = $('.bubble');
      allBubbles.click(popBubble);
      ```

      Your bubbles should now disappear when clicked.
      {:.checkpoint}


  ##########


  - title: hovercolourchange
    class: centered-slide

    notes: |

      :)

    content: |

      ## Hover to Change Bubble Colour

      Here's a function to change a bubble red:

      ```javascript
      function makeBubbleRed() {
      var bubble = $(this);
      bubble.css('background-color', 'red');
      }
      ```

      And a function to change a bubble back to white:

      ```javascript
      function makeBubbleWhite() {
      var bubble = $(this);
      bubble.css('background-color', 'white');
      }
      ```

      And finally a hover watcher for all bubbles:

      ```javascript
      var allBubbles = $('.bubble');
      allBubbles.hover( makeBubbleRed, makeBubbleWhite );
      ```

      Bubble colour should change when your mouse goes over.
      {:.checkpoint}


  ##########


  - title: creatingbubbles
    class: centered-slide

    notes: |

      You've already got a `createBubble` function, <br>
      we just need to run it when spacebar is pressed.

    content: |

      ## Spacebar to Create Bubbles

      Here's a keyboard event watcher:

      ```javascript
      $(window).keyup( handleKeyUp );

      ```

      And a function which creates a bubble if the key was spacebar:

      ```javascript
      function handleKeyUp(event) {
        if(event.keyCode == 32){
          createBubble();
        }
      }
      ```

      You can find other key codes [here](http://www.asquare.net/javascript/tests/KeyCode.html)

      A new bubble should appear when you press spacebar.
      {:checkpoint}


  ##########


  - title: timerevent
    class: centered-slide

    notes: |

      :)

    content: |

      ## Timer Events


  ##########


  - title: challenge
    class: centered-slide

    notes: |

      See if you can change your interactions to match your theme.

    content: |

      ## Challenge: Interesting Interactions

      Use at least two interactions to make your animations<br>
      a bit weird or kinda funny.


  ##########


  - title: summary
    class: centered-slide

    notes: |

      Good work. Now you can do interactions too!

      Through this chapter you have learned about:

      - Click events
      - Hover events
      - Keyboard events
      - Timer events
      - Running functions when events happen

      Well done :)

    content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## Interaction: Complete

      Good work! I bet you could make a game out of this...

      [Take me to the next chapter!](gamification.html)


---
