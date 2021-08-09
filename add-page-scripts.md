# Add page scripts

Up smart profile project was integrated with two UI libraries. 

* Metronic \(Backend\)
* Canvas \(Frontent\)

To manage the page scripts or styles, you have to open the same `webpack.mix.json` file like plugins. 

### Add page for specific UI library

1. [Add **Metronic** page scripts and styles](add-page-scripts.md#1-add-metronic-page-scripts-and-styles)
2. [Add **Canvas** page scripts and styles](add-page-scripts.md#2-add-canvas-page-scripts-and-styles)

## 1. Add Metronic page scripts and styles

Open `webpack.mix.json` , you will see there are two properties **meteronic\_pages\_scripts** and **meteronic\_pages\_styles** under **backend** object.

If you're going to add javascript files of Metronic, you can append the js link under **meteronic\_pages\_scripts** array.

Same with css style, you can append css link under **meteronic\_pages\_styles** array.

Example

```javascript
{
    "backend":{
        "meteronic_pages_scripts":[
            "resources/backend/metronic/js/pages/login/login-1.js"
        ],
        "meteronic_pages_styles":[
            "resources/backend/metronic/sass/pages/login/login-1.scss"
        ]
    }
}
```

## ~~2. Add Canvas page scripts and styles~~

~~Currently there is no script for Canvas UI library~~

~~~~

