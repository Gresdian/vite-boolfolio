<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    AppHeader
  }
}
</script>
<template lang="">
  <div>
    <AppHeader />
    <router-view></router-view>
  </div>
</template>
<style lang="scss">
  @use './styles/general.scss';
</style>
