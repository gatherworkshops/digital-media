---
title: FlexBox Layouts

slides: 

  - content: |

      # FlexBox Layouts
      _The CSS3 answer to floats_

      
  - content: |

      We've already used a flex layout for the header,
      and now we'll explore what it is and how it works.

  - content: |

      The `display` values you may be familiar with 
      are inline, block, inline-block, and none.

  - content: |

      CSS3 introduces some new display values, 
      one of which is the mighty **flex**.

  - content: |

      Setting `display: flex` on a container 
      allows us to do fancy sizing on its children.


  - content: |

      ![FlexBox Layout Examples](https://css-tricks.com/wp-content/uploads/2014/05/align-items.svg)

      Here are a few examples of layouts
      you can easily achieve using flexbox.

      Image credit [CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

  - content: |

      In the "old days", layouts like these were achieved 
      (with difficulty) using inline-block elements or floats.

  - content: |

      In this chapter we will explore flexbox as a 
      developer and mobile friendly option for layout.










  - content: |

      ## Columns

      We can use flexbox to arrange elements 
      in a responsive horizontal layout.


  - content: |

      Columns should never contain so much text 
      that you can't view the whole thing at once.


  - content: |

      We will create some panels advertising
      the various content on our site.


  - content: |

      In your `home` page, create a new container,
      with the extra class `panel-links`.

      ```html
      <div class="container">
          <h1>Hello!</h1>
      </div>

      <div class="panel-links container">
          
      </div>
      ```

  - content: |

      Inside the new container, add three links:

      ```html
      <div class="panel-links container">

          <a href="/shop.html">
            <h2>Online Shop</h2>
            <p>
              Browse the yummy treats we have to offer
              before you come by for a visit.
            </p>
          </a>

          <a href="/gallery.html">
            <h2>Photo Gallery</h2>
            <p>
              See photos of our space and our food so
              you feel at home even before you arrive.
          </a>

          <a href="/contact.html">
            <h2>Visit Us</h2>
            <p>
              Find our address and open hours, we'd love
              to see you. You can even give us a call.
          </a>

      </div>
      ```


  - content: |

      In your stylesheet, create a style
      for the panel links:

      ```css
      .panel-links a {
        display: block;
        text-decoration: none;
        color: black;
        text-align: center;
        background-color: white;
        border: 1px solid #333;
        border-radius: 3px;
        padding: 20px;
      }

      .panel-links a:hover {
        background-color: lightblue;
      }
      ```

  - content: |

      To lay out the panels horizontally,
      use `display: flex` on the parent.

      ```css
      .panel-links {
        display: flex;
        align-content: space-between;
      }

      .panel-links a {
        display: block;
        text-decoration: none;
        color: black;
        text-align: center;
        background-color: white;
        border: 1px solid #333;
        border-radius: 3px;
        padding: 20px;
      }

      .panel-links a:hover {
        background-color: lightblue;
      }
      ```

  - content: |

      We can add spacing between using margins:

      ```css
      .panel-links a {
        display: block;
        text-decoration: none;
        color: black;
        text-align: center;
        background-color: white;
        border: 1px solid #333;
        border-radius: 3px;
        padding: 20px;
        margin-right: 20px;
      }
      ```

  - content: |

      And we can remove the margin from
      the last panel using a pseudo selector.

      ```css
      .panel-links a:last-of-type {
        margin-right: 0;
      }
      ```











  - content: |

      ## Challenge: Two-Column Layout

      Use flexbox to add a Google Map beside
      contact information on your `contact` page.










---