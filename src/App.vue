<template>
  <div id="nav">
    <p>Hello Vue!</p>
    <MainWrapper />
  </div>
</template>
<script lang="ts">
import MainWrapper from '@/components/MainWrapper.vue';
import {defineComponent} from 'vue';
export default defineComponent({
  name: 'app',
  components: {
    MainWrapper,
  },
  computed: {},
  methods: {},
  watch: {},
  mounted() {}
});
</script>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
