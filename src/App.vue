<template>
  <div id="app">
    <div v-if="showContent">
      <Nav :msg="'this is nav I\'m in views'"></Nav>
    </div>
    <router-view />
    <div v-if="showContent">
      <Footer></Footer>
    </div>
  </div>
</template>
<script lang="ts">
import { Vue, Watch } from "vue-property-decorator";
import Component from "vue-class-component";
import Footer from "@/layout/footer/index.vue";
import Nav from "@/layout/nav/index.vue";
@Component({
  components: {
    Nav,
    Footer
  }
})
export default class App extends Vue {
  private showContent: boolean = true;
}
</script>
<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
