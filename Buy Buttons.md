### [Universal Cheerleaders Association (UCA) - Home (varsity.com)](https://www.varsity.com/uca/)

<details>
  <summary>Buy Button Code</summary>
``` js
<div id='collection-component-1719261018638'></div>
<script type="text/javascript">
/*<![CDATA[*/
(function () {
  var scriptURL = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js';
  if (window.ShopifyBuy) {
    if (window.ShopifyBuy.UI) {
      ShopifyBuyInit();
    } else {
      loadScript();
    }
  } else {
    loadScript();
  }
  function loadScript() {
    var script = document.createElement('script');
    script.async = true;
    script.src = scriptURL;
    (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(script);
    script.onload = ShopifyBuyInit;
  }
  function ShopifyBuyInit() {
    var client = ShopifyBuy.buildClient({
      domain: 'shopvarsity.myshopify.com',
      storefrontAccessToken: 'c66e77a891523900453baa88a9acbf5a',
    });
    ShopifyBuy.UI.onReady(client).then(function (ui) {
      ui.createComponent('collection', {
        id: '270606073954',
        node: document.getElementById('collection-component-1719261018638'),
        moneyFormat: '%24%7B%7Bamount%7D%7D',
        options: {
  "product": {
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "calc(33.33333% - 30px)",
          "margin-left": "30px",
          "margin-bottom": "50px",
          "width": "calc(33.33333% - 30px)"
        },
        "img": {
          "height": "calc(100% - 15px)",
          "position": "absolute",
          "left": "0",
          "right": "0",
          "top": "0"
        },
        "imgWrapper": {
          "padding-top": "calc(75% + 15px)",
          "position": "relative",
          "height": "0"
        }
      },
      "title": {
        "font-family": "Roboto, sans-serif"
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "price": {
        "font-family": "Roboto, sans-serif"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "buttonDestination": "modal",
    "contents": {
      "options": false
    },
    "text": {
      "button": "View product"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "productSet": {
    "styles": {
      "products": {
        "@media (min-width: 601px)": {
          "margin-left": "-30px"
        }
      }
    }
  },
  "modalProduct": {
    "contents": {
      "img": false,
      "imgWithCarousel": true,
      "button": false,
      "buttonWithQuantity": true
    },
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "100%",
          "margin-left": "0px",
          "margin-bottom": "0px"
        }
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "title": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "26px",
        "color": "#4c4c4c"
      },
      "price": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "18px",
        "color": "#4c4c4c"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "description": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "option": {
    "styles": {
      "label": {
        "font-family": "Roboto, sans-serif"
      },
      "select": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "cart": {
    "styles": {
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      }
    },
    "text": {
      "total": "Subtotal"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "toggle": {
    "styles": {
      "toggle": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "background-color": "#5ea5da",
        ":hover": {
          "background-color": "#5595c4"
        },
        ":focus": {
          "background-color": "#5595c4"
        }
      },
      "count": {
        "font-size": "16px"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  }
},
      });
    });
  }
})();
/*]]>*/
</script>
```
</details>

---
### [National Cheerleaders Association — The Work Is Worth It ® (varsity.com)](https://www.varsity.com/nca/)

```js
<div id='collection-component-1719261113089'></div>
<script type="text/javascript">
/*<![CDATA[*/
(function () {
  var scriptURL = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js';
  if (window.ShopifyBuy) {
    if (window.ShopifyBuy.UI) {
      ShopifyBuyInit();
    } else {
      loadScript();
    }
  } else {
    loadScript();
  }
  function loadScript() {
    var script = document.createElement('script');
    script.async = true;
    script.src = scriptURL;
    (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(script);
    script.onload = ShopifyBuyInit;
  }
  function ShopifyBuyInit() {
    var client = ShopifyBuy.buildClient({
      domain: 'shopvarsity.myshopify.com',
      storefrontAccessToken: 'c66e77a891523900453baa88a9acbf5a',
    });
    ShopifyBuy.UI.onReady(client).then(function (ui) {
      ui.createComponent('collection', {
        id: '270606270562',
        node: document.getElementById('collection-component-1719261113089'),
        moneyFormat: '%24%7B%7Bamount%7D%7D',
        options: {
  "product": {
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "calc(33.33333% - 30px)",
          "margin-left": "30px",
          "margin-bottom": "50px",
          "width": "calc(33.33333% - 30px)"
        },
        "img": {
          "height": "calc(100% - 15px)",
          "position": "absolute",
          "left": "0",
          "right": "0",
          "top": "0"
        },
        "imgWrapper": {
          "padding-top": "calc(75% + 15px)",
          "position": "relative",
          "height": "0"
        }
      },
      "title": {
        "font-family": "Roboto, sans-serif"
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "price": {
        "font-family": "Roboto, sans-serif"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "buttonDestination": "modal",
    "contents": {
      "options": false
    },
    "text": {
      "button": "View product"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "productSet": {
    "styles": {
      "products": {
        "@media (min-width: 601px)": {
          "margin-left": "-30px"
        }
      }
    }
  },
  "modalProduct": {
    "contents": {
      "img": false,
      "imgWithCarousel": true,
      "button": false,
      "buttonWithQuantity": true
    },
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "100%",
          "margin-left": "0px",
          "margin-bottom": "0px"
        }
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "title": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "26px",
        "color": "#4c4c4c"
      },
      "price": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "18px",
        "color": "#4c4c4c"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "description": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "option": {
    "styles": {
      "label": {
        "font-family": "Roboto, sans-serif"
      },
      "select": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "cart": {
    "styles": {
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      }
    },
    "text": {
      "total": "Subtotal"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "toggle": {
    "styles": {
      "toggle": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "background-color": "#5ea5da",
        ":hover": {
          "background-color": "#5595c4"
        },
        ":focus": {
          "background-color": "#5595c4"
        }
      },
      "count": {
        "font-size": "16px"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  }
},
      });
    });
  }
})();
/*]]>*/
</script>
```

---
### [The official site of the UDA | Universal Dance Association - Home (varsity.com)](https://www.varsity.com/uda/)

``` js
<div id='collection-component-1719261727232'></div>
<script type="text/javascript">
/*<![CDATA[*/
(function () {
  var scriptURL = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js';
  if (window.ShopifyBuy) {
    if (window.ShopifyBuy.UI) {
      ShopifyBuyInit();
    } else {
      loadScript();
    }
  } else {
    loadScript();
  }
  function loadScript() {
    var script = document.createElement('script');
    script.async = true;
    script.src = scriptURL;
    (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(script);
    script.onload = ShopifyBuyInit;
  }
  function ShopifyBuyInit() {
    var client = ShopifyBuy.buildClient({
      domain: 'shopvarsity.myshopify.com',
      storefrontAccessToken: 'c66e77a891523900453baa88a9acbf5a',
    });
    ShopifyBuy.UI.onReady(client).then(function (ui) {
      ui.createComponent('collection', {
        id: '270606139490',
        node: document.getElementById('collection-component-1719261727232'),
        moneyFormat: '%24%7B%7Bamount%7D%7D',
        options: {
  "product": {
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "calc(33.33333% - 30px)",
          "margin-left": "30px",
          "margin-bottom": "50px",
          "width": "calc(33.33333% - 30px)"
        },
        "img": {
          "height": "calc(100% - 15px)",
          "position": "absolute",
          "left": "0",
          "right": "0",
          "top": "0"
        },
        "imgWrapper": {
          "padding-top": "calc(75% + 15px)",
          "position": "relative",
          "height": "0"
        }
      },
      "title": {
        "font-family": "Roboto, sans-serif"
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "price": {
        "font-family": "Roboto, sans-serif"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "buttonDestination": "modal",
    "contents": {
      "options": false
    },
    "text": {
      "button": "View product"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "productSet": {
    "styles": {
      "products": {
        "@media (min-width: 601px)": {
          "margin-left": "-30px"
        }
      }
    }
  },
  "modalProduct": {
    "contents": {
      "img": false,
      "imgWithCarousel": true,
      "button": false,
      "buttonWithQuantity": true
    },
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "100%",
          "margin-left": "0px",
          "margin-bottom": "0px"
        }
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "title": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "26px",
        "color": "#4c4c4c"
      },
      "price": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "18px",
        "color": "#4c4c4c"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "description": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "option": {
    "styles": {
      "label": {
        "font-family": "Roboto, sans-serif"
      },
      "select": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "cart": {
    "styles": {
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      }
    },
    "text": {
      "total": "Subtotal"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "toggle": {
    "styles": {
      "toggle": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "background-color": "#5ea5da",
        ":hover": {
          "background-color": "#5595c4"
        },
        ":focus": {
          "background-color": "#5595c4"
        }
      },
      "count": {
        "font-size": "16px"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  }
},
      });
    });
  }
})();
/*]]>*/
</script>
```

---
### [National Dance Alliance — The Work Is Worth It ® (varsity.com)](https://www.varsity.com/nda/)

``` js
<div id='collection-component-1719261783596'></div>
<script type="text/javascript">
/*<![CDATA[*/
(function () {
  var scriptURL = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js';
  if (window.ShopifyBuy) {
    if (window.ShopifyBuy.UI) {
      ShopifyBuyInit();
    } else {
      loadScript();
    }
  } else {
    loadScript();
  }
  function loadScript() {
    var script = document.createElement('script');
    script.async = true;
    script.src = scriptURL;
    (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(script);
    script.onload = ShopifyBuyInit;
  }
  function ShopifyBuyInit() {
    var client = ShopifyBuy.buildClient({
      domain: 'shopvarsity.myshopify.com',
      storefrontAccessToken: 'c66e77a891523900453baa88a9acbf5a',
    });
    ShopifyBuy.UI.onReady(client).then(function (ui) {
      ui.createComponent('collection', {
        id: '270606336098',
        node: document.getElementById('collection-component-1719261783596'),
        moneyFormat: '%24%7B%7Bamount%7D%7D',
        options: {
  "product": {
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "calc(33.33333% - 30px)",
          "margin-left": "30px",
          "margin-bottom": "50px",
          "width": "calc(33.33333% - 30px)"
        },
        "img": {
          "height": "calc(100% - 15px)",
          "position": "absolute",
          "left": "0",
          "right": "0",
          "top": "0"
        },
        "imgWrapper": {
          "padding-top": "calc(75% + 15px)",
          "position": "relative",
          "height": "0"
        }
      },
      "title": {
        "font-family": "Roboto, sans-serif"
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "price": {
        "font-family": "Roboto, sans-serif"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "buttonDestination": "modal",
    "contents": {
      "options": false
    },
    "text": {
      "button": "View product"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "productSet": {
    "styles": {
      "products": {
        "@media (min-width: 601px)": {
          "margin-left": "-30px"
        }
      }
    }
  },
  "modalProduct": {
    "contents": {
      "img": false,
      "imgWithCarousel": true,
      "button": false,
      "buttonWithQuantity": true
    },
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "100%",
          "margin-left": "0px",
          "margin-bottom": "0px"
        }
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "title": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "26px",
        "color": "#4c4c4c"
      },
      "price": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "18px",
        "color": "#4c4c4c"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "description": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "option": {
    "styles": {
      "label": {
        "font-family": "Roboto, sans-serif"
      },
      "select": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "cart": {
    "styles": {
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      }
    },
    "text": {
      "total": "Subtotal"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "toggle": {
    "styles": {
      "toggle": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "background-color": "#5ea5da",
        ":hover": {
          "background-color": "#5595c4"
        },
        ":focus": {
          "background-color": "#5595c4"
        }
      },
      "count": {
        "font-size": "16px"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  }
},
      });
    });
  }
})();
/*]]>*/
</script>
```

---
### [Home - USA (varsity.com)](https://www.varsity.com/usa/)

``` js
<div id='collection-component-1719261803882'></div>
<script type="text/javascript">
/*<![CDATA[*/
(function () {
  var scriptURL = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js';
  if (window.ShopifyBuy) {
    if (window.ShopifyBuy.UI) {
      ShopifyBuyInit();
    } else {
      loadScript();
    }
  } else {
    loadScript();
  }
  function loadScript() {
    var script = document.createElement('script');
    script.async = true;
    script.src = scriptURL;
    (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(script);
    script.onload = ShopifyBuyInit;
  }
  function ShopifyBuyInit() {
    var client = ShopifyBuy.buildClient({
      domain: 'shopvarsity.myshopify.com',
      storefrontAccessToken: 'c66e77a891523900453baa88a9acbf5a',
    });
    ShopifyBuy.UI.onReady(client).then(function (ui) {
      ui.createComponent('collection', {
        id: '270606401634',
        node: document.getElementById('collection-component-1719261803882'),
        moneyFormat: '%24%7B%7Bamount%7D%7D',
        options: {
  "product": {
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "calc(33.33333% - 30px)",
          "margin-left": "30px",
          "margin-bottom": "50px",
          "width": "calc(33.33333% - 30px)"
        },
        "img": {
          "height": "calc(100% - 15px)",
          "position": "absolute",
          "left": "0",
          "right": "0",
          "top": "0"
        },
        "imgWrapper": {
          "padding-top": "calc(75% + 15px)",
          "position": "relative",
          "height": "0"
        }
      },
      "title": {
        "font-family": "Roboto, sans-serif"
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "price": {
        "font-family": "Roboto, sans-serif"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "buttonDestination": "modal",
    "contents": {
      "options": false
    },
    "text": {
      "button": "View product"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "productSet": {
    "styles": {
      "products": {
        "@media (min-width: 601px)": {
          "margin-left": "-30px"
        }
      }
    }
  },
  "modalProduct": {
    "contents": {
      "img": false,
      "imgWithCarousel": true,
      "button": false,
      "buttonWithQuantity": true
    },
    "styles": {
      "product": {
        "@media (min-width: 601px)": {
          "max-width": "100%",
          "margin-left": "0px",
          "margin-bottom": "0px"
        }
      },
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      },
      "quantityInput": {
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px"
      },
      "title": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "26px",
        "color": "#4c4c4c"
      },
      "price": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "18px",
        "color": "#4c4c4c"
      },
      "compareAt": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "unitPrice": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "normal",
        "font-size": "15.299999999999999px",
        "color": "#4c4c4c"
      },
      "description": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "option": {
    "styles": {
      "label": {
        "font-family": "Roboto, sans-serif"
      },
      "select": {
        "font-family": "Roboto, sans-serif"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "cart": {
    "styles": {
      "button": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "font-size": "16px",
        "padding-top": "16px",
        "padding-bottom": "16px",
        ":hover": {
          "background-color": "#5595c4"
        },
        "background-color": "#5ea5da",
        ":focus": {
          "background-color": "#5595c4"
        },
        "border-radius": "5px"
      }
    },
    "text": {
      "total": "Subtotal"
    },
    "googleFonts": [
      "Roboto"
    ]
  },
  "toggle": {
    "styles": {
      "toggle": {
        "font-family": "Roboto, sans-serif",
        "font-weight": "bold",
        "background-color": "#5ea5da",
        ":hover": {
          "background-color": "#5595c4"
        },
        ":focus": {
          "background-color": "#5595c4"
        }
      },
      "count": {
        "font-size": "16px"
      }
    },
    "googleFonts": [
      "Roboto"
    ]
  }
},
      });
    });
  }
})();
/*]]>*/
</script>
```
