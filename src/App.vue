<script>
import AppHeader from "./components/AppHeader.vue";
import { store } from "./store.js";
export default {
  data() {
    return {
      store,
    }
  },
  components: { AppHeader }
}
</script>

<template>
<AppHeader />
<router-view></router-view>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
