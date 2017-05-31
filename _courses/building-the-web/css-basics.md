---
layout: default
title: Styley Design
slides:

  - class: title-slide
    content: |

      # Styley Design

      _Designing your content_

    notes: |

      Now we're going to look at how we can use CSS code to apply design ideas to our HTML.


  - content: |

      ![Grumpy Cat](http://gathergather.co.nz/grumpy-cat.png){: width="300"}

      ## CSS With Grumpy Cat

      Open this link in a new tab: <a href="http://codepen.io/gatherworkshops/pen/yyrQpd?editors=110" target="_blank">Grumpy Cat Code</a>

      Keep it open! We are going to be using CSS
      to make it look way better.

      {:.checkpoint}
      I have the link open in a new tab.

    notes: |

      Meet Grumpy Cat. Grumpy Cat is going to help us learn some CSS.


  - content: |
      ## CodePen Editor

      ![Screenshot of CodePen UI](assets/images/codepen-css.png)

      CodePen can show us both our HTML and our CSS.

    notes: |

      You should now have a new CSS panel open in CodePen.

      The top panel is the HTML, which you are already familiar with.

      The bottom panel is the CSS, where we are going write all of our design code.


  - content: |
      ## Grumpy Cat Example

      <p data-height="550" style="height:550px;" data-theme-id="19418" data-slug-hash="yyrQMr" data-default-tab="result" data-user="gatherworkshops" class='codepen'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/yyrQMr/'>Otter Challenge Demo</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
      <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

      We will use CSS code to make our output look something like this.

    notes: |

      Using CSS we can add colour, fonts, sizes, background images, drop shadows, and heaps more.



  - content: |
      ## Classes

      In your **CSS panel**, add this piece of code which
      creates a new design rule called `profile-pic`.
      
      ```css 
      .profile-pic {
        width: 200px;
      }
      ```
      {:.big-code}

      In CSS, a design rule like this is called a **class**.

      {:.checkpoint}
      Nothing will happen yet!

    notes: |

      We use CSS to write code about how objects on our page should look.

      This code says that anything on our page with the class `profile-pic` should be displayed as 200 pixels wide.

      One little trick - don't forget the `.` dot in front of the class name in CSS!

      Also notice that in CSS we use `{` `}` curly wiggly mustache brackets. Mustaches are super fancy, just like CSS.

      The curly brackets `{` `}` are an easy way to spot CSS, compared to the `<` `>` angle brackets of HTML.

  - content: |
      ## Applying Classes

      <br>

      In your HTML panel, find the first image:

      ```html
      <img src="http://gathergather.co.nz/grumpy-cat.png">
      ```
      {:.big-code}

      <br>

      And add `class="profile-pic"`, so it looks like this:

      ```html
      <img class="profile-pic" src="http://gathergather.co.nz/grumpy-cat.png">
      ```
      {:.big-code}

      <br>

      {:.checkpoint}
      Cartoon Grumpy Cat should now be much smaller.

    notes: |
      When we've created a CSS class, we can apply that class to any HTML element.

      The class in the HTML and the class name in the CSS need to match **exactly**. 

      There is no dot before the class name in our HTML but we _do_ need that dot in our CSS code.

  - content: |
      ## Font Styles
      
      In your CSS panel, on a new line,
      create another class called `page-title`:

      ```css
      .page-title {
        font-family: "Comic Sans MS";
        font-size: 50px;
        text-align: center;
        text-shadow: 5px 5px 5px rgba(0,0,0,0.5);
      }
      ```

      <br>

      Then in your HTML, find the h1 and apply the class:

      ```html
      <h1 class="page-title">Grumpy Cat</h1>
      ```
      {:.big-code style="max-width:700px; margin: 0 auto;"}

      <br>

      {:.checkpoint}
      The page heading should now be fancy as!

    notes: |

      There are many font options in CSS. We can create another class to try them out.

      This class says that any HTML element with the class `page-title` should:

      - use the Comic Sans MS font
      - have a font size of 50 pixels
      - be centered
      - have a drop shadow

      The drop shadow is made up of:

      - `5px 5px 5px` <br> is offset left-right, offset up-down, and blur size
      - `rgba(0,0,0,0.5)` <br> is red, green, blue, and transparency

      You can tweak the numbers to see what happens.

      Red, green and blue are numbers between `0` and `255` that get mixed together.

      Transparency is a number between `0` and `1` which is how see-through it should be. 


  - content: |

      ## Whole Page Styles

      At the top of your CSS, on a new line,
      add this new design rule called `body`:

      ```css
      body {
        background-color: gold;
        background-image: url(http://subtlepatterns.com/patterns/food.png);
        font-family: sans-serif;
      }
      ```

      {:.checkpoint}
      Your background should now be yellow with a pattern.

    notes: |

      Notice that this new design rule doesn't have a dot in front of it.

      That's because this design rule is **not a class rule**. The dot means a rule is a class rule.

      This design rule is an **element** rule. That means it adds design to all HTML elements of that type, without us adding anything extra to the HTML.

      This element rule says that the `body` element should have:

      - a default background colour of gold
      - a background image which is a pattern
      - should use non-serif fonts

      The `body` HTML element is hidden in CodePen, but you will see it later when we make our own websites.


  - content: |

      ## Paragraph Styles

      Below the `body` rule you just created, on a new line,
      create another element rule for all `p` tags.

      ```css
      p {
        color: brown;
        font-size: 12px;
        line-height: 130%;
      }
      ```

      {:.checkpoint}
      Your paragraphs should now be brown and a bit bigger.

    notes: |

      This element rule applies to all `<p>` paragraph elements in your HTML.

      The rule says that paragraphs should:

      - have brown text
      - use a 12px font size
      - have lines that are 30% taller than normal




  - content: |

      ## Stuff We Covered

      - **Rule Structure**
        A design rule is made up of a target and a bunch of lines of design.
      - **Class Styles**
        A design rule can be applied to specific elements using a class name
      - **Element Styles**
        A design rule can be applied to all elements of one kind by the element name
      {:.flex-list}

    notes: |

      *No notes*



  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## Styley Design: Complete!

      Great, now let's take a quick look at layout containers...

      [Take me to the next chapter!](layout-basics.html)


    notes: |

      Great! Now that we know the basics, let's look at layout containers.






---