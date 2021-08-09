# Add a new plugin

You can manage plugins in `webpack.mix.json` under root folder. There are two main properties called "backend" and "frontend".

> If you add a plugin for **backend** , make sure that you add under the **backend** object.

Example `webpack.mix.json` 

```javascript
{
    "backend":{
        "no_npm_plugins":[
            ...
        ],
        "npm_plugins":[
            ...
        ],
        "meteronic_pages_scripts":[
            ...
        ],
        "meteronic_pages_styles":[
            ...
        ]
    },

    "frontend":{
        "no_npm_plugins":[
            ...
        ],
        "npm_plugins":[
            ... 
        ]
    }
}
```

## Plugin Types

There are 3 types of plugins 

1. [Global plugin](add-a-new-plugin.md#1-global-plugin)
2. [Plugin that has no NPM or custom built plugin](add-a-new-plugin.md#2-plugin-that-has-no-npm-or-custom-built-plugin)
3. [Plugin that installed via NPM](add-a-new-plugin.md#3-plugin-that-installed-via-npm)

### ~~1 Global Plugin~~

~~Most of the time we don't need to manage Global plugins such as Jquery, Bootstrap and those are bundled as Metronic or Canvas plugins.~~ 

### 2 Plugin that has no NPM or custom built plugin

If you open `wepack-mix.config.json` file ,  under`no_npm_plugins` array and add your new plugin folder.

Example

```javascript
 let no_npm_plugins = [
     "resources/backend/plugins/custom/clipboard",
     "resources/backend/plugins/custom/datatables",
     // Your new plugin directory
 ]

```

### 3 Plugin that installed via NPM

If a plugin has npm package it's better to install via NPM to save storage in development.

To add a new plugin that has **npm** package, open `webpack.mix.config` file, add a new object to `npm_plugins` array.

Object must include the properties **name** and **dist\_folder.**

Example object

```javascript
{
     name:'intl-tel-input',
     dist_folder:'node_modules/intl-tel-input/build'
 }
```

Example npm\_plugins

```javascript
 const npm_plugins = [
    {
        name:'intl-tel-input',
        dist_folder:'node_modules/intl-tel-input/build'
    },
    {
     // Your new npm plugin here, object must contains 'name' and 'dist_folder'
    }
]
```

### 



