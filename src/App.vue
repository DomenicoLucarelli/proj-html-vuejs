<script>
import AppInfo from './components/AppInfo.vue';

import AppHeader from './components/AppHeader.vue';
import AppServices from './components/AppServices.vue';
import AppNetwork from './components/AppNetwork.vue';


export default {
    data() {
        return {};
    },
    components: { AppInfo, AppHeader, AppServices, AppNetwork }
}
</script>

<template>

  <AppInfo></AppInfo>

  <AppHeader></AppHeader>
  
  <AppServices></AppServices>

  <AppNetwork></AppNetwork>

</template>

<style lang="scss">
  
</style>