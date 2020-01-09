<template>
  <div>nav</div>
</template>
<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";
@Component
export default class Nav extends Vue {
  @Prop() private msg: string = "";
}
</script>
<style lang="scss">
div {
  font-size: 34px;
  color: #f40;
}
</style>
