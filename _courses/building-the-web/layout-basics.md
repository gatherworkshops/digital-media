---
layout: default
title: Stacked Layouts
slides:


  - class: title-slide
    content: |

      # Stacked Layouts

      _Laying out your content_


  - content: |
      ## Block Elements

      Block elements are the "building blocks" of our website. 

      Block elements are used for layout, and can contain other elements.

    notes: |
      `header` might contain our h1 and menu bar<br>
      `section` could be an intro, gallery, or general info<br>
      `footer` might contain copyright and contact info

      Pages often have one **header**, lots of **sections** and one **footer**.

  
  - content: |
      ## Header HTML

      Our header block will contain the profile pic, 
      "Grumpy Cat" heading and the first paragraph of text.

      **In your HTML, on the line *before* the profile pic:**

      ```html
      <header class="page-header">
      ```
      {:.big-code style="max-width:600px; margin:0 auto;"}

      **In your HTML, *after* the first paragraph:**

      ```html
      </header>
      ```
      {:.big-code style="max-width:600px; margin:0 auto;"}

      {:.checkpoint}
      Nothing should happen yet!

    notes: |

      Notice that this time we have added the class in the HTML *before* creating a matching rule in the CSS.

      That's okay - nothing will happen until both parts have been done.

      The html simply ignores any class rules that don't exist.

  
  - content: |
      ## Header Styles

      In your CSS, on a new line,
      design a class rule for the header.

      ```css
      .page-header {
        background-color: darkblue;
        color: white;
        font-size: 22px;
        font-weight: bold;
        text-align: center;
      }
      ```

      {:.checkpoint}
      The header should have large, centered, bold text.

    notes: |

      Web designers often use really obvious background colour or borders on their elements while they are designing, so that it is easy to see where the edges of the element are.

      Once you are happy with your header, you can remove the line `background-color: darkblue;` so that your header becomes see-through.


  - content: |
      ## Info Section HTML

      This content block is a **section** not a **header**, 
      so we use the `section` tag to create this block.

      **In your HTML, *before* the second paragraph:**

      ```html
      <section class="info-section">
      ```
      {:.big-code style="max-width:600px; margin:0 auto;"}

      **And *after* the third paragraph:**

      ```html
      </section>
      ```
      {:.big-code style="max-width:600px; margin:0 auto;"}

      {:.checkpoint}
      Nothing will happen yet, we need a CSS rule!


  - content: |
      ## Info Section Styles

      Now we want a box around the other two paragraphs.

      **In your CSS, on a new line:**

      ```css
      .info-section {
        background-color: yellow;
        padding: 20px;
        margin-top: 30px;
        margin-bottom: 30px;
      }
      ```
      {:.big-code}

      {:.checkpoint}
      There should now be a yellow block around two paragraphs.
    
    notes: |

      Just like before, once you are happy with the layout you can change the background colour to whatever you like.

      In this case we recommend a `white` background.


  - content: |
      ## Gallery Section HTML

      Now create the section block around your gallery images.

      **In your HTML, *before* the first gallery image:**
      
      ```html   
      <section class="gallery-section">
      ```
      {:.big-code style="max-width:600px; margin:0 auto;"}

      **And *after* the last gallery image:**

      ```html
      </section>
      ```
      {:.big-code style="max-width:600px; margin:0 auto;"}

      {:.checkpoint}
      Nothing happens, create a CSS rule!
    

  - content: |
      ## Gallery Section Styles

      We can style our gallery section the same way.

      **In your CSS:**

      ```css
      .gallery-section {
        background-color: darkgreen;
        text-align: center;
      }
      ```
      {:.big-code}

      {:.checkpoint}
      You should now have a dark green section around your gallery images.

    notes: |

      Once you are done, you can remove the background colour on the gallery too.

  - content: |
      ## Gallery Image Styles

      We can also use a trick to style the images *inside* the 
      gallery section, without adding a class to every single one.

      **In your CSS, on a new line:**

      ```css
      .gallery-section img {
        border: 5px solid white;
        height: 150px;
      }
      ```
      {:.big-code}

      {:.checkpoint}
      Your images should be small with white borders.

    notes: |
      
      This CSS rule has two parts to its name. When a rule has more than one part to it, we can read it backwards to see what it's doing.

      A space means "look inside".

      So this rule says "Apply to all `img` elements **inside** `.gallery-section`."


  - content: |
      ## Element Selectors

      Rather than always using classes, we can also choose 
      to style all HTML elements of the same type.

      **At the top of your CSS, on a new line:**

      ```css
      header,
      section {
        width: 700px;
        margin-left: auto;
        margin-right: auto;
        line-height: 130%;
      }
      ```

      {:.checkpoint}
      All your block should be centered on the page.

    notes: |

      This is an **element rule** just like we did for the `body` element earlier.

      In this rule, the `,` comma means "and".

      So this rule says "Apply to all `header`s **and** all `section`s"



  - content: |
      ## Tidy Up

      If you haven't already done it, remove the 
      background colours we used for planning our layout.

      **In your CSS:**

      - Find `.page-header` and remove the background
      - Find `.info-section` and change background to white
      - Find `.gallery-section` and remove the background

      {:.checkpoint}
      My page looks awesome now!

    notes: |

      You may have done this as we went along, but if not you should tidy it up now!

  - content: |
      ## Grumpy Cat Output

      Your own output window should now look like this:

      <div style="height:570px" data-height="570" data-theme-id="0" data-slug-hash="yyrQMr" data-default-tab="result" data-user="gatherworkshops" class='codepen'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/yyrQMr/'>yyrQMr</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.</div>
      <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

      If it doesn't, check that all your styles are correct! 
    
    notes: |

      Your site should look a bit like this, but may include a few tweaks of your own!

  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## Stacked Layouts: Complete!

      Woohoo! HTML and CSS masters!

      [Take me to the next chapter!](infrastructure.html)


    notes: |

      Woohoo! HTML and CSS masters!

---