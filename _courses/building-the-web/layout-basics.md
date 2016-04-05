---
layout: chapter
title: Stacked Layouts
slides:


  - class: title-slide
    content: |

      ![Gather Workshops Logo]([[BASE_URL]]/theme/assets/images/gw_logo.png)

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

      Our header block will contain the profile pic, "Grumpy Cat" heading and the first paragraph of text.

      **In your HTML, on the line *before* the profile pic:**

      ```html
      <header class="page-header">
      ```

      **In your HTML, *after* the first paragraph:**

      ```html
      </header>
      ```

      There should now be a dark blue box at the top of your page.

  
  - content: |
      ## Header Styles

      Let's design a header to contain Grumpy Cat's profile pic, page title, and first paragraph.

      **In your CSS, on a new line:**

      ```css
      .page-header {
        background-color: darkblue;
        color: white;
        font-size: 22px;
        font-weight: bold;
        text-align: center;
      }
      ```

      Our header block will have large, centered, bold text.


  - content: |
      ## Info Section HTML

      This content block is a section not a header, so we use the `section` tag.

      **In your HTML, *before* the second paragraph:**

      ```html
      <section class="info-section">
      ```

      **And *after* the third paragraph:**

      ```html
      </section>
      ```

      There should now be a yellow block around two paragraphs.


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


  - content: |
      ## Gallery Section HTML

      Now create the section block around your gallery images.

      **In your HTML, *before* the first gallery image:**
      
      ```html   
      <section class="gallery-section">
      ```

      **And *after* the last gallery image:**

      ```html
      </section>
      ```

      You should now have a dark green section around your gallery images.
    

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

      Then in your HTML code, add `section` tags around your gallery images. Remember to add the class!

      If you can't remember how, there is code on the next page...


  - content: |
      ## Gallery Image Styles

      We can also use a trick to style the images *inside* the gallery section, without adding a class to every single one.

      **In your CSS, on a new line:**

      ```css
      .gallery-section img {
        border: 5px solid white;
        height: 150px;
      }
      ```

      Your gallery images should now have white borders and all be the same height.

    notes: |

      This style says "find a block with the class `gallery`, then find every `img` element inside it and apply these styles"


  - content: |
      ## Element Selectors

      Rather than always using classes, we can also choose to style all HTML elements of the same type.

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

      All your sections (and your header) should now be centered on the page.


  - content: |
      ## Whole Page Styles

      When we have styles we want to apply to the whole page, we can target the `body`, because all other tags are between the `body` tags.

      **At the top of your CSS, on a new line:**

      ```css
      body {
        background-color: gold;
        background-image: url(http://subtlepatterns.com/patterns/food.png);
        font-family: sans-serif;
      }
      ```

      Your background should now be yellow with a pattern.


  - content: |
      ## Element Selectors

      Now all that we have to do is tidy up our colours. We need to remove the backgrounds we used for planning our layout.

      **In your CSS:**

      - Find `.page-header` and remove the background
      - Find `.info-section` and change background to white
      - Find `.gallery-section` and remove the background


  - content: |
      ## Grumpy Cat Output

      Your own output window should now look like this:

      <div style="height:570px" data-height="570" data-theme-id="0" data-slug-hash="yyrQMr" data-default-tab="result" data-user="gatherworkshops" class='codepen'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/yyrQMr/'>yyrQMr</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.</div>
      <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

      If it doesn't, check that all your styles are correct! 


  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## Stacked Layouts: Complete!

      Great, now let's explore where we'll build our own site...

      [Take me to the next chapter!](infrastructure.html)


    notes: |

      Great! Now that we know the basics, let's get started on our own projects.

---