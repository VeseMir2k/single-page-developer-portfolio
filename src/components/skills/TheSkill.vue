<template>
  <div class="skill-card">
    <h3 class="skill-card__title">{{ name }}</h3>
    <p class="skill-card__exp">{{ exp }} Experience</p>
  </div>
</template>

<script setup>
defineOptions({
  name: 'TheSkill'
})

defineProps({
  name: {
    type: String
  },
  exp: {
    type: String
  }
})
</script>

<style lang="scss" scoped>
.skill-card {
  text-align: center;

  &__title {
    margin-bottom: 1px;
  }
  &__exp {
    color: $grey-color;
  }
}

@media (min-width: $tablet-breakpoint) {
  .skill-card {
    text-align: left;
    width: 50%;
    &__title {
      margin-bottom: 14px;
    }
  }
}

@media (min-width: $desktop-breakpoint) {
  .skill-card {
    width: 33.33%;
  }
}
</style>
