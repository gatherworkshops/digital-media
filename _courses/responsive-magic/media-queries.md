---
layout: default
title: Media Queries
slides:

  - class: title-slide

    content: |

      # Media Queries

      _Displaying device-specific styles_


  - content: |

      ## Media queries can apply CSS based on screen size. <br> They can not modify HTML.

  - content: |

      ## Structure of a Media Query

      ```css
      @media (min-width: 800px) {
        .header {
          background: url(images/background.jpg);
        }
      }
      ```

      On all screens larger than 800 pixels,
      make the header background gray.

      {:.checkpoint}
      On big screens, your header should now be an image.


  - content: |

      ## Good cases for media queries

      - Horizontal menu becomes stacked on mobile
      - Plain background on mobile, photo on desktop
      - Grid layout becomes column on mobile
      - Sidebar hidden on mobile


  - content: |

      ## Layout switching

      ```css
      @media (max-width: 800px) {
        .main-menu {
          flex-direction: column;
        }
      }
      ```

      On all screens **smaller** than 800 pixels,
      make the main menu use a column layout.

      {:.checkpoint}
      On small screens, the main menu should be stacked.

  - content: |

      ## What we learned

      - Media query structure
      - Min width and max width settings



---