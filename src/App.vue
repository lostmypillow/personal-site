<!--App.vue-->
<script lang="ts" setup>
import ToolBar from "./components/ToolBar.vue";
import ProjectSection from "./components/ProjectSection.vue";
</script>

<template>
  <div class="app-wrapper">
    <main class="layout-main">
      <ToolBar/>
      <div class="content-container">
        <div class="main-column">
          <div class="skills-container">
            <h1 class="main-title">我會...</h1>

            <ul class="skills-list" role="list">
              <li>
                <strong class="highlight">前端、後端</strong>(Python、Vue、React)
              </li>

              <li>
                <strong class="highlight">資料庫</strong> (MySQL, MSSQL)
              </li>

              <li>
                <span class="highlight">服務</span>
                (Postfix + Dovecot 郵件伺服器、Caddy/Apache/Nginx 反向代理、Nextcloud、FreeIPA LDAP、Keycloak SSO IAM)
              </li>

              <li>
                <span class="highlight">伺服器</span> (Ubuntu Server、Fedora Server、Windows Server)
              </li>
              <li>
                <span class="highlight">虛擬機</span> (Proxmox)
              </li>

            </ul>
          </div>
          <ProjectSection/>
        </div>
      </div>
    </main>
    <footer class="footer">
      Made by Johnny with Vue
    </footer>
  </div>
</template>

<style scoped>
.app-wrapper {
  position: relative;
  min-height: 100vh;
}
.layout-main {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: center;
  min-height: 100vh;
  width: 100%;
  padding: 1.5rem;
  box-sizing: border-box;
}

.content-container {
  display: flex;
  flex: 1;
  width: 100%;
  align-items: center;
  justify-content: center;
}

.footer {
  width: 100%;
  text-align: center;
  padding: 2rem 1.5rem;
  box-sizing: border-box;
  color: #262626;
  font-weight: 300;
  font-size: 0.875rem;
}

.main-column {
  display: flex;
  flex-direction: column;
}

.skills-container {
  display: flex;
  flex-direction: column;
  align-self: flex-start;
  box-sizing: border-box;
  width: 100%;
  max-width: 1024px;
  margin-left: 0;
  margin-right: auto;
  padding: 0.5rem 2.1rem;
  line-height: 1.625;
  font-weight: 300;
  color: #262626;
  font-size: 1.125rem;
}


@media (min-width: 768px) {
  .skills-container {
    font-size: 1.5rem;
  }
}

.main-title {
  font-size: 2.25rem;
  font-weight: 700;
  color: #7f1d1d;
  margin-bottom: 1rem;
}

@media (min-width: 768px) {
  .main-title {
    font-size: 3rem;
  }
}

.skills-list {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  list-style: none;
  padding: 0;
}

.skills-list li {
  margin-bottom: 0.5rem;
}

.highlight {
  font-weight: 600;
}
</style>