---
layout: default
title: Timer Events
slides:

  - class: title-slide

    content: |

      # Timer Events

      _Automated events and repeating events using timers_


  ##########

  - content: |

      ## How timer events work

      - Create a **function** that runs some code
      - Create a **timer** for a number of milliseconds
      - The timer runs the function on each **timer event**


  - content: |

      ## Creating a single-run timer

      ```javascript
      var millisecondsToWait = 3000;

      function timerFinished() {
        console.log('Time\'s up!');
      }

      var timer = setTimeOut(timerFinished, millisecondsToWait);
      ```

      {:.checkpoint}
      The console says "Time's up" 3 seconds after the page loads.


  - content: |

      ## Creating a repeating timer

      ```javascript
      var timeBetweenMessages = 1000;

      function displayMessage() {
        console.log('Hello!');
      }

      var repeatingTimer = setInterval(displayMessage, timeBetweenMessages);
      ```

      {:.checkpoint}
      The console says "Hello!" every second.


  - content: |

      ## Timer use cases

      The two timers `setTimeout` and `setInterval` can be 
      used to achieve many commen effects.

      - Live-updating clock (setInterval)
      - Countdown to an event (setInterval)
      - Time limit on a game (setTimeout)
      - Automatically check for new messages (setInterval)
      - Automatic log out (setTimeout)
      - Updating a slideshow (setInterval)
      - Revealing content in steps (either)


  - content: |

      ## Example: Revealing content in steps

      We want to make these things happen:

      - Title show immediately
      - Subtitle show after 1 second
      - Images start showing after 2 seconds
      - Images appear only 0.2 seconds apart


  - content: |

      ## Step One: Hide everything

      ```javascript
      .hidden {
        opacity: 0;
      }
      ```

      ```html
      <h1 id="title" class="hidden">Magic Show</h1>
      ```

      Add the `hidden` class to all the elements 
      we want to animate.

      {:.checkpoint}
      All my elements are hidden in the browser.


  - content: |

      ## Step Two: Show the title immediately

      ```javascript
      var title = document.getElementById('title');
      title.classList.removeClass('hidden');
      ```

      {:.checkpoint}
      My title has come back in the browser.


  - content: |

      ## Step Three: <br> Show the subtitle after 1 second

      ```javascript
      var subtitle = document.getElementById('subtitle');
      var subtitleDelay = 1000;

      function showSubtitle() {
        subtitle.classList.removeClass('hidden');
      }

      setTimeout(showSubtitle, subtitleDelay);
      ```

      {:.checkpoint}
      My subtitle shows up after 1 second.


  - content: |

      ## Step Four: <br> Show the images after 2 seconds

      ```javascript
      var images = document.getElementsByClass('circleImage');

      for( var imageNum=0; imageNum < images.length; imageNum++) {
        var image = images[imageNum];
        var imageDelay = 2000;

        function showImage() {
          image.classList.removeClass('hidden');
        }

        var imageTimer = setTimeout(showImage, imageDelay);
      }
      ```

      {:.checkpoint}
      My images show up after 2 seconds.


  - content: |

      ## Step Five: <br> Show the images in sequence

      ```javascript
      var images = document.getElementsByClass('circleImage');

      for( var imageNum=0; imageNum < images.length; imageNum++) {
        var image = images[imageNum];
        var extraDelay = imageNum * 0.2;
        var imageDelay = 2000 + extraDelay;

        function showImage() {
          image.classList.removeClass('hidden');
        }

        var imageTimer = setTimeout(showImage, imageDelay);
      }
      ```

      {:.checkpoint}
      My images show up one after another.
  

  - content: |

      ## Bonus: Fading in content

      ```css
      .circleImage {
        opacity: 1;
        transition-property: opacity;
        transition-duration: 0.5s;
      }
      ```
  
  - content: |

      ## What we learned:

      - Single-run timers
      - Repeating timers
      - CSS transitions




---