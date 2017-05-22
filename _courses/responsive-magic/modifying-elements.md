---
layout: default
title: Modifying Elements
slides:

  - class: title-slide

    content: |

      # Modifying Elements

      _Finding and manipulating HTML elements using JavaScript_


  ##########


  - content: |

      ## Getting an element by its `id`

      Before we can use JavaScript to modify an element,
      we need a way to identify it and target it.

      One way to do this is using its HTML `id`,
      because an `id` should be used only once on a page.


  - content: |

      ## Using the `getElementById` function

      Open up your Developer Tools, open the **Console** tab, and type

      ```javascript
      document.getElementById('first-box')
      ```

      When you press enter, what do you see?


  - content: |

      ## Save target elements under given names

      In your console, create a variable `box` and save `first-box` into it

      ```javascript
      var firstBox = document.getElementById('first-box')
      ```

    notes: |

      By saving an element to a variable, we can give it a name
      and then use that name to do things to it.

  
  - content: |

      ## Access a variable by its name

      In your console, type `box` and press enter.
      The `firstBox` element should be given back to you.


  - content: |

      ## Modify an element's content

      Using your console, change the text content
      inside the first box from `frog` to `lion`.

      ```javascript
      box.innerHTML = 'lion'
      ```

  - content: |

      ## Modify an element's CSS

      Using your console, change the text colour
      of the first box from `green` to `gold`.

      ```javascript
      box.css.color = 'gold'
      ```


  - content: |

      ## Make your code permanent

      The console can only make temporary changes.
      Copy the code you've learned into your `site-script.js`.

      ```javascript
      var firstBox = document.getElementById('first-box');
      firstBox.innerHTML = 'lion'
      firstBox.css.color = 'gold';
      ```

  - content: |

      ## Do some practice

      Use what you've learned to:

      - Make the second box say 'tiger' with an orange background
      - Make the third box say 'elephant' and upsize to 300px x 300px


  - content: |

      ## Explore your code in real-time

      Use `debugger` lines in your code to freeze it at any time.
      While frozen, you can look at the value in a variable!

      ```javascript
      var firstBox = document.getElementById('first-box');
      firstBox.innerHTML = 'lion'
      firstBox.css.color = 'gold';

      debugger;

      var secondBox = document.getElementById('second-box');
      secondBox.innerHTML = 'tiger';
      secondBox.css.backgroundColor = 'orange';
      ```


  - content: |

      ## What we learned

      - Getting an element by its id
      - Saving elements to variables
      - Modifying an element's css
      - Using debugger break points


---



