---
layout: chapter
title: Menu Bar
slides:

  - class: title-slide
    content: |

      ![Gather Workshops Logo]([[BASE_URL]]/theme/assets/images/gw_logo.png)

      # Menu Bar
      _Adding buttons to click around your page_

    notes: |
      A menu bar will allow visitors to click between the different pages in our website.

      To add a menu bar, we will need some extra HTML and CSS code. 



  - content: |

      ## Menu Bar

      ![The menu bar goes between the header and the content area. It will be a plain box containing some links.]({{ site.baseurl }}/slides/workshop/menubar/images/layout-menubar.svg)

      _Adding a menu bar to your page_

    notes: |

      The navigation we'll be creating is a horizontal nav across the top of your screen.

      You can just as easy create a vertical one if you like - you'll just have to tweak the CSS! ;)




  - content: |

      ## Navigation HTML

      Add the `nav` on the line after your closing `</header>` tag:

      ```html
      <nav class="main-menu">

      </nav>
      ```

      _Create the layout container for your menu bar_
      


    notes: |
      Hey, a new type of HTML element! 

      The `nav` element is used for creating navigation. It has matching start and end tags, and between those tags you put a set of links that you want to include in your navigation.

      We'll get to that on the next slide!

      If you preview your navigation right now, it won't look like anything - it doesn't have any styles yet! 

      We did set up the class `main-menu` though, so we'll be able to style this nav from our CSS.





  - content: |

      ## Navigation Links

      Add your page links, between the `nav` tags:

          <a href="index.html">Home</a>
          <a href="pictures.html">Pictures</a>
          <a href="videos.html">Videos</a>

      _Add some links to your menu bar_

    notes: |

      Each link is just an `a` element, like we tried out earlier.

      Remember that links always need their `href` set to a web address where we want the link to go. 

      The _Home_ link will go back to our `index.html`, so we can fill that in.

      We haven't created a `pictures.html` or a `videos.html` yet, but we can fill in the link and then create the page later.

      If you preview your page now, it won't look like much but the links should at least be showing up! We'll give them some style next.





  - content: |

      ## Navigation Styles

      In your CSS, create a new rule:

          .main-menu {
              background: #FF0000;
          }

      _Add a background to your nav, so you can see it_

    notes: |
      Our nav has the class `main-menu` so we can use this in our CSS to add some design to our nav.

      Keep in mind that we are currently just styling the `nav` element, which is a container for all our navigation links.

      We'll get to styling the links soon, and make them look a bit more like buttons.





  - content: |

      ## Navigation Button Styles

      In your CSS, create two new rules:

      ```css
      .main-menu a {
          background-color: #00FF00;
          border-color: #00DD00;
          font-weight: bold;
          display: inline-block;
          padding: 5px 10px;
      }

      .main-menu a:hover {
          background-color: #00DD00;
          color: #FFFFFF;
      }
      ```


      _Style your links to look like buttons_


    notes: |
  
      The first CSS rule says how we want the menu buttons to look.

      The second CSS rules says how we want the buttons to look when we move our mouse pointer over them, when we "hover".

      You can change these values to make your buttons look however you like.


  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## The Internet: Complete!

      Great, now let's explore where we'll build our own site...

      [Take me to the next chapter!](ownership.html)


    notes: |

      Great! Now that we know the basics, let's get started on our own projects.

---




