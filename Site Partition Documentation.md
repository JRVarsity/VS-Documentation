### **Creating Multiple Headers**

1. Within Shopify, navigate to “Online Store” > “Themes” > “•••” > “Edit code”
2. In the theme’s code editor, navigate to “Sections” and select “+ Add a new section”
3. Name your new section however you’d like, using “header” as the prefix (e.g. header1, header-main, etc.) using the ”liquid” format; “.liquid” will be included in the file name so there’s no reason to add it when naming. 
	- To have multiple headers, our global header (the default theme header) will be hidden/disabled so we’ll need to recreate it first, followed by any subsequent headers we may need.
1. Now that you’ve recreated your new main header liquid file (in this example using the filename “header1.liquid”), go to the global header file (“header.liquid” within “Sections”)and copy/paste its contents into the new “header1.liquid” file you’ve created.
	- Be sure to overwrite ALL content of the new “header1.liquid” file so there isn’t conflicting JSON schema data, which is populated by default when you create a new liquid file.
5. In “header1.liquid” navigate down to the {% schema %} of the file and change the "en" (English) name to match your newly created header so you can easily identify it within the theme customizer.
6. Add a "presets" attribute to the schema under "name" following the same naming structure. 
	- Adding the "presets" attribute is the only way to make a user created section be available in the theme customizer.
	- Capitalization doesn't really matter here and is only seen in the theme customizer.
	- The "presets" "category" can be called whatever you like. This is a deprecated function of the Shopify theme editor that may or may not return, allowing you to categorize/filter different template sections as you're building your site.
```json
{% schema %}
{
    "name": {
        "en": "Header1",
        "de": "Überschrift",
        "es": "Encabezado",
        "fr": "En-tête",
        "pt-PT": "Cabeçalho"
    },
  "presets": [
    {
    "name": "header1",
    "category": "CUSTOM"
    }],
```
<em>*In this example, notice how I've included mismatched capitalization to show that it will still work within the theme customizer, just display differently when you search for the section (lowercase) vs when the section is being edited (uppercase).</em>
7. Continue this process of creating a new header section for as many as you need, giving each a unique file name ("header2.liquid", "header3.liquid", etc.) as well as unique schema name and presets name.
8. After saving your work, go into the theme customizer and toggle the eye icon on the global "Header" under the "Header" section, rendering it invisible sitewide.
	![Pasted image 20240417144802](https://github.com/JRVarsity/VS-Documentation/assets/137803222/992f4313-2558-428a-a5cd-42384ea397a6)
![Pasted image 20240417145119](https://github.com/JRVarsity/VS-Documentation/assets/137803222/385cccbf-edca-49b1-b67b-f2e9e0cdae2e)
![Pasted image 20240417145535](https://github.com/JRVarsity/VS-Documentation/assets/137803222/5ccc14e1-41e3-4396-8fdd-a89a3a4e34cb)
9. Your newly created headers will appear as selectable sections within the "Template" portion of the page after you've searched for them.
	![Pasted image 20240417144802](https://github.com/JRVarsity/VS-Documentation/assets/137803222/992f4313-2558-428a-a5cd-42384ea397a6)
![Pasted image 20240417145119](https://github.com/JRVarsity/VS-Documentation/assets/137803222/385cccbf-edca-49b1-b67b-f2e9e0cdae2e)
![Pasted image 20240417145535](https://github.com/JRVarsity/VS-Documentation/assets/137803222/5ccc14e1-41e3-4396-8fdd-a89a3a4e34cb)
	<em>*Notice how we can see the lowercase "h" populated from our "presets" schema.</em>
10. Once you've selected your new header, it will appear in the Template section and can be edited uniquely and moved to any position, but since this is the "header" of the page we're editing, we should always keep it as the top section.
	![Pasted image 20240417144802](https://github.com/JRVarsity/VS-Documentation/assets/137803222/992f4313-2558-428a-a5cd-42384ea397a6)
![Pasted image 20240417145119](https://github.com/JRVarsity/VS-Documentation/assets/137803222/385cccbf-edca-49b1-b67b-f2e9e0cdae2e)
![Pasted image 20240417145535](https://github.com/JRVarsity/VS-Documentation/assets/137803222/5ccc14e1-41e3-4396-8fdd-a89a3a4e34cb)
	<em>*Notice how we see the uppercase "H" from our schema "name" here.</em>
11. Even though this was easy to create multiple headers, each page/page type template has to have a header applied to it since we've removed the global header.
