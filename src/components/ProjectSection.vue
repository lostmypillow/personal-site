<script setup lang="ts">
import ProjectCard from "./ProjectCard.vue";
import projects from "../projects.json"
</script>

<template>
  <div class="projects-grid">
    <ProjectCard
        v-for="(project, index) in projects"
        :key="index"
        :title="project.title"
        :subtitle="project.subtitle"
        :content="project.content"
        :show-demo="project.showDemo"
        :demo-link="project.demoLink"
        :show-github="project.showGithub"
        :github-link="project.githubLink"
        :tech-stack="project.techStack"
    />
  </div>
</template>

<style scoped>
.projects-grid {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: space-between;

  width: 100%;
  box-sizing: border-box;
  padding: 1.5rem 1rem 0 1rem;
  gap: 2rem;
}
</style>