---
layout: chapter
title: Styley Design
slides:

  - class: title-slide
    content: |

      # Styley Design

      _Designing your content_

    notes: |

      In website development, we use code describe the content _and_ the design.

      We can use CSS code to tell our web pages how our content should look.




  - content: |

      ![Icecream Scoops](assets/images/icecream-scoops.png){: width="220"}

      ## CSS With Icecream

      Open this link in a new tab: <a href="http://codepen.io/gatherworkshops/pen/yyrQpd?editors=110" target="_blank">Icecream Code</a>
      We'll use CSS to make it look way better.

    notes: |

      Here's another activity for you, this time using Icecream to explore CSS!

      Open up the CodePen link and then continue to the next slide for instructions.




  - content: |

      ## CodePen Editor

      ![Screenshot of CodePen UI](assets/images/codepen-css.png)

      Open up both your HTML and CSS panels in CodePen.

    notes: |

      This time in CodePen we need to have both the HTML and CSS code panels open.

      To apply design using CSS, we'll need to use both.




  - class: demo
    content: |

      <iframe src="assets/demos/icecream/"></iframe>

      ## Icecream Example

      We will use code to make our output look like this.

    notes: |

      After we've completed all the steps in this chapter, your final output should look something like this.



  - content: |

      ## Designing a Class

      In your CSS panel, create the `main-heading` class.

      ```css 
      .main-heading {
        color: hotpink;
        font-size: 100px;
        text-align: center;
        font-family: Comic Sans MS;
      }
      ```
      {:.big-code}

      Nothing on your page will change yet!
      {:.checkpoint}

    notes: |

      This class describes what a "main-heading" should look like.

      This class says that anything called "main-heading" will be hot pink with a font size of 100 pixels. It will also be center-aligned and the font will be Comic Sans.

      Problem is, we don't have anything called "main-heading" on our page yet.

      See the next slide for how to apply this class.

      

  - content: |

      ## Applying a Class

      ```html
      <h1 class="main-heading">Icecream</h1>
      ```
      {:.big-code}

      To apply a class, we add the `class` attribute to an opening HTML tag.

      Your main heading should now be large, pink and centered.
      {:.checkpoint}

    notes: |

      If your CSS didn't work, check for these common problems:

      - The class name `main-heading` must be spelled exactly the same in both the CSS and the HTML
      - In the CSS there is a full stop before the class name, in HTML there is not.
      - Your CSS class must have opening and closing brackets.
      - Your CSS class must have a semicolon ; on the end of each line.




  - content: |

      ## Modifying a Class

      If we ever want to change how something looks,
      we can add or remove lines from its class.

      ```css
      .main-heading {
        color: hotpink;
        font-size: 100px;
        text-align: center;
        font-family: Comic Sans MS;
        text-shadow: 2px 2px 2px brown;
      }
      ```
      {:data-line="1-5, 7"}

      Your main heading should now have a drop shadow.
      {:.checkpoint}


    notes: |

      To change how things look on our page, we create classes for each piece
      of our design and we update those classes as needed.

      It's best practice to avoid creating more than one class with the same name in your CSS - all design for a particular element should be in a single class definition.




  - content: |

      ## Styling our Tagline

      Use what you've learned about classes to design your `tagline`.
      That's the paragraph directly below the main heading.

      ```html
      <p class="tagline">The icy summer treat of New Zealand</p>
      ```
      {:.big-code}

      This time, add the class in the HTML before doing the CSS.
      {:.checkpoint}


    notes: |

      You can create the CSS class first, or you can add the HTML class first - either way is fine!

      As long as the names match up, you can do the steps in any order.

      Just remember that you won't see any changes until you've done both steps!



  - content: |

      ## Designing our Tagline

      Use what you've learned about CSS classes to design your `tagline`.

      ```css
      .tagline {
        color: brown;
      }
      ```
      {:.big-code}

      Add some lines to make your tagline text bigger, centered and in Comic Sans.
      {:.checkpoint}


    notes: |

      You can add as many lines to each CSS class as you like, as long as they are all between the curly brackets.



  - content: |

      ## Styling Images

      We can also style images using CSS, such as the
      image on our page with the class `icecream-scoops`.

      ```css
      .icecream-scoops {
        width: 300px;
      }
      ```
      {:.big-code}

      Your icecream scoops should now be much smaller.
      {:.checkpoint}


  - content: |

      ## Aligning Images

      To center-align images, you need three extra lines of CSS:

      ```css
      .icecream-scoops {
        width: 300px;
        display: block;
        margin-left: auto;
        margin-right: auto;
      }
      ```
      {:.big-code data-line="1-2, 6"}

      Your icecream scoops should now be centered.
      {:.checkpoint}


    notes: |

      Images are weird, they're not text so we can't use text-align to center them.

      Instead, we have to first tell an image that it is a "block" element, then we need to make it have automatic spacing on either side, to push it to the middle.

      Very strange, but it should make a little more sense once we cover alignment and stacked layouts.




  - content: |

      ## Styling all Subheadings

      You can style all tags of one type by using the
      tag name instead of a class name, without the full stop.

      ```css
      h2 {
        color: hotpink;
        font-size: 30px;
      }
      ```
      {:.big-code}

      All your subheadings should now be hot pink.
      {:.checkpoint}
      

    notes: |

      Rather than adding a class to every single element, we can also design based on the **type** of element.

      When styling in this way, the name of the CSS rule is the tag name rather than a class name, and it doesn't have a full stop at the start.




  - content: |

      ## Styling all Paragraphs

      Use what you learned about styling by tag name
      to style all your paragraphs to be:

      - 14px in size 
      - Verdana as the font
      - Coloured brown
      - Line height of 150%

      Create a CSS rule to make your paragraphs look like the description.
      {:.checkpoint}


  - content: |

      ## Vertical spacing

      

  - class: demo
    content: |

      <iframe src="assets/demos/icecream/"></iframe>

      ## Final Result

      Your own output window should now look something like this.

      TODO: [Edit on CodePen](http://codepen.io/gatherworkshops/pen/gbyXgo/)



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

      Great, now let's get started on our own projects...

      [Take me to the next chapter!](layout-basics.html)


    notes: |

      Great! Now that we know the basics, let's get started on our own projects.






---