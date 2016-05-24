---
title: Static Data

slides: 

  - content: |
      # Static Data


  - content: |
      ## Data Files

  - content: |
      Create a folder called _data in your project folder.

      It is part of your content not your theme.

  - content: |







  - content: |
      ## Defining Data


  - content: |

      Jekyll data is defined using a markup language called YAML.

  - content: |

      YAML is used for marking up data files, and also for marking up data in the front matter.

  - content: |

      All YAML data consists of properties and lists.

  - content: |

      To create a list item we use a dash at the start of each one.

      ```yaml
      - name: Chocolate Cake
      - name: Spring Water
      - name: Mentos
      ```

  - content: |

      To add extra information to items we add more lines under each.

      ```yaml
      - name: Chocolate Cake
        price: 5.50

      - name: Spring Water
        price: 3.70

      - name: Mentos
        price: 2.00
      ```

  - content: |

      YAML is fussy about spacing. All items must have a dash then a space,
      and must have extra properties lined up vertically.







  - content: |
      ## Displaying Data


  - content: |

      Data files can be accessed from any page which has front matter.
      That means content files, templates and includes can use data.

  - content: |

      To display data, we need to run a loop and show each piece of data.

  - content: |

      Open your shop.html and add a loop over the shop data

      ```html
      <div class="shop-items">
      {% for item in site.data.forsale %}

          {{ item.name }}

      {% endfor %}
      </div>
      ```

  - content: |

      You can also put HTML inside the loop.

      ```html
      <div class="shop-items">
      {% for item in site.data.forsale %}

          <div class="item">
              <span class="name">{{ item.name }}</span>
              <span class="price">{{item.price}}</span>
          </div>

      {% endfor %}
      </div>
      ```



---

TODO: Simple data (properties only)

TODO: Simple data (list only)

TODO: Simple data with list

TODO: Object data (list only)

TODO: Object data (properties and list)

TODO: Mixed simple data and object data