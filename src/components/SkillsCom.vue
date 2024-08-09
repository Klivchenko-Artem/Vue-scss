<template>
  <div class="skills-component">
    <h1>Skills</h1>
    <SkillsRow/>
  </div>
</template>

<script>
import SkillsRow from './SkillsRow.vue';



export default {
  name: 'SkillsCom',
  components: {
    SkillsRow,
  },
};
</script>

<style lang="scss" scoped>
@import "./SkillsComStyle"
</style>