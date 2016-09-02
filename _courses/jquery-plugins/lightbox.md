---
title: Lightbox
slides:


##########


  - content: |

      # Lightbox
      _Popup image gallery_

    notes: |

      :)

    


##########


  - content: |

      ## Featherlight

      ![Lightbox Logo](assets/images/lightbox-logo.png)

      Provides a simple way to create a gallery 
      with both thumbnails and full-view images.

    notes: |

      :)

    


  ##########


  - content: |

      ## Download Lightbox

      Download Lightbox from [here](http://lokeshdhakar.com/projects/lightbox2/).

      Unzip the folder once it's downloaded - we'll need 
      to add some of the files to our site!


    notes: |

      :)

    

##########


  - content: |

      ## What's in the Zip

      There are three folders: css, img, js<br>
      And two files: index.html, README.markdown

      We need to copy just a few of the files:

      - css/lightbox.css
      - js/lightbox.js
      - img/close.png
      - img/next.png
      - img/prev.png
      - img/loading.png

    notes: |

      :)

    


##########


  - content: |

      ## Add the files to your site

      Copy the files specified on the previous slide,
      making sure to keep them in their correct folders!

    notes: |

      :)

    



##########


  - content: |

      ## Include the LightBox CSS and JavaScript

      Now that we've uploaded the files, we need 
      to tell our HTML page that they exist.
      
      First add the CSS to your page's head:
      
      ```html
      <head>
          <title>My Website</title>
          
          <link rel="stylesheet" href="css/lightbox.css">
      </head>
      ```
      {: data-line="1-3,5" }
      
      Then add the Lightbox JavaScript after jQuery:
      
      ```html
          <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
          <script src="js/lightbox.js"></script>
      </body>
      ```
      {: data-line="1,3"}


    


##########


  - content: |

      ## Initialise Lightbox

      This plugin doesn't need JavaScript initialisation.

      Instead, wrap each image in a link with a `data-lightbox` attribute.

      ```html
      <a href="image.png" data-lightbox="gallery">
          <img src="image.png">
      </a>
      ```


    

##########


  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200"}

      ## Lightbox: Complete!

      Great, now for the next bit...

      [Take me to the next chapter!](slideshow.html)

    notes: |

      Great! Now that we know the basics, let's get started on our own projects.

    


---







