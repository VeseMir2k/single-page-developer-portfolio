<template>
  <section class="projects-section">
    <ProjectsHeader />
    <div class="projects-section__container">
      <ProjectCard
        v-for="project in projects"
        :key="project.name"
        :name="project.name"
        :images="project.images"
        :tags="project.tags"
        :links="project.links"
      />
    </div>
  </section>
</template>

<script>
import { ref } from 'vue'
import ProjectCard from './ProjectCard.vue'
import ProjectsHeader from './ProjectsHeader.vue'
import ProjectImgSmall_1 from '../../assets/thumbnail-project-1-small.webp'
import ProjectImgSmall_2 from '../../assets/thumbnail-project-2-small.webp'
import ProjectImgSmall_3 from '../../assets/thumbnail-project-3-small.webp'
import ProjectImgSmall_4 from '../../assets/thumbnail-project-4-small.webp'
import ProjectImgSmall_5 from '../../assets/thumbnail-project-5-small.webp'
import ProjectImgSmall_6 from '../../assets/thumbnail-project-6-small.webp'

export default {
  name: 'TheProjects',
  components: {
    ProjectsHeader,
    ProjectCard
  },
  setup() {
    const projects = ref([
      {
        images: {
          small: ProjectImgSmall_1
        },
        name: 'DESIGN PORTFOLIO',
        tags: ['HTML', 'CSS'],
        links: {
          project: '#',
          code: '#'
        }
      },
      {
        images: {
          small: ProjectImgSmall_2
        },
        name: 'E-LEARNING LANDING PAGE',
        tags: ['HTML', 'CSS'],
        links: {
          project: '#',
          code: '#'
        }
      },
      {
        images: {
          small: ProjectImgSmall_3
        },
        name: 'TODO WEB APP',
        tags: ['HTML', 'CSS', 'JAVASCRIPT'],
        links: {
          project: '#',
          code: '#'
        }
      },
      {
        images: {
          small: ProjectImgSmall_4
        },
        name: 'ENTERTAINMENT WEB APP',
        tags: ['HTML', 'CSS', 'JAVASCRIPT'],
        links: {
          project: '#',
          code: '#'
        }
      },
      {
        images: {
          small: ProjectImgSmall_5
        },
        name: 'MEMORY GAME',
        tags: ['HTML', 'CSS', 'JAVASCRIPT'],
        links: {
          project: '#',
          code: '#'
        }
      },
      {
        images: {
          small: ProjectImgSmall_6
        },
        name: 'ART GALLERY SHOWCASE',
        tags: ['HTML', 'CSS', 'JAVASCRIPT'],
        links: {
          project: '#',
          code: '#'
        }
      }
    ])

    return {
      projects
    }
  }
}
</script>

<style lang="scss" scoped>
.projects-section {
  padding: 80px 16px;

  &__container {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }
}
</style>
