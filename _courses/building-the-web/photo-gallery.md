---
layout: default
title: Photo Gallery
slides:

  - class: title-slide
    content: |

      # Photo Gallery
      _Display a series of images_



  - content: |
      ## Download Photos

      <img src="/Building-the-Web/slides/workshop/gallery/images/flickr-image-download.gif" width="100%">

      _Download some Creative Commons images from [Flickr](https://www.flickr.com/creativecommons/by-2.0/)_

    notes: |
      Find and download some images to use in your gallery.

      It is important to use images which are shared under a Creative Commons licence, which means that the owner of the image has given permission for it to be used by other people for free.

      You can use Flickr to search for Creative Commons images.

      Right click an image and choose "Save Image As..." to download it.



  - content: |

      ## Upload Gallery Images

      <img src="/Building-the-Web/slides/workshop/gallery/images/upload-gallery-image.gif" width="100%">

      _Upload the images to your `images` folder_

    notes: |
      Upload the photos to your Cloud Cannon project.

      The photos should all be uploaded to your `images` folder.




  - content: |

      ## Rename Image Files

      <img src="/Building-the-Web/slides/workshop/gallery/images/rename-gallery-image.gif" width="100%">

      _Change your image names to simple ones_

    notes: |
      Rename each of your photos to have simple names. This will make it easier to type the file names into your code.

      Remember that file names for websites should be all lowercase letters (no capitals!) and should have no spaces.

      Instead of a space, you can use underscore `_` or dash `-`.




  - content: |

      ## Adding Images

      In your `page-content` section, add the images:

        ```css
        <img src="images/first-pic.jpg">
        <img src="images/another-pic.jpg">
        <img src="images/cool-photo.jpg">
        <img src="images/cute-bunny.jpg">
        ```

      _Add the images to your HTML_

    notes: |

      Add at least three images to your pictures page.

      Don't worry about the sizes for now, we will fix that next.



  - content: |

      ## Gallery Styles

      ```css
      .gallery {
        background-color: #222222;
        padding: 30px;
        width: 700px;
        margin: 0 auto;
        margin-top: 30px;
        text-align:center;
      }
      ```

    notes: |
      :)





  - content: |

      ## Gallery Image CSS

      ```css
      .gallery img {
          height: 100px;
          border-width: 5px;
          border-color: #FFFFFF;
          border-style: solid;
          box-shadow: 3px 3px 5px 6px #000000;
          margin: 5px;
      }
      ```

    notes: |
      :)



  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## Photo Gallery: Complete!

      Great, now let's explore where we'll build our own site...

      [Take me to the next chapter!](videos.html)


    notes: |

      Great! Now that we know the basics, let's get started on our own projects.


---
