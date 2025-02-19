This is a custom theme section designed for the Varsity Athlete pages.
```liquid
{% schema %}
{
  "name": "Athlete Section",
  "settings": [
    {
      "type": "image_picker",
      "id": "main_image",
      "label": "Main Image",
    },
    {
      "type": "text",
      "id": "title",
      "label": "Title",
      "default": "ALIYAH SIMS"
    },
    {
      "type": "textarea",
      "id": "description",
      "label": "Description",
      "default": "Aliyah is a dynamic fitness trainer with a background in competitive cheerleading, boxing, and strength training. Aliyah's upbeat teaching style and passion for self-defense empower her clients to feel confident and strong. Known for her fun, high-energy approach, she helps people enjoy working out while promoting a balanced, healthy lifestyle."
    },
    {
      "type": "text",
      "id": "subtitle",
      "label": "Subtitle",
      "default": "Her Favorite Looks"
    },
    {
      "type": "url",
      "id": "athlete-button_link",
      "label": "Button Link"
    },
    {
      "type": "text",
      "id": "athlete-button_text",
      "label": "Button Text",
      "default": "Explore Her Favorites"
    }
  ,
     {
      "type": "select",
      "id": "section_width",
      "label": "t:all.Width",
      "options": [
        {
          "value": "full-width",
          "label": "t:all.Full_width"
        },
        {
          "value": "content",
          "label": "t:all.Content_width"
        },
        {
          "value": "narrow",
          "label": "t:all.Narrow"
        }
      ],
      "default": "content"
    },
    {
      "type": "range",
      "id": "section_padding_top",
      "label": "t:all.Spacing_top",
      "min": 0,
      "max": 150,
      "step": 5,
      "unit": "t:all.px",
      "default": 60
    },
    {
      "type": "range",
      "id": "section_padding_bottom",
      "label": "t:all.Spacing_bottom",
      "min": 0,
      "max": 150,
      "step": 5,
      "unit": "t:all.px",
      "default": 60
    },
  ],
  "blocks": [
    {
      "type": "image_link",
      "name": "Image with Link",
      "limit": 4,
      "settings": [
        {
          "type": "image_picker",
          "id": "image",
          "label": "Small Image"
        },
        {
          "type": "url",
          "id": "link",
          "label": "Link to Product"
        }
      ]
    }
  ],
  "presets": [
    {
      "name": "Athlete Section",
    }
  ]
}
{% endschema %}
{%-  liquid
  assign full_width = false
  if section.settings.section_width == 'full-width'
    assign full_width = true
  endif
-%}
<div class="athlete-section {% unless full_width %}width--{{ section.settings.section_width }} {% endunless %} wrapper-spacing--v{% unless full_width %} wrapper-spacing--h{% endunless %} container width--{{ section.settings.section_width }}" style="padding-top: {{ section.settings.section_padding_top }}px; padding-bottom: {{ section.settings.section_padding_bottom }}px;">
  <div class="container">
    <!-- Main Image -->
    <div class="main-image">
      <img src="{{ section.settings.main_image | image_url }}" alt="Athlete Image">
    </div>

    <!-- Text Content -->
    <div class="text-content">
      <h2 class="title">{{ section.settings.title }}</h2>
      <p class="description">{{ section.settings.description }}</p>
      <h3 class="subtitle">{{ section.settings.subtitle }}</h3>

      <!-- Small Images -->
      <div class="small-images-container">
        <div class="small-images">
          {% for block in section.blocks %}
          <a href="{{ block.settings.link }}" class="small-image">
            <img src="{{ block.settings.image | image_url }}" alt="Small Image">
          </a>
          {% endfor %}
        </div>
      </div>

      <!-- Button -->
      <a href="{{ section.settings.athlete-button_link }}" class="athlete-button btn">{{ section.settings.athlete-button_text }}</a>
    </div>
  </div>
</div>

<style>
/* General Section Styling */
.athlete-section {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 20px;
}

.container {
  display: flex;
  align-items: center;
  gap: 20px;
  padding: 0vw 9vw 0vw 3vw;
}

.main-image {
  flex: 1;
  display: flex;
  justify-content: right;
  max-width: 80%;
}

.main-image img {
  max-height: 100%;
  width: 50%;
  object-fit: contain;
}

.text-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.title {
  font-family: termina, sans-serif;
  font-style: normal;
  font-weight: 900;
  font-size: 30px;
  margin-bottom: 10px;
}

.description {
  font-size: 16px;
  margin-bottom: 20px;
}

.subtitle {
  font-family: termina, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  margin-bottom: 10px;
}

/* Small Images */
.small-images-container {
  overflow-x: auto;
  padding-bottom: 5px;
}

.small-images {
  display: flex;
  gap: 10px;
}

.small-image img {
  max-width: 80px;
  height: auto;
}

.small-image img:hover {
  transform: scale(1.05);
  transition: transform 0.2s ease;
}

/* Button Styling */
.athlete-button {
  font-family: termina, sans-serif;
  font-style: normal;
  font-weight: 500;
  padding: 10px 20px;
  background-color: #5ea5da;
  color: black;
  text-decoration: none;
  font-size: var(--button-font-size-px);
  text-align: center; 
  max-width: 25em; 
  margin: 10px 0 0 0;
}

/* Responsive Design */
@media (max-width: 768px) {
  .athlete-section {
    flex-direction: column;
  }

  .container {
    flex-direction: column;
    align-items: center;
    margin-right: unset;
    padding: 3vw;
  }

  .main-image {
    order: -1;
    width: 100%;
    justify-content: center;
  }

  .main-image img {
    width: unset;
    max-width: 100%;
    max-height: none;
    object-fit: contain;
  }

  .text-content {
    width: 100%;
    margin-top: 20px;
  }

  .small-images-container {
    overflow-x: auto;
    display: flex;
    width: 100%;
    margin-top: 10px;
    gap: 15px;
  }

  .small-image img {
    max-width: 80px;
    height: auto;
  }

  .athlete-button {
    width: 100%;
    max-width: none;
    margin-top: 20px;
  }
}
</style>
```
