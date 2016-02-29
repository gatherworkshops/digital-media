---
layout: chapter
title: Welcome Section
slides:


  - class: title-slide
    content: |

      ![Gather Workshops Logo]([[BASE_URL]]/theme/assets/images/gw_logo.png)

      # Stacked Layouts

      _Designing your content_




  - content: |

      ## Content Section

      Add to your `index.html`, on a new line after your closing `</header>` tag:

      ```html
      <header class="page-header">
          <h1>My Awesome Website</h1>
      </header>

      <section class="page-content">

          <h2>Hello there, amazing person!</h2>

          <p>
          This is a site all about my favourite stuff, 
          thanks so much for visiting.
          </p>

      </section>
      ```
      {:data-line="1-4"}

      We will use this `page-content` section on every page,
      but we will change the content inside it for each page.

    notes: |
      A section is just another layout rectangle, like header.

      It has no design by itself, it's just an invisible box to hold content.

      First we will put in some content, then we will design the section.

      Notice that we have given this section a name, or "class".





  - content: |

      ## Content Section Design

      Add to your `style.css`:

      ```css
      .page-content {
          background-color: #222222;
          padding: 30px;
          width: 700px;
          margin: 0 auto;
          margin-top: 30px;

          color: #FFFFFF;
          font-size: 14px;
          line-height: 130%;
      }
      ```

      This code will give you a starting point to begin
      designing your content section.

    notes: |
  
      Our content is on the page, but it is just kind of... floating.

      By adding some CSS, we can make our content section visible and start working on how we'd like it to look.

      In our HTML, we gave our section the class `page-content`, so we can use that name to apply styling from our CSS code.

      The blank line is just to split up the layout stuff from the text design stuff, it doesn't affect the code.




  - content: |

      ## Content Section Ideas

      <iframe height='450' scrolling='no' src='//codepen.io/gatherworkshops/embed/rVzZRp/?height=450&theme-id=16068&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/gatherworkshops/pen/rVzZRp/'>rVzZRp</a> by Gather Workshops (<a href='http://codepen.io/gatherworkshops'>@gatherworkshops</a>) on <a href='http://codepen.io'>CodePen</a>.
      </iframe>

      _Take a few minutes to make your content section_<br>
      _look how you want it._

    notes: |
      Take some time to tweak the CSS for your content section.

      There are a whole bunch of different design ideas you can play with! Ask a mentor if you've got an idea but you're not sure how to achieve it.


      

  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## Stacked Layouts: Complete!

      Great, now let's explore how we'll host our own site...

      [Take me to the next chapter!](infrastructure.html)


    notes: |

      Great! Now that we know the basics, let's get started on our own projects.

---