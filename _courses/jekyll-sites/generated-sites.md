---
title: Generated Sites

slides:

  - content: |
      # Generated Sites

    notes: |

      This chapter will covers installing and running Jekyll, site structure, configuration, and creating pages.


  - content: |

      A **static website** contains only HTML, CSS and JS. 
      There is no server code or database.

    notes: |

      The word "static" means "unchanging". A static website displays the output of files you have written, as you wrote them. 

      In contrast, the word "dynamic" means "changeable". A dynamic website uses the files you have written to create pages as needed, for example creating a product page for every product in the database.

  - content: |
      A **Static Site Generator** is a computer program which 
      combines separate design and content into a static website.

    notes: |

      Using a static site generator we can still do many of the "dynamic" actions of a dynamic website, such as generating a product page for every product in a list (no databases though!).

      The main difference is that the files we publish are still static. We "dynamically" generate the "static" files for the website.


  - content: |

      Static site generators are helpful for creating simple sites
      where you want to easily maintain the content separate from
      the design, without using a CMS like wordpress.

    notes: |

      The layout is written in one file, and the content which should be inserted into the layout is written in another file.

      This makes it fairly easy to update content without worrying about accidentally breaking the layout.

      By letting a static site generator do the hard work, we don't have to worry about introducing complexity to our site by including a database and a server-side language like Python, Ruby or PHP.

      As a site gets bigger and more complex you may decide that it would be better to build a full-stack project using a database and a server-side language. 

      Static site generators are good for small to medium-sized sites, and it's up to you to decide if your site is big enough that it needs to evolve.








  - content: |
      ![Jekyll Logo](images/jekyll-logo.png)

      ## Jekyll
      {:.hidden}

      The most popular static site generator.

    notes: |

      Jekyll is the static site generator we will be using for this course.

      It's the most popular one in use today. It was created by engineers at GitHub, the most popular website for publishing and sharing open source code projects.


  - content: |

      There are many static site generators,
      each with different strengths.

      [Top static site generators](https://www.staticgen.com/)

    notes: |

      Jekyll is just one of many static site generators. Some other popular ones are Gitbook and Octopress. 

      Each static site generator has different strengths, so you might choose a different one for a different purpose.

      Once you understand how one static site generator works, it should be fairly straighforward to understand other ones with the help of tutorials on their websites.


  - content: |

      Jekyll was originally created for blogging, 
      but has evolved to support all kinds of sites.

    notes: |

      It's most commonly used for small promo websites, blogging, and for project documentation.

      Jekyll has support for blog posts, pages, and custom categories for a product shop or image gallery.

      Even this website and slideshow are built in Jekyll!

  - content: |

      Jekyll is a program that runs on your computer,
      converting project files into a live website preview.
    
    notes: |

      To use Jekyll, you install it on your computer and then run it from a website project folder. Jekyll then turns the website files into an actual website you can view in your web browser.


  - content: |

      Jekyll is written using the Ruby programming language, 
      so we need to install Ruby and then install Jekyll.

    notes: |

      If you are unable to install Ruby or Jekyll on your computer, we recommend creating an account with CloudCannon and skipping the install instructions here.

      Instead, go straight to creating a project and skip any bits talking about the command line.


  - content: |

      ### Install Ruby

      - **Windows**
        Download and run the installer
        [Download here](http://rubyinstaller.org/)
      - **Mac**
        Has Ruby pre-installed - yay!
      {:.flex-list}

      Run the installer and complete the installation process.
      {:.checkpoint}

    notes: |

      Ruby comes pre-installed on Macs, but you will still need to check that you have the correct version in the next step.

      Windows users need to run the installer.

  - content: |

      Open a command line so that we can check
      the status of our Ruby installation.

      - **Mac**
        Press Command + Space
        Type "Terminal"
        Press Enter

      - **Windows**
        Click "Windows"
        Click "Run"
        Type "cmd"
        Press Enter
      {:.flex-list}

      You should have CMD or Terminal open.
      {:.checkpoint}

    notes: |

      We'll be using the command line a lot when working with Jekyll, so you may want to lock the app to your taskbar or launcher bar for easy access.

  - content: |

      To check if Ruby is installed correctly, 
      type in `ruby -v` and press enter.

      The displayed Ruby version should be 2.0.0 or higher.
      {:.checkpoint}

    notes: |

      If you have a higher version than 2.0.0 that's fine, just make sure it's not version 1 of Ruby!

  - content: |

      ### Install Jekyll

      In your command window, type in 
      `gem install jekyll` and press enter.

      Wait for the Jekyll installer to complete.
      {:.checkpoint}

    notes: |

      The `gem` program was installed along with the ruby programming language. In Ruby, a gem is a program written in Ruby which has been published for other developers to download and use. Jekyll is a Ruby Gem. 

      You can browse other published gems on the [RubyGems](https://rubygems.org/) website.

  - content: |

      Check Jekyll is installed by typing in 
      `jekyll -v` and then pressing enter.

      Your Jekyll version should be 3.0.0 or higher.
      {:.checkpoint}

    notes: |

      If you have a higher version it's fine, it just means a new version of Jekyll has been released since these instructions were written. That's cool, new stuff!







  - content: |

      ## Creating a Project

      Create a new folder on your computer with 
      a name for your site, for example `jekyll-site`.

      This name can be changed later.

      Create a folder called `jekyll-site` in a safe place.
      {:.checkpoint}

    notes: |

      You can create this folder anywhere you like, but we recommend having a Projects folder where you keep all of your programming projects so you don't accidentally misplace them!

  - content: |

      Open the project folder in your favourite 
      text editor so we can begin adding files.

      Open your project in a text editor.
      {:.checkpoint}

    notes: |

      We recommend [Visual Studio Code](https://code.visualstudio.com/) or [Atom](https://atom.io/) editor. Both are free and work on both Mac and Windows.






  - content: |

      ## Create an index page

      Create an `index.html` in your project folder,
      with the following code which should be familiar!
      

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

      Make sure to save your index page!
      {:.checkpoint}
    
    notes: |

      At this point your project is exactly the same as a normal website. Could open in browser.





  - content: |
      ## Jekyll Configuration

      Create a new file in your project called 
      `_config.yml` and add the following code.

      ```yaml
      name: Jekyll Site
      ```
     

    notes: |

      For a set of files to be considered a Jekyll site, we need to add a configuration file with some information for the Jekyll app, and we need our project to have a specific structure.

      The bare minimum we need is a name for our site.

      We will add more configurations here as we need them.

  
  - content: |

      It is also a good idea to specify
      which version of Jekyll you are using.

      ```yaml
      name: Jekyll Site
      version: 3.0.3
      ```

      Make sure to save your configuration file!
      {:.checkpoint}

    notes: |
      Different versions of Jekyll have different functionality, so it's a good idea to specify the version so that others running your code know which version to use.

      If you are using Jekyll via the command line, your version number is the one you see when you run `jekyll -v` from the command line.

      CloudCannon supports Jekyll versions `2.4.0`, `2.5.3`, and `3.0.3`. You should use `3.0.3` which is the newest version.

      If you do not specify a version, `2.4.0` will be used.

      [CloudCannon Jekyll Documentation](https://docs.cloudcannon.com/building/jekyll/)


  - content: |
      ## Running Your Site

      Using the command line, 
      navigate into your project folder.

    notes: |

      Some handy commands for navigating through folders using the command line:

      - **ls** on Mac or **dir** on Windows
        _Shows all the files and folders in your current folder._

      - **cd foldername**
        _Type cd then the name of a folder to go into that folder. It must be one of the folders listed when you type **ls** or **dir**._

      - **cd ..**
        _Like a back button, this will take you back to the previous folder._
  
  - content: |
      Run your site from the command line by 
      typing `jekyll serve` and pressing enter.

    notes: |

      Running `jekyll serve` generates a website from your project files and starts a web server so you can preview it in a web browser.

      The `serve` command also watches out for any changes to your project. That means that every time you change a file and save it, Jekyll will automatically rebuild your website.

  - content: |

      In your browser, go to
      [http://localhost:4000/](http://localhost:4000/){: target="_blank"}

      You should see the word "Hello!"
      {:.checkpoint}

    notes: |

      The website "localhost" is a name for your own computer, when your computer is running a web server.

      Jekyll started a web server for us, which is why we can see the site on the localhost URL.

      4000 is the port number. You can run more than one website on your computer at the same time, so using different port numbers allows us to look at each different site while still using the localhost URL.

  - content: |

      Closing the command line will shut down your website preview.

    notes: |

      Because we are running Jekyll from the command line, it will only continue to run as long as the command window is open.

      If you close the window or type Ctrl+C, Jekyll will stop running and the localhost web server will shut down until you run `jekyll serve` again.





  
  - content: |

      ## The Site Folder

      After running `jekyll serve`, you'll see 
      that a folder called `_site` was created.

      This is the generated output of your project.

    notes: |

      These files are the "static files" we were talking about. As your Jekyll site becomes more complex, you'll begin to see the differences between the "input" files (your project files) and the "output" files (your site files).

  - content: |

      Every time you make a change, 
      Jekyll updates the site folder.

    notes: |

      Because the site files are generated, make sure when you're editing that you don't try editing these files, as any changes you make will be overwritten.
  
  - content: |
      If you were uploading to a web server which didn't support Jekyll, 
      you would upload the contents of this folder.

    notes: |

      The files in the site folder don't need Jekyll to run them. They were generated by Jekyll, but once they're generated they're just plain HTML, CSS and JavaScript.

  - content: |
      Some hosting providers support Jekyll, which means 
      you can publish the working files and it will generate site.

      GitHub and CloudCannon both support Jekyll.

    notes: |

      These sites don't even show you your site folder, they just take your input project files and generate the site output in the background.







  - content: |
      ## Adding Pages

      Extra pages can be added by making 
      a new HTML file for each page.

    notes: |

      For individual website pages, you create one file for each page just like in a normal website.

  - content: |

      Create a new page called `contact.html`

      ```html
      <!doctype html>
      <html>

          <head>
              <title>My Jekyll Site</title>
          </head>

          <body>
              <h1>Contact Me!</h1>
          </body>

      </html>
      ```

      Make sure to save your contact page!
      {:.checkpoint}

    notes: |

      This page is identical to the index page, except for the heading text.




  - content: |

      Preview in your browser at `localhost:4000/contact.html`.

    notes: |

      Because we are running `jekyll serve`, this new page will be automatically picked up by Jekyll, and will be available on localhost after a couple of seconds delay.

      All your pages can be found on localhost, with a forward slash followed by the file name for pages other than the index page.








  - content: |
      ## Summary

      - **Config Files**
        The config file tells Jekyll that the project folder is a Jekyll site.
      - **Creating Pages**
        Pages can be added by creating normal HTML files for each page.
      - **Live Preview**
        Serving your site with Jekyll enables browser preview.
      {:.flex-list}

    notes: |

      Now that we've covered the basics of running a Jekyll site, we can begin to introduce some of the nifty tricks it offers us.

  - content: |

      ### Generated Sites: Complete

      [Next Chapter](themes.html)

    notes: |

      You've completed the Generated Sites chapter, well done!

      Continue to the next chapter for more.







    

---