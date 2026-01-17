<script setup lang="ts">
import {saveAs} from "file-saver";
const openLink = (url: string) => {
  window.open(url, '_blank', 'noopener');
};
</script>

<template>
  <header class="custom-toolbar">
    <div class="toolbar-start">
      <div class="avatar-container">
        <img
            src="/icon.webp"
            alt="User Avatar"
            class="native-avatar"
        />
      </div>


      <h1 class="page-title">
        林家民
      </h1>
    </div>

    <nav class="toolbar-end">
      <button
          class="nav-button btn-primary"
          @click="saveAs('/Resume - ZH.pdf', '林家民-履歷.pdf')"
      >
          <span class="material-symbols-outlined">
download
</span>
        下載履歷
      </button>

      <button
          class="nav-button btn-primary"
          @click="openLink('https://github.com/lostmypillow')"
      >
          <span class="material-symbols-outlined">
open_in_new
</span>
        參觀我的GitHub
      </button>
    </nav>
  </header>


</template>

<style scoped>
.material-symbols-outlined {
  font-variation-settings: 'FILL' 0,
  'wght' 400,
  'GRAD' 0,
  'opsz' 24
}

.custom-toolbar {
  position: sticky;
  top: 1rem;
  z-index: 1000;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  backdrop-filter: blur(40px);
  border-radius: 3rem;
  padding: 1rem 1.4rem;
  background-color: rgba(255, 255, 255, 0.4);
  box-sizing: border-box;
}

@media (min-width: 640px) {
  .custom-toolbar {
    flex-direction: row;
  }
}

.avatar-container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  height: 3rem;
}

/* Avatar & Title */
.toolbar-start {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 1rem;
  height: 100%;
}

.native-avatar {
  width: 3rem;
  height: 3rem;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}

.page-title {
  font-weight: 800;
  font-size: 1.875rem;
  margin: 0;
  padding: 0;
  line-height: 1;
  display: flex;
  align-items: center;
  height: 3rem;
}

.toolbar-end {
  display: flex;
  flex-direction: column;

  align-items: center;
  gap: 0.5rem;
  width: 100%;
  margin-top: 1rem;
}

@media (min-width: 640px) {
  .toolbar-end {
    width: auto;
    margin-top: 0;
    flex-direction: row;
  }
}

.nav-button {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.6rem 1.25rem;
  border-radius: 2rem;
  border: none;
  cursor: pointer;
  font-weight: 600;
  font-size: 1.2rem;
  text-decoration: none;
  transition: opacity 0.2s;
  white-space: nowrap;

  background-color: #7f1d1d;
  color: white;
}

.nav-button:hover {
  opacity: 0.8;
}
</style>