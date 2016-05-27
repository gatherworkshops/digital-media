---
title: Responsive Design

slides: 

  - content: |

      # Responsive Design

      _Designing a site for all screens_

    notes: |

      This chapter will look at relative sizing of boxes and text using percentages.

  - content: |

      The content in a site built with responsive 
      design principles will flow to fit any screen.

  - content: |

      **Responsive design** is often confused with **adaptive design**,
      where a site will have multiple sizes it can snap to.

  - content: |

      One way to think about the difference between them is
      smooth resizing (responsive) vs snap resizing (adaptive). 

      ![Responsive and Adaptive design comparison](https://cdn.css-tricks.com/wp-content/uploads/2015/11/rwd-vs-adapt-example.gif)

      Responsive on top, adaptive on the bottom.
      Credit: [CSS Tricks](https://css-tricks.com/the-difference-between-responsive-and-adaptive-design/)
  
  - content: |

      **Responsive** and **adaptive** are just design ways of thinking,
      and any site can use principles from both philosophies.







  - content: |

      ## Chrome Device View

      Google Chrome has a built-in "responsive" mode,
      for web developers to easily test a site's layout.

  - content: |

      Open the Chrome Developer Tools for your website
      using the keyboard shortcut for your system.

      Mac: Command + Option + i
      Windows: Ctrl + Shift + i

  - content: |

      Once you have the dev tools open, you can toggle
      mobile view using a keyboard shortcut:

      Mac: Command + Shift + M
      Windows: Ctrl + Shift + M

  - content: |

      The mobile view offers a variety of 
      specific screen sizes to test against.

      Select the mobile view called "Responsive".
      {:.checkpoint}








  - content: |

      ## Enabling Responsive Design

    notes: |

      Laptops and desktops will respond to percentage-based layouts automatically.

      Smaller devices like tablets and phones know that many people have websites which haven't been designed for smaller screens. For this reason, smaller devices will scale down (zoom out) your site to fit it on the screen.

      This isn't what we want! We're taking responsibility for our design being responsive, so we need to tell browsers about our decision.

  - content: |

      In Responsive View, scale your site 
      down to less than 970px wide.

      Your whole site should start scaling down.
      {:.checkpoint}

    notes: |

      Using the Responsive View in Chrome Dev Tools, you can easily demonstrate the zooming effect on smaller devices.

  - content: |

      We can prevent this from happening by adding
      a responsive viewport meta tag to our HTML.

    notes: |

      Using a small piece of code, we can tell devices not to zoom our content.

      You should only do this for websites which have been designed to handle smaller screen sizes.

  - content: |

      In your `page` layout, add the viewport
      meta tag to the HTML head section.

      ```html
      <head>

        <meta name="viewport" content="width=device-width">

        <title>{{ site.name }}</title>
        <link rel="stylesheet" href="/theme/css/styles.css">

      </head>
      ```

      Your site should now stay the same scale at any width.
      {:.checkpoint}

    notes: |

      No notes







  - content: |

      ## Responsive Layout

      Long story short: use percentage
      sizing wherever you can!


  - content: |

      At the moment, our site's content always 
      takes up the full width of the screen.


  - content: |

      This is fine on small screens, but on larger screens
      our content looks really weird and stretched out.

  - content: |

      We can solve this problem by giving
      our content a maximum possible width.

  - content: |

      Let's tidy up our shop page as
      an example of responsive design.

  - content: |

      In your `shop` page, add a section with
      the class "container" around the shop items.

      ```html
      <h1>Shop</h1>

      <div class="container">
        <ul class="shop-items">

          {% for item in site.data.shop %}

            <li>
              <span class="name">{{ item.name }}</span>
              <span class="price">${{ item. price }}</span>
            </li>

          {% endfor %}

        </ul>
      </div>
      ```

    notes: |

      We are using this restricted-width container in our page instead of in our layout because we don't want it to apply to all content on all pages.

      It's common in web design to have portions of the page which are centered, and portions which are full-width.

      Only using the `container` class in specific instances allows for that flexibility.

  - content: |

      In your stylesheet, create a new 
      style for the `container` class.


      ```css
      .container {
        max-width: 800px;
        padding: 0 20px;
        margin: 0 auto;
        border: 1px solid red;
      }
      ```

    notes: |

      The red border is just so we can see where the content is.

  - content: |

      Test your layout in Responsive View.

      Your item list area should stop growing at 800px wide.
      {:.checkpoint}




  - content: |

      ## Hero Images

      Modern websites often have a big and bold
      "hero" image at the top of their pages.


  - content: |

      Our "Shop" heading is still sticking to the left,
      we can give it some character using a hero image. 


  - content: |

      In your `shop` page, create a 
      `hero` div around your heading.

      ```html
      <div class="hero">
        <h1>Shop</h1>
      </div>

      <div class="container">
        <ul class="shop-items">

          {% for item in site.data.shop %}

            <li>
              <span class="name">{{ item.name }}</span>
              <span class="price">${{ item. price }}</span>
            </li>

          {% endfor %}

        </ul>
      </div>
      ```

  - content: |

      Also add a more friendly heading 
      and welcome message for guests.

      ```html
      <div class="hero">

        <h1>Welcome to the Store</h1>

        <p>
        We've got a great selection of scrummy treats,<br>
        we hope you'll visit us soon for a taste!
        </p>

      </div>
      ```

  - content: |

      In your stylesheet, create a `hero` style
      with some vertical padding and a background.

      ```css
      .hero {
        padding: 50px 0;
        min-height: 400px;
        background: lightgreen;
      }
      ```

      You should now have a green panel in your shop.
      {:.checkpoint}


  - content: |

      Our welcome text is still sticking to the left,
      but we can use our `container` to center it.

      ```html
      <div class="hero">
        <div class="container">

          <h1>Welcome to the Store</h1>

          <p>
          We've got a great selection of scrummy treats,<br>
          we hope you'll visit us soon for a taste!
          </p>

        </div>
      </div>
      ```


  - content: |

      Find a Creative Commons image on Flickr
      to use as the hero image on your shop page.

      [Search Flickr Creative Commons]()


  - content: |

      Save the image to your theme's `img` 
      folder with a short and clear name.


  - content: |

      Add the image to your credits page.


  - content: |

      Create a new class called `.hero.shop`

      ```css
      .hero.shop {
        background-color: lightgreen;
        background-image: url('/theme/img/shop-hero.jpg');
        background-size: cover;
        background-position: center;
      }
      ```

    notes: |

      For your background colour, you should choose a colour similar to the colour scheme of your background image.

      This is because if the image doesn't load for some reason, you still want your site to look okay and for the text to be readable.




  


  - content: |

      ## Fixed-Width Header

      We can use the same concept as we did
      for the hero image, to center our header content.

  - content: |

      In your `header` include, add a `container`
      around the  title and links.

      ```html
      <header>
        <div class="container">

          <h1>{{ site.name }}</h1>

          <nav>
            <a href="/">Home</a>
            <a href="/shop.html">Shop</a>
            <a href="/contact.html">Contact</a>
            <a href="/credits.html">Credits</a>
          </nav>

        </div>
      </header>
      ```

  - content: |

      You'll also need to modify the styles,
      as the container should now have the `flex` display.

      ```css
      header {
        background: #222;
        color: white;
      }

      header .container {
        display: flex;
        align-items: baseline;
      }
      ```






  - content: |

      ## Fixing Funky Box Sizing

      By default, browsers **add** padding to a box's width,
      rather than just pushing the content in by the padding value.

  - content: |

      This means that if you have a container which is 800px wide,
      and it has 30px padding either side, its full width is 860px.

  - content: |

      To stop this from happening, we can use the
      `border-box` sizing on all elements.

      ```css
      html {
        font-family: 'Roboto', sans-serif;
        font-size: 14px;
        line-height: 150%;
        box-sizing: border-box;
      }

      *, *:before, *:after {
        box-sizing: inherit;
      }
      ```


  - content: |

      Add a hero image to your home page.




#  - content: |
#
#      ## Responsive Text
#
#
#  - content: |
#
#      vw, vh, vmin, vmax



---