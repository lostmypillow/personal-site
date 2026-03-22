<script setup lang="ts">
import {useNow, useDateFormat} from "@vueuse/core";
</script>
<template>
  <div class="skills-content">
    <h1>Hi.<br>我叫林家民。<br>我是一位軟體開發工程師。<br> <br>請參考我的經歷：</h1>

    <div class="experience-section">
      <h2>2024/07 以前：自學和個人專案</h2>
      <ul class="skills-list">
        <li>自高中時期開始自學 Python，隨後深入學習 FastAPI 和 前端，並將這些技術廣泛應用於個人專案和後續的職場工作中。
        </li>
        <li>前端技術從自學 React 和 Next.js 開始，目前主要專精於 Vue。包含工作專案、個人開發，以及你現在正在瀏覽的這個個人網站，都是使用
          Vue。
        </li>
      </ul>
      <h2>2024/07 - 2024/10： 達豐公關 - 實習生</h2>
      <ul class="skills-list">
        <li> 在擔任非技術職位期間，為解決每日為高階主管彙整科技新聞報表的繁瑣流程，利用閒暇時間自主開發了
          Chrome 擴充元件，叫 AutoDMS。
        </li>
        <li>系統結合了 LINE API 和 Firebase。只需將新聞連結傳送至 LINE 聊天機器人，Firebase
          就會自動執行基礎的網頁爬蟲和資料擷取；針對防止爬蟲的網站，擴充功能會自動開啟新分頁並在利用分頁API完成進一步的爬蟲和資料擷取作業。
          <details class="context-details">
            <summary>為什麼一定要 LINE？</summary>
            <p>因為要處理的新聞連結原本就是從 LINE
              聊天室傳送過來的。在開發這個工具之前，我通常必須逐一開啟這些連結，然後手動複製並排版標題、日期、作者和內文。</p>
          </details>
        </li>


        <li>Chrome 擴充元件儀表板的功能解決了過去在 Word 中手動複製貼上（標題、日期、作者、內文）以及難以調整排序的痛點，只需點擊幾下即可輕鬆更改新聞分類和排列順序。
        </li>
        <li>在儀表板點擊「匯出」後，系統會自動套用所有複雜的格式，匯出Word檔。
        </li>
        <li><a href="https://youtube.com" target="_blank" rel="noopener noreferrer">實際操作展示影片</a></li>
        <li><a href="https://github.com/lostmypillow/autodms-ext" target="_blank" rel="noopener noreferrer">擴充元件
          GitHub</a></li>
        <li><a href="https://github.com/lostmypillow/autodms-api" target="_blank" rel="noopener noreferrer">Firebase API
          GitHub</a></li>
        <li><a href="https://dms.lostmypillow.com" target="_blank" rel="noopener noreferrer">技術文件</a></li>
      </ul>

      <h2>2024/10 - {{ useDateFormat(useNow(), 'YYYY/MM') }}：高偉數學補習班 - 資訊部⼯讀⽣ </h2>
      <ul class="skills-list">
        <li>擔任資訊部工讀生，處理日常的 IT 維運工作，同時也負責開發和維護多個補習班內部的全端網頁和系統專案。</li>

        <li>輔導老師管理和打卡系統：
          <ul>
            <li>
              以  <strong>PySide6/Qt</strong>  為 Raspberry Pi 和 Windows 平板開發實體打卡機 GUI和。
            </li>
            <li>
              以 FastAPI建立串連以上GUI及前端的
            </li>
            <li>以 Vue 建置打卡即時狀態公告看板，以及其專屬管理頁面。</li>
          </ul>

         讓老師能手動打卡、修改個人資料、上傳大頭貼（使其同步顯示於看板）並發布公告。
        </li>

        <li><strong>學生補位系統：</strong>開發基於 Vue 和 FastAPI 的互動平台，於 Windows Edge Kiosk
          模式下運行。介面上方輪播當日課程和時間，中段提供學生劃位、填寫輔導老師評分及申請獎學金，下方則串流播放廣告影片（影片由
          FastAPI 快取，並透過 Caddy 反向代理伺服器提供）。
        </li>

        <li><strong>虛擬機系統：</strong>開發基於 Electron 的桌面應用程式，透過 virt-viewer 和 SPICE
          協定連接虛擬機。將此程式封裝進客製化的精簡版 Debian ISO 中，並燒錄至 USB 供實體桌機開機使用。該程式會向 FastAPI
          請求連線資訊，而後端則負責和內部資料庫及 Proxmox API 進行資料互動和調度。
        </li>

        <li><strong>補習班新內部系統：</strong>使用 Vue 開發全新的內部管理平台，用於即時顯示各班級狀態。提供員工檢視和處理線上試聽表單的介面、監控自製
          SMS 簡訊 API 的發送狀態，並能透過專屬 FastAPI 直接檢視和管理前述 USB 系統所啟用的虛擬機狀態。
        </li>

        <li><strong>後端 API 開發：</strong>撰寫多個 FastAPI 服務以自動同步內部資料庫和 FreeIPA LDAP 的資料。此外，也開發了
          Nextcloud Talk API 的 Wrapper，成功將其和公司舊有的內部通訊系統進行對接和整合。
        </li>

        <li><strong>基礎設施維運和伺服器建置：</strong>參和並協助公司基礎架構從 VMware 轉移至 Proxmox
          虛擬化環境的大型專案。除了管理虛擬機，也負責大量實體 Windows 工作站和 Ubuntu 伺服器的建置、部署和日常維護。
        </li>
      </ul>
    </div>

    <div class="contact-section">
      <h2>想看更多嗎？</h2>
      <p>如果你想看到自己出現在上方，現在就 <a class="nav-button" href="mailto:jmlin0101@gmail.com">寄工作機會給我吧!</a>
      </p></div>
  </div>
</template>

<style scoped>
.skills-content {
  width: 100%;
  font-size: clamp(1rem, 4vw, 1.2rem);
  line-height: 1.6;
  color: #333;
}

h1 {
  font-size: 1.4em;
  margin-bottom: 1.5em;
  font-weight: bold;
}

.experience-section {
  margin-bottom: 2em;
}

.experience-section h2 {
  font-size: 1.1em;
  margin-bottom: 0.5em;
  color: #2c3e50;
}

.skills-list {
  margin-left: 1.5em;
  margin-bottom: 1em;
}

.skills-list li {
  margin-bottom: 0.3em;
}

.contact-section {
  margin-top: 3em;
  padding-top: 2em;
  border-top: 2px dashed #ccc;
}

.contact-section h2 {
  font-size: 1.1em;
  margin-bottom: 0.5em;
}

.contact-section p {
  margin-bottom: 1.5em;
}

.mailto-btn {
  display: inline-block;
  padding: 0.6em 1.2em;
  background-color: #42b883; /* Vue green */
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-weight: bold;
  transition: background-color 0.2s ease, transform 0.1s ease;
}

.mailto-btn:hover {
  background-color: #35495e; /* Vue dark */
  transform: translateY(-2px);
}

.context-details {
  font-size: 0.8em;
}


.nav-button {
  display: inline-flex;
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

  background-color: #7f1d1d;
  color: white;
}

.nav-button:hover {
  opacity: 0.8;
}
</style>