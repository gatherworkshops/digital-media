---
title: jQuery Basics
slides:


##########



  - content: |
      
      # jQuery Basics
      _Getting started with jQuery_


##########


  - content: |

      ## A web page is made of three main languages

      ![Venn diagram of HTML, CSS and JS all overlapping](assets/images/html-css-js.png)

    notes: |
      Websites are made of many languages, but your most basic web page, what you see in your browser, is made up of three programming languages.

      That's three different types of code, each with their own rules.

      They all work together to display what you see on the screen.

    

##########


  - content: |

      ## **HTML** is the markup language

      ![Screenshot of Google with only HTML enabled](assets/images/google-html.png)


    notes: |
      HTML is used to define the content of a web page: the words, the pictures, the links.

      It does not define any sizes, colours or layout.

      HTML stand for HyperText Markup Language.

      This is a picture of what Google looks like when you see only the HTML - no CSS or Javascript.

    

##########

  
  - content: |

      ### **CSS** is the design language

      ![Screenshot of Google with both HTML and CSS enabled](assets/images/google-css.png)


    notes: |
      CSS is used to define the appearance of a web page: the colours, the sizes, the layout.

      It can be thought of as the design language.

      It tells our web browser how to display the HTML.

      CSS stands for Cascading Style Sheets.

      This is a picture of what Google looks like when you combine the HTML and CSS.

    

##########


  - content: |

      ## **JavaScript** is the programming language

      ![Screenshot of Google with all of HTML, CSS, JS enabled](assets/images/google-javascript.png)


    notes: |
      JavaScript is used to define any interactivity on a web page: dropdowns, popups, anything that changes after the page is first loaded.

      It can be thought of as the interaction language.

      JavaScript is often known as JS for short, and is actually quite different from Java, which is another programming laguage with a similar name. Tricky!

      This is a picture of what Google looks like when you see all the HTML, CSS and JS working together.

    
      

##########


  - content: |

      ## Adding jQuery to your site

      Before we can use jQuery, we need to import it into our site.
      
      ```html
      <html>
      
        <head>
            <title>My Website</title>
        </head>
        
        <body>
            
            <h1>Welcome to my site!</h1>
            <p>A paragraph about stuff...</p>
            
            <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
        </body>
        
      </html>
      ```
      {: data-line="1-11, 13-15" }
      
      JavaScript imports go in the website `body`, 
      but after all the body content.
      
      


    notes: |

      jQuery needs to be included on **every** HTML page.
      
      We put it as the last thing inside the `body` so that no scripts run until all the website content is loaded.
      
      This prevents lag when a user loads your site.
      
      It also prevents some JavaScript errors which can occur when you try to modify page elements which haven't finished loading yet.

    
 ##########
  

  - content: |

      ![Thumbs Up!]([[BASE_URL]]/theme/assets/images/thumbs-up.svg){: height="200" }

      ## jQuery Basics: Complete!

      Great, now we can start using jQuery plugins...

      [Take me to the next chapter!](lightbox.html)

    notes: |

      Great! Now that we know the basics, let's get started on our own projects.

    





---
