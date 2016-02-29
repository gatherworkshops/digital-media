---
layout: chapter
title: Tidy Layouts
slides:

    - class: title-slide

      content: |

        ![Gather Workshops Logo]([[BASE_URL]]/theme/assets/images/gw_logo.png)

        # Tidy Layouts
        _Organising content with HTML and CSS_


      notes: |

        :)



    - content: |

        ## Otter Page Layout Demo

        <p data-height="550" style="height:550px;" data-theme-id="19418" data-slug-hash="yerRvR" data-default-tab="result" data-user="gatherworkshops" class='codepen'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/yerRvR/'>Otter Challenge Layout Demo</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
        <script async src="//assets.codepen.io/assets/embed/ei.js"></script> 

        In this chapter we'll use both HTML and CSS to add some structure.



    - content: |

        ## Everything is Boxes

        Layouts are made entirely of boxes




    - content: |

        ## The "Whole Page" Box

        Our whole page comes wrapped up in a box by default. 

        ```css
        html {
          background-color: silver;
        }
        ```
        {:.big-code}

        The element which wraps around your whole 
        page is called... `html`! And we can style it!

        Your background should turn grey.
        {:.checkpoint}



    - content: |

        ## Background Images

        ```css
        html {
          background-color: silver;
          background-image: url(http://tiny.cc/otter-pic);
        }
        ```
        {:.big-code data-line="1-2, 4"}

        You can also add an image as a background.

        You should see your chosen image in the background.
        {:.checkpoint}




    - content: |

        ## Sizing a Background Image

        ```css
        html {
          background-color: silver;
          background-image: url(http://tiny.cc/otter-pic);
          background-size: cover;
          background-attachment: fixed;
        }
        ```
        {:.big-code data-line="1-3, 6"}

        A single image can be stretched to fit any screen size,
        and can be "fixed" to keep it from scrolling.

        Your image should fill the whole background.
        {:.checkpoint}






    - content: |

        ## Creating Your Own Boxes

        We can also create our own boxes. 

        We will add one around all our content.



    - content: |

        ## Find the "Start" and "End" Points

        To add our own box we need to identify the start and end



    - content: |

        ## Add Section Tags

        ```html
        <h1 class="pageHeading">Otters</h1>

        <p class="tagline">
        They're otterly adorable.
        </p>

        <section>

        ... subheadings and paragraphs and images here ...

        </section>
        ```
        {:data-line="1-6, 8-10"}

        Add in 'section start' and 'section end' tags 
        at the correct positions in your HTML code.

        Nothing will change visually, yet...
        {:.checkpoint}




    - content: |

        ## Name Your Section

        ```html
        <section class="pageContent">
        ```
        {:.big-code}

        By default, a `section` box looks like nothing. Sad face.

        Give your section a class name so it can be styled.
        {:.checkpoint}


    - content: |

        ## Create a New Design Rule

        ```css
        .pageContent {
          background-color: white;
        }
        ```
        {:.big-code}

        Check that your section and rule are linked
        by adding a background colour.

        Your page content should now be inside a white box.
        {:.checkpoint}




    - content: |

        ## Section Styles

        ```css
        .pageContent {
          background-color: white;
          padding: 30px;
          border-radius: 10px;
          box-shadow: 5px 5px 5px black;
        }
        ```
        {:.big-code data-line="1-2, 6"}

        And if it works, add more style.

        Your text should move in from the edges.
        {:.checkpoint}


    - content: |

        ## Centering Page Content

        ```css
        .pageContent {
          background-color: white;
          padding: 30px;
          border-radius: 10px;
          box-shadow: 5px 5px 5px black;
          width: 500px;
          margin-left: auto;
          margin-right: auto;
        }
        ```
        {:.big-code data-line="1-5, 9"}

        You can center-align your whole box by giving it 
        a fixed width and using automatic margins.

        Your section should sit in the middle of the page.
        {:.checkpoint}



    - content: |

        ## Vertical Alignment

        ```css
        .pageContent {
          background-color: white;
          padding: 30px;
          border-radius: 10px;
          box-shadow: 5px 5px 5px black;
          width: 500px;
          margin-left: auto;
          margin-right: auto;
          margin-top: 500px;
        }
        ```
        {:.big-code data-line="1-8, 10"}

        Last but not least, we can use vertical margins to 
        make more room for our background image to be seen.




    - content: |

        ## Final Result

        <p data-height="550" style="height:550px;" data-theme-id="19418" data-slug-hash="yerRvR" data-default-tab="result" data-user="gatherworkshops" class='codepen'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/yerRvR/'>Otter Page Layout Demo</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
        <script async src="//assets.codepen.io/assets/embed/ei.js"></script> 

        Your own output should now look something like this.
        {:.checkpoint}




    - content: |

        ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

        ## Tidy Layouts: Complete!

        And you're done! Your first web page is complete.

        [What did you think? Let us know!](http://gathergather.co.nz/workshops/feedback/digital-media-web-dev-taster/)



      notes: |

        Great! Now that we know the basics, let's get started on our own projects.

---