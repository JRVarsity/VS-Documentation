#### Preface:

Similar to [Creating Multiple Site Headers](https://github.com/JRVarsity/VS-Documentation/blob/main/Creating%20Multiple%20Site%20Headers.md), we're going to be removing the global footer and making a new section to allow for unique footers per page / page type template.

1. In the theme’s code editor, navigate to “Sections” and select “+ Add a new section”

2. Name your new section however you’d like, using “footer” as the prefix (e.g. footer-main1, footer-main-alt, etc.) using the ”liquid” format; “.liquid” will be included in the file name so there’s no reason to add it when naming.

    - To have multiple footers, our global footer (the default theme footer) will be hidden/disabled so we’ll need to recreate it first, followed by  any subsequent footers we may need.

3. Now that you’ve recreated your new main footer liquid file (in this example using the filename “footer-main1.liquid”), go to the global header file (“footer-main.liquid” within “Sections”)and copy/paste its contents into the new “footer-main1.liquid” file you’ve created.

4. Be sure to overwrite ALL content of the new “footer-main1.liquid” file so there isn’t conflicting JSON schema data, which is populated by default when you create a new liquid file.

5. In “footer-main1.liquid” navigate down to the {% schema %} of the file and change the "en" (English) name to match your newly created footer so you can easily identify it within the theme customizer.

```json
{% schema %}
{
    "name": {
        "en": "Footer-main1"
    },
      "max_blocks": 4,
```

6. Towards the bottom of the schema, delete the entire "default" attribute section. The "default" attribute cannot exist with a "presets" attribute, which is required to make a user created section available in the theme customizer.

```json
    "default": {
        "blocks": [
            {
                "type": "text",
                "settings": {
                    "title": "Contact us",
                    "richtext": "<p>Share store details, promotions, or brand content with your customers.<\/p>"
                }
            },
            {
                "type": "menu",
                "settings": {
                    "menu_title": "Links",
                    "footer_linklist": "main-menu"
                }
            },
            {
                "type": "newsletter",
                "settings": {
                    "menu_title": "Join our Mailing List",
                    "footer_newsletter_description": ""
                }
            }
        ]
    }
```

7. Add the following code where the "default" attribute was deleted, then update the "presets" attribute "name" following the same naming structure as step 5.

```json
 "presets": [
        {
        "name": "footer-main1",
        "category": "ADVANCED LAYOUT"
        }]
```

<em>Capitalization doesn't really matter here aside from readability and is only seen in the theme customizer. The "presets" "category" can be called whatever you like. This is a deprecated function of the Shopify theme editor that may or may not return, allowing you to categorize/filter different template sections as you're building your site.</em>

8. Continue this process of creating a new main footer section for as many as you need, giving each a unique file name ("footer-main2.liquid", "footer-main3.liquid", etc.) as well as unique schema name and presets name.

9. After saving your work, go into the theme customizer and toggle the eye icon (section visibility) on the global "Footer main" under the "Footer" section, rendering it invisible sitewide.

10. Your newly created footers will appear as selectable sections within the "Template" portion of the page after you've searched for them.

11. Once you've selected your new footer, it will appear in the Template section and can be edited uniquely and moved to any position, but since this is the "footer" of the page we're editing, we should always keep it as the bottom section.

12. Now that we have multiple footers, each page/page type template has to have one of our unique footers applied to it (and each edited) as an individual Section since we've removed the global footer. This is a bit of a pain, but it's the only way to have different footers for specific pages of the site.
