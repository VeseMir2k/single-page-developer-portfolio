<template>
  <section class="skills-section">
    <TheSkill v-for="skill in skills" :key="skill.name" :name="skill.name" :exp="skill.exp" />
  </section>
</template>

<script setup>
import { ref } from 'vue'
import TheSkill from './TheSkill.vue'

defineOptions({
  name: 'TheSkills'
})

const skills = ref([
  {
    name: 'HTML',
    exp: '4 Years'
  },
  {
    name: 'CSS',
    exp: '4 Years'
  },
  {
    name: 'JavaScript',
    exp: '4 Years'
  },
  {
    name: 'Accessibility',
    exp: '4 Years'
  },
  {
    name: 'React',
    exp: '3 Years'
  },
  {
    name: 'Sass',
    exp: '3 Years'
  }
])
</script>

<style lang="scss" scoped>
.skills-section {
  display: flex;
  flex-direction: column;
  gap: 24px;
  padding: 40px 16px;
  position: relative;

  &::before,
  &::after {
    background-color: $white-color;
    content: '';
    height: 1px;
    left: 16px;
    position: absolute;
    right: 16px;
  }
  &::before {
    top: 0;
  }
  &::after {
    bottom: 0;
  }
}

@media (min-width: $tablet-breakpoint) {
  .skills-section {
    padding: 52px 32px;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 52px 0;
    &::before {
      left: 32px;
      right: 32px;
    }
    &::after {
      height: 0;
    }
  }

  @media (min-width: $desktop-breakpoint) {
    .skills-section {
      padding: 72px 0;
      &::before {
        left: 0;
        right: 0;
      }
    }
  }
}
</style>
