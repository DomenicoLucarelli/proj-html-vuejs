<script>
import AppInfo from './components/AppInfo.vue';

import AppHeader from './components/AppHeader.vue';
import AppServices from './components/AppServices.vue';


export default {
    data() {
        return {};
    },
    components: { AppInfo, AppHeader, AppServices }
}
</script>

<template>

  <AppInfo></AppInfo>

  <AppHeader></AppHeader>
  
  <AppServices></AppServices>

</template>

<style lang="scss">
  
</style>