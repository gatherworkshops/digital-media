---
title: Slideshow
slides:

  - class: title-slide
    content: |

      # Slideshow
      _Adding simple movement_ 


  - content: |

      ## Backstretch

      ![Backstretch Logo](assets/images/backstretch-logo.png)

      Allows you to add a dynamically-resized, slideshow-capable 
      background image to any page or element.

      Download from [here](http://srobbin.com/jquery-plugins/backstretch/).

  - content: |
      
      ## Copy Backstretch to your site

      Find the `jquery.backstretch.min.js` file you 
      downloaded and copy it into your site's `js` folder.


  - content: |

      ## Include the plugin

      ```html
      <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
      <script src="jquery.backstretch.min.js"></script>
      ```

      Add a script tag after your jQuery import, linking to the plugin file.



  - content: |

      ## Initialise the plugin

      The backstretch website says to use the following code:

      ```javascript
      $.backstretch([
            "http://dl.dropbox.com/u/515046/www/outside.jpg",
            "http://dl.dropbox.com/u/515046/www/garfield-interior.jpg",
            "http://dl.dropbox.com/u/515046/www/cheers.jpg"],
            {duration: 3000, fade: 750}
      );
      ```

      You can copy this code from the Backstretch website.

      Make sure to put in your own image URLs!


  - content: |

      ## Header-only slideshow

      We can restrict our slideshow to be displayed inside an element.

      ```javascript
      $('header').backstretch([
          ...
      );
      ```

      We want ours to play in the background of the header, so we add `$('header')` to the start of our code.


  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200"}

      ## jQuery Plugins: Complete!

      Well done! Now you know the basics of using jQuery.

---
