#### Preface:

Collection templates, regardless of individual customization within the theme customizer, all reference the main "template--collection.liquid" file which pulls in and renders content based on a variety of parameters, chained references and resources (other .liquid files, .css files, etc.) in the code. Because id's and classes are styled and defined deeper in the theme's custom code (theme.min.css, etc.), minimal changes are the best route to take versus updating a class or id to allow for further customization or identification; there's no telling how many places from which it's being used or styled.

For this task, we're specifically changing the shape of the individual product grid items to "Tall" (2:3) versus the square 1:1 format that's defined in the global settings for the theme. The "template--collection.liquid" Section renders the "product-grid--indiv-product.liquid" Snippet so we'll be creating a new version of each in order for this to work.

1. From the theme customizer, create a new collection template and modify/customize it as normal.
2. In the theme's edit code within "Sections" create a new liquid section called "template--collection2" or whatever you'd like to name it. 
3. Under "Snippets" create a new liquid snippet called "product-grid--indiv-product2" or whatever you'd like to name it. 
4. Under "Templates", navigate to the JSON file of the new collection template you made in Step 1 and change the main section type ("sections" > "main" > "type") in order to have this new collection template reference your new "template--collection2.liquid" file.
```JSON
 "main": {
      "type": "template--collection2",
```
 5. Within this same file, scroll down and change the quick view image size ("sections" > "quick-view" > "settings") from square to "tall to force the 2:3 image format within quick view. Once done, save the file.
```JSON
 "quick-view": {
          "type": "quick-view",
          "settings": {
            "quick-view-image-size": "tall",
```
*As a side note, you'll find some other interesting settings within the quick view JSON here that aren't available within the theme customizer such as being able to show or hide the dynamic checkout buttons (Shop Pay, Apple Pay, etc.), display or hide quick view on mobile, etc.
6. Now that the new collection template JSON is ready, navigate back to the newly created "template--collection2.liquid" file you created in Step 2. Copy and paste the entirety of the original "template--collection.liquid" file into this file, overwriting any default schema or code.
7. Within the new "template--collection2.liquid" file, find the div with id "AjaxinateContainer" and scroll down to the "render" section of code. Here, you'll replace the original 'product-grid--indiv-product' with your newly created liquid file from Step 3. Once done, save the file.
```js
<div id="AjaxinateContainer" class="clearfix{% if settings.product-grid != 'natural' %} has-aspect-ratio{% else %} natural-images{% endif %}">
                    <ol class="grid__item product-grid {{ grid_item_width }} indiv-product-wrapper collection-image-anim {{ olclasses }}" data-grid-id="{{section.id}}"
                    id="template--collection">
                        {% for product in collection.products %}
                            {%- comment %}<locksmith:d138>{% endcomment -%}
                              {%- capture var %}{% render 'locksmith-variables', scope: 'subject', subject: product, subject_parent: collection, variable: 'transparent' %}{% endcapture %}{% if var == "true" %}{% else %}{% continue %}{% endif -%}
                            {%- comment %}</locksmith:d138>{% endcomment -%}
                            <li>
                                {%-
                                    render 'product-grid--indiv-product2',
                                    liquidObject: product,
                                    quick_view_aspect_ratio: img_aspect_ratio,
                                    show_quick_view_on_mobile: enable_mobile_quick_view,
                                    quick_view_enabled: has_quick_view,
                                    discount_display: discount_display,
                                    description_enabled: description_enabled,
                                    variant_labels_enabled: show_variant_labels,
                                    show_sold_out_variants: sold_out_variants_enabled,
                                    show_dynamic_checkout: show_dynamic_checkout
                                -%}
                            </li>
```
8. Navigate back to the newly created "product-grid--indiv-product2.liquid" file you created in Step 3. Copy and paste the entirety of the original "product-grid--indiv-product.liquid"  into this file, overwriting any default schema or code.
9. In this new "product-grid--indiv-product2.liquid" file, <u>REMOVE</u> the lines of code from "assign crop_setting" to "end if" since we don't want to reference the image crop from the global settings at all.
```js
{% assign crop_setting = settings.product-grid %}
{% assign image_crop = nil %}
{% if crop_setting == "square" %}
    {% assign image_crop = "aspect-ratio--square" %}
{% elsif crop_setting == "tall" %}
    {% assign image_crop = "aspect-ratio--tall" %}
{% elsif crop_setting == "wide" %}
    {% assign image_crop = "aspect-ratio--wide" %}
{% endif %}
``` 
10. Within this same file (product-grid--indiv-product2.liquid), add in the following code at the top of the file. This will force each individual product within our collection product grid to display in a tall 2:3 format. Once done, save the file.
```js
{% assign image_crop = "aspect-ratio--tall" %}
```
This is a great example of why we wouldn't want to create an entirely separate CSS class as this class "aspect-ratio--tall" is referenced and defined in a number of other locations throughout the theme files. We're leveraging what's defined within the global settings.
