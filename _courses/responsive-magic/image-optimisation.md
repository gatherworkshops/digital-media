---
layout: default
title: Image Optimisation
slides:

  - class: title-slide

    content: |

      # Image Optimisation

      _Effective use of images on the web_

  - content: |

      ## View loading time for images

      The developer console shows a timeline
      of how long your images take to load.

      Try throttling to 3G to see the result for mobile.

  - content: |

      ## Gotta keep 'em small

      - Small images load faster
      - Data costs real money
      - Users give up on slow sites

  - content: |

      ## Always keep your originals

      Create a new folder called "originals"
      and copy in all your images.

      {:.checkpoint}
      You should now have two copies of every image.


  - content: |

      ## Downsizing image dimensions

      Using Photoshop or Pixlr, scale your background image
      down to **1280 pixels wide** and **1024 pixels high**.

      {:.checkpoint}
      Your header image should now be 1280 x 1024 pixels.

    notes: |

      Images should be only as big as needed.
      Resize the images in your site to sensible sizes.

      How did this affect the file size?


  - content: |

      ## Downsizing image quality

      Using Photoshop or Pixlr, save your 
      image as a JPG at 60% quality.

      {:.checkpoint}
      Your header image should now be lower quality.

    notes: |

      JPG images can be saved at different quality levels.
      Modify the quality of the images in your site.

      How did this affect the file size?

  
  - content: |

      ## Only load what you need

      ```css
      .header {
        background: url(images/background-small.jpg);
      }

      @media (min-width: 800px) {
        .header {
          background: url(images/background-large.jpg);
        }
      }
      ```

      Use media queries to only load big images when needed.

      {:.checkpoint}
      Your mobile site should be smaller than on desktop.


  - content: |

      ## Cropping images to size

      Using Photoshop or Pixlr, crop the three panel 
      images into square shapes of 400 x 400 pixels.

      {:.checkpoint}
      Your panel images should now be square.

  - content: |

      ## What we learned

      - Looking at file sizes and loading times
      - Downscaling image dimensions
      - Downscaling image quality
      - Cropping images to the correct shape

---