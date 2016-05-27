---
title: Adaptive Design

slides: 

  - content: |

      # Adaptive Design
      _Considering specific screen sizes_


  - content: 

      ## Navigation

      The most obvious target for adaptive design
      is our menu bar, which doesn't fit on small screens.


  - content: |

      The most common solution to this problem is to
      hide the menu on small screens, with a "show" button.

  - content: |

      To achieve this effect, on small 
      devices we will need to:

      - Design a vertical menu layout
      - Add a button to show/hide it
      - Hide the menu by default
      - Make a class for the visible menu
      - Toggle the class using jQuery



  - content: |

      Add a menu button to your nav bar.

      ```html
      <h1>{{ site.name }}</h1>

      <span class="menu-button">Menu</span>
      <nav>
        <a href="/">Home</a>
        <a href="/shop.html">Shop</a>
        <a href="/contact.html">Contact</a>
        <a href="/credits.html">Credits</a>
      </nav>
      ```
  
  - content: |

      Make the menu button hidden by default

      ```css
      header .menu-button {
        display: none;
      }
      ```

  - content: |

      Create a media query for screens 500px or smaller

      ```css
      @media only screen and (max-width: 500px) {

      }
      ```

  - content: |

      For this screen size we want our menu button to be visible

      ```css
      @media only screen and (max-width: 500px) {

        header .menu-button {
          display: block;
        }

      }
      ```

  - content: |

      We can also make it nicer-looking by using 
      uppercase letters and a smaller font size.

      ```css
      @media only screen and (max-width: 500px) {

        header .menu-button {
          display: block;
          text-transform: uppercase;
          font-size: 12px;
        }

      }
      ```

  - content: |

      We can make our menu drop to the next line by 
      making it 100% wide and enabling flex-wrap on its parent.

      ```css
      @media only screen and (max-width: 500px) {

        header .menu-button {
          display: block;
          text-transform: uppercase;
          font-size: 12px;
        }

        header nav {
          width: 100%;
        }

        header .container {
          flex-wrap: wrap;
        }

      }
      ```

  - content: |

      Now we can style our nav buttons to be vertical by making them display block.

      ```css
      @media only screen and (max-width: 500px) {

        header .menu-button {
          display: block;
          text-transform: uppercase;
          font-size: 12px;
        }

        header nav {
          width: 100%;
        }

        header nav a {
          display: block;
        }

        header .container {
          flex-wrap: wrap;
        }

      }
      ```

  - content: |

      And we can further style them to look nicer:

      ```css
      header nav a {
        display: block;
        border-top: 1px solid #777;
        margin: 0;
        text-align: center;
        padding: 8px 0 3px;
      }
      ```

  - content: |

      The last bit of CSS we need is a class
      to optionally hide the menu.

      ```css
      header nav {
        width: 100%;
      }

      header nav.hide-on-mobile {
        display: none;
      }
      ```

  - content: |

      Add the `hide-on-mobile` class in your HTML

      ```html
      <span class="menu-button">Menu</span>
      <nav class="hide-on-mobile">
        <a href="/">Home</a>
        <a href="/shop.html">Shop</a>
        <a href="/contact.html">Contact</a>
        <a href="/credits.html">Credits</a>
      </nav>
      ```







  - content: |

      ## Toggling Classes with jQuery


  - content: |

      In your theme folder,
      create a folder called `js`.

  - content: |

      Download jQuery 2 production version, unzip, 
      and copy the `jquery.min.js` file to your `js` folder.

      [Download jQuery](https://jquery.com/download/)

  - content: |

      In the `js` folder, create a
      new file called `menu.js`.

  - content: |

      In menu.js:

      ```javascript
      function enableMobileMenu(){
        // code here
      }
      ```

  - content: |

      In `menu.js`:

      ```javascript
      function enableMobileMenu(){

        var menuButton = $('.menu-button');
        var menu = $('header nav');

        function toggleMenu(){
          menu.toggleClass('hide-on-mobile');
        }

        menuButton.click(toggleMenu);
      }
      ```


  - content: |

      ```javascript
      $(document).ready(enableMobileMenu);

      function enableMobileMenu(){

        var menuButton = $('.menu-button');
        var menu = $('header nav');

        function toggleMenu(){
          menu.toggleClass('hide-on-mobile');
        }

        menuButton.click(toggleMenu);
      }
      ```


  - content: |

      In your `page` template, add a script tag
      to import jQuery and your menu script into your site.

      ```html
      <body>
        
        {% include header.html %}
        
        {{ content }}
        
        <script src="/theme/js/jquery-2.1.4.min.js"></script>
        <script src="/theme/js/menu.js"></script>
      
      </body>
      ```

  - content: |

      Your menu should now display like normal on large screens
      and be hidden under a menu button on smaller screens.









  - content: |
      ## Summary

      - **Media Queries**
        We can choose to make piece of CSS only apply on specific screen sizes.
      - **Class Toggling**
        jQuery can be used to show and hide elements by adding and removing classes.
      {:.flex-list}

    notes: |

      No notes

  - content: |

      ### Adaptive Design: Complete

      [Next Chapter](flexbox-layouts.html)

    notes: |

      You've completed the Adaptive Design chapter, well done!

      Continue to the next chapter for more.


  




---