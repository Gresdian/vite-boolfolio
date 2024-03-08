<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppMain,
    AppHeader
  }
}
</script>
<template lang="">
  <div>
    <AppHeader />
    <AppMain />
  </div>
</template>
<style lang="scss">
  @use './styles/general.scss'
</style>
