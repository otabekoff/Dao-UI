## Welcome to Dao-UI

This is not just a UI Framework. It is intended to help VueJS developers to solve problems that are belonged to MDC(Material Design Components. And you can find so many helpful things related to design except the Material Deisgn, too.

## Installation

### CDN Usage
Just easily integrate the component you want by calling just only that component not an entire library.
```html
<html>
  <head>
    <link rel="stylesheet"
      href="https://cdnjs.com/libraries/normalize">
    <link rel="stylesheet"
      href="https://fonts.googleapis.com/css?family=Roboto:300,400,500" type="text/css">
    <link rel="stylesheet"
      href="https://fonts.googleapis.com/icon?family=Material+Icons">
    <link rel="stylesheet"
      href="https://unpkg.com/material-components-vue/dist/typography/typography.min.css">
    <link rel="stylesheet"
      href="https://unpkg.com/material-components-vue/dist/button/button.min.css">
  </head>
  <body>
    <div id="app">
      <m-typography>
        <m-button>Example</m-button>
      </m-typography>
    </div>
    <script src="https://unpkg.com/vue"></script>
    <script
      src="https://unpkg.com/material-components-vue/dist/typography/typography.min.js">
    </script>
    <script
      src="https://unpkg.com/material-components-vue/dist/button/button.min.js">
    </script>
    <script>
      const app = new Vue({
        el: '#app'
      })
    </script>
  </body>
 </html>
```

### Theming
You can setup your own colors by integrating a theme component in your template. And not you should pass n an object with CSS custom properties. But you always should remember the browser compability.
```html
<head>
  <link rel="stylesheet"
      href="https://unpkg.com/material-components-vue/dist/theme/theme.min.css">
</head>
<body>
  <m-theme :customStyle="material">
    <m-button>
      Example
    </m-button>
  </m-theme>
  <script>
    const app = new Vue({
      el: '#app',
      data() {
        return {
          material: {
            '--mdc-theme-primary':  '#5e35b1',
            '--mdc-theme-secondary': '#ff5722',
            '--mdc-theme-background': '#ffffff'
          }
        }
      }
    })
  </script>
</body>
```
For more details see [Material Web Design - Custom CSS properties](https://github.com/material-components/material-components-web/blob/master/packages/mdc-theme/README.md#css-custom-properties).

### Bundler usage
##### Installing
```bash
npm install --save dao-ui

# or with yarn
yarn add dao-ui
```

##### Importing
```html
<template>
  <m-button>Hello</m-button>
</template>

<script>
import Button from 'material-components-vue/dist/button'
Vue.use(Button)

export default {
  // ...
}
</script>

<style lang="scss">
  @import "material-components-vue/dist/button/styles";
</style>
```

And adding default Roboto font in your app root component gives you full compatibility when using this framework.
```html
<style>
  @import url("https://fonts.googleapis.com/css?family=Roboto:300,400,500");
  @import url("https://fonts.googleapis.com/icon?family=Material+Icons");
</style>
```

### Using SASS, Color-System and more coming soon
