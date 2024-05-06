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

7. Towards the bottom of the schema, delete the entire "default" section and add the following code, updating the "presets" attribute to the schema under "name" following the same naming structure.

    - Adding the "presets" attribute is the only way to make a user created section be available in the theme customizer.
    - Capitalization doesn't really matter here and is only seen in the theme customizer.
    - The "presets" "category" can be called whatever you like. This is a deprecated function of the Shopify theme editor that may or may not return, allowing you to categorize/filter different template sections as you're building your site.
