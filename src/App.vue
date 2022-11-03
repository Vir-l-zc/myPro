<template>
  <div id="app">
    {{msg}}
  <abc></abc>
  <efg></efg>
  <Parent></Parent>
  <A></A>
  <B></B>
  </div>
</template>

<script>
import abc from './components/About.vue'
import efg from './components/hello.vue'
import Parent from './components/parent.vue'
import A from './components/A.vue'
import B from './components/B.vue'

export default {
  name: 'App',
  components: {
    abc,
    efg,
    Parent,
    A,
    B
  },
  data() {
    return {
      msg:'你好'
    }
  },
}
</script>

<style>
#app {
 color: red;
 font-size: 50px;
}
</style>
