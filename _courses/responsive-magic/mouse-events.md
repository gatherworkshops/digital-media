---
layout: default
title: Mouse Events
slides:

  - class: title-slide

    content: |

      # Mouse Events

      _User interaction with clicks and mouse-overs_


  ##########


  - content: |

      ## How events work

      - Create a **function** that runs some code
      - Find an **element** on your page
      - Run the function when **something happens** to the element


  ##########

  - content: |

      ## Step One: <br> Create a function

      In `site-script.js` create a new function:

      ```javascript
      function makeLionRoar() {
        console.log('Raaaaahr!');
      }
      ```

      You need: 
      
      - the key word `function` 
      - a name for it like `makeLionRoar`,
      - some lines of code `{` in between curly brackets `}`.

  - content: |

      ## Step Two: <br> Find an element

      We already know how to do that!

      ```javascript
      function makeLionRoar() {
        console.log('Raaaaahr!');
      }

      var lionBox = document.getElementById('lion-box');
      ```


  - content: |

      ## Step Three: <br> Run the function when an event happens

      ```javascript
      function makeLionRoar() {
        console.log('Raaaaahr!');
      }

      var lionBox = document.getElementById('lion-box');

      lionBox.addEventListener('click', makeLionRoar);
      ```

      {:.checkpoint}
      When I click my lion, the console says "Raaaahr!".


  - content: |

      ## Challenge: Change "Lion" to "Raaaahr!"

      Add more lines of code inside the function so that when you 
      click the "lion" box, its innerHTML changes to "Raaaahr!"

      {:.checkpoint}
      When I click the "lion" box, it changes to "Raaaahr!".

  


  - content: |
      
      ## Why use a function?

      A function lets us wrap up several lines of code under one 
      single name, so we can easily run it as many times as we like.


  - content: |

      ## Mouse Over Events

      In your code, add another function and another event listener:

      ```javascript
      function makeLionMeow() {
        lionBox.innerHTML = 'Meow!';
      }

      lionBox.addEventListener('mouseover', makeLionMeow);
      ```

      When I mouse-over "lion", it says "meow";


  - content: |

      ## Challenge: Make Lion Relax 

      In your code, add another function and another event listener
      so that when you `mouseout` the text changes back to `lion`.


  ##########


  - content: |

      ## What we learned

      - Writing a function
      - Adding an event listener
      - Click events
      - Mouse over events


---