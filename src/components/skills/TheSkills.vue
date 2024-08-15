<template>
  <section class="skills-section">
    <TheSkill v-for="skill in skills" :key="skill.name" :name="skill.name" :exp="skill.exp" />
  </section>
</template>

<script>
import { ref } from 'vue'
import TheSkill from './TheSkill.vue'

export default {
  name: 'TheSkills',
  components: { TheSkill },

  setup() {
    const skills = ref([
      { name: 'HTML', exp: '4 Years' },
      { name: 'CSS', exp: '4 Years' },
      { name: 'JavaScript', exp: '4 Years' },
      { name: 'Accessibility', exp: '4 Years' },
      { name: 'React', exp: '3 Years' },
      { name: 'Sass', exp: '3 Years' }
    ])

    return { skills }
  }
}
</script>

<style lang="scss" scoped>
.skills-section {
  position: relative;
  padding: 40px 16px;
  display: flex;
  flex-direction: column;
  gap: 24px;
  &::before,
  &::after {
    content: '';
    position: absolute;

    left: 16px;
    right: 16px;
    height: 1px;
    background-color: $white-color;
  }
  &::before {
    top: 0;
  }
  &::after {
    bottom: 0;
  }
}
</style>
