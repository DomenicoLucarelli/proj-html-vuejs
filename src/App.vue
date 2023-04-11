<script>
import AppInfo from './components/AppInfo.vue';

import AppHeader from './components/AppHeader.vue';
import AppServices from './components/AppServices.vue';
import AppNetwork from './components/AppNetwork.vue';
import AppProjects from './components/AppProjects.vue';
import AppResults from './components/AppResults.vue';
import AppSponsor from './components/AppSponsor.vue';


export default {
    data() {
        return {};
    },
    components: { AppInfo, AppHeader, AppServices, AppNetwork, AppProjects, AppResults, AppSponsor }
}
</script>

<template>

  <AppInfo></AppInfo>

  <AppHeader></AppHeader>
  
  <AppServices id="Services"></AppServices>

  <AppNetwork id="About"></AppNetwork>

  <AppProjects id="Projects"></AppProjects>

  <AppResults id="Results"></AppResults>
  
  <AppSponsor></AppSponsor>

</template>

<style lang="scss">
  
</style>