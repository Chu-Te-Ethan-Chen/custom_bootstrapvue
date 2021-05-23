# bootstrapvue

![](https://github.com/Jordon-Chen/BootstrapVue/blob/master/src/assets/original.jpg?raw=true)
![](https://github.com/Jordon-Chen/BootstrapVue/blob/master/src/assets/custom.jpg?raw=true)

## Create project

```bash
# https://cli.vuejs.org/guide/installation.html#installation
sudo npm install -g @vue/cli

vue create bootstrapvue

#Vue CLI v4.5.13
#? Please pick a preset: Manually select features
#? Check the features needed for your project: Choose Vue version, Babel, Router, Vuex, CSS Pre-processors, Linter, Unit
#? Choose a version of Vue.js that you want to start the project with 2.x
#? Use history mode for router? (Requires proper server setup for index fallback in production) Yes
#? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported by default): Sass/SCSS (with dart-sass)
#? Pick a linter / formatter config: Prettier
#? Pick additional lint features: Lint on save
#? Pick a unit testing solution: Mocha
#? Where do you prefer placing config for Babel, ESLint, etc.? In dedicated config files
#? Save this as a preset for future projects? (y/N)
```

## Install BootstrapVue

```bash
# https://bootstrap-vue.org/docs#vue-cli-3
npm install bootstrap-vue

# main.js
import Vue from "vue";
import App from "./App.vue";
import router from "./router";
import store from "./store";
import { BootstrapVue, BootstrapVueIcons } from 'bootstrap-vue'

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue)
Vue.use(BootstrapVueIcons)

Vue.config.productionTip = false;

new Vue({
  router,
  store,
  render: (h) => h(App),
}).$mount("#app");
```

## Custom style

```bash
# https://getbootstrap.com/docs/4.5/getting-started/theming/

your-project/
├── scss
│   └── custom.scss
└── node_modules/
    └── bootstrap
        ├── js
        └── scss

# /scss/custom.scss

// File: custom.scss

// Define your variable overrides here

// Theme color default definitions
// https://mdbootstrap.com/docs/standard/content-styles/colors/
$primary: #1266F1;
$secondary: #B23CFD;
$success: #00B74A;
$info: #F93154;
$warning: #FFA900;
$danger: #39C0ED;
$light: #FBFBFB;
$dark: #262626;

// Include Bootstrap and BootstrapVue SCSS files
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
@import '../../node_modules/bootstrap-vue/src/index.scss';

// General style overrides and custom classes

```
