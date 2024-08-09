<template>
  <div class="skills-row">
    <div
      v-for="(skill, index) in skills"
      :key="index"
      class="skill-item"
      :class="{ active: skill.expanded }"
    >
      <div class="skill-header">
        <span class="skill-name">{{ skill.name }}</span>
        <button @click="toggleSkill(index)" class="skill-toggle">
          {{ skill.expanded ? '-' : '+' }}
        </button>
      </div>
      <div v-if="skill.expanded" class="skill-details">
        {{ skill.details }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SkillsRow',
  data() {
    return {
      skills: [
        { name: 'HTML', details: 'HTML details here', expanded: false },
        { name: 'CSS', details: 'Do you sometimes have the feeling that you’re running into the same obstacles over and over again? Many of my conflicts have the same feel to them, like “Hey, I think I’ve been here before,” but I can’t figure out how I wound up in the same place.  The situation is different, but the conflict feels the same. I first read this poem in “The Tibetan Book of Living and Dying” by Sogyal Rinpoche. When I “Googled” it, I found fourteen pages of links. It’s clearly a favorite with many people; I know it speaks volumes to me. “Autobiography in Five Chapters”', expanded: false },
        { name: 'JavaScript', details: 'JavaScript details here', expanded: false },
        { name: 'Vue.js', details: 'Vue.js details here', expanded: false },
      ],
    };
  },
  methods: {
    toggleSkill(index) {
      this.skills[index].expanded = !this.skills[index].expanded;
    },
  },
};
</script>

<style lang="scss" scoped>
@import './SkillsRowStyle'
</style>