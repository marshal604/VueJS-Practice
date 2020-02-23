#coding/vuejs

# Use Vuejs interact with Dom
### Property Purpose
```javascript
new Vue({
	el: '#app', // use css selector to get template,
  data: {}, // store variable to provide both template and vue other property, e.g, methods, computed etc.
  methods: {}, // provide function to interact to Dom, will call methods again if dom re-render
  computed: {}, // like javascript ‘get’ and call when computed function property change. just work in sync enviroment
  watch: {}, // observe property change and call when property change. could work to aysnc e.g, setTimeout, ajax etc.
})
```
### Template Syntax
> could use Object.keys() or Number() in template
- v-once : just render once in template, and don’t case other change
- v-if: control element in the Dom or not
- v-show: use css `display: none` to control element show or not
- v-for: could loop the list
	- default mode is `in-place patch` , in short,  will random insert or delete, change element in dom, just for result correct.
	- `:key` could safe `in-place patch` problem, it could trace the exist element and just move it or change property, insert lost property.
- v-bind: bind attributes and sugar syntax is `:`
- v-on: listen event and sugar syntax is `@`
- v-model: two-way binding 
- v-html: add html to content