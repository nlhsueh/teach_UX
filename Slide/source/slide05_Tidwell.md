---
marp: true
theme: default
paginate: true
header: 'Tidwell Interaction Design Patterns'
footer: '薛念林 教授 | 逢甲大學資訊工程學系'
size: 16:9
transition: fade
style: |
  section {
    font-family: 'PingFang SC', 'PingFang TC', 'Noto Sans CJK TC', 'Microsoft JhengHei', sans-serif;
    font-size: 24px;
    padding: 40px 50px;
    background-color: #f8fafc;
    color: #1e293b;
  }
  footer {
    font-size: 14px;
    color: #64748b;
  }
  section::after {
    font-size: 12px;
    color: #64748b;
  }
  h1 {
    color: #0f172a;
    font-size: 42px;
    margin-bottom: 20px;
    border-bottom: 3px solid #3b82f6;
    padding-bottom: 10px;
  }
  h2 {
    color: #1e40af;
    font-size: 32px;
    margin-top: 5px;
    margin-bottom: 16px;
    border-bottom: 2px solid #93c5fd;
    padding-bottom: 6px;
  }
  h3 {
    color: #0369a1;
    font-size: 24px;
    margin-top: 8px;
    margin-bottom: 8px;
  }
  p, li {
    line-height: 1.6;
  }
  ul, ol {
    margin-top: 6px;
    margin-bottom: 10px;
  }
  blockquote {
    background: #e0f2fe;
    border-left: 6px solid #0284c7;
    padding: 10px 18px;
    border-radius: 4px;
    margin: 12px 0;
    color: #0369a1;
    font-style: italic;
  }
  code {
    background: #f1f5f9;
    color: #b91c1c;
    padding: 2px 6px;
    border-radius: 4px;
    font-family: 'JetBrains Mono', 'Fira Code', Consolas, monospace;
    font-size: 0.9em;
  }
  pre {
    background: #f1f5f9;
    color: #1e293b;
    border: 1px solid #cbd5e1;
    padding: 14px;
    border-radius: 8px;
    font-size: 18px;
    line-height: 1.4;
  }
  pre code {
    background: transparent;
    color: inherit;
    padding: 0;
  }
  table {
    width: 95%;
    max-width: 1100px;
    border-collapse: collapse;
    margin: 16px auto;
    font-size: 19px;
  }
  th {
    background-color: #1e40af;
    color: white;
    padding: 10px 14px;
    text-align: left;
  }
  td {
    padding: 8px 14px;
    border-bottom: 1px solid #cbd5e1;
    vertical-align: middle;
  }
  tr:nth-child(even) {
    background-color: #f1f5f9;
  }
  .badge-good {
    background-color: #10b981;
    color: white;
    padding: 3px 8px;
    border-radius: 4px;
    font-weight: bold;
    font-size: 0.85em;
  }
  .badge-bad {
    background-color: #ef4444;
    color: white;
    padding: 3px 8px;
    border-radius: 4px;
    font-weight: bold;
    font-size: 0.85em;
  }
  .prompt-box {
    background-color: #f0fdf4;
    border: 2px solid #86efac;
    border-radius: 8px;
    padding: 12px 16px;
    margin-top: 10px;
  }
  .lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: linear-gradient(135deg, #eff6ff 0%, #dbeafe 100%);
  }
  .lead h1 {
    font-size: 50px;
    border-bottom: none;
    color: #1e3a8a;
    margin-bottom: 12px;
  }
  .lead h2 {
    font-size: 30px;
    color: #2563eb;
    font-weight: normal;
    border-bottom: none;
  }
  .part-cover {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: linear-gradient(135deg, #1e3a8a 0%, #1e40af 100%);
    color: #ffffff;
  }
  .part-cover h1 {
    color: #ffffff;
    font-size: 52px;
    border-bottom: 4px solid #60a5fa;
    padding-bottom: 16px;
    margin-bottom: 16px;
  }
  .part-cover h2 {
    color: #93c5fd;
    font-size: 30px;
    border-bottom: none;
    font-weight: normal;
  }
  .two-columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  .two-columns-64 {
    display: grid;
    grid-template-columns: 6fr 4fr;
    gap: 20px;
  }
  .two-columns-73 {
    display: grid;
    grid-template-columns: 7fr 3fr;
    gap: 20px;
  }
  .three-columns {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 14px;
  }
  .card {
    background: white;
    padding: 16px 18px;
    border-radius: 8px;
    box-shadow: 0 4px 6px -1px rgba(0,0,0,0.08);
    border: 1px solid #e2e8f0;
  }
  .full-img {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px 50px;
  }
  .full-img p {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    margin: 0;
  }
  .full-img img, img.full-img {
    max-width: 95%;
    max-height: 540px;
    object-fit: contain;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  }
  .img-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 480px;
  }
  .img-container img {
    max-width: 95%;
    max-height: 100%;
    object-fit: contain;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  }
  .card-img {
    display: flex;
    justify-content: center;
    align-items: center;
    background: transparent;
    border: none;
    box-shadow: none;
    padding: 0;
  }
  .card-img img {
    max-width: 100%;
    max-height: 440px;
    object-fit: contain;
    border-radius: 8px;
    border: none;
    box-shadow: none;
  }

---

<script>
  // 1. 支援由首頁 index.html 控制是否啟用換頁動畫
  const params = new URLSearchParams(window.location.search);
  const transitionPref = params.get('transition') ?? localStorage.getItem('marp-transition');
  if (transitionPref === 'false' || transitionPref === 'none') {
    document.querySelectorAll('section[data-transition], section[data-transition-back]').forEach(el => {
      el.removeAttribute('data-transition');
      el.removeAttribute('data-transition-back');
    });
  }

  // 2. 支援鍵盤輸入「數字 + Enter」直接跳轉至指定頁碼
  (function() {
    let pageBuffer = '';
    let bufferTimer = null;

    function getOrCreateIndicator() {
      let el = document.getElementById('marp-page-jump-indicator');
      if (!el) {
        el = document.createElement('div');
        el.id = 'marp-page-jump-indicator';
        el.style.cssText = 'position: fixed; bottom: 30px; right: 30px; background: rgba(15, 23, 42, 0.9); color: white; padding: 8px 16px; border-radius: 8px; font-family: system-ui, sans-serif; font-size: 16px; font-weight: 600; letter-spacing: 0.5px; z-index: 9999; box-shadow: 0 4px 14px rgba(0,0,0,0.25); backdrop-filter: blur(8px); border: 1px solid rgba(255,255,255,0.2); display: none; transition: all 0.15s ease;';
        document.body.appendChild(el);
      }
      return el;
    }

    window.addEventListener('keydown', function(e) {
      if (['INPUT', 'TEXTAREA'].includes(e.target.tagName) || e.altKey || e.ctrlKey || e.metaKey) return;

      const indicator = getOrCreateIndicator();

      if (e.key >= '0' && e.key <= '9') {
        pageBuffer += e.key;
        clearTimeout(bufferTimer);
        indicator.textContent = '📄 跳至第 ' + pageBuffer + ' 頁 (按 Enter 確認)';
        indicator.style.display = 'block';

        bufferTimer = setTimeout(function() {
          pageBuffer = '';
          indicator.style.display = 'none';
        }, 2500);
      } else if (e.key === 'Enter' && pageBuffer.length > 0) {
        e.preventDefault();
        const target = parseInt(pageBuffer, 10);
        pageBuffer = '';
        indicator.style.display = 'none';
        clearTimeout(bufferTimer);

        if (!isNaN(target) && target > 0) {
          const oldHash = window.location.hash;
          const newHash = '#' + target;
          if (oldHash === newHash) {
            window.dispatchEvent(new HashChangeEvent('hashchange'));
          } else {
            window.location.hash = newHash;
          }
        }
      } else if (e.key === 'Escape' || e.key === 'Backspace') {
        if (e.key === 'Backspace' && pageBuffer.length > 1) {
          pageBuffer = pageBuffer.slice(0, -1);
          indicator.textContent = '📄 跳至第 ' + pageBuffer + ' 頁 (按 Enter 確認)';
        } else {
          pageBuffer = '';
          indicator.style.display = 'none';
          clearTimeout(bufferTimer);
        }
      }
    });
  })();
</script>


<!-- _class: lead -->
# Tidwell 經典網頁與介面設計模式
## Designing Interfaces: Patterns for Effective Interaction Design

**薛念林 教授**
逢甲大學 資訊工程學系

<span style="font-size: 14px; color: #64748b; margin-top: 24px; display: block;">（本講義與 Gemini AI 共同協作編製）</span>

---

## Tidwell UX 設計模式 9 大核心分類

<div class="three-columns">
<div class="card">

**1. 一般性互動**
(General Interaction)
- 安全探索
- 立即喜悅
- 空間記憶

</div>
<div class="card">

**2. 組織內容**
(Organizing Content)
- 凸顯/搜尋/瀏覽
- 儀表板
- 精靈模式

</div>
<div class="card">

**3. 到處走走：導覽**
(Navigation)
- 逃生門
- 麵包屑
- 深連接

</div>
</div>

<div class="three-columns" style="margin-top: 16px;">
<div class="card">

**4. 網頁元素排版**
(Layout of Elements)
- 中央舞台
- 手風琴
- 模組化分頁

</div>
<div class="card">

**5. 行動裝置介面**
(Mobile Interfaces)
- 垂直堆疊
- 底部導航
- 無限清單

</div>
<div class="card">

**6. 清單展示**
(Lists)
- 雙面板選擇器
- 卡片
- 輪播轉盤

</div>
</div>

---

## Chapter 1: 一般性模式 (General Patterns)

<div class="two-columns">
<div>

- **TW1.1 安全探索 (Safe Exploration)**
- **TW1.2 立即喜悅 (Instant Gratification)**
- **TW1.3 足夠滿足 (Satisficing)**
- **TW1.4 中途改變 (Changes in Midstream)**
- **TW1.5 延遲選擇 (Deferred Choice)**
- **TW1.6 漸進建構 (Incremental Construction)**

</div>
<div>

- **TW1.7 習慣就好 (Habituation)**
- **TW1.8 零碎空檔 (Microbreaks)**
- **TW1.9 空間記憶 (Spatial Memory)**
- **TW1.10 預期記憶 (Prospective Memory)**
- **TW1.11 流暢重複 (Streamlined Repetition)**
- **TW1.12 只用鍵盤 (Keyboard Only)**

</div>
</div>

---

## TW1.1 ~ TW1.3：探索、即時與滿足

<div class="three-columns">
<div class="card">

### TW1.1 安全探索
- **「讓我放心探索，不會迷路也不會搞砸」**
- 提供隨時可用的返回與撤銷鍵，避免不可逆的阻撓畫面。
- 對應 NS01, NS03, NS09。

</div>
<div class="card">

### TW1.2 立即喜悅
- **「我想現在立刻完成任務，而不是等很久」**
- 第一畫面保持極簡，不要在第一個動作前塞入冗長說明或強制廣告。
- 對應 NS07。

</div>
<div class="card">

### TW1.3 足夠滿足
- **「看得懂、能用就好，不要強迫我詳讀」**
- 提示字精簡，以顏色與形狀傳達含義，直覺點擊即可完成。
- 對應 NS08。

</div>
</div>

---

## TW1.4 ~ TW1.6：彈性、延遲與漸進

<div class="three-columns">
<div class="card">

### TW1.4 中途改變
- **「我改主意了，讓我隨時調整」**
- 高鐵查詢結果頁上方直接保留搜尋列，可立即更換時段。
- 對應 NS03, NS07。

</div>
<div class="card">

### TW1.5 延遲選擇
- **「我現在不想填這個，讓我先用」**
- 降低註冊門檻，必填欄位降到最低，提供「稍後再設定」。
- 對應 NS08。

</div>
<div class="card">

### TW1.6 漸進建構
- **「改一點、看一下，逐步完善」**
- 即時反應變化，自動暫存草稿，提供即時預覽反饋。
- 對應 NS01。

</div>
</div>

---

## TW1.7 ~ TW1.12：習慣、空間與鍵盤

<div class="three-columns">
<div class="card">

### TW1.7 習慣就好
- 遵循使用者的肌肉記憶（`Ctrl+C`、儲存圖示）。
- 確認鍵位置切勿頻繁變換。
- 對應 NS04。

</div>
<div class="card">

### TW1.9 空間記憶
- **「別幫我亂移桌上的東西」**
- 常用功能固定在相同位置，避免選單位置動態亂跳。
- 對應 NS04, NS06。

</div>
<div class="card">

### TW1.12 只用鍵盤
- 專家使用者不希望手離開鍵盤。
- 支援完整 Tab 切換與快速鍵，Enter 鍵設定安全預設。
- 對應 NS07。

</div>
</div>

---

## Chapter 2: 組織內容 (Organizing Content)

<div class="two-columns">
<div>

- **TW2.1 凸顯、搜尋與瀏覽 (Feature, Search, Browse)**
- **TW2.2 行動裝置快速反應 (Mobile Direct Access)**
- **TW2.3 持續及時的訊息供給 (Streams and Feeds)**
- **TW2.4 媒體瀏覽器 (Media Browser)**
- **TW2.5 儀表板 (Dashboard)**
- **TW2.6 畫布加工具盤 (Canvas plus Palette)**

</div>
<div>

- **TW2.7 精靈模式 (Wizard)**
- **TW2.8 設定編輯器 (Settings Editor)**
- **TW2.9 備擇檢視 (Alternative Views)**
- **TW2.10 多工作空間 (Multiple Workspaces)**
- **TW2.11 協助系統 (Help Systems)**
- **TW2.12 標記分類 (Tagging)**

</div>
</div>

---

## TW2.1 凸顯、搜尋與瀏覽 (Feature, Search, Browse)

<div class="two-columns-64">
<div class="card">

### 現代內容發現的三大支柱
- **凸顯 (Feature)** ：在首頁核心視覺區推薦最重要、最吸引人的焦點內容或即時活動。
- **搜尋 (Search)** ：針對目標明確的使用者，提供自動補全搜尋框與多維度篩選器 (Facets)。
- **瀏覽 (Browse)** ：針對探索型使用者，提供圖文分類網格與清晰目錄。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：電商首頁 (Momo, Amazon)、串流影音 (Netflix)、新聞入口。
- **核心價值** ：同時滿足「隨意逛逛」與「精準找尋」兩種截然不同的使用者意圖。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_2_1_feature_search_browse.jpg)

---

## 內容組織核心模式：精靈、儀表板與漸進揭露

<div class="three-columns">
<div class="card">

### TW2.5 儀表板 (Dashboard)
- 以豐富圖表視覺化呈現關鍵 KPI 與即時數據。
- 定期自動更新，支援點擊鑽取 (Drilldown)。

</div>
<div class="card">

### TW2.7 精靈 (Wizard)
- 針對複雜任務，拆解為 `Step 1 ➔ 2 ➔ 3` 的線性引導。
- 降低使用者的認知負擔。

</div>
<div class="card">

### 漸進式揭露 (Progressive Disclosure)
- **回應式生效 (Responsive Enabling)** ：勾選某選項後才啟用相關子欄位。
- 預設隱藏進階參數。

</div>
</div>

---

## TW2.8 設定編輯器 (Settings Editor)

<div class="two-columns-64">
<div class="card">

### 集中式參數與個人化偏好管理
- **分類分群** ：將繁雜設定依模組分類（帳號、隱私安全、外觀、API 整合），避免單頁過長。
- **即時反饋 (Auto-save)** ：首選即時儲存並在頂部顯示狀態提示（如「已自動儲存」），減少額外點擊儲存按鈕。
- **防呆警示 (Danger Zone)** ：將敏感或破壞性操作（如刪除帳號）隔離於底部並以紅色標註二次確認。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：SaaS 控制台、系統偏好設定、VS Code 設定頁。
- **核心價值** ：提供清晰的控制權（NS03），降低誤觸風險（NS05）。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_2_8_settings_editor.jpg)

---

## TW2.9 備擇檢視 (Alternative Views)

<div class="two-columns-64">
<div class="card">

### 同一資料的多維度視角切換
- **模式本質** ：底層資料模型完全相同，但在介面上提供多種呈現維度以滿足不同工作情境。
- **常見檢視類型** ：
  - 📋 **表格清單 (Table List)** ：適合批次檢視、排序與精確欄位比對。
  - 🗂️ **看板模式 (Kanban Board)** ：強調工作流程與狀態推進。
  - 📅 **行事曆 / 時間軸 (Calendar & Timeline)** ：聚焦死線與時程依賴關係。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：Notion 數據庫、Jira 專案看板、Airtable。
- **核心價值** ：大幅提升專業工作效率與彈性（NS07）。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_2_9_alternative_views.jpg)

---

## Chapter 3: 到處走走（導航與路標）

<div class="two-columns">
<div>

- **TW3.1 清楚的進入點 (Clear Entry Points)**
- **TW3.2 選單頁面 (Menu Page)**
- **TW3.3 金字塔結構 (Pyramid)**
- **TW3.4 強制回應面板 (Modal Panel)**
- **TW3.5 深連接 (Deep Links)**
- **TW3.6 逃生門 (Escape Hatch)**
- **TW3.7 寬選單 (Fat Menus / Mega Menus)**

</div>
<div>

- **TW3.8 網站地圖頁尾 (Sitemap Footer)**
- **TW3.9 登入工具 (Sign-in Tools)**
- **TW3.10 進度指示器 (Progress Indicator)**
- **TW3.11 麵包屑記號 (Breadcrumbs)**
- **TW3.12 註解式捲軸 (Annotated Scrollbar)**
- **TW3.13 動畫轉場效果 (Animated Transition)**

</div>
</div>

---

## 關鍵導航模式解析：逃生門與網站地圖

<div class="two-columns">
<div class="card">

### TW3.6 逃生門 (Escape Hatch)
- 清楚醒目的退出按鈕，讓使用者隨時跳出當前流程，回到首頁或安全區。
- 如客服電話：「按 0 由專人服務」。

</div>
<div class="card">

### TW3.8 網站地圖頁尾 (Sitemap Footer)
- 在網頁最底部以分類展開完整連結目錄。
- 釋放 Header 負擔，善用無限垂直空間。

</div>
</div>

---

## TW3.5 深連接 (Deep Links)

<div class="two-columns-64">
<div class="card">

### 直達內容核心的精確導航
- **模式本質** ：為特定頁面中的「特定區塊、標題、評論或項目」提供獨立可分享的專屬 URL。
- **核心互動** ：
  - 懸浮於段落或標題時出現 🔗 錨點圖示。
  - 提供「複製特定段落連結 (Copy Deep Link)」與一鍵分享。
  - 點擊進入時，頁面自動平滑捲動至目標位置並以高亮提示。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：Figma 畫布定位連結、Notion 區塊連結、Google Docs 評論錨點。
- **核心價值** ：消除「進去首頁後找不到在哪」的溝通摩擦，團隊協作效率倍增。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_3_5_deep_links.jpg)

---

## TW3.7 寬選單 / 超級選單 (Fat Menus / Mega Menus)

<div class="two-columns-64">
<div class="card">

### 一覽無遺的二維全站架構導航
- **突破傳統下拉限制** ：將傳統單欄長下拉選單展開為橫跨畫面的多欄二維資訊矩陣。
- **架構要素** ：
  - 🗂️ **分欄分類** ：依產品線或服務類型分欄，搭配圖示與簡短副標。
  - 🌟 **特色推薦** ：在選單右側嵌入精選產品圖卡或行銷 Banner。
  - ⚡ **視覺階層** ：粗體主類別 + 易讀子連結，讓視線一秒掃描全貌。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：大型電商 (Amazon, ASOS)、企業雲端官網 (Microsoft, AWS)。
- **核心價值** ：將 3 層點擊縮短為 1 次懸停，降低架構迷航率。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_3_7_mega_menus.jpg)

---

## TW3.11 麵包屑記號 (Breadcrumbs)

<div class="two-columns-64">
<div class="card">

### 清楚標示「身在何處」的階層路標
- **模式本質** ：以水平文字鏈展示當前頁面在網站樹狀階層中的相對位置。
- **路徑格式** ：`首頁 > 3C 數位 > 耳機音響 > 無線降噪耳機`
- **設計規範** ：
  - 末端項目為當前頁面（不設超連結並加粗顯示）。
  - 每個父層級均可點擊，方便使用者一鍵回溯至上一層或根節點。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：深層電商商品頁、大型知識庫與說明文件。
- **核心價值** ：增強空間認知與安全感，大幅降低跳出率。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_3_11_breadcrumbs.jpg)

---

## Chapter 4: 網頁元素的排版 (Layout)

<div class="two-columns">
<div class="card">

### 排版模式清單
- **TW4.1 視覺框架 (Visual Framework)**
- **TW4.2 中央舞台 (Center Stage)**
- **TW4.3 同質性網格 (Grid of Equals)**
- **TW4.4 標題分區 (Titled Sections)**
- **TW4.5 模組化分頁 (Module Tabs)**
- **TW4.6 手風琴模式 (Accordion)**
- **TW4.7 可折疊面板 (Collapsible Panels)**
- **TW4.8 可移動面板 (Movable Panels)**

</div>
<div class="card">

### 核心原則
- **階層分明** ：利用標題、格線與負空間明確劃分資訊權重。
- **節省空間** ：在有限視窗內，利用 Tab 分頁與手風琴摺疊隱藏次要內容。
- **直覺對齊** ：保持網格對齊，消除視覺混亂。

</div>
</div>

---

## TW4.5 模組化分頁 (Module Tabs)

<div class="two-columns-64">
<div class="card">

### 在有限空間切換同一容器的內容模組
- **模式本質** ：將同一卡片或容器內的多組關聯資料，透過頂部分頁標籤進行切換顯示。
- **互動設計重點** ：
  - **當前狀態明顯** ：以底線、背景色反差或顏色高亮標記目前作用中的分頁。
  - **即時載入** ：切換時無需重新整理整個網頁，保持流暢體驗。
  - **資訊計數** ：分頁標籤可附帶數字徽章（如 `錯誤 (3)`、`待審核 (12)`）。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：開發者控制台、產品規格/評價頁籤、個人檔案設定。
- **核心價值** ：極致利用垂直空間，維持頁面視覺清爽（NS08）。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_4_5_module_tabs.jpg)

---

## TW4.6 手風琴模式 (Accordion)

<div class="two-columns-64">
<div class="card">

### 垂直堆疊與按需展開的折疊清單
- **模式本質** ：垂直排列的標題面板，點擊可向下展開詳細內容；展開新項目時可選擇自動收合其餘項目。
- **關鍵視覺要素** ：
  - 右側提供明確的展開/收合狀態圖示（`+ / −` 或 `⌵ / ⌃`）。
  - 平滑的高度過渡動畫，避免畫面突兀跳動。
  - 適合內容長短不一、使用者僅需挑選特定項目閱讀的情境。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：常見問答 (FAQ)、多步驟購物結帳表單、行動端篩選器。
- **核心價值** ：漸進式揭露資訊，避免超長頁面造成滾動疲勞。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_4_6_accordion.jpg)

---

## TW4.7 可折疊面板 (Collapsible Panels)

<div class="two-columns-64">
<div class="card">

### 彈性伸縮的專業工作區側邊欄
- **模式本質** ：將輔助功能（如檔案樹、屬性檢查器、AI 助理）置於可折疊收納的側邊欄。
- **核心機制** ：
  - 👈 **一鍵收折** ：點擊側欄切換按鈕或邊界圖示，側欄滑入/收合為緊湊圖示列。
  - ↔️ **邊界拖曳** ：支援拖曳邊界自訂寬度，適應不同螢幕大小。
  - 💻 **聚焦畫布** ：需要專注時收合兩側面板，最大化中央主要工作舞台。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：VS Code / Cursor 編輯器、Figma 設計介面、Notion 側邊導航。
- **核心價值** ：兼顧工具完整度與主要任務專注度（NS07, NS08）。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_4_7_collapsible_panels.jpg)

---

## Chapter 7: 清單展示模式 (Lists)

<div class="two-columns">
<div>

- **TW7.1 雙面板選擇器 (Two-Panel Selector / Split View)**
- **TW7.2 單視窗深入 (One-Window Drilldown)**
- **TW7.3 清單嵌板 (List Inlay，如 Google Map 路線詳情)**
- **TW7.4 卡片化設計 (Cards，圖像、文字與操作合一)**
- **TW7.5 縮圖網格 (Thumbnail Grid)**

</div>
<div>

- **TW7.6 旋轉木馬 / 輪播 (Carousel)**
- **TW7.7 分頁標註 (Pagination，長清單拆頁載入)**
- **TW7.8 跳至項目 (Jump to Item)**
- **TW7.9 字母/數字索引捲軸 (Alpha/Numeric Scroller)**
- **TW7.10 新項目預備列 (New-Item Row)**

</div>
</div>

---

## 清單模式對比：雙面板 vs 卡片 vs 嵌板

<div class="three-columns">
<div class="card">

### TW7.1 雙面板選擇器
- 左側為項目清單，右側為詳細內容。
- 適合寬螢幕桌面端 (如 Email 客戶端、檔案管理器)。

</div>
<div class="card">

### TW7.4 卡片 (Cards)
- 將圖文、標籤與操作封裝在獨立矩形卡片中。
- 響應式佈局極佳，適合手機與跨裝置呈現。

</div>
<div class="card">

### TW7.3 清單嵌板 (List Inlay)
- 點擊清單項目後，在原地向下展開詳細資訊。
- 無需跳轉頁面，保持上下文連貫。

</div>
</div>

---

## TW7.3 清單嵌板 (List Inlay)

<div class="two-columns-64">
<div class="card">

### 清單項目原地下拉展開的上下文延續
- **模式本質** ：點擊清單中的某一列時，直接在該列下方原地「嵌入展開」詳細資訊區塊。
- **設計優勢** ：
  - 🚫 **無需跳轉頁面** ：完全避免進入新頁面再按返回的繁瑣流程。
  - 🧭 **保持上下文** ：展開時使用者依然能看到清單前後的相鄰項目。
  - 📈 **階層式詳情** ：適合呈現時間軸軌跡、配送站點、訂單明細。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：Google Maps 路線轉乘詳情、物流行程追蹤、銀行交易明細。
- **核心價值** ：保持空間記憶與任務連貫性，大幅提升瀏覽效率。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_7_3_list_inlay.jpg)

---

## TW7.4 卡片化設計 (Cards)

<div class="two-columns-64">
<div class="card">

### 異質資訊的獨立模組化封裝
- **模式本質** ：將圖片、標題、標籤、摘要、作者資訊與操作按鈕封裝在獨立的矩形卡片中。
- **設計要素** ：
  - 🖼️ **視覺錨點** ：頂部特色封面圖吸引第一眼注意力。
  - 🏷️ **分類晶片 (Chips)** ：彩色標籤標示類別與狀態。
  - 🖱️ **清晰邊界與懸浮反饋** ：卡片具備微陰影與 Hover 浮起動效，暗示可點擊性。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：社群動態 (Pinterest)、文章列表 (Medium)、儀表板小工具。
- **核心價值** ：極佳的響應式適配能力，在手機與電腦間無縫重排。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_7_4_cards.jpg)

---

## TW7.6 旋轉木馬 / 輪播 (Carousel)

<div class="two-columns-64">
<div class="card">

### 橫向滑動的多項目探索展示
- **模式本質** ：在固定寬度區域內，以橫向排列卡片或橫幅，支援左右滑動切換。
- **必備互動指引** ：
  - 左右兩側提供清晰的箭頭切換按鈕。
  - 底部提供當前頁數指示圓點（Pagination Dots）。
  - 兩側邊緣卡片「稍微露出一角（Peek-a-boo）」，視覺暗示右側還有更多內容。

</div>
<div class="card">

### 💡 設計心法與適用情境
- **經典範例** ：Netflix 影集分類推薦、App Store 精選輪播、課程平台熱門推薦。
- **核心價值** ：在有限第一屏展示多個推薦項目，引導手勢橫向探索。

</div>
</div>

---

<!-- _class: full-img -->

![](../../img/tw_7_6_carousel.jpg)

---

## 綜合期末演練 🏄🏻‍♀️：全面系統 UX 健檢

<div class="card">

### 任務：挑選一個你常用的系統進行全方位診斷
1. **問題診斷** ：找出系統中違反 **Nielsen 10 大原則** 的 3 個具體問題。
2. **模式套用** ：挑選 2 個 **Tidwell 設計模式** （如 Wizard、Breadcrumbs、Cards 等）來改善該流程。
3. **AI Prompt 實踐** ：寫出一段具備工程師思維的 Prompt，要求 AI 生成符合該 UX 規範的前端組件程式碼。

</div>

---

<!-- _class: lead -->
# Thank You!
## 打造以人為本、流暢優雅的使用者體驗

**Q & A / 交流討論**
