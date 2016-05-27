---
title: Static Data

slides: 

  - content: |
      # Static Data
      _Managing basic data with Jekyll_

    notes: |

      One handy feature of Jekyll is its support for basic data structures.

  - content: |

      Collections of data are common in websites,
      and we usually code these lists by hand.

    notes: |

      Some common examples would be a menu for a restaurant, or a list of items for sale for a shop.

  - content: |

      With Jekyll we can store list-like data in 
      data files, then generate HTML lists from them.

    notes: |

      No notes

  - content: |

      Jekyll data files use the YAML language,
      like we use in our `_config.yml` file.

    notes: |

      No notes

  - content: |

      Data files are simple lists, where each
      list item can have multiple properties.








  - content: |
      ## Data Files

      We can have as many data files as we like.
      Each data file should store one kind of data.

    notes: |

      For those with database experience, the closest approximation of data files is that each data file would be roughly equivalent to a table in a traditional database.

      This isn't strictly true, as data files can have top-level properties and can have nested lists, but it may be a helpful way to think about it to begin with.

  - content: |

      In your project folder, 
      create a new folder called `_data`.

    notes: |

      It is part of your content not your theme, because data is specific to your project.

      The folder name starts with an underscore as we don't want the actual data copied over to the output site.

  - content: |

      In your data folder, 
      create a new file called `shop.yml`

    notes: |

      This file will contain all the items we want to display in our shop.









  - content: |
      ## Defining Data

      All YAML data consists of properties and lists.

  - content: |

      In `shop.yml` create a list of shop items.

      ```yaml
      - name: Chocolate Cake
      - name: Spring Water
      - name: Mentos
      ```

    notes: |

      In YAML, the dash followed by a space is very important. If you forget the space, Jekyll won't be able to read the data file.

  - content: |

      To add extra information to items,
      we add more lines under each one.

      ```yaml
      - name: Chocolate Cake
        price: '5.50'

      - name: Spring Water
        price: '3.70'

      - name: Mentos
        price: '2.00'
      ```

      Remember to save your data file!
      {:.checkpoint}

    notes: |

      In YAML the whitespace is very important.

      Indentation must be done with spaces not tabs, and every indentation is 2 spaces wide.

      Properties must line up vertically.

      We need to put the prices in quote marks, otherwise Jekyll will treat them as numbers and won't display the trailing zeros.







  - content: |
      ## Displaying Data

      Data is dislayed on a page
      using a Jekyll for loop.

    notes: |

      No notes

  - content: |

      Data files can be accessed from 
      any page, template or include.

    notes: |

      That means content files, templates and includes can use data.

  - content: |

      To display data, we need to run a loop 
      to show each piece of data individually.

    notes: |

      No notes

  - content: |

      In your `shop.html`, add a loop which 
      displays the name of each shop item.

      ```html
      <ul class="shop-items">
      {% for item in site.data.shop %}

          <li>
            {{ item.name }}
          </li>

      {% endfor %}
      </ul>
      ```

    notes: |

      No notes

  - content: |

      Visit the shop page in your web browser.

      You should see a list of item names.
      {:.checkpoint}

    notes: |

      No notes

  - content: |

      Add the price and some additional
      HTML structure to allow for styling.

      ```html
      <ul class="shop-items">
      {% for item in site.data.shop %}

          <li>
              <span class="name">{{ item.name }}</span>
              <span class="price">${{ item.price }}</span>
          </li>

      {% endfor %}
      </ul>
      ```

      Your shop page should now display the item and its price.
      {:.checkpoint}

    notes: |

      No notes

  - content: |

      Here's some CSS to get you started
      with styling up your shop items.

      ```css
      .shop-items {
        list-style-type: none;
        padding-left: 0;
      }

      .shop-items li {
        padding: 5px 10px;
        border-bottom: 1px solid #666;
        display: flex;
      }

      .shop-items .name {
        flex: 1;
        font-weight: bold;
      }

      ```

      Your shop items should now be in a tidy list!
      {:.checkpoint}
    
    notes: |

      No notes



#  - content: |
#
#      ## Smart Navigation
#
#      Most sites have an "active" state on nav buttons,
#      so the button for the current page is highlighted.
#
#    notes: |
#
#      No notes
#
#  - content: |
#
#      We can achieve smart navigation using static data
#      along with some logic inside our `header` include.
#
#    notes: |
#
#      No notes


  - content: |
      ## Summary

      - **Data Files**
        Simple data can be created using YAML.
      - **Jekyll Loops**
        Data can be dislayed by looping over the values in a page
      {:.flex-list}

    notes: |

      Now that we've covered the basics of running a Jekyll site, we can begin to introduce some of the nifty tricks it offers us.

  - content: |

      ### Static Data: Complete

      [Next Chapter](responsive-design.html)

    notes: |

      You've completed the Static Data chapter, well done!

      Continue to the next chapter for more.



---