---
layout: chapter
title: Styling Content
slides:

    - class: title-slide

      content: |

        ![Gather Workshops Logo]([[BASE_URL]]/theme/assets/images/gw_logo.png)

        # Styley Design
        _Making things pretty with CSS_


      notes: |

        :)



    - content: |

        ## Naming Things

        Find the `h1` and add the class `pageHeading`

        ```html
        <h1 class="pageHeading">Otters</h1>
        ```
        {:.big-code}

        We can now design the heading using its class name




    - content: |

        ## Design by Code

        SCREENSHOT
        

        Open the CSS panel. 

        Design code is written in a separate place from the HTML content.



    - content: |

        ## Writing a Rule

        ```css
        .pageHeading {
          color: red;
        }
        ```
        {:.big-code}

        We create one design rule for each class name we make up.

        Your page heading should now be red.
        {:.checkpoint}




    - content: |

        ## Font Options

        ```css
        .pageHeading {
          color: red;
          font-family: Comic Sans MS;
          font-size: 50px;
        }
        ```
        {:.big-code data-line="1-2, 5" }

        Many lines of design can be added to a single rule.

        Your page heading should now be large and Comic Sans.
        {:.checkpoint}




    - content: |

        ## Text Design Options

        ```css
        .pageHeading {
          color: red;
          font-family: Comic Sans MS;
          font-size: 50px;
          text-align: center;
          text-shadow: 3px 3px 3px black;
        }
        ```
        {: data-line="1-4, 7" }

        You can also use CSS to align and decorate your text.

        Your heading should be centered with a drop shadow.
        {:.checkpoint}





    - content: |

        ## Identify the Tagline

        ```html
        <p class="tagline">
        They're otterly adorable.
        </p>
        ```
        {:.big-code}

        Follow the same process to design the tagline under your heading.

        Find the tagline and add a class.
        {:.checkpoint} 




    - content: |

        ## Create a matching design rule

        ```css
        .tagline {
          color: purple;
          font-family: Comic Sans MS;
          font-size: 25px;
          font-weight: bold;
          text-align: center;
        }
        ```
        {:.big-code}

        In your CSS panel, create a new rule for the tagline.

        Your tagline should be big, bold, purple and Comic Sans.
        {:.checkpoint}





    - content: |

        ## Challenge: Design your Subheadings

        Make a new design rule called `subheading` 
        and apply it to all three subheadings.



    - content: |

        ## Styling based on Element Type

        ```css
        p {
          color: darkblue;
          font-size: 16px;
          line-height: 150%;
        }
        ```
        {:.big-code}

        We can style all paragraphs at the same time.

        Notice there is no dot in front of the rule name
        when styling elements by their tag name!




    - content: |

        ## Styling all Images

        ```css
        img {
          border-style: solid;
          border-width: 5px;
          border-color: white;
          box-shadow: 5px 5px 5px black;
        }
        ```
        {:.big-code}

        We can use the same approach to design all images at once.





    - content: |

        ## Stuff We Covered

        - **Rule Structure**
          A design rule is made up of a target and a bunch of lines of design.
        - **Class Styles**
          A design rule can be applied to specific elements using a class name
        - **Element Styles**
          A design rule can be applied to all elements of one kind by the element name
        {:.flex-list}



    - content: |

        ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

        ## Styley Design: Complete!

        Great, now a wee bit about layout...

        [Take me to the next chapter!](layout-basics.html)


      notes: |

        Great! Now that we know the basics, let's get started on our own projects.

---