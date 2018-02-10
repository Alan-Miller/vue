# Vue
## Overvue
- Component-based like React and Angular 5.
- Rapidly growing. Will soon surpass Angular 5.
- Virtual DOM. Reacts to updates.
  - Has built-in shouldComponentUpdate method, so only child components that need to be rerendered will be.
- Faster than React.
- Can use JSX, but prefers HTML template.
- Major parts:
  - Vue Core.
  - vuex (Vue's Redux).
  - vue-router.

## Install Vue
```bash
# install Vue globally once
npm i -g vue-cli
```

## Create Vue Project
```bash
# initialize project with Vue's create-react-app
vue init webpack project-name

# choose setup options

# Project name project-name
# Project description A Vue.js project
# Author Your-Name your_email@email.com
# Vue build
#   Runtime + Compiler (recommended for most users)
#   Runtime-only
# Install vue-router? (Y/n)
# Use ESLint to lint your code? (Y/n)
# Set up unit tests? (Y/n)
# Set up e2e tests with Nightwatch? (Y/n)
# Should we use 'npm install'? (recommended)
#   Yes, use NPM 
#   Yes, use Yarn
#   No, I will handle that myself

# go into the project directory
cd project-name/

# start front-end server (Vue's 'npm start')
npm run dev
```

## Build with Vue

Global Vue constructor to make new Vue instances.


webpack simple, webpack


only have to export if using JS in the <script>
if exporting

```javascript
<script>
export default {
  data() {
    return {

    }
  }
}
</script>
```



v-bind:value="message"
shorthand -> :value="message"

v-on:input='handleChange'
shortnand -> @input='handleChange'

:value="message" @input='handleChange' v-model='message'

Vue has modifiers you can add to events, lie submit.prevent

List
v-for is like ng-repeat

Components

Props




You cannot declare data variables inside template. It only watches variables when it was created. Variables added later are not watched.


Vue converts camelCase to kebab-case, like Angular does.






# test

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
