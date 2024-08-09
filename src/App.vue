<template>
  <div class="container">
    <HeaderApp/>
    <MenuNav/>
    <SkillsCom/>
    <LastPost/>
    <FooterApp/>
  </div>
</template>

<script>

import FooterApp from './components/FooterApp.vue';
import HeaderApp from './components/HeaderApp.vue';
import LastPost from './components/LastPost.vue';
import MenuNav from './components/MenuNav.vue';
import SkillsCom from './components/SkillsCom.vue';

export default {
  name: 'App',
  components: {
    HeaderApp,
    MenuNav,
    SkillsCom,
    LastPost,
    FooterApp
  }
}
</script>

<style lang="scss" scoped>

@import '@/AppStyle.scss'


</style>
