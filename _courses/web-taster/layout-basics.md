---
layout: chapter
title: Styling Content
slides:

    - class: title-slide

      content: |

        ![Gather Workshops Logo]([[BASE_URL]]/theme/assets/images/gw_logo.png)

        # Tidy Layouts
        _Organising content with HTML and CSS_


      notes: |

        :)



    - content: |

        Layouts are made entirely of boxes



    - content: |

        Our whole page is already wrapped up in a box with the type 'html' which we can style

        ```css
        html {
          background: url(blah.jpg);
        }
        ```


    - content: |

        We can also create our own boxes. 

        We will add one around all our content.



    - content: |

        To add our own box we need to identify the start and end



    - content: |

        Then put the start and end in our code

        ```html
        <section>

        ...

        </section>
        ```


    - content: |

        But it looks like nothing. give it a name.

        ```html
        <section class="pageContent">
        ```


    - content: |

        Then create a basic style to test

        ```css
        .pageContent {
          background-color: white;
        }
        ```


    - content: |

        And if it works, add more style.

        ```css
        .pageContent {
          background-color: white;
          padding: 30px;
          border-radius: 10px;
          box-shadow: 5px 5px 5px black;
        }
        ```


    - content: |

        You can even center it on the page

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




    - content: |

        ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

        ## Tidy Layouts: Complete!

        And you're done! Your first web page is complete.



      notes: |

        Great! Now that we know the basics, let's get started on our own projects.

---