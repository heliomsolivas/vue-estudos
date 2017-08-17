# Arrow Functions

new Vue({
  el: '#app',
  render: h => h(App)
})

-------------------

'use strict';

new Vue({
  el: '#app',
  render: function render(h) {
    return h(App);
  }
});