<!--App.vue-->
<script lang="ts" setup>
import ToolBar from "./components/ToolBar.vue";
// import ProjectSection from "./components/ProjectSection.vue";
import Footer from "./components/Footer.vue";
import SkillsSection from "./components/SkillsSection.vue";
</script>

<template>
    <main class="main-container">
      <ToolBar/>
      <div class="content-container">
        <SkillsSection/>
<!--        <ProjectSection/>-->
      </div>
    </main>
    <Footer/>

</template>

<style scoped>


.main-container {
  display: flex;
  flex: 1;
  flex-direction: column;
  gap: 1rem;
  align-items: center;
  width: 100%;
  padding: 1.5rem;
  box-sizing: border-box;
}

.content-container {
  display: flex;
  flex: 1;
  width: 100%;
  align-items: center;
  justify-content: start;
  flex-direction: column;
  box-sizing: border-box;
  padding-left: 1rem;
  padding-right: 1rem;
}

@media (min-width: 768px) {
  .content-container {
    padding-left: 4rem;
    padding-right: 4rem;
  }
}
</style>