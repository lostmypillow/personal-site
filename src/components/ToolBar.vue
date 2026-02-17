<script setup lang="ts">

import pkg from 'file-saver';
const {saveAs} = pkg;
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
        <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#e3e3e3"><path d="M480-320 280-520l56-58 104 104v-326h80v326l104-104 56 58-200 200ZM240-160q-33 0-56.5-23.5T160-240v-120h80v120h480v-120h80v120q0 33-23.5 56.5T720-160H240Z"/></svg>
        下載履歷
      </button>

      <button
          class="nav-button btn-primary"
          @click="openLink('https://github.com/lostmypillow')"
      >
        <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#e3e3e3"><path d="M200-120q-33 0-56.5-23.5T120-200v-560q0-33 23.5-56.5T200-840h280v80H200v560h560v-280h80v280q0 33-23.5 56.5T760-120H200Zm188-212-56-56 372-372H560v-80h280v280h-80v-144L388-332Z"/></svg>
        GitHub
      </button>
    </nav>
  </header>


</template>

<style scoped>
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
  flex-direction: row;

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