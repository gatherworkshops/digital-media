---
layout: default
title: Responsive Design
slides:

  - class: title-slide

    content: |

      # Responsive Design

      _Mobile-first design and responsive layouts_


  - content: |

      ## Responsive Design View

      Use the developer tools to test how your
      site looks on different device sizes.

  - content: |

      ## Use percentages for widths

      This lets you maximise screen use on mobile.

      ```css
      .container {
        width: 100%;
      }
      ```

  - content: |

      ## Use a max width to limit size

      Combining a pixel `max-width` and a percentage `width`
      gives you full-width on mobile and limited width on desktop.

      ```css
      .container {
        width: 100%;
        max-width: 800px;
      }
      ```

  - content: |

      ## Use view-relative sizing for heights

      This helps you size things so that they fit
      vertically on a small screen.

      ```css
      .header {
        height: 60vh;
      }
      ```

      {:.checkpoint}
      Resize your browser height to see the header change.

  - content: |

      ## Responsive text sizing

      To go along with responsive layouts, you may also
      find a need for responsive font size.

      ```css
      .title {
        font-size: 30vh;
      }
      ```


  - content: |

      ## Use FlexBox for any kind of column layout

      If you know what a `float` is, then FlexBox is
      kind of like that, but better.

      If you don't know what a float is, don't panic!


  - content: |

      ## FlexBox for sidebars

      ```html
      <div class="container">

        <div class="sidebar"></div>

        <div class="content"></div>

      </div>
      ```

      ```css
      .container {
        display: flex;
      }

      .sidebar {
        width: 200px;
        flex: 0;
      }

      .content {
        flex: 1;
      }
      ```


  - content: |

      ## FlexBox for navigation bars

      ```html
      <nav class="main-menu">
        <a href="#">Home</a>
        <a href="#">Gallery</a>
        <a href="#">Contact</a>
      </nav>
      ```

      ```css
      .main-menu {
        display: flex;
      }

      .main-menu a {
        width: 200px;
      }
      ```


  - content: |

      ## FlexBox for content panels

      ```html
      <div class="panels">
        <div class="panel">
          <img src="#">
          <span>Title One</span>
        </div>
        <div class="panel">
          <img src="#">
          <span>Title Two</span>
        </div>
        <div class="panel">
          <img src="#">
          <span>Title Three</span>
        </div>
      </div>
      ```

      ```css
      .panels {
        display: flex;
      }
      ```

  - content: |

      ## What we learned

      - Percentage widths
      - View-relative heights
      - View-relative font sizes
      - FlexBox layouts



  ##########


---