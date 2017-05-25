---
layout: default
title: Responsive Design
slides:

  - class: title-slide

    content: |

      # Responsive Design

      _Mobile-ready design and responsive layouts_

  
  - content: |

      ## Responsive Design View

      Use the developer tools to test how your
      site looks on different device sizes.


  - content: |

      ## Tell the browser you got dis

      ```html
      <meta name="viewport" content="width=device-width,initial-scale=1">
      ```

      This prevents the browser from just using
      the desktop version and zooming it out.

      {:.checkpoint}
      Your site should now be zoomed in on mobile.

    notes: |

      Open the site in a new window.

      Use dev tools to load it up on a mobile layout.

      Observe how the text is itty bitty. This is because the browser is using the desktop version and just zooming it out to fit.

  - content: |

      ## Use percentages for widths

      ```css
      .container {
        width: 100%;
      }
      ```

      This lets you maximise screen use on mobile.

      {:.checkpoint}
      Your main content box should resize with the browser.

  - content: |

      ## Use a max width to limit size

      ```css
      .container {
        width: 100%;
        max-width: 800px;
      }
      ```

      Combining a pixel `max-width` and a percentage `width`
      gives you full-width on mobile and limited width on desktop.

      {:.checkpoint}
      Your main content size should be limited on large screens.


  - content: |

      ## Use view-relative sizing for heights

      ```css
      .header {
        height: 60vh;
      }
      ```

      The `vh` measurement is like `%`, but it's a percentage 
      of the **view** height not the **container** height.

      {:.checkpoint}
      Your header box should resize as the browser height changes.

  - content: |

      ## Use view-relative sizing for text

      ```css
      .title {
        font-size: 30vh;
      }
      ```

      The `vh` and `vw` units can also be used
      for font sizes, instead of using pixels.

      {:.checkpoint}
      Your page title should resize as the browser height changes.



  - content: |

      ## Use FlexBox for any kind of column layout

      A container with its `display` set to `flex` 
      automatically sizes elements inside it to fit.

    notes: |

      If you know what a `float` is, then FlexBox is
      kind of like that, but better.


  - content: |

      ## FlexBox navigation bar

      ```css
      .main-nav {
        display: flex;
      }

      .main-nav a {
        width: 200px;
      }

      .main-nav .title {
        flex: 1;
      }
      ```

      {:.checkpoint}
      Your title should be on the left, and links on the right.


  - content: |

      ## FlexBox content panels

      ```css
      .panels-container {
        display: flex;
      }

      .panel {
        flex: 1;
      }
      ```

      {:.checkpoint}
      Your panels should now be horizontal and equally sized.



  - content: |

      ## What we learned

      - Percentage widths
      - View-relative heights
      - View-relative font sizes
      - FlexBox layouts



  ##########


---