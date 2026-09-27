---
marp: true
theme: default
paginate: true
header: 'Introduction to User Experience Design'
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
  // 支援由首頁 index.html 控制是否啟用換頁動畫
  const params = new URLSearchParams(window.location.search);
  const transitionPref = params.get('transition') ?? localStorage.getItem('marp-transition');
  if (transitionPref === 'false' || transitionPref === 'none') {
    document.querySelectorAll('section[data-transition], section[data-transition-back]').forEach(el => {
      el.removeAttribute('data-transition');
      el.removeAttribute('data-transition-back');
    });
  }
</script>


<!-- _class: lead -->
# Introduction to User Experience Design
## 使用者體驗設計導論

**薛念林 教授**
逢甲大學 資訊工程學系

<span style="font-size: 14px; color: #64748b; margin-top: 24px; display: block;">（本講義與 Gemini AI 共同協作編製）</span>

---

## 本單元大綱 (Outline)

<div class="two-columns">
<div class="card">

### 🔍 日常體驗與設計反思
- 生活中的體驗與設計
- 什麼是壞的 UX？經典案例與日常痛點
- 諾曼門 (Norman's Door) 與心智模型
- 糟糕設計類型分析（夜市擺攤型、顏料不用錢型、不知從何下手型）

</div>
<div class="card">

### 💡 UX 核心概念與實踐流程
- 什麼是使用者體驗 (UX)？
- UI (使用介面) vs. UX (使用體驗)
- 設計思考 (Design Thinking) 5 大階段流程
- 課堂觀念檢測與討論 (CCQ & QA)

</div>
</div>

---

## 生活中的體驗與設計

我們在生活的每一天，不斷地 **體驗** 各種 **設計** 。

- 🚌 搭乘大眾交通工具（公車動態、捷運刷卡閘門）
- 📱 滑手機使用 App（社群瀏覽、外送點餐、行動支付）
- 💻 辦公與學習系統（選課系統、請假系統、線上會議）
- 🚗 駕駛或操作各類設備（汽車中控螢幕、家電開關）

> **好的設計** 讓你如沐春風、自然流暢；
> **壞的設計** 讓你懷疑人生、挫折抓狂。

---

## 生活中處處是 UX

<div class="two-columns">
<div class="card">

### <span class="badge-good">好的 UX</span>
- 生活有效率、順手
- 感覺舒服、自然
- 帶來愉快的心情 😀
- 直覺無負擔，一次就做對

</div>
<div class="card">

### <span class="badge-bad">不好的 UX</span>
* 容易誤操作、迷路
* 浪費大量寶貴時間
* 讓人感到挫折與焦慮
* 產生困惑、生氣惱怒 😡

</div>
</div>

---

## 經典反面教材：Norman's Door (諾曼門)

<div class="two-columns">
<div class="card">

### 什麼是「諾曼門」？
當你看到一扇門，上面裝了漂亮的「拉手把」，你下意識用力往外拉——結果門紋絲不動，因為它是 **「推門」** 。門上甚至貼了手寫字條：`「請用推的 PUSH」`。

- **設計缺陷** ：外觀視覺特徵（Affordance / 預設用途）與實際操作邏輯相衝突。
- **使用者心理** ：使用者拉不開時往往會覺得「自己很蠢」，但 **這完全是設計師的責任** ！
- 參考來源：[Norman Door at Apple Store](https://www.reddit.com/r/CrappyDesign/comments/5wolzl/a_norman_door_at_the_apple_store/)

</div>
<div class="card-img">

<img src="../../img/normans_door.png" alt="Norman's Door">

</div>
</div>

---

## 遇到糟糕的 UI/UX，你會感到…

當系統介面難用、卡關、報錯不明時，使用者的真實情緒反映：

- 😣 **情緒受挫** ：丟臉、煩躁、委屈、羞恥
- ❓ **認知迷失** ：不悅、困惑、生氣、挫折
- 🚫 **信任崩塌** ：對該產品甚至品牌喪失信心，不再願意嘗試

<div data-marpit-fragment>

> 設計不良不僅僅是外觀難看，更會直接傷害使用者的心理安全感與效率！

</div>

---

![bg 100%](../../img/bad_ui_ux_frustration.jpg)

---

## 糟糕設計類型 (1)：夜市擺攤型

<div class="card">

### 特徵：資訊雜亂無章、隨機塞滿畫面
- **模式識別失效** ：現代電商的商品區塊（圖片、價格、名稱）位置固定。若區塊長寬比、對齊線、字體完全隨機，大腦無法建立模式，必須對每個點重新「對焦」，造成大腦極度疲勞。
- **缺乏視覺錨點** ：缺乏嚴格的網格系統（Grid System），使用者的視線無法沿著水平或垂直軸順暢掃描。
- **成因** ：往往不是審美問題，而是技術不足（例如只會用 Flow Layout 依序硬塞元件，且未規劃架構）。

</div>

---

<!-- _class: full-img -->

![](../../img/bad_design_night_market_arngren.png)

---

## 糟糕設計類型 (2)：顏料不用錢型

<div class="card">

### 「視覺虐待」與易讀性的毀滅
- **色彩對比崩壞（Color Contrast）** ：藍色漸層橫條紋搭配深紅細體字，產生視覺閃爍感，對色弱與年長使用者完全不可讀。
- **排版災難（Typography Nightmares）** ：隨機浮雕陰影增加視覺噪音；文字列表「左右交錯」長短不一，強迫視線痛苦地 Z 字型掃視。
- **缺乏負空間（White Space）** ：內容塞得密不透風，讓人感覺呼吸困難。
- **摧毀品牌信賴感** ：專業醫療或科技器材網站若採用五顏六色的隨意混搭，會直接摧毀安全感與專業度。

</div>

---

![bg 80%](../../img/bad_design_color_contrast_xray.png)

---

## 糟糕設計類型 (3)：不知從何下手型

<div class="card">

### 特徵：視覺過載、內容過剩、導覽失能
- **資訊洪流** ：首頁塞滿大量電話、Email、跑馬燈與未分類圖示，完全沒有視覺焦點。
- **寬度失控** ：文字段落橫跨整個螢幕且字距緊湊。
  - 人類最舒適的閱讀長度為 **每行 45 ~ 75 個字元** 。
  - 超寬排版強迫讀者的脖子與眼球頻繁左右擺動，嚴重損害閱讀體驗。
- **死連結（Broken Links）** ：大量按鈕點進去無效或 404，使用者徹底迷航。

</div>

---

![bg 80%](../../img/bad_design_cluttered_gates.png)

---

![bg 80%](../../img/bad_design_fcu_cs_old.png)

---

![bg 80%](../../img/mask_order_app_quiz.png)

---

![bg 80%](../../img/mask_order_app_answer.png)

---

## UX 為何如此困難？

<div class="two-columns">
<div class="card">

### 常見的開發盲點
- ❌ **只有模組思考，沒有系統思考** ：疊床架屋，來一個做一個。
- ❌ **只有系統思考，沒有使用者思考** ：忽略同理心與實際體驗。
- ❌ **沒有使用者研究，沒有需求分析** ：閉門造車。
- ❌ **沒有設計就直接施工** ：邊寫邊改，架構混亂。
- ❌ **沒有測試反饋與修正** 。
- 💸 **No Money** → 便宜行事；😴 **Lazy** → 知錯不改。

</div>
<div class="card-img">

<img src="../../img/why_ux_is_hard.jpg" alt="Why UX is Hard - Chaotic System Architecture">

</div>
</div>

---

## 迷思破解：系統難用只是美工不好嗎？

> **老師** ：「這個系統很難用，操作體驗很不順。」
> **學生** ：「我又不會畫圖，我美工很差沒辦法……」

<div class="card">

### 系統難用只和「美工」有關嗎？
- **絕對不是！** 美工（Visual Graphic）只負責視覺外觀與修飾。
- 系統難用通常源於：
  1. 資訊架構混亂（找不到功能）
  2. 互動流程繁瑣（多餘步驟）
  3. 狀態反饋缺失（不知道有沒有成功）
  4. 認知模型不匹配（用語只有工程師看得懂）

</div>

---

## 什麼是使用者體驗 (User Experience, UX)？

<div class="card">

### 權威定義 (ISO 9241-210 / Wikipedia)
> **The user experience (UX)** is how a user interacts with and experiences a product, system or service. It includes a person's perceptions of **utility**, **ease of use**, and **efficiency**.

- **使用者體驗 (UX)** 是使用者在與產品、系統或服務互動過程中的整體體驗與內在感受。
- 核心三要素：
  1. **效用 (Utility)** ：能否滿足使用者需求、解決問題？
  2. **易用性 (Ease of Use)** ：容易學習與操作嗎？
  3. **效率 (Efficiency)** ：完成任務是否迅速流暢？

</div>

---

## UI (使用介面) vs. UX (使用體驗)

<div class="two-columns">
<div class="card">

### UI (User Interface)
- **外在視覺與互動介面**
- 關注按鈕顏色、字體大小、排版、視覺階層、動效。
- 核心問題： **「產品看起來如何？操作元件長怎樣？」**

</div>
<div class="card">

### UX (User Experience)
- **內在心理感受與整體旅程**
- 關注按鈕位置合不合理、流程順暢度、能否減輕痛點。
- 核心問題： **「使用者用起來感覺如何？是否順利達成目標？」**

</div>
</div>

---

![bg fit](../../img/ui_vs_ux_comparison_new.jpg)

---

![bg fit](../../img/ui_vs_ux_comparison.jpg)

---

## 什麼是使用者體驗設計 (UX Design)？

<div class="card">

### UX Design 的定義
> **User Experience Design** is the process that design teams use to create products that provide meaningful and relevant experiences to users.
> It involves the design of the entire process of acquiring and integrating the product, including aspects of **branding**, **design**, **usability**, and **function**.

UX 設計是團隊為了打造 **有意義且具高度關聯性體驗** 的完整設計流程，涵蓋品牌塑造、介面設計、可用性評估及核心功能。

</div>

---

![bg fit](../../img/ux_core_process.jpg)

---

## UX 設計的標準核心流程：步驟解析

- **1. 探索 (Research)** ：研究使用者行為，理解他們「為什麼」這樣做。
- **2. 分析 (Analyze)** ：從調研結果提煉關鍵使用者目標與核心痛點。
- **3. 構思 (Ideate)** ：結合使用者目標、商業需求與技術規格擬定設計要求。
- **4. 設計 (Design)** ：產出低/高保真原型並提出具體解決方案。
- **5. 確認 (Test)** ：與真實使用者進行可用性測試，驗證方案是否達成目標。

---

<!-- id: ux-ch01-ccq1 -->
## 🙋 概念核對問答 (CCQ1)

<div class="two-columns-64">
<div class="card">

### UX 和 UI 的差異
**[ 是 / 否 ]**

> 對於使用者而言，UX 決定了系統是否「好用」，而 UI 則決定了系統是否「好看」。兩者相輔相成，缺一不可，共同構築了最終的使用者體驗。

請判斷上述說法是否正確，並簡述兩者的定義邊界。

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-ccq1)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-ccq1" target="_blank"><img src="../../img/ch01/ux-ch01-ccq1.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- id: ux-ch01-ccq2 -->
## 🙋 概念核對問答 (CCQ2)

<div class="two-columns-64">
<div class="card">

### UX
**[ 是 / 否 ]**

> 登入系統的時間過長，是屬於系統架構和效能的問題，與 UX 無關。

請參考 ISO9241-11 對 UX 的定義，判斷上述說法是否正確。

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-ccq2)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-ccq2" target="_blank"><img src="../../img/ch01/ux-ch01-ccq2.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- id: ux-ch01-ccq3 -->
## 🙋 概念核對問答 (CCQ3)

<div class="two-columns-64">
<div class="card">

### UX process
以下哪個活動 **不算** 在 UX 的標準流程中？

* **(A)** 了解使用者的痛點
* **(B)** 進行畫面的設計與確認
* **(C)** 進行市場的分析與調查
* **(D)** 開發一個雛形進行試用
* **(E)** 對系統進行壓力測試

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-ccq3)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-ccq3" target="_blank"><img src="../../img/ch01/ux-ch01-ccq3.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- id: ux-ch01-qa1 -->
## 🙋 問答討論 (QA1)

<div class="two-columns-64">
<div class="card">

### 分享你的糟糕 UX 體驗
請回想並描述一個你在日常生活中遇過 **UX 最糟糕的系統** （如學校系統、政府網站、點餐 App、售票系統等）：

1. **系統名稱與使用情境**
2. **操作時遇到的最大障礙或崩潰瞬間**
3. **這帶給你什麼心理感受？（困惑、生氣、無助）**
4. **如果你是設計師，你第一步想如何改善它？**

[線上作答](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-qa1)

  

</div>
<div class="card-img">

<a href="https://nlhsueh.github.io/nickedupocket/#/student/ux-ch01-qa1" target="_blank"><img src="../../img/ch01/ux-ch01-qa1.png" alt="QR Code" style="max-height: 280px;"></a>

</div>
</div>

---

<!-- _class: lead -->
# Thank You!
## 打造以人為本、流暢優雅的使用者體驗

**Q & A / 交流討論**
