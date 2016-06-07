---
layout: default
title: Coding Content
slides:

    - class: title-slide

      content: |

        # Coding Content

        _Putting content on your page with HTML_

      notes: |

        Every web page has HTML at its foundations. 

        An HTML file consists of the text and images which make up the content of the web page, with some extra code added to describe the different types of content.

        HTML stands for "HyperText Markup Language", and we use HTML code to _mark up_ our content. 


    - content: |

        ## HTML With Alpacas

        Open this link in a new tab: <a href="http://codepen.io/gatherworkshops/pen/KDvtC?editors=100" target="_blank">Alpacas Code</a>

        Keep it open! We are going to be using HTML
        to make it look way better.

      notes: |

        To introduce you to HTML code, we've created some text content for you to mark up.

        Open the Alpacas Code activity and then switch to the next slide to start working through the steps.




    - content: |

        ## CodePen Editor

        ![Screenshot of CodePen UI](assets/images/codepen-html.png){:height="350"}

        CodePen shows us our code on the left,
        and the output on the right.

      notes: |

        The grey text at the top is a comment. It is not visible in the output.

        The white text is code. It is visible in the output.



    - class: demo
      content: |

        <iframe src="assets/demos/alpacas/"></iframe>

        ## Alpaca Text Example

        We will use code to make our output look like this.

      notes: |

        After we've completed all the steps in this chapter, your final output should look something like this.


    - content: |

        ## Headings

        ```html
        <h1>Alpacas</h1>

        An alpaca is a domesticated species of
        South American camelid. It resembles a
        small llama in appearance.
        ```
        {:.big-code .fit-code data-line="3-5"}

        Add heading tags around the word `Alpacas`.

        The word "Alpacas" should now be big and bold.
        {:.checkpoint}

      notes: |

        Let's start with some really common HTML elements.

        The first line is how we make large heading text, using the `h1` element. That's a "one" after the "h" by the way!
        
        See how the start and end of the element are written the same, except for the  extra "slash" at the end? That's a really common format in HTML.

        `<h1>` means _"start the heading here"_
        `</h1>` means _"end the heading here"_



    - content: |

        ## Subheadings

        Now use `<h2>` tags to make `Alpaca Hair` and `Habitat` big.

        ```html
        <h2>Alpaca Hair</h2>
        ```
        {:.big-code .fit-code}

        Your page should now have a main heading and two subheadings.
        {:.checkpoint}



      notes: |

        Just like we used `h1` for the most important title on the page, we can use `h2` for headings which are second most important.

        The start and end of the element are still written the same, with the extra "slash" in the closing tag.


    - content: |

        ## Sub-Subheadings

        `h1` is the biggest heading
        `h2` is the second biggest heading
        `h3` is the third biggest heading

        `h6` is the smallest heading


      notes: |

        The biggest heading is `h1` and the smallest heading is `h6`.

        There are only six sizes, but you should very rarely need to use all of them.

        If you somehow manage to get down to `h4` you may need to re-think the structure of your web page!


    - content: |

        ## Paragraphs

        Now use `<p>` tags to split up your paragraphs.

        ```html
        <p>
        An alpaca is a domesticated species of 
        South American camelid. It resembles a 
        small llama in appearance.
        </p>
        ```
        {:.big-code .fit-code data-line="2-4" }

        Put a `<p>` *before* each paragraph,
        and a `</p>` *after* each paragraph.

      notes: |

        Paragraphs of text use the `p` element.

        A paragraph of text will automatically have some space before and after it.


    - content: |

        ## Link Tags

        ```html
        <a>Wikipedia</a>
        ```
        {:.big-code .fit-code}

        In the last paragraph, add `a` tags around the word Wikipedia.

        Nothing will change yet, we have more to do!
        {:.checkpoint}


      notes: |

        Links help us connect our website to the rest of the World Wide Web.

        The `a` element stands for "anchor" but you can think of it as meaning "action" if that's easier to remember. Clicking a link takes you to another web page.


    - content: |

        ## Link href

        Now add the `href` attribute to the opening tag.

        ```html
        <a href="#">Wikipedia</a>
        ```
        {:.big-code .fit-code}

        Your link should be blue, but we need another step to make it clickable.
        {:.checkpoint}

      notes: |

        Links help us connect our website to the rest of the World Wide Web.

        The `a` element stands for "anchor" but you can think of it as meaning "action" if that's easier to remember. Clicking a link takes you to another web page.


    - content: |

        ## Link URL

        Replace the hashtag with a link to an actual web page.

        ```html
        <a href="http://en.wikipedia.org/wiki/Alpaca">Wikipedia</a>
        ```
        {:.fit-code}

        Your link should now work when you click it.
        {:.checkpoint}

      notes: |

        The attribute `href` stands for "hyperlink reference" which is just a fancy way of saying "website address".

        The `href` attribute is what we use to tell a link where it should link to.


    - content: |
    
        ## Image Tags

        Add an `img` tag to the very bottom of your code:

        ```html
        <img src="#">
        ```
        {:.big-code .fit-code}

        You should see a small box with a "broken image" icon.
        {:.checkpoint} 

      notes: |

        The image tag is an odd one - where is its closing tag?

        That's the trick, it doesn't have one! Image tags need only an opening tag, plus the `src` attribute, which say where on the Internet the actual image is stored.

        Here we are using a hashtag as the source. Just as for links, we can use the hashtag until we know the actual image URL we want to use.


    - content: |

        ## Image Source

        Find an image online, and copy the link to it.

        ```html
        <img src="http://placekitten.com/200/300">
        ```
        {:.big-code .fit-code}

        Replace the `#` as the `src` value, using paste.

        Your image should now be visible.
        {:.checkpoint}

      notes: |

        Setting the image source to a valid image link should make the image show up on your page.

        Occasionally this won't work, such as if you link directly from Google's cached images, or if you link to an image on a site which is blocking image linking.

        Linking to an image doesn't copy it to your site, it loads the image from the original location every time you load the page. If the original owner takes the image offline, it will disappear from your site.


    - content: |

        ## Image Size

        ```html
        <img src="http://placekitten.com/200/300" height="100">
        ```
        {:.big-code .fit-code}

        **`height` is the height of the image**<br>
        This is optional, it is the height in pixels. 

      notes: |

        The width and height of an image is considered to be part of its design, so we should really be setting the width and height from CSS **not** from HTML.

        We'll use the `height` attribute for now, because we haven't done CSS yet.


    - content: |

        ## More Images

        Add at least two more images to your page.

        ```html
        <img src="http://placekitten.com/200/300" height="100">
        <img src="http://placekitten.com/300/400" height="100">
        <img src="http://placekitten.com/100/150" height="100">
        ```
        {:.big-code .fit-code}

        Your page should now have at least three images.
        {:.checkpoint}

      notes: |

        Notice that you need a whole separate image tag for every image you want to include.

        Usually, you would put each image on a new line in your code to make it easy to read.


    - class: demo
      content: |

        <iframe src="assets/demos/alpacas/"></iframe>

        ## Final Result

        Your own output window should now look something like this.

        [Edit on CodePen](http://codepen.io/gatherworkshops/pen/gbyXgo/)

      notes: |

        Your HTML demo page should now be pretty much done!

        If you'd like to see the code we wrote for it, you can explore the HTML and CSS for it on [CodePen](http://codepen.io/gatherworkshops/pen/gbyXgo/)].

        If your own page doesn't look like the example, check that all your tags are correct!

        Remember most tags come in pairs:

            <h1> </h1>

            <h2> </h2>

            <p> </p>

            <a href="#"> </a>

        But images only need one tag:<br>
          
            <img src="#">



    - content: |

        ## Stuff We Covered

        - **Headings**
          Biggest is h1, smallest is h6, and size is based on heading importance
        - **Paragraphs**
          Split our content up into manageable pieces.
        - **Images**
          Don't have a closing tag, and use the `src` attribute to define an image.
        - **Links**
          Use the `href` attribute to link to another page on the web.
        {:.flex-list}


      notes: |

        We only covered a few HTML elements, but there is heaps that we can do with them!




    - content: |

        ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

        ## Coding Content: Complete!

        Great, now it's time to do some design...

        [Take me to the next chapter!](css-basics.html)

      notes: |

        Great, now it's time to do some design...


---