---
layout: default
title: Using JavaScript
slides:

  - class: title-slide

    content: |

      # Using JavaScript

      _Adding those first lines of JavaScript to your site_

    notes: |

      In this section we will add a JavaScript file to a web page and test that it works.


  ##########


  - content: |

      ## Create a file called `site-script.js`

      This file needs to be in the same folder
      as your `index.html` and `style.css` files.

    notes: |

      You can actually name this file whatever you like, and you can also put it in a subfolder if you choose.

      Script files are commonly named after their project, so a site about Top Tomato Recipes might be called `top-tomato-recipes.js`.


  ##########


  - content: |

      ## Include the script into your `index.html`

      You need to include JavaScript files at the end of your 
      HTML `body` so that the scripts load after the HTML and CSS.

      ```html
        ...

        <script src="site-script.js"></script>

      </body>
      ```


    notes: |

      Sometimes you will see websites where the JavaSCript is loaded in the `head`.

      Although it is possible to make the JavaScript work that way, it can often result in errors when you try to use JavaScript to access or modify HTML elements which haven't yet been created when the script runs.


  ##########


  - content: |

      ## Use Chrome Developer Tools to check <br>that the file was included correctly

      In Chrome, press `Command + Option + I` to open the developer tools.
      Click the *Network* tab, refresh, and make sure `site-script.js` is listed.


  ##########


  - content: |

      ## Add a `console.log()` to check your script runs

      In `site-script.js`, add a message to yourself using `console.log()`.
      This function can display code values in the Developer Tools window.

      ```javascript
      console.log('Testing, testing, 123...');
      ```


  ##########


  - content: |

      ## Check your console output in the Developer Tools

      Open developer tools, refresh your page, and look in the **Console** tab.
      Your message should be displayed.

      If you have an error, try to understand the error and correct your code.

      {:.checkpoint}
      Hooray, I got a message with no errors!


  ##########


  - content: |

      ## Things we learned

      - Adding a JavaScript file
      - Viewing network activity
      - Logging to the console


      

---