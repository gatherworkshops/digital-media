---
layout: default
title: Grouped Mouse Events
slides:

  - class: title-slide

    content: |

      # Grouped Mouse Events

      _Watching groups of elements, and finding where events came from_


  ##########

  - content: |

      ## How grouped events work

      - Create a **function** that runs some code
      - Find a group of **elements** on your page
      - Run the function when **something happens** to any of the elements
      - Use the **event** data to find which element was the trigger

  - content: |

      ## Step One: <br> Create a function

      We already know how to do this!

      ```javascript
      function crossOffItem(){
        console.log('cross the item off the list');
      }
      ```

  - content: |

      ## Step Two: <br> Find a group of elements

      Here's a new function called `getElementsByClass`:

      ```javascript
      function crossOffItem(){
        console.log('cross the item off the list');
      }

      var listItems = document.getElementsByClass('item');
      ```

  - content: |

      ## Step Three: <br> Watch for an event

      Use a loop to add a listener to every item

      ```javascript
      function crossOffItem(){
        console.log('cross the item off the list');
      }

      var listItems = document.getElementsByClass('item');

      for( var counter=0; counter<listItems.length; counter++){
        listItems[i].addEventListener('click', crossOffItem);
      }
      ```

  - content: |

      ## Step Four: <br> Find the trigger element

      ```javascript
      function crossOffItem( event ){
        console.log('cross the item off the list');
        console.log( event.target );
        event.target.css.textDecoration = 'line-through';
      }

      var listItems = document.getElementsByClass('item');

      for( var counter=0; counter<listItems.length; counter++){
        listItems[i].addEventListener('click', crossOffItem);
      }
      ```

      {:.checkpoint}
      When I click an item, it gets crossed off!


  - content: |

      ## Whoa there, hold up, this just got tricky!

      Let's use our `debugger` to step through this line by line.

      ```javascript
      function crossOffItem( event ){
        console.log('cross the item off the list');
        console.log( event.target );
        event.target.css.textDecoration = 'line-through';
        debugger;
      }

      var listItems = document.getElementsByClass('item');
      debugger;

      for( var counter=0; counter<listItems.length; counter++){
        listItems[i].addEventListener('click', crossOffItem);
        debugger;
      }
      ```


  - content: |

      ## And how does this loop thing actually work?

      - `for` is like a function, it groups lines of code
      - `for` requires a **counter**, a **limit** and a **stepper**
      - `counter` starts at 0
      - the **limit** is the length of `listItems`
      - the **stepper** goes up by 1 each time


  - content: |

      ## What we learned

      - Finding a group of elements by class
      - Using a loop to go through a group
      - Using event data to identify an element



---