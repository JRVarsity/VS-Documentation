#### Preface:

In relation to [Creating Multiple Site Headers](https://github.com/JRVarsity/VS-Documentation/blob/main/Creating%20Multiple%20Site%20Headers.md) and [Creating Multiple Site Footers](https://github.com/JRVarsity/VS-Documentation/blob/main/Creating%20Multiple%20Site%20Footers.md), the same unique section may need to go on a number of different related pages/templates, and in the case of unique headers and footers for site partitioning, this will always be the case.

Upon saving the theme from the customizer when you create and modify a new section on a page template, Shopify automatically generates a unique ID for that specific section on that specific template. Creating that same section with the same settings on a different page template will result in a different unique ID every time. In order to keep things organized, and CSS all in one place, we're going to copy the unique ID for these sections and paste them into the JSON of any other template or page we want to use them on. This alleviates the need of the theme customizer for these sections that are more "global" to our site and will preserve the unique ID for easy CSS customization wherever these unique sections are used.

#### Example: If we create a unique footer with specific blocks that we'd like to use on other page templates, we would just need to copy the JSON code from the first template footer section we created within the theme customizer and then paste that code into the {% schema %} of another page template (typically a JSON file).

For example, this already created, unique footer can be pasted in your JSON file as the last "section" before the closing bracket "}" within your schema.
```json
,
    "footer_main_lifestyle_Lz9M6T": {
      "type": "footer-main-lifestyle",
      "blocks": {
        "image_Jc7zA6": {
          "type": "image",
          "settings": {
            "image": "shopify:\/\/shop_images\/Collection_Item_4_552209b3-6c99-40ca-84bc-1c8c425db181.jpg",
            "image_max_width": 70,
            "link": "",
            "title": ""
          }
        },
        "menu_Taakwr": {
          "type": "menu",
          "settings": {
            "menu_title": "Lifestyle Menu",
            "footer_linklist": "main-menu"
          }
        },
        "menu_yM3Vjg": {
          "type": "menu",
          "settings": {
            "menu_title": "Information",
            "footer_linklist": "product-information"
          }
        },
        "text_MmybPg": {
          "type": "text",
          "settings": {
            "title": "Contact us",
            "richtext": "<p>Share store details, promotions, or brand content with your customers.<\/p>"
          }
        }
      },
      "block_order": [
        "image_Jc7zA6",
        "menu_Taakwr",
        "menu_yM3Vjg",
        "text_MmybPg"
      ],
      "custom_css": [
        "footer {background: #25347b !important;}"
      ],
      "settings": {
        "alignment": "left"
      }
    }
```
Looking at the code, you'll be able to see the exact details of what make up that section you created and modified within the theme customizer. Notice the Shopify generated unique ID that's been appended to the new footer section name as well. This same ID will need to be paste at the bottom of the page "order" within your schema.
```json
  "order": [
    "header2_E9XTHq",
    "main",
    "171051606848c03709",
    "product-recommendations",
    "image_image_with_text_overlay_thRt7D",
    "featured-collection",
    "footer_main_lifestyle_Lz9M6T"
  ]
```
<em> I've included the entire "order" section to show what this looks like. This is the literal order of the page </em>

Continue to repeate this process for any unique sections that need to appear on multiple page templates, preserving the uniquely generated Shopify section ID.
