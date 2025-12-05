---
theme: seriph
background: https://cover.sli.dev
title: WebConf 2025 網站開發分享
info: |
  ## Slidev Starter Template
  Presentation slides for developers.
  Learn more at [Sli.dev](https://sli.dev)
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# WebConf 2025 網站開發分享

2025.12.05

---
transition: fade-out
---

# 成員介紹

<div>
<span v-mark.underline.orange class="text-white text-2xl">
  Antonio
</span>
<ul class="mt-2">
  <li>全端工程師</li>
  <li>熱血青年</li>
</ul>
</div>

<div class="mt-10">
<span v-mark.underline.orange class="text-white text-2xl">
  Shin
</span>
<ul class="mt-2">
  <li>前端工程師</li>
  <li>目中無人的居巴老人</li>
  <li>文案糾察隊</li>
</ul>
</div>

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
<h1>🐰你找到彩蛋了嗎🥚</h1>

<div
v-motion
  :initial="{ opacity: 0 }"
  :enter="{ opacity: 1, transition: { duration: 300 } }"
  v-mark.underline.orange>提示 1：前端工程師的開發日常
  </div>
<div
v-motion
  :initial="{ opacity: 0 }"
  :enter="{ opacity: 1, transition: { duration: 300 } }"
  v-mark.underline.orange
  class="mt-4"
  >提示 2：JavaScript 的慣例</div>
</div>

---
transition: fade-out
---

# 開發內容

- 環境建置
- v-directive 特效
- p5 特效
- GSAP 特效
- SEO 優化
- Markdown 內容轉譯
  
<hr class="mt-4"/>

懶人包： 
- Antonio 做了 7 成
- Shin 是一個目中無人的居巴老人，負責使喚年輕人，糾察各種小地方

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
<h1>🛠️技術觀念篇</h1>

<ul>
 <li>網頁特效的底層邏輯</li>
 <li>SSR 框架的意義</li>
</ul>
</div>

---
transition: fade-out
---

# 網頁特效的底層邏輯

## 三大繪圖系統  
  
- CSS Animation：操縱 HTML 元素
- SVG：透過 SVG 標籤系統控制圖形變化（[參考](https://penspulse326.github.io/notes/web-effects/svg-morph/)）
- Canvas：異世界，常用於遊戲或生成式藝術

## 三個共通點  
  
- 圖像狀態：大小、顏色、位置
- 關鍵影格：圖像在指定幀的變化目標
- 時間函式：線性、快進慢出、抖動等

---
transition: fade-out
---

# SSR 框架的意義

## 傳統 MVC 怎麼處理前端？
- HTML：1 頁 = 1 支 HTML 檔
- JavaSciprt：jQuery 再戰十年
- 模組化：拆檔案，每支 HTML 各自用 `<script>` 載入需要的部分
- SEO：每支 HTML 個別填入 Meta Data

<div class="mt-10">
其實，好像沒有什麼特別不 OK 的地方對吧？<br/>
現在還是很多網站這樣做啊！
</div>

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
所以要不要使用前端框架<br/>
完全取決於團隊文化與專案性質<br/>
<del v-click="1">當然為了潮而使用的公司也很多</del><br/>
</div>

---
transition: fade-out
---

# SSR 框架的意義

## SPA 的特性
- 基於 Node.js 與 NPM 的開發環境，前端程式碼高度模組化
- 不依賴 JSP、CSHTML 等後端模板，統一使用框架的模板語言
- 只有 1 支 HTML，網頁內容由 JS 程式碼注入

## SSR 解決什麼問題

- 解決 SPA 動態注入網頁內容，而無法產生完整網站結構與 sitemap（透過預渲染產生完整 HTML 檔）
- 利用函式 / 元件快速客製化 Meta Data
- 很多好用的 config 可以一鍵處理打包、壓縮、CDN、Server 等 SEO 或維運設定
- 可以使用 Serverless，不需要全時運行的伺服器

---
transition: fade-out
---

# SSR 框架的意義

技術選型永遠是一體兩面的，有優點當然就會有缺點

### 技術門檻
- 需要對系統設計有一定程度了解，框架語法本身不是重點
- SSG/SSR/Client 的分層的分層做得不好可能更花錢、使用體驗更差

--

### 維運成本
- 有 SSR 的需求就要配置一個 Node.js Runtime 運行它，需要準備一個伺服器、容器或應用程式來跑
- 安全性更新很頻繁，基本上每個月都要更，更新後就壞了那是你家的事，沒寫測試也是你家的事 T_T

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
<h1>👄軟性溝通篇</h1>

<ul>
<li>工作項目打架了？</li>
<li>一句話說服設計師？</li>
</ul>
</div>

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
<h1
  v-motion
  :initial="{ y: 50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 800 } }"
>🤜工作項目打架了？</h1>

<div
  v-motion
  :initial="{ y: 30, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 300 } }"
  v-click=1
><del>那就去練舞室打！🤜🤜🤜</del></div>
<div
  v-motion
  :initial="{ y: 30, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 300 } }"
  v-click=2
  class="mt-4"
>要做什麼、誰來做、改了哪裡、哪裡有問題<br/>
直接講，「討論」出結論<br/>

<img src="./images/meme_manga.png" class="w-100"/>

拒絕當埋頭苦幹的松鼠隊友
</div>
</div>

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
<h1
  v-motion
  :initial="{ y: 50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 800 } }"
>🧐一句話說服設計師？</h1>

<div
  v-motion
  :initial="{ y: 30, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 300 } }"
  v-click=1
>「可能會影響品牌形象或使用體驗」</div>
<div
  v-motion
  :initial="{ y: 30, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 300 } }"
  v-click=2
><del>以上沒有在本次合作中講過</del></div>
</div>

---
transition: fade-out
---

# QA 時間
不知道要問什麼的話，下面也有一些備選話題🤣
- 研討會志工都在做什麼
- 六角教練的工作都在做什麼
- 最不想合作的星座前三名
- 其他八卦

---
class: text-center
transition: fade-out
---

<div class="h-full flex flex-col justify-center items-center font-bold">
<h1>😄Thanks for listening😄</h1>
</div>
