<script lang="ts" setup>
defineProps({
  title: {type: String, default: "Default Title"},
  subtitle: {type: String, default: "Default Subtitle"},
  content: {type: String, default: "Default Content"},
  showDemo: {type: Boolean},
  demoLink: {type: String, default: "https://example.com"},
  showGithub: {type: Boolean},
  githubLink: {type: String, default: "https://github.com"},
  techStack: {type: Array as () => string[], default: () => []},
});
</script>

<template>
  <div class="project-card">
    <template #title>{{ title }}</template>
    <template #subtitle>{{ subtitle }}</template>

    <template #content>
      <div v-if="techStack.length > 0" class="tech-stack">
        <Chip v-for="tech in techStack" :key="tech" :label="tech" class="tech-chip">

        </Chip>
      </div>

      <div class="card-description" v-html="content"></div>
    </template>

    <template #footer>
      <div class="card-actions">
        <Button
            v-if="showGithub"
            :href="githubLink"
            as="a"
            class="action-button"
            icon="pi pi-github"
            label="GitHub"
            outlined
            rel="noopener"
            rounded
            severity="secondary"
            target="_blank"
        />
        <Button
            v-if="showDemo"
            :href="demoLink"
            as="a"
            class="action-button"
            icon="pi pi-external-link"
            label="Demo"
            rel="noopener"
            rounded
            target="_blank"
        />
      </div>
    </template>
  </div>
</template>

<style scoped>
.project-card {
  width: 25rem;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

.tech-stack {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}

.card-description {
  margin: 0;
}

.card-actions {
  display: flex;
  gap: 1rem;
  margin-top: 0.25rem;
}

.action-button {
  width: 100%;
}


.tech-stack svg {
  margin-right: 0.25rem;
  vertical-align: middle;
}
</style>