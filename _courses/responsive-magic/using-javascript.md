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

      ## Create a JavaScript file

      In the **root** of your project,
      create a new file called `site-script.js`.

      {:.checkpoint}
      You should have a new file called `site-script.js`.

    notes: |

      The **root** is the top level folder where `index.html` and `style.css` are kept.

      You can actually name this file whatever you like, and you can also put it in a subfolder if you choose.

      Script files are commonly named after their project, so a site about Top Tomato Recipes might be called `top-tomato-recipes.js`.


  ##########


  - content: |

      ## Include the script into your HTML

      ```html
        ...

        <script src="site-script.js"></script>

      </body>
      ```

      JavaScript includes go at the end of the `body`.
      This is so they load after the HTML and CSS.

      {:.checkpoint}
      Nothing will change yet! The JavaScript file is empty.


    notes: |

      Sometimes you will see websites where the JavaSCript is loaded in the `head`.

      Although it is possible to make the JavaScript work that way, it can often result in errors when you try to use JavaScript to access or modify HTML elements which haven't yet been created when the script runs.


  ##########


  - content: |

      ## Use Chrome Developer Tools to check <br>that the file was included correctly

      Open the developer tools using `Ctrl + Option + I`.
      Change to the **Network** tab, then refresh the page.

      {:.checkpoint}
      The file `site-script.js` should be listed.


  ##########


  - content: |

      ## Write some code to check your script runs

      ```javascript
      console.log('Hello!');
      ```

      In `site-script.js`, use the `console.log()` function
      to log a message to yourself in the developer console.

      {:.checkpoint}
      Make sure your file is saved!
      


  ##########


  - content: |

      ## Check your output in the developer console

      Open the dev tools and switch to the **Console** tab.
      Refresh the page, and your message should be displayed.

      **If you have an error, try to understand** 
      **the error and correct your code.**

      {:.checkpoint}
      Hooray, I got a message with no errors!


  ##########


  - content: |

      ## Things we learned

      - Adding a JavaScript file
      - Viewing network activity
      - Logging to the console


      

---