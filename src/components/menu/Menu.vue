<template>
  <div class="menu">
    <div class="menu__horiontal"></div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
export default class Home extends Vue {
  mounted() {
    console.log("hello");
  }
}
</script>

<style scoped>
</style>