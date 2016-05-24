---
title: Themes

slides: 

  - content: |
      # Themes

  - content: |
      In a Jekyll site, the content is separate from the layout.

  - content: |
      Content is written in the pages where we want it, as normal.

  - content: |
      Design is applied by using a page template, which in Jekyll is called a "layout".

  - content: |
      A page layout can be a single file, or can be made up of separate pieces such as a header, content area and footer. These are known as 'includes'.

  - content: |
      Our site's theme will contain all layouts, includes and styles for our site.
  





  - content: |
      ## Creating a Theme

  - content: |

      Create a new folder called 'theme'.

    notes: |

      By keeping all of our theme files in one folder, we could easily re-use this theme on another site by copying it. A whole new website with different content but the same design, really easy.





  - content: |
      ## Creating Layouts

  - content:

      In your theme folder, create a new folder called _layouts.

    notes: |

      The underscore is a naming convention. That is, we don't need it but it is common in Jekyll sites to use underscores for theme folders.

  - content: |

      Tell Jekyll the location of this folder.

      ```yaml
      layouts: '_theme/layouts'
      ```

  - content: |

      In the layouts folder, create a new file called page.html

  - content: |

      Add the following code:

      ```html
      <!doctype html>
      <html>
          <head>
              <title>My Awesome Site</title>
          </head>

          <body>
              {{ content }}
          </body>
      </html>
      ```

  - content: |

      The curly brackets are a placeholder for where we 
      want the page content to be inserted by Jekyll.







  - content: |
      ## Applying Layouts

  - content: |

      Open your index page and at the top add:

      ```html
      ---
      layout: page
      ---
      ```

  - content: |

      This extra bit at the top of our index page is a Jekyll thing called "front matter".
      It's extra information about the page that can be used by Jekyll or by us.






  - content: |
      ## Styling


  - content: |

      In your theme folder create a new folder called 'css'

  - content: |

      Inside the CSS folder make a new file called styles.css

  - content: |

      Add some basic styling for your site.

      ```css
      body, html {
          background: black;
          color: white;
      }
      ```

  - content: |

      Update your layout to import the CSS.

      ```html
      <link rel="stylesheet" href="theme/css/styles.css">
      ```

    notes: |

      Paths in the generated site may be different from project structure.






  - content: |

      ## Images

  - content: |

      Create a folder called 'img' in your theme folder.

  - content: |

      Add background image.

  - content: |

      Use image in CSS.

  - content: |

      Add logo image.

  - content: |

      Use image in header.
      





  - content: |
      ## Includes

  - content: |

      In your theme create a new folder called _includes.

  - content: |

      Tell Jekyll the location of this folder.

      ```yaml
      layouts: '_theme/layouts'
      ```

  - content: |

      Create an include called 'header.html'


  - content: |
      Code it up

      ```html
      <header>

          <h1>Site Name Here</h1>

          <nav>
              <a href="home.html">Home</a>
              <a href="contact.html">Contact</a>
          </nav>

      </header>
      ```

  - content: |
      Include the header in our page layout.

      ```html
      <!doctype html>
      <html>
          <head>
              <title>My Awesome Site</title>
          </head>

          <body>

              {% include header.html %}

              {{ content }}
          </body>
      </html>
      ```

  - content: |

      Templating language:

      Double brackets means output a simple value.

      Bracket percent means do some kind of processing.






  - content: |

      ## Challenge: Add Another Page

      Add a "shop" page and apply the same theme.
      Also add the new page to the navigation.

      Your site should have three pages, with a nav on every page.



---

TODO: selected page nav item