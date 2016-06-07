---
layout: default
title: jQuery Basics
slides:

  - title: title-page
    class: title-slide

    notes: |

      :)

    content: |

      # jQuery Basics
      _Using jQuery on top of HTML and CSS_


  ##########


  - title: weblanguages
    class: centered-slide

    notes: |

      :)

    content: |

      ## Languages of The Web

      ![HTML, CSS and JS Venn Diagram](assets/images/html_css_js.png){:height="500"}

      The visible part of every website is made up of these languages.


  ##########


  - title: html
    class: centered-slide

    notes: |

      :)

    content: |

      ## HTML: Coding Our Content

      ![](assets/images/google_html.png)


  ##########


  - title: css
    class: centered-slide

    notes: |

      :)

    content: |

      ## CSS: Coding Our Design

      ![](assets/images/google_html_css.png)


  ##########


  - title: javascript
    class: centered-slide

    notes: |

      :)

    content: |

      ## JavaScript: Coding Our Interactions

      ![](assets/images/google_html_css_js.png)


  ##########


  - title: getelements
    class: centered-slide

    notes: |

      We can use jQuery to find and capture elements on a page.

      To get an element or group of elements, we can use an ID, a class,
      or the type of element.

    content: |

      ## Getting Elements

      We can get an element the same way as in CSS,<br>
      with its `id` its `class` or the element tag type.
      
      ```javascript
      var header = $('#pageHeader');
      var allPhotos = $('.photo');
      var allImages = $('img');
      ```

      When we find an element, we give it a `var` name,<br>
      so we can do stuff to it later using an easy name.


  ##########


  - title: changingelements
    class: centered-slide

    notes: |

      One we've got an element, we can do stuff to it:

    content: |

      ## Changing Elements

      Add or remove a class to change how it looks:
      
      ```javascript
      var header = $('#pageHeader');
      header.addClass('fancyBorder');
      header.removeClass('plainBorder');
      ```

      Change its size and position:

      ```javascript
      var allPhotos = $('.photo');
      allPhotos.width(100);
      allPhotos.left(300);
      ```

      Fade in or fade out:

      ```javascript
      var allImages = $('img');
      allImages.fadeIn();
      allImages.fadeOut();
      ```


  ##########


  - title: jquerywithunicorns
    class: centered-slide

    notes: |

      Open this practice in codepen.

    content: |

      ![](assets/images/unicorn.svg){:height="300"}

      ## jQuery Basics with Unicorns

      <a href="http://codepen.io/gatherworkshops/pen/merJYM" target="_blank">Click here to start</a>


  ##########


  - title: unicornclasses
    class: centered-slide

    notes: |

      Open this practice in codepen.

    content: |

      ## Make January Golden

      In your JavaScript panel, add the class "gold" to January:

      ```javascript
      var january = $('#january');
      january.addClass('gold');
      ```

      **Challenge:**

      - February should be orange
      - March should be pink
      - April should be blue
      - The others can be any colour


  ##########


  - title: unicornsizes
    class: centered-slide

    notes: |

      Change the sizes of specific unicorns using their names.

      The CSS says that every `unicorn` should have a height of 50%.

    content: |

      ## Make the August Unicorn Smaller

      In your JavaScript panel:

      ```javascript
      var august = $('#august .unicorn');
      august.height('40%');
      ```

      **Challenge:**

      - May should be the same height as August
      - March should be 70% of the height of her box
      

  ##########


  - title: events
    class: centered-slide

    notes: |

      Sometimes we dont want to do things automatically as soon
      as the page loads.

      Sometimes we want to do something after a certain amount
      of time, or when something happens like a click or a keyboard
      button being pressed.

    content: |

      ## Flying Pegasus Ponies

      Create a function containing the code you want to run:
      ```javascript
      function fly() {
        var unicorn = $(this);
        unicorn.animate({'margin-bottom':'+=15'}, 1000);
        unicorn.animate({'margin-bottom':'-=15'}, 1000, fly);
      }
      ```

      Tell the selected objects when to run the function:
      ```javascript
      var pegasusPonies = $('.pegasus');
      pegasusPonies.click(fly);
      ```

      Pegasus ponies should now fly when clicked.
      <!-- .element class="checkpoint" -->


  ##########


  - title: unicornevents
    class: centered-slide

    notes: |
      :)

    content: |

      ## June's Disappearing Trick

      Create the `turnInvisible` function:
      ```javascript
      function turnInvisible() {
      var clickedUnicorn = $(this);
      clickedUnicorn.fadeOut();
      }
      ```

      Run the function when June is clicked:
      ```javascript
      var june = $('#june .unicorn');
      june.click( turnInvisible );
      ```

      June should now disappear when clicked.
      <!-- .element class="checkpoint" -->



  ##########


  - title: jumpingunicorns
    class: centered-slide

    notes: |
      :)

    content: |

      ## Jumping Jacks

      Here's a function to make a unicorn jump:

      ```javascript
      function jump() {
        var unicorn = $(this);
        unicorn.animate({'margin-bottom': '+=20'}, 300);
        unicorn.animate({'margin-bottom': '-=20'}, 300);
      }
      ```

      **Challenge:**<br>
      Make one of the unicorns jump when the `mouseover` event happens.


  ##########


  #- title: apps
  #  class: centered-slide

  #  notes: |

  #    Today we will be doing all of our coding online.

  #    We will be using GitHub to store our code, and Cloud9 to edit it.

  #  content: |

  #    ## Apps We Will Use

  #    **GitHub** for storing our code

  #    **Cloud9** for editing our code


  #########



  #- title: github
  #  class: centered-slide

  #  notes: |

  #    Sign up for GitHub. This is where all our code will be safely stored.

  #  content: |

  #    ![GitHub Logo](assets/images/github.png)
  #    <!-- .element height="300" -->
  #    ## Sign Up For GitHub

  #    [Click here to sign up for free](https://github.com/)


  ##########


  #- title: copyproject
  #  class: centered-slide

  #  notes: |
  #    Fork the project. This will copy all the project files to your
  #    own GitHub account, so you can save and make changes without
  #    changing the original one.

  #  content: |

  #    ## Fork the project


  ##########


  #- title: cloud9signin
  #  class: centered-slide

  #  notes: |

  #    Sign in to cloud9 using your github account.

  #  content: |

  #    ## Sign in to cloud 9


  ##########


  #- title: openproject
  #  class: centered-slide

  #  notes: |

  #    Open the project

  #  content: |

  #    ## Open the project



  ##########


  #- title: files
  #  class: centered-slide

  #  notes: |

  #    Project tour

  #  content: |

  #    ## Project files


  ##########


  - title: summary
    class: centered-slide

    notes: |

      Great! Now that we know the basics, let's get started on our own projects.

    content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){:height="200"}

      ## jQuery Basics: Complete!

      Great, now it's time to build our own...

      [Take me to the next chapter!](pixel-art.html)




---
