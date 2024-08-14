<template>
  <section class="projects-section">
    <ProjectsHeader />
    <ProjectCard v-for="project in projects" :key="project.name" />
  </section>
</template>

<script>
import { ref } from 'vue'
import ProjectCard from './ProjectCard.vue'
import ProjectsHeader from './ProjectsHeader.vue'

export default {
  name: 'TheProjects',
  components: { ProjectsHeader, ProjectCard },
  setup() {
    const projects = ref([
      {
        imgSmall: '../../assets/thumbnail-project-1-small.webp',
        name: 'DESIGN PORTFOLIO',
        tags: 'HTML CSS',
        viewProjectLink: '#',
        viewCodeLink: '#'
      },
      {
        imgSmall: '../../assets/thumbnail-project-2-small.webp',
        name: 'E-LEARNING LANDING PAGE',
        tags: 'HTML CSS',
        viewProjectLink: '#',
        viewCodeLink: '#'
      },
      {
        imgSmall: '../../assets/thumbnail-project-3-small.webp',
        name: 'TODO WEB APP',
        tags: 'HTML CSS JAVASCRIPT',
        viewProjectLink: '#',
        viewCodeLink: '#'
      },
      {
        imgSmall: '../../assets/thumbnail-project-4-small.webp',
        name: 'ENTERTAINMENT WEB APP',
        tags: 'HTML CSS JAVASCRIPT',
        viewProjectLink: '#',
        viewCodeLink: '#'
      },
      {
        imgSmall: '../../assets/thumbnail-project-5-small.webp',
        name: 'MEMORY GAME',
        tags: 'HTML CSS JAVASCRIPT',
        viewProjectLink: '#',
        viewCodeLink: '#'
      },
      {
        imgSmall: '../../assets/thumbnail-project-6-small.webp',
        name: 'ART GALLERY SHOWCASE',
        tags: 'HTML CSS JAVASCRIPT',
        viewProjectLink: '#',
        viewCodeLink: '#'
      }
    ])

    return { projects }
  }
}
</script>

<style lang="scss" scoped>
.projects-section {
  padding: 80px 0;
}
</style>
