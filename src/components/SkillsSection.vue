<script setup lang="ts">
import {useNow, useDateFormat} from "@vueuse/core";
</script>
<template>
  <div class="skills-content">
    <h1>Hi.<br>我叫林家民。<br>我是一位軟體開發工程師。<br> <br>請參考我的相關經歷：</h1>

    <div class="experience-section">
      <h2>2024/07 以前：自學與個人專案</h2>
      <ul class="skills-list">
        <li>自高中時期開始自學 Python，隨後深入學習 Django 與 FastAPI，並將這些技術廣泛應用於個人專案與後續的職場工作中。</li>
        <li>前端技術從自學 React 與 Next.js 起步，目前則主要專注於 Vue。包含工作專案、個人開發，以及你現在正在瀏覽的這個個人網站，皆是使用 Vue 所建置。</li>
      </ul>
      <h2>2024/07 - 2024/10： 達豐公關 - 實習生</h2>
      <ul class="skills-list">
        <li>首次職場專案開發： 這是第一次在專業職場環境中進行大型專案開發，將原本非技術性質的繁瑣業務轉化為系統化的解決方案。</li>
        <li>自主開發 AutoDMS 自動化工具： 在擔任非技術職位期間，為解決每日為高階主管彙整科技新聞報表的繁瑣流程，利用閒暇時間開發了
          Chrome 擴充元件。
        </li>
        <li>系統結合了 LINE API 與 Firebase。只需將新聞連結傳送至 LINE 聊天機器人，Firebase
          就會自動執行基礎的網頁爬蟲與資料擷取；針對結構較複雜的網站，擴充功能會自動開啟新分頁並在背景完成進階爬蟲作業。
          <details class="context-details">
            <summary>為什麼需要串接 LINE？</summary>
            <p>因為要處理的新聞連結原本就是從 LINE 聊天室傳送過來的。在開發這個工具之前，我通常必須逐一開啟這些連結，然後手動複製並排版標題、日期、作者和內文。</p>
          </details> </li>


        <li>Chrome 擴充元件儀表板解決了過去在 Word 中手動複製貼上（標題、日期、作者、內文）以及難以調整排序的痛點。
        </li><li> 透過這個儀表板，只需點擊幾下即可輕鬆更改新聞分類與排列順序。
        </li>
        <li>將原本耗時的手動排版完全自動化，在儀表板點擊「匯出」後，系統會自動套用所有複雜的報表格式，提升工作效率。
        </li>
        <li><a href="https://youtube.com" target="_blank" rel="noopener noreferrer">實際操作展示影片</a></li>
        <li><a href="https://github.com/lostmypillow/autodms-ext" target="_blank" rel="noopener noreferrer">擴充元件 GitHub</a></li>
        <li><a href="https://github.com/lostmypillow/autodms-api" target="_blank" rel="noopener noreferrer">Firebase API GitHub</a></li>
        <li><a href="https://dms.lostmypillow.com" target="_blank" rel="noopener noreferrer">技術文件</a></li>
      </ul>

      <h2>2024/10 - {{useDateFormat(useNow(), 'YYYY/MM')}}：高偉數學補習班 - 資訊部⼯讀⽣ </h2>
      <ul class="skills-list">
        <li>-</li>
        <li>-</li>
        <li>-</li>
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