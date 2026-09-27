---
marp: true
theme: default
paginate: true
header: 'UX for AI: Human-Centered AI System Design'
footer: '薛念林 教授 | 逢甲大學資訊工程學系'
size: 16:9
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

<!-- _class: lead -->
# UX for AI: 以人為本的 AI 系統介面與互動設計
## Nielsen Heuristics in the AI Era (AI 產品的體驗設計心法)

**薛念林 教授**
逢甲大學 資訊工程學系

<span style="font-size: 14px; color: #64748b; margin-top: 24px; display: block;">（本講義與 Gemini AI 共同協作編製）</span>

---

## 本單元大綱 (Outline)

<div class="two-columns">
<div class="card">

### 🌐 AI 系統與現代互動挑戰
* 什麼是深度封裝的 AI 系統 (AI Systems)
* 知名應用案例：Copilot, Midjourney, Notion AI
* AI 時代的 6 大體驗痛點 (延遲、空白框、黑盒等)

</div>
<div class="card">

### 🛠️ 10 大原則在 AI 系統的心法與 Prompt
* NS01 ~ NS10 在 AI 時代的演進與心法
* 具體設計實務與建議提示詞架構
* 師生互動實踐 (CCQ & QA)

</div>
</div>

---

![bg fit](../../img/ux_for_ai_concept.png)

---

## AI 系統與應用的全面普及

<div class="two-columns">
<div class="card">

### 💡 什麼是 AI 系統 (AI Systems)？
* **非單純的大語言模型 (LLM)** ：它不是叫使用者去跟 ChatGPT/Claude 網頁版聊天，而是將 AI 能力深度封裝於工作流中的 **應用產品** 。
* **以人為本的系統整合** ：AI 扮演背景運算、自動完成、智能建議或自主代理人 (Agent) 的角色，提供直覺且自然的互動介面。

</div>
<div class="card">

### 🎯 AI 系統的關鍵應用範疇
* **智慧輔助與自動完成 (Co-piloting)** ：在開發或創作中給予行內建議。
* **上下文關聯操作 (Contextual Actions)** ：根據使用者目前選取的內容主動提供功能。
* **多模態智慧轉換 (Multimodal)** ：將文字、圖像、語音、程式碼等多種媒介進行無縫轉譯。

</div>
</div>

---

## 知名 AI 系統與應用案例 (Famous AI Systems)

<div class="two-columns">
<div class="card" style="font-size: 21px;">

* 💻 **GitHub Copilot** ：整合於 IDE 的 AI 結對程式員。透過灰色預測字元 (Ghost Text) 在行內即時推薦程式碼，極大提升開發效率。
* 🎨 **Midjourney / DALL-E 3** ：文字生成圖像系統。將複雜的藝術創作過程簡化為 Prompt 對話，從根本改變了創意設計流程。
* 📝 **Notion AI** ：將 AI 融入文件編輯器的右鍵/斜線選單。提供選取文字一鍵潤飾、翻譯、總結或擴寫的情境功能。

</div>
<div class="card" style="font-size: 21px;">

* 🌐 **DeepL** ：基於神經網絡的 AI 機器翻譯系統。具備極強的上下文理解力，能生成自然流暢的商業與學術翻譯。
* 🚗 **Tesla FSD (Full Self-Driving)** ：車載自動駕駛系統。採用純視覺神經網路，為車主提供端到端 (End-to-End) 的輔助駕駛體驗。
* 🔬 **AlphaFold** ：蛋白質結構預測系統。為生物學家提供高精度預測，將傳統實驗需耗時數年的工作縮短至數秒。

</div>
</div>

---

## AI 時代的 UX 挑戰與心法

> 面對大語言模型與生成式 AI（黑盒子、思考延遲、幻覺、輸出不確定性），如何以人為本重塑可用性原則？

<div class="three-columns">
<div class="card">

### 1. 緩解等待焦慮
* 拒絕靜態 Loading
* 打字機 Streaming 輸出
* 展開式 Thinking Steps

</div>
<div class="card">

### 2. 消除空白框恐懼
* 拒絕單一空白對話框
* 提示詞晶片 (Prompt Chips)
* 反白文字 AI 快捷懸浮球

</div>
<div class="card">

### 3. 對抗不確定性
* 隨時中斷生成 (Stop)
* 歷史版本輪播 (Carousel)
* 幻覺防範與優雅降級

</div>
</div>

---

## Slide 01: AI and NS01 (系統狀態能見度) - UX 設計心法

> *“系統應在合理時間內，透過適當的反饋，隨時讓使用者掌握目前狀態。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **緩解 AI 的「思考延遲（Latency）」：** 
  * 避免只用靜態的「Loading...」，改用 **打字機效果（Streaming）** 即時輸出內容。
  * 引入 **展開式「思考步驟（Thinking Steps）」** （如 DeepSeek/O1 的 CoT 摺疊面板），讓使用者清楚 AI 正在進行「聯網搜尋」、「閱讀文件」或「執行程式碼」。
* **多步驟 AI 工作流（Multi-Agent Workflows）：**
  * 使用狀態節點圖（Node Graph）或微步進器，向使用者顯示目前 AI 助理正在進行 5 個步驟中的第 2 步（例如：生成草稿 → 翻譯 → 校對）。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **DeepSeek-R1 / OpenAI o1** 思考摺疊面板。
* AI 進行推理時，介面會呈現一個名為 `Thought` 或 `Thinking` 的摺疊區塊，即時顯示其思考步驟（ **Chain of Thought, CoT** ）。使用者可展開查看詳細邏輯，以緩解等待焦慮。

</div>
</div>

---

![bg 80%](../../img/ns01_thinking_process.jpg)

---

## Slide 01: AI and NS01 (系統狀態能見度) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「我正在開發一個 [AI 簡報生成功能]。當使用者輸入主題後，AI 需要進行：資料檢索、大綱生成、內容撰寫、投影片排版等 4 個耗時步驟。
> 請為我設計符合 **Visibility of System Status** 原則的 UI 反饋機制：
> 1. 請規劃每一個步驟的狀態文案（如：正在尋找資料... 預估剩餘 10 秒）。
> 2. 請提供前端 React 或 Vue 的狀態變數（Variables，如 `isSearching`, `progressPercent`）之設計邏輯，讓工程師能直接套用。」

</div>

---

## Slide 02: AI and NS02 (真實世界與系統的對應) - UX 設計心法

> *“系統應說使用者的日常語言，而非工程師的技術術語，並遵循真實世界的邏輯習慣。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **將「模型參數」具象化：**
  * 避免在一般介面直接呈現 Temperature、Top_p、Token Limit 等大模型底層術語。
  * 將技術參數轉化為直覺的「擬真滑桿」或「單選按鈕」（例如：將 Temperature 轉化為「💡 創意表現：保守 → 豐富想像力」）。
* **擬真隱喻與控制：**
  * 使用「副駕駛（Copilot）」或「助理（Assistant）」的擬人化視覺隱喻，讓使用者知道它可以對話，而非面對一個冰冷的 Command Line。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Notion AI** 的「變更語氣」下拉選單。
* 後台模型參數如 `Temperature` （溫度）對大眾而言過於技術化。 Notion AI 將其轉化為直覺的「語氣調整」（例如：專業、日常、幽默、友善），更貼近使用者的日常語音習慣。

</div>
</div>

---

![bg 80%](../../img/ns02_match_real_world.jpg)

---

## Slide 02: AI and NS02 (真實世界與系統的對應) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「我們正在為非技術背景的主管開發一個 [AI 行銷文案助手]。大模型後台有 `Temperature`、`Presence Penalty`、`Frequency Penalty` 等參數需要調整。
> 請基於 **Match Between System and Real World** 原則，幫我重新設計這套設定介面：
> 1. 請將這些參數重新命名，換成商務人士直覺、大眾化的字眼（例如：『文案創意度』等）。
> 2. 請描述介面互動方式，並附上調整不同等級時，文字生成的模擬效果對照範例。」

</div>

---

## Slide 03: AI and NS03 (使用者控制與自由) - UX 設計心法

> *“使用者常會誤觸功能，系統必須提供明確的『緊急出口』與隨時能復原的 Undo/Redo 控制權。”*

<div class="two-columns-64">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **對抗 AI 的不確定性：**
  * 提供隨時 **「中斷生成（Stop Generating）」** 的按鈕，防止 AI 輸出過長或失控的內容。
  * 引入 **「版本輪播（Version Carousel）」** ：在 AI 生成的結果旁，提供 1/3 的左右切換鍵，允許使用者對比並找回前幾次生成的滿意版本。
  * **Prompt 局部編輯** ：使用者可以編輯對話歷史中的任何一則 Prompt，點擊後系統自動在該節點分支「重新生成」，不破壞原始對話。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **ChatGPT / Claude** 的「中斷生成」與「歷史版本切換」。
* 當 AI 輸出的內容偏離預期或陷入無限迴圈時，使用者可隨時點擊「■ 中斷生成 (Stop Generating)」按鈕；生成完成後，若對答案不滿意，可使用 `1/2` 左右按鈕切換並對比歷史生成的不同版本。

</div>
</div>

---

![bg 80%](../../img/ns03_user_control.jpg)

---

## Slide 03: AI and NS03 (使用者控制與自由) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「當我們的 [AI 程式碼生成器] 在輸出一段 50 行的程式碼時，使用者發現方向錯了，或者大模型陷入了無限循環。
> 請基於 **User Control and Freedom** 原則，為我設計介面的控制流程：
> 1. 設計一個隨時『中斷生成』的 UI 機制（包含視覺提示）。
> 2. 當使用者發現 AI 修改了他們原本的程式碼，應如何設計『一鍵還原 (Revert)』或『顯示差異對照 (Diff View)』的選項，以降低修改錯誤的焦慮。」

</div>

---

## Slide 04: AI and NS04 (一致性與標準) - UX 設計心法

> *“使用者不應懷疑不同的詞彙、操作或位置是否代表同一件事。需遵循平台既有慣例。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **建立 AI 互動的「新標準」：**
  * 雖然 AI 介面日新月異，但已建立起業界標準（Standards），設計時必須遵循：
    * `Cmd + K` 或 `Ctrl + K` 喚醒全域 AI 搜尋/指令面板。
    * 輸入框按 `Enter` 為發送，`Shift + Enter` 為換行。
    * 每一則 AI 回覆的底部必備「複製（Copy）」與「重新生成（Regenerate）」圖標。
* **反饋機制的一致性：** 全站統一使用「👍 / 👎」或「星星評分」收集使用者對 AI 回覆的滿意度，不可隨意更換評分標準。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Cursor / ChatGPT** 的標準輸入框按鍵設計。
* 全網 AI 助手已形成通用的操作標準：使用 `Enter` 鍵發送、 `Shift + Enter` 鍵進行換行；回覆內容底部一致使用「📋 複製」與「👍/👎 回饋評分」圖標。

</div>
</div>

---

![bg 80%](../../img/ns04_standards.jpg)

---

## Slide 04: AI and NS04 (一致性與標準) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「我們正在為企業內部多個不同業務系統（如：HR 系統、財務系統）設計內嵌的 [AI 對話助理]。
> 請基於 **Consistency and Standards** 原則，幫我制定一套跨系統的 AI 互動規範（UI Style Guide）：
> 1. 請定義 AI 輸入框的通用功能與快捷鍵規範（如發送鍵、清除鍵、歷史紀錄按鈕的位置）。
> 2. 請統一一套收集 AI 回覆品質反饋（👍/👎 評分）以及錯誤提示的共通 UI 樣式。」

</div>

---

## Slide 05: AI and NS05 (錯誤預防) - UX 設計心法

> *“比起提供好用的錯誤訊息，更好的設計是防範錯誤於未然（預防不合理的輸入或操作）。”*

<div class="two-columns-64">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **預防「糟糕輸入導致垃圾輸出（Garbage in, Garbage out）」：**
  * 一般使用者極度不擅長寫 Prompt。提供 **「提示詞晶片（Prompt Chips/Suggestions）」** 或模板（Templates），點擊即代入標準提示。
  * 輸入框中預設豐富的 **Placeholder 提示字** （例如：試試看輸入：『幫我把這段報告翻譯成日文...』），引導正確輸入。
* **智慧 Prompt 預檢（Pre-flight Check）：** 當檢測到使用者上傳了不支援的檔案格式，或輸入的 Prompt 語意含混時，在發送前以「Inline Suggestion」主動提醒。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **ChatGPT / Claude** 的「提示字晶片 (Prompt Chips)」與「預設預檢」。
* 一般使用者不擅長撰寫 Prompt 。輸入框下方預設提供常用範本的晶片（例如「分析數據」、「撰寫郵件」），點擊即可套用；且當上傳不支援的檔案格式時，發送按鈕會轉為禁用狀態，防止無效點擊。

</div>
</div>

---

![bg 80%](../../img/ns05_error_prevention.jpg)

---

## Slide 05: AI and NS05 (錯誤預防) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「使用者在使用我們的 [AI 圖表分析助理] 時，常常上傳了不支援的檔案格式（例如上傳了 `.rar` 壓縮檔，但系統僅支援 `.csv` 試算表），或者直接輸入了不具實質內容的 Prompt（如『哈囉』、『幫我做圖』）。
> 請基於 **Error Prevention** 原則，幫我設計一套防範機制的互動邏輯：
> 1. 在使用者點選發送前，如何進行檔案與文字的智慧預檢，並給予就地提示？
> 2. 設計一個 Prompt 引導輸入區，利用 Prompt Chips 與選單功能限制使用者的不當輸入。」

</div>

---

## Slide 06: AI and NS06 (易於識別，而非憑空記憶) - UX 設計心法

> *“讓資訊、動作與選項保持可見，降低使用者的記憶負荷。使用者不應背誦指令。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **告別「萬惡的空白輸入框（Empty State Fear）」：**
  * 不要只給使用者一個空無一物的對話框，這會帶來極高的認知摩擦（Cognitive Friction）。
  * 畫面上應常駐 **「最近使用的 Agent 助理」** 、 **「常用 Prompt 歷史紀錄」** 、或一鍵調用最近編輯的檔案。
* **情境選單（Contextual Actions）：**
  * 當使用者在網頁上反白選取一段文字時，立刻在游標旁彈出「AI 快捷懸浮球」（如：翻譯、總結、潤飾），讓使用者「看得到就能點」，不需手動複製貼上。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Notion AI** 的「文字選取 AI 懸浮選單」。
* 當使用者在頁面中反白選取任何文字時，系統會自動在游標旁彈出懸浮工具列，提供翻譯、摘要、重寫等 AI 情境按鈕。使用者「看見即可點選」，不需要回憶 `/` 指令或複製貼上。

</div>
</div>

---

![bg 80%](../../img/ns06_recognition.jpg)

---

## Slide 06: AI and NS06 (易於識別，而非憑空記憶) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「我們正在重構一個 [AI 寫作助手]。目前使用者進入系統後，只有一個全黑的空白輸入框，必須自行回想所有 AI 指令（例如：/summarize, /translate）。
> 請遵循 **Recognition Rather Than Recall** 原則：
> 1. 設計一個在輸入框下方、可橫向滑動的常用指令卡片區。
> 2. 當使用者在左側打字區選取特定段落時，設計一個在右側或游標旁彈出的快捷工具列（Contextual Menu），列出最適合該段落的 AI 工具選單。」

</div>

---

## Slide 07: AI and NS07 (使用彈性與效率) - UX 設計心法

> *“系統應能滿足新手與專家的不同需求。提供快捷操作以提高效率。”*

<div class="two-columns-64">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **專為高頻使用者設計的快捷路徑（Shortcuts）：**
  * **斜線指令（Slash Commands）：** 輸入 `/` 即可快速喚起功能選單（如 Notion AI 或 Slack）。
  * **@Mentions 跨領域調用：** 輸入 `@` 快速指派特定專長的 AI 代理人或引用外部知識庫（如 `@Designer`、`@CodingBot`）。
  * **一鍵自訂（Prompt Presets）：** 允許使用者將自己調校好、最常用的長 Prompt 存檔，設定成自訂按鈕（如：『以專業金融顧問的口吻回覆』快捷鍵）。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Cursor** 的 `@-mentions` 與 Notion AI 的 `/` 斜線指令。
* 針對高頻專業使用者， Cursor 允許在輸入框輸入 `@` 快速調用檔案 ( `@Files` )、資料夾 ( `@Folders` ) 或網頁 ( `@Web` )； Notion AI 支援輸入 `/` 快速喚起 AI 寫作助手，極大提升專家的操作效率。

</div>
</div>

---

![bg 80%](../../img/ns07_efficiency.jpg)

---

## Slide 07: AI and NS07 (使用彈性與效率) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「我們需要為 [AI 智能合約審查系統] 同時設計給『新手（一般法務助理）』與『專家（資深律師）』使用的介面。
> 請遵循 **Flexibility and Efficiency of Use** 原則，為我規劃功能：
> 1. 針對新手，提供步驟式點選審查（精靈引導）。
> 2. 針對專家，設計一個可通過鍵盤快捷操作的『命令控制台』（例如輸入 `/review` 快速審查、輸入 `@compliance` 調用合規知識庫），並支持自訂 Prompt 範本的快捷按鈕。」

</div>

---

## Slide 08: AI and NS08 (美學與簡約設計) - UX 設計心法

> *“投影片與介面不應包含無關或極少需要的資訊。每一個額外的資訊都會與重要資訊競爭注意波段。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **避免 AI「資訊轟炸（Information Overload）」：**
  * AI 生成內容空間有限且往往極長。避免一次性將幾千字全部扔給使用者。
  * **預設折疊與展開（Show More）：** 對於長篇文章、程式碼區塊或詳細的分析過程，預設僅顯示前 3 行與摘要，使用者有興趣再展開。
  * **善用資訊層級：** 使用粗體、高亮、標籤晶片和適度的卡片區塊區隔資訊，保持版面的整潔與高度可讀性。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Claude Artifacts** 獨立雙面板設計。
* Claude 將生成的長篇程式碼、網頁或圖表等複雜內容，自動拆分至右側獨立的預覽面板（ **Artifacts** ）中，避免左側對話框被幾千行的程式碼淹沒，保持版面極簡與高度可讀性。

</div>
</div>

---

![bg 80%](../../img/ns08_minimalist.jpg)

---

## Slide 08: AI and NS08 (美學與簡約設計) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「當我們的 [AI 商務分析師] 完成一個市場調研後，會自動生成一份包含數據表格、長篇分析、參考文獻、與 5 個圖表在內的巨大報告。目前的介面將這份報告像純文字檔一樣直接瀑布流灌入畫面，視覺非常混亂。
> 請遵循 **Aesthetic and Minimalist Design** 原則，重新排版此報告介面：
> 1. 請提供折疊與層級化方案，將文獻與長段落數據進行智慧收納。
> 2. 設計一個極簡的『資訊看板（Dashboard）』，只突出 3 個關鍵數據點，其他細節隱藏在點擊互動後呈現。」

</div>

---

## Slide 09: AI and NS09 (協助辨識、診斷與從錯誤中復原) - UX 設計心法

> *“錯誤訊息應以清晰白話呈現，精確指出問題，並建設性地提供具體解決方案。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **優雅防範 AI「幻覺（Hallucination）」與「失效」：**
  * 當 AI 的回答可能不準確或不符合事實時，介面應明確標記（如：「⚠️ 此回答由 AI 生成，關鍵資訊請交叉核對」），並提供快速重新生成。
* **API 連線/超時報錯優雅降級（Graceful Degradation）：**
  * 當 AI 服務過載（如 Token 耗盡、超時斷線），不要只拋出「HTTP 502 Bad Gateway」等狀態碼。
  * 應白話告訴使用者：「目前 AI 連線人數眾多，您的 Prompt 檔已自動儲存，您可以[一鍵重試]。」

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Cursor** 的終端機錯誤「Fix with AI」按鈕。
* 當編譯或執行出錯時， Cursor 在終端機輸出區直接提供「Fix with AI」一鍵修復按鈕。點擊後 AI 會讀取錯誤訊息並自動生成修正方案，協助使用者快速從錯誤中復原，而非僅僅拋出看不懂的錯誤碼。

</div>
</div>

---

![bg 80%](../../img/ns09_error_recovery.jpg)

---

## Slide 09: AI and NS09 (協助辨識、診斷與從錯誤中復原) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「當我們的 [AI 自動翻譯器] 在處理使用者上傳的 50MB 超大型 PDF 檔時，因為超時（Timeout）導致系統斷開連線。
> 請遵循 **Help Users Recognize, Diagnose, and Recover from Errors** 原則，幫我撰寫一套 UI 錯誤彈窗（Error Dialog）的文案與互動：
> 1. 說明原因（避免艱深程式碼）。
> 2. 提供具體復原手段（如：建議使用者一鍵將文件自動拆分成 3 個小檔案上傳、或一鍵重試）。」

</div>

---

## Slide 10: AI and NS10 (說明文件與輔助說明) - UX 設計心法

> *“雖然不需文件就能操作系統是最好的，但隨時提供易於檢索、聚焦任務且簡潔的說明文件依然不可或缺。”*

<div class="two-columns-73">
<div class="card" style="font-size: 21px;">

### 💡 AI 產品設計心法 (UX for AI)
* **「可解釋性 AI」（XAI, Explainable AI）即是最好的說明：**
  * AI 產生的推薦或決策，往往像個黑盒子。
  * 介面中必須在決策旁提供 **「解釋說明（Explain this recommendation）」** 的互動提示。例如：「為什麼我會看到這筆推薦？因為您在 3 天內曾瀏覽過 Python 與 UI 設計相關職缺。」這就是 AI 時代的「說明文件」。
* **情境化動態引導（Context-sensitive Copilot）：**
  * 揚棄傳統的大部頭 Help PDF。在輸入框旁設計輕量化的「互動式提示指南」，引導使用者逐步學會如何精準寫出「好 Prompt」。

</div>
<div class="card" style="font-size: 21px;">

### 🔍 真實系統應用案例
* **Perplexity AI / ChatGPT Search** 的數字引文腳註。
* AI 生成的內容可能存在幻覺。介面在每個事實論點旁標記數字腳註（例如 `[1]` , `[2]` ），滑鼠懸停或點擊可顯示該資訊的原始新聞或網頁來源，作為可信度的即時輔助說明。

</div>
</div>

---

![bg 80%](../../img/ns10_help_doc.jpg)

---

## Slide 10: AI and NS10 (說明文件與輔助說明) - 建議 Prompt

<div class="prompt-box" style="font-size: 19px;">

### 📝 建議 Prompt (AI for UX)
> 「我們正在為一個 [AI 個人理財投資分析助理] 設計新手引導。
> 請遵循 **Help and Documentation** 原則，幫我設計一套引導使用者如何對話的互動方案：
> 1. 設計一個 interactive tooltip（互動提示框），教導使用者如何包含『投資預算、風險偏好、時間軸』三個核心要素來向 AI 提問。
> 2. 提供 3 個新手一鍵套用的理財 Prompt 範本。」

</div>

---

## 實用講義精進技巧 (師生互動建議)

<div class="two-columns">
<div class="card">

### 1. 「Before & After」對比法
* **不好的傳統 AI 介面** ：
  * 空白對話框、缺少指引
  * 毫無狀態提示、死等 30 秒
  * 拋出 Raw Exception Log
* **現代 UX for AI 介面** ：
  * 打字機 Streaming + 思考步驟 CoT
  * 豐富 Prompt 晶片與懸浮快捷選單
  * 友善降級與可解釋性 (XAI)

</div>
<div class="card">

### 2. 課堂即時測試與互動
* 讓學生在課堂中拿出手機，打開主流 AI 工具（ChatGPT, Claude, Cursor, Notion AI）：
  * 找出它們在 **NS01 - NS10** 中分別做對了哪些設計？
  * 哪些地方仍有改進空間？
* 以實務體驗連結學術理論，大幅提升課堂參與度！

</div>
</div>

---

<!-- id: ux-ch04-ccq1 -->
## 🙋 概念核對問答 (CCQ1)

<div class="two-columns-64">
<div class="card">

### ❓ AI 信心度 (Confidence) 與防呆設計
**[ 是 / 否 ]**

> **「在 AI 輔助醫療診斷或智慧報稅系統中，為了建立使用者對 AI 的強大信任感，介面應一律以 100% 篤定的語氣呈現 AI 的分析結果，避免顯示『信心度 (Confidence Score: 68%)』或替代方案，以免引發使用者的懷疑與猶豫。」**

請判斷上述說法是否正確，並思考過度信任 (Over-reliance) 的風險。

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch04-ccq1)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch04-ccq1" target="_blank"><img src="../../img/ch04/ux-ch04-ccq1.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- id: ux-ch04-ccq2 -->
## 🙋 概念核對問答 (CCQ2)

<div class="two-columns-64">
<div class="card">

### ❓ 複雜長任務的 AI 等待體驗
當 AI 執行需耗時 15~20 秒的深度研究（如文獻交叉驗證）時，以下哪一種介面反饋設計最符合現代 UX for AI 的「透明度與等待心理學」？

* **(A)** 顯示全螢幕單一旋轉 Spinner，註明「運算中請勿關閉」
* **(B)** 採用動態思考進度（CoT），即時滾動顯示「正在搜尋 12 篇文獻 ➔ 萃取論點 ➔ 驗證數據」，並支援折疊
* **(C)** 立即顯示空白頁，待全部完成後瞬間重新整理
* **(D)** 將 Timeout 強制縮短為 3 秒，未完成直接中斷報錯

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch04-ccq2)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch04-ccq2" target="_blank"><img src="../../img/ch04/ux-ch04-ccq2.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- id: ux-ch04-qa1 -->
## 🙋 問答討論 (QA1)

<div class="two-columns-64">
<div class="card">

### 全面系統 UX 健檢
請挑選一個你常用的系統進行全方位診斷與優化構想：

1. **問題診斷** ：找出系統中違反 **Nielsen 10 大原則** 的 3 個具體問題。
2. **AI Prompt 實踐** ：寫出一段具備工程師思維的 Prompt，要求 AI 生成符合該 UX 規範的前端組件。
3. **AI 產品優化** ：若將該系統升級為 AI 智慧助手，你將如何設計防呆反饋與錯誤復原機制？

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch04-qa1)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch04-qa1" target="_blank"><img src="../../img/ch04/ux-ch04-qa1.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- _class: lead -->
# Thank You!
## 打造以人為本、流暢優雅的使用者體驗

**Q & A / 交流討論**
