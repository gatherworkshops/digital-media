---
layout: default
title: Gamification
slides:

  - title: title-page
    class: title-slide

    notes: |

      In this section we will make our randomised bubble artwork into a game.

    content: |

      # Gamification
      _Turning your bubble popper into a game_


  ##########


  - title: demo
    class: centered-slide

    notes: |

      Here's an example of something you might create.

    content: |

      ## Animation Demo

      <iframe height='500' scrolling='no' src='//codepen.io/gatherworkshops/embed/KdNmLe/?height=500&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/KdNmLe/'>Animated Bubble Art</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      Try clicking a bubble or pressing spacebar.


  ##########


  - title: bubblecounter
    class: centered-slide

    notes: |

      Display how many bubbles have been popped.

    content: |

      ## Bubble Counter

      You'll need a little bit of extra HTML:

      ```html
      <div id="bubbleCounter">0</div>
      ```

      And some CSS to design it:

      ```css
      #bubbleCounter {
      background-color: white;
      position: absolute;
      top: 0;
      left: 0;
      }
      ```

      You should be able to see the bubble counter.
      {:.checkpoint}


  ##########


  - title: livebubblecounter
    class: centered-slide

    notes: |

      :)

    content: |

      ## Live Updating Bubble Counter

      Every time a bubble is popped, you'll need to track it and display it.

      ```javascript
      var bubblesPopped = 0;

      function popBubble() {
      var bubble = $(this);
      bubble.remove();

      bubblesPopped = bubblesPopped + 1;

      var bubbleCounter = $('#bubbleCounter');
      bubbleCounter.textContent = bubblesPopped;
      }
      ```
      {:data-line="1, 7, 9-10"}

      Your counter should update when a bubble is popped.
      {:.checkpoint}


  #########


  - title: countdowntimer
    class: centered-slide

    notes: |

      :)

    content: |

      ## Countdown Timer

      You'll need a little bit of extra HTML:

      ```html
      <div id="countdownTimer">60</div>
      ```

      And some CSS to design it:

      ```css
      #countdownTimer {
      background-color: white;
      position: absolute;
      top: 0;
      right: 0;
      }
      ```

      You should be able to see the countdown timer.
      {:.checkpoint}


  ##########


  - title: livecountdowntimer
    class: centered-slide

    notes: |

      :)

    content: |

      ## Live Countdown Timer

      Every second, we want to update the countdown timer:

      ```javascript
      var secondsRemaining = 60;
      var timer = setInterval(minusOneSecond, 1000);

      function minusOneSecond() {
      secondsRemaining = secondsRemaining - 1;

      var timerDisplay = $('#countdownTimer');
      timerDisplay.textContent = secondsRemaining;
      }
      ```

      Your timer should count down to zero... and beyond?
      {:.checkpoint}


  ##########


  - title: stoppingthetimer
    class: centered-slide

    notes: |

      :)

    content: |

      ## Stopping The Timer

      When we get to zero, we want to stop the timer:

      ```javascript
      function minusOneSecond() {
      
      if( secondsRemaining == 0 ) {
      window.clearInterval( timer );
      }

      else {
      secondsRemaining = secondsRemaining - 1;

      var timerDisplay = $('#countdownTimer');
      timerDisplay.textContent = secondsRemaining;
      }
      }
      ```
      {:data-line="3-7, 12"}

      Your timer should now stop at zero.
      {:.checkpoint}


  ##########


  - title: scoredisplay
    class: centered-slide

    notes: |
      :)

    content: |

      ## Challenge: Score Display

      When the timer runs out, display the person's score
      in a big box with big text.
      

  ##########


  - title: summary
    class: centered-slide

    notes: |

      Good work. Now you have even made a game :)

      Well done :)

    content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){:height="200"}

      ## Gamification: Complete

      Good work! Now you know how to jQuery All Of The Things!


---
