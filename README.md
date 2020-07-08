# p11-vue

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

### To build only one vue component

**with version control**
npx vue-cli-service build --target lib --formats umd-min --no-clean --dest dist --name "Test.[chunkhash]" src/components/Test.vue

**without version control**
npx vue-cli-service build --target lib --formats umd-min --name Test src/components/Test.vue
