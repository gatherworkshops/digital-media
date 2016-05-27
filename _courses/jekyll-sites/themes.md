---
title: Themes

slides: 

  - content: |
      # Themes

    notes: |

      This chapter will cover splitting a header and footer out into separate files for easy maintenance.

  - content: |
      In a Jekyll site, the content is separate from the layout.

    notes: |

      By "separate" we mean that the content is written in one file, and the layout code is written in another file.

  - content: |
      Content is written in the pages where we want it, as normal.

    notes: |

      At the moment our pages contain all of their content **and** all of their layout HTML. We want to remove the layout from the pages, so that each `page.html` contains only its content.

  - content: |
      Design is applied by using a page template, 
      which in Jekyll is called a "layout".

    notes: |

      Once the pages contain only their content, and the layout is in a separate file, we can combine a single layout with multiple pages of content.

      Structuring our site this way means that we can change the layout in one place and have that change show up on every page.

  - content: |
      A page layout can be a single file
      with an area specified for the content.

    notes: |

      This is the simplest type of layout, and will be enough for many small websites.

  - content: |

      A page layout can also be made up of separate 
      pieces such as a header, content area and footer. 

      These pieces are known as "includes".

    notes: |

      More complex layouts made up of separate includes become useful when you have many layouts which have some parts in common and other parts different.

      For example, you may have a site where the layout has the same header, footer, and content area **except** the home page, which has a large slideshow at the top of the layout.

      Rather than having two layouts "home" and "page" which are the same except for the slideshow, you culd make the slideshow an include and only choose to show it on the home page.

      With this structure, you can still edit your header and footer code in a single place.

  - content: |
      Our theme will contain all layouts, includes, 
      stylesheets and design images for our site.

    notes: |

      We'll build up our theme as we go through this course.
  





  - content: |
      ## Creating a Theme

      We want to have one place where we keep all files
      related to the look and feel of our website.

    notes: |

      A Jekyll theme is a set of folders and files containing all the bits and pieces we need to achieve the desired appearance of our website.

  - content: |

      In your project folder,
      create a new folder called "theme".

      Create a theme folder.
      {:.checkpoint}

    notes: |

      By keeping all of our theme files in one folder, we could easily re-use this theme on another site by copying it. A whole new website with different content but the same design, really easy.





  - content: |
      ## Creating Layouts

      A layout defines one way that a page can be displayed.
      Each layout defines a content area and may use includes.

    notes: |

      You should have at least one layout for your site, though you can have as many as you need.

      The purpose of layouts is to reduce repetition of code.

  - content:

      In your theme folder, create a 
      new folder called `_layouts`.


    notes: |

      The underscore is a naming convention. That is, we don't need it but it is common in Jekyll sites to use underscores for theme-related folders.

      In Jekyll, folders with underscores generally contain files which are used in generating the output site, but which are not actual content to be directly copied to the site.

  - content: |

      Add a new line to your `_config.yml`,
      telling Jekyll the location of your layouts.

      ```yaml
      name: Jekyll Site
      version: 3.0.3

      # where things are
      layouts_dir:  ./theme/_layouts
      ```

    notes: |

      By default, Jekyll expects your layouts folder to be directly inside your project folder.

      We have moved the layouts folder inside a theme folder for tidiness, to keep our content separate from our design. 

      This is a good idea for keeping the project tidy, but it does mean that we need additional configuration to tell Jekyll that we moved the folder.

  - content: |

      Stop Jekyll by pressing `Ctrl + C` in the command line.

      Restart Jekyll with the new configuration
      by typing `jekyll serve` and pressing enter.

    notes: |

      When we make a change to the Jekyll config we need to restart Jekyll.

      This is because Jekyll only loads the config file once, when it starts. It doesn't notice changes to the config file once it is already running.

  - content: |

      In the layouts folder, create a 
      new file called `page.html`

    notes: |

      This file will define the basic layout for pages in our site.

  - content: |

      Add the following code to `page.html`:

      ```html
      <!doctype html>
      <html>
          <head>
              <title>My Awesome Site</title>
          </head>

          <body>
              {{ content }}
          </body>
      </html>
      ```

      Make sure to save your page layout!
      {:.checkpoint}

    notes: |

      You'll notice that this code is almost exactly the same as the code we have for our two existing pages, index and contact.

      The only difference is that instead of our content (a heading) we've added a special Jekyll tag `{{content}}`.

  - content: |

      The curly brackets are a placeholder for where we 
      want the page content to be inserted by Jekyll.

    notes: |

      The `{{ content }}` code will be replaced by all of the page content for each page which uses this layout.

      Currently our pages have all the HTML structure for the whole page. Our next goal is to remove the layout code from the individual pages, and use this layout instead.


  - content: |

      Use your site name from `_config.yml` as the page title:

      ```html
      <!doctype html>
      <html>
          <head>
              <title>{{ site.name }}</title>
          </head>

          <body>
              {{ content }}
          </body>
      </html>
      ```

    notes: |

      We can also use the double curly brackets to display other information, such as values from our site's `_config.yml`. Config values are accessed using {{ site.VALUE_NAME }}.

      Any custom values you add to `_config.yml` will be available across your whole site by using the `site.` prefix.






  - content: |
      ## Applying Layouts

      To apply our `page` layout to our pages,
      we need to modify each page's HTML file.

    notes: |

      Jekyll doesn't know to apply layouts automatically. We need to tell each of our pages which layout they should use.

  - content: |

      Open your `index.html` and remove everything
      except for the heading which says "Hello!"

      ```html
      <!doctype html>
      <html>

          <head>
              <title>My Jekyll Site</title>
          </head>

          <body>
              <h1>Hello!</h1>
          </body>

      </html>
      ```

      Your `index.html` should now only contain a heading.
      {:.checkpoint}

    notes: |

      We don't need this layout code in the individual pages anymore, because it will be supplied by our layout.

  - content: |

      Now at the top of your `index.html` add some front matter:

      ```html
      ---
      layout: page
      ---

      <h1>Hello!</h1>
      ```

      Make sure to save your changes!
      {:.checkpoint}

    notes: |

      The triple dash defines a "front matter" section for your page.

      Front matter goes at the very top of a file, and it tells Jekyll to process the file as a Jekyll page rather than a plain text file.

      This front matter tells Jekyll that this page should use the `page` layout.

      Layout names must match the name of a file in the layouts folder, without the `.html` on the end.

      We have a file `page.html` in our layouts folder, so the `page` layout is available for us to use.

  - content: |

      Preview your site and view source to check
      that the full HTML page is being built.

      Your page source should still contain `head` and `body` tags.
      {:.checkpoint}

    notes: |

      Your site should still run, and your index page should have the same code.

      Even though you've removed the structural HTML code from `index.html`, all of that code should still be there because we have applied the `page` layout.
  
  - content: |

      ### Challenge
      Apply the `page` layout to your contact page.

    notes: |

      Follow the same process as you did for the index page, then use View Source to check that your page is being built correctly.








  - content: |
      ## Styling

      All of your CSS should also be
      included in your site's theme.

    notes: |

      No notes


  - content: |

      In your theme folder, create a new folder called `css`.

    notes: |

      This folder doesn't start with an underscore, because we want the css folder to be copied over to our generated site.

  - content: |

      Inside the CSS folder, make a new file called `styles.css`.

    notes: |

      This file is a normal CSS file, which works exactly the same way as CSS in normal websites.

  - content: |

      Add some basic styling for your site.

      ```css
      /* import the Roboto font from Google Fonts */
      @import url(https://fonts.googleapis.com/css?family=Roboto:400,700,400italic,700italic);

      html {
        font-family: 'Roboto', sans-serif;
        font-size: 14px;
        line-height: 150%;
      }

      body {
        margin: 0;
        background: red;
      }

      ```

    notes: |

      This is "test" styling. We want it to be really obvious so we can see if we've linked up our CSS to our site correctly.

  - content: |

      Update your `page` layout to import the CSS.

      ```html
      <!doctype html>
      <html>

          <head>
              <title>My Jekyll Site</title>
              <link rel="stylesheet" href="/theme/css/styles.css">
          </head>

          <body>
              <h1>Hello!</h1>
          </body>

      </html>
      ```

    notes: |

      Because we are making this change in the `page` layout which is used by both `index.html` and `contact.html`, the styles should be applied to both pages.

      Something to note is that file paths in the generated site may be different from their path in the project structure.

      If you're unsure about file paths, you can look in the `_site` folder to check the path to the file you want.


  - content: |

      Refresh your page to check
      that the stylesheet is working.

      Your site should be horribly colourful.
      {:.checkpoint}

    notes: |

      Because we linked the stylesheet in the `page` layout, and both of our pages use that layout, the CSS is applied to both pages without us having to specify it individually for each page.


  - content: |

      Remove the background colour from your CSS.

      ```css
      /* import the Roboto font from Google Fonts */
      @import url(https://fonts.googleapis.com/css?family=Roboto:400,700,400italic,700italic);

      html {
        font-family: 'Roboto', sans-serif;
        font-size: 14px;
        line-height: 150%;
      }

      body {
        margin: 0;
        background: red;
      }

      ```

      Your site should be back to normal.
      {:.checkpoint}






      





  - content: |
      ## Includes

      These are re-usable pieces of code
      which can be used in multiple layouts.

    notes: |

      Even if we don't intend to use an include more than once, it can still help us to keep our code tidy by making it easy to split up logically discrete code into separate named files.

      For example, even with only one page layout it might still be helpful to have a header include, a nav include, and a footer include so that you can easily edit those pieces of your layout from individual files.

  - content: |

      In your theme, create a new folder called `_includes`.

    notes: |

      This folder starts with an underscore, because Jekyll will use the includes to generate output pages but won't copy the individual include files to our output site.

  - content: |

      Tell Jekyll the location of this folder.

      ```yaml
      layouts_dir: ./theme/_layouts
      includes_dir: ./theme/_includes
      ```

      Make sure to save your configuration!
      {:.checkpoint}

    notes: |

      As with the layouts, we need to tell Jekyll where it can find our includes.

  - content: |

      Restart Jekyll with the new configuration.

      Ctrl + C
      jekyll serve

    notes: |

      The configuration has changed, so restart Jekyll with the new config.


  - content: |

      In your includes folder,
      create a file called `header.html`

    notes: |

      No notes.



  - content: |
      Create some header code in `header.html`

      ```html
      <header>

          <h1>{{ site.name }}</h1>

          <nav>
              <a href="/">Home</a>
              <a href="/contact.html">Contact</a>
          </nav>

      </header>
      ```

      Save your new header include.
      {:.checkpoint}

    notes: |

      The header code should be familiar, it's just regular HTML with the extra Jekyll functionality to display the site name from `_config.yml` as we did for the tab bar title.

  - content: |

      In your `page` layout, include the header
      in the body, before your content.

      ```html
      <!doctype html>
      <html>
          <head>
              <title>My Awesome Site</title>
          </head>

          <body>

              {% include header.html %}

              {{ content }}

          </body>
      </html>
      ```

    notes: |

      Double brackets means output a simple value.

      Bracket percent means do some kind of processing.

      Includes must be processed using `{% %}` rather than just displayed using `{{ }}` because they might have special Jekyll tags in them which need to be processed befoer being displayed.


  - content: |

      Because we added the header to our template,
      it should show up on both of our pages.

      Check that your navigation works.
      {:.checkpoint}
      

  - content: |

      Add these styles to get your header looking snazzy:

      ```css
      header {
        background: #222;
        color: white;
        padding: 10px 30px;
        display: flex;
        align-items: baseline;
      }

      header h1 {
        font-size: 16px;
        flex-grow: 1;
      }

      header nav a {
        display: inline-block;
        color: white;
        font-size: 12px;
        text-transform: uppercase;
        letter-spacing: 2px;
        margin: 0 10px;
        text-decoration: none;
        border-bottom: 2px solid transparent;
      }

      header nav a:hover {
        color: lightblue;
        border-color: lightblue;
      }
      ```

  - content: |

      ### Challenge: Add Another Page

      Add a "shop" page and apply the same theme.
      Also add the new page to the navigation.

      Your site should have three pages, with a nav on every page.

    notes: |

      No notes

















  - content: |

      ## Images

      Page designs often use images,
      which we can include in our theme.

    notes: |

      For our Jekyll site, we need to think about the difference between "content" images and "design" images.

      Design images are part of our theme, and would make sense to use on another site.

      Content images are part of our website content, and are unique to this particular site.

  - content: |

      In your theme folder, 
      create a new folder called `img`.

    notes: |

      We're calling this folder `img` rather than `images` to keep us from confusing our design images (which go here) with our content images (which will be in another folder called `images`).

      This folder also does not start with an underscore. This is because we want our `img` folder to be included in the output site, so the live website can use the images.


  - content: |

      Download a Creative Commons background 
      for your website from Subtle Patterns.

      [Visit Subtle Patterns](http://subtlepatterns.com/){:target="_blank"}

    notes: |

      It's really important that we keep legal and ethical obligations in mind when sourcing images.

      You should use only images which you own, or which are clearly labeled as having a Creative Commons licence.

      Images from Subtle Patterns are "CC BY-SA 3.0", which they specify in their website footer.

      A CC BY-SA 3.0 licence means:

      - **CC: Creative Commons licence**
        Means you can use it for free
      - **BY: By Attribution**
        Means you need to link back to the original source
      - **SA: Share Alike** 
        Means any copies or modified versions must be shared with the same licence
      - **3.0: Licence version 3.0**
        The version of the CC licence to refer to for more information 


  - content: |

      Extract the zip file from Subtle Patterns and copy
      the pattern image to your `img` folder with a tidy name.

    notes: |

      Subtle Patterns gives you two sizes of the background, one at normal size and one 2x bigger.

      You can choose whichever you like, and copy it into your `img` folder.

      It would also make sense to rename the files to something short and clear like maybe "background.png", but this name is up to you.

  - content: |

      In your site folder, create a new page called `credits.html`.
      Add the credit for your image to this page and save.

      ```html
      ---
      layout: page
      ---

      <ul class="image-credits">

        <li>

          <img src="/theme/img/background.png">

          <div class="info">
            <span class="title">
              GPlay by <a href="http://dhesign.com/">Dimitrie Hoekstra</a> 
            </span>
            <span class="licence">Licence: CC BY-SA 3.0</span>
            <a class="source" href="http://subtlepatterns.com/gplay/">Original Source</a>
          </div>
        </li>

      </ul>
      ```

    notes: |

      By starting a page with all of your attributions right away, you can avoid the frustration of having to find them again later.

      You can attribute images in many different ways, and it's polite to attribute the image as clearly as possible - preferably right next to it.

      By keeping track of these attributions, you know where they came from and you can change the way they are displayed later.

  - content: |

      Add the credits page to your header navigation.

      ```
      <nav>
        <a href="/">Home</a>
        <a href="/contact.html">Contact</a>
        <a href="/credits.html">Credits</a>
      </nav>
      ```

    notes: |

      You can remove the credits link from your navigation **only if** you have appropriately attributed all borrowed content in another clear and appropriate way.


  - content: |

      And here's some CSS to format
      your image credits list.

      ```css
      .image-credits li {
        padding: 10px 0;
        border-bottom: 1px dotted #666;
        display: flex;
      }

      .image-credits img {
        width: 150px;
        margin-right: 15px;
      }

      .image-credits .title,
      .image-credits .licence,
      .image-credits .source  {
        display: block;
      }

      .image-credits .title {
        font-weight: bold;
        font-size: 16px;
        line-height: 200%;
      }
      ```



  - content: |

      You can now use the image in your CSS as usual:

      ```css
      body {
        margin: 0;
        background: url('/theme/img/background.png');
      }
      ```

    notes: |

      Note that the path to the image is through the `theme` and `img` folders.


#  - content: |
#
#      You can also use theme images in your layouts.
#      Save the image below to your theme `img` folder.
#
#    notes: |
#
#      No notes
#
#  - content: |
#
#      Add the image to your header using HTML.
#
#      ```html
#      <img src="/theme/img/logo.svg">
#      ```
#
#    notes: |
#
#      No notes






  - content: |
      ## Summary

      - **Layouts**
        Every page uses a layout, which defines a content area.
      - **Includes**
        Layouts can be made up of other pieces of code called includes.
      - **Images**
        Borrowed images must be Creative Commons and clearly credited.
      {:.flex-list}

    notes: |

      No notes

  - content: |

      ### Themes: Complete

      [Next Chapter](static-data.html)

    notes: |

      You've completed the Themes chapter, well done!

      Continue to the next chapter for more.



---
