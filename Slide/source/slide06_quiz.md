---
marp: true
theme: default
paginate: true
header: 'UX Design 綜合題庫: 全章節實戰測驗與核心解析'
footer: '薛念林 教授 | 逢甲大學資訊工程學系'
size: 16:9
transition: fade
html: true
style: |
  section {
    font-family: 'PingFang SC', 'PingFang TC', 'Noto Sans CJK TC', 'Microsoft JhengHei', sans-serif;
    font-size: 24px;
    padding: 30px 45px;
    background-color: #f8fafc;
    color: #1e293b;
  }
  header {
    position: absolute;
    left: auto !important;
    right: 50px !important;
    top: 16px;
    font-size: 14px;
    color: #64748b;
    text-align: right;
    z-index: 1000;
  }
  header a.header-nav-arrow {
    display: inline-block;
    padding: 2px 6px;
    border-radius: 4px;
    color: #475569;
    text-decoration: none;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", system-ui, sans-serif;
    font-size: 13px;
    line-height: 1;
    transition: background 0.15s ease, color 0.15s ease;
  }
  header a.header-nav-arrow:hover {
    background: #e2e8f0;
    color: #1e293b;
  }
  .header-nav-wrapper {
    position: relative;
    display: inline-block;
  }
  .header-nav-title {
    display: inline-flex;
    align-items: center;
    cursor: pointer;
    padding: 3px 8px;
    border-radius: 6px;
    font-weight: 500;
    color: #475569;
    transition: background 0.15s ease, color 0.15s ease;
  }
  .header-nav-wrapper:hover .header-nav-title,
  .header-nav-wrapper.is-open .header-nav-title {
    background: #e0f2fe;
    color: #0369a1;
  }
  .nav-caret {
    font-size: 10px;
    margin-left: 4px;
    opacity: 0.6;
    transition: transform 0.2s ease;
    display: inline-block;
  }
  .header-nav-wrapper:hover .nav-caret,
  .header-nav-wrapper.is-open .nav-caret {
    transform: rotate(180deg);
    opacity: 1;
  }
  .nav-dropdown {
    display: none;
    position: absolute;
    right: 0;
    top: 100%;
    margin-top: 4px;
    width: 600px;
    max-height: 480px;
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(16px);
    -webkit-backdrop-filter: blur(16px);
    border: 1px solid #cbd5e1;
    border-radius: 12px;
    box-shadow: 0 16px 36px -4px rgba(15, 23, 42, 0.18), 0 6px 12px -2px rgba(15, 23, 42, 0.08);
    padding: 12px 14px;
    text-align: left;
    z-index: 99999;
    overflow-y: auto;
    box-sizing: border-box;
  }
  .nav-dropdown::before {
    content: '';
    position: absolute;
    top: -14px;
    left: 0;
    right: 0;
    height: 14px;
    background: transparent;
  }
  .header-nav-wrapper:hover .nav-dropdown,
  .header-nav-wrapper.is-open .nav-dropdown {
    display: block;
    animation: navFadeIn 0.18s cubic-bezier(0.16, 1, 0.3, 1);
  }
  @keyframes navFadeIn {
    from { opacity: 0; transform: translateY(-4px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .nav-dropdown-header {
    font-size: 13px;
    font-weight: 700;
    color: #1e293b;
    border-bottom: 1px solid #e2e8f0;
    padding-bottom: 8px;
    margin-bottom: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .nav-dropdown-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4px 10px;
  }
  .nav-dropdown-item {
    display: flex;
    align-items: center;
    padding: 6px 8px;
    border-radius: 6px;
    text-decoration: none;
    color: #334155 !important;
    font-size: 12px;
    line-height: 1.3;
    transition: all 0.12s ease;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .nav-dropdown-item:hover {
    background: #eff6ff !important;
    color: #1d4ed8 !important;
    font-weight: 600;
    transform: translateX(2px);
  }
  .nav-dropdown-item.active {
    background: #dbeafe !important;
    color: #1e40af !important;
    font-weight: 700;
  }
  .nav-dropdown-item .badge {
    display: inline-block;
    font-size: 11px;
    font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
    font-weight: 600;
    color: #64748b;
    background: #f1f5f9;
    padding: 1px 5px;
    border-radius: 4px;
    margin-right: 6px;
    flex-shrink: 0;
  }
  .nav-dropdown-item:hover .badge {
    background: #bfdbfe;
    color: #1e40af;
  }
  .nav-dropdown-item.active .badge {
    background: #3b82f6;
    color: #ffffff;
  }
  .nav-dropdown-item .item-text {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  footer {
    font-size: 13px;
    color: #64748b;
    bottom: 12px;
  }
  section::after {
    font-size: 12px;
    color: #64748b;
    bottom: 12px;
  }
  h1 {
    color: #0f172a;
    font-size: 40px;
    margin-bottom: 16px;
    border-bottom: 3px solid #3b82f6;
    padding-bottom: 10px;
  }
  h2 {
    color: #1e40af;
    font-size: 27px;
    margin-top: 0;
    margin-bottom: 12px;
    border-bottom: 2px solid #93c5fd;
    padding-bottom: 5px;
  }
  h3 {
    color: #0369a1;
    font-size: 20px;
    margin-top: 6px;
    margin-bottom: 6px;
  }
  .card {
    background: white;
    border-radius: 12px;
    border: 1px solid #e2e8f0;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    padding: 20px 24px;
  }
  .part-cover {
    background: linear-gradient(135deg, #1e3a8a 0%, #1e40af 50%, #2563eb 100%) !important;
    color: #ffffff !important;
    text-align: center;
  }
  .part-cover h1 {
    color: #ffffff;
    border-bottom: 3px solid #60a5fa;
    padding-bottom: 16px;
  }
  .part-cover h2 {
    color: #93c5fd;
    border-bottom: none;
    font-size: 26px;
  }
  .badge-topic {
    display: inline-block;
    background: #e0f2fe;
    color: #0369a1;
    font-weight: 700;
    font-size: 13px;
    padding: 2px 10px;
    border-radius: 6px;
    margin-bottom: 6px;
  }
  
  /* Quiz Interactive Grid */
  .quiz-grid {
    display: grid;
    grid-template-columns: 1.18fr 0.82fr;
    gap: 18px;
    align-items: stretch;
    height: 560px;
  }
  .quiz-card-left {
    background: white;
    border-radius: 12px;
    border: 1px solid #cbd5e1;
    box-shadow: 0 4px 10px rgba(15, 23, 42, 0.04);
    padding: 18px 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-sizing: border-box;
  }
  .quiz-scenario {
    font-size: 15.5px;
    line-height: 1.5;
    color: #334155;
    margin: 4px 0 8px 0;
  }
  .quiz-prompt {
    font-size: 16px;
    font-weight: 700;
    color: #0f172a;
    margin-bottom: 10px;
    line-height: 1.45;
  }
  .quiz-options-group {
    display: flex;
    flex-direction: column;
    gap: 7px;
  }
  .quiz-option-btn {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 8px 12px;
    border-radius: 8px;
    border: 1.5px solid #cbd5e1;
    background: #f8fafc;
    color: #1e293b;
    font-size: 14.5px;
    line-height: 1.4;
    cursor: pointer;
    text-align: left;
    transition: all 0.15s ease;
    user-select: none;
  }
  .quiz-option-btn:hover {
    background: #eff6ff;
    border-color: #3b82f6;
    transform: translateX(3px);
    color: #1d4ed8;
  }
  .quiz-option-btn .opt-badge {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 24px;
    height: 24px;
    border-radius: 6px;
    background: #e2e8f0;
    color: #475569;
    font-weight: 700;
    font-size: 12px;
    flex-shrink: 0;
    transition: all 0.15s ease;
  }
  .quiz-option-btn:hover .opt-badge {
    background: #3b82f6;
    color: white;
  }
  .quiz-option-btn.is-wrong {
    background: #fef2f2 !important;
    border-color: #f87171 !important;
    color: #991b1b !important;
    animation: quizShake 0.4s ease;
  }
  .quiz-option-btn.is-wrong .opt-badge {
    background: #ef4444 !important;
    color: white !important;
  }
  .quiz-option-btn.is-correct {
    background: #f0fdf4 !important;
    border-color: #22c55e !important;
    color: #166534 !important;
    font-weight: 600;
    box-shadow: 0 0 0 2px rgba(34, 197, 94, 0.2);
  }
  .quiz-option-btn.is-correct .opt-badge {
    background: #16a34a !important;
    color: white !important;
  }

  /* Right feedback column */
  .quiz-card-right {
    background: white;
    border-radius: 12px;
    border: 1px solid #cbd5e1;
    box-shadow: 0 4px 10px rgba(15, 23, 42, 0.04);
    padding: 18px 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    box-sizing: border-box;
    overflow-y: auto;
  }
  .quiz-status-pending {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    color: #64748b;
    padding: 24px 16px;
  }
  .quiz-status-pending .pending-icon {
    font-size: 46px;
    margin-bottom: 12px;
    opacity: 0.9;
  }
  .quiz-status-pending .pending-title {
    font-size: 18px;
    font-weight: 700;
    color: #1e3a8a;
    margin-bottom: 6px;
  }
  .quiz-status-pending .pending-desc {
    font-size: 13.5px;
    line-height: 1.5;
    color: #64748b;
    max-width: 290px;
  }
  
  .quiz-status-wrong {
    display: none;
    background: #fff1f2;
    border: 1.5px solid #fda4af;
    border-radius: 10px;
    padding: 14px 16px;
    margin-bottom: 12px;
    animation: quizFadeDown 0.25s ease;
  }
  .quiz-status-wrong .wrong-title {
    font-size: 16px;
    font-weight: 700;
    color: #e11d48;
    display: flex;
    align-items: center;
    gap: 6px;
    margin-bottom: 4px;
  }
  .quiz-status-wrong .wrong-desc {
    font-size: 13.5px;
    color: #9f1239;
    line-height: 1.45;
  }

  .quiz-status-correct {
    display: none;
    flex-direction: column;
    height: 100%;
    animation: quizFadeUp 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    box-sizing: border-box;
  }
  .quiz-encourage-banner {
    background: linear-gradient(135deg, #15803d 0%, #16a34a 100%);
    color: white;
    border-radius: 8px;
    padding: 10px 14px;
    margin-bottom: 10px;
    box-shadow: 0 4px 12px rgba(22, 163, 74, 0.2);
    flex-shrink: 0;
  }
  .quiz-encourage-banner .encourage-title {
    font-size: 16px;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .quiz-encourage-banner .encourage-sub {
    font-size: 12.5px;
    color: #dcfce7;
    margin-top: 2px;
  }
  .quiz-explanation-box {
    background: #f8fafc;
    border: 1px solid #cbd5e1;
    border-left: 4px solid #16a34a;
    border-radius: 8px;
    padding: 12px 14px;
    flex: 1;
    overflow-y: auto;
    box-sizing: border-box;
  }
  .quiz-explanation-box .exp-tag {
    display: inline-block;
    font-size: 12px;
    font-weight: 700;
    color: #15803d;
    background: #dcfce7;
    padding: 2px 8px;
    border-radius: 4px;
    margin-bottom: 6px;
  }
  .quiz-explanation-box .exp-text {
    font-size: 14px;
    line-height: 1.55;
    color: #1e293b;
  }
  .quiz-retry-btn {
    margin-top: 8px;
    background: white;
    border: 1px solid #cbd5e1;
    color: #475569;
    border-radius: 6px;
    padding: 5px 12px;
    font-size: 12.5px;
    font-weight: 600;
    cursor: pointer;
    align-self: flex-start;
    transition: all 0.15s ease;
    flex-shrink: 0;
  }
  .quiz-retry-btn:hover {
    background: #f1f5f9;
    border-color: #94a3b8;
    color: #0f172a;
  }

  @keyframes quizShake {
    0%, 100% { transform: translateX(0); }
    20%, 60% { transform: translateX(-6px); }
    40%, 80% { transform: translateX(6px); }
  }
  @keyframes quizFadeUp {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes quizFadeDown {
    from { opacity: 0; transform: translateY(-8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @media print {
    .nav-dropdown, .nav-caret, header a.header-nav-arrow {
      display: none !important;
    }
    .quiz-status-pending, .quiz-status-wrong, .quiz-retry-btn {
      display: none !important;
    }
    .quiz-status-correct {
      display: flex !important;
    }
    .quiz-option-btn.is-correct-key {
      background: #f0fdf4 !important;
      border-color: #16a34a !important;
      color: #15803d !important;
      font-weight: 700 !important;
    }
    .quiz-option-btn.is-correct-key .opt-badge {
      background: #16a34a !important;
      color: white !important;
    }
  }
---

<!-- _class: lead -->
<!-- _header: '' -->
# 全課程易用性與互動設計實戰題庫
## 24 題即時互動測驗、作答回饋與深度解析

**薛念林 教授**
逢甲大學 資訊工程學系

<span style="font-size: 15px; color: #64748b; margin-top: 24px; display: block;">涵蓋 UCD 導論、尼爾森 10 大原則、AI for UX、UX for AI 與 Tidwell 設計模式</span>

---
<!-- header: '本題庫大綱 (Outline)' -->

## 本題庫大綱 (Outline)

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px;">
<div class="card">

### 📘 前半部：基礎概念與尼爾森原則
- **[Part 1: 使用者體驗導論實戰測驗 (Q01 ~ Q03)](#3)**
  - UX vs UI 界線、UCD 核心心法、雙鑽石設計模型
- **[Part 2: 尼爾森 10 大原則與 AI-UX 測驗 (Q04 ~ Q13)](#7)**
  - NS01 狀態能見度 ~ NS09 錯誤復原全情境題
  - 1-10-100 品質成本法則與 RTCF 提示框架

</div>
<div class="card">

### 🚀 後半部：AI 體驗與設計模式
- **[Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)](#18)**
  - 上下文孤島、Planning Mode、閉環驗證、信心度與優雅降級
- **[Part 4: Tidwell 介面設計模式精選 (Q19 ~ Q24)](#24)**
  - Wizard 精靈、Deep Linking、Accordion、Breadcrumbs、Card List 等實戰題

</div>
</div>

---
<!-- header: 'Part 1: 使用者體驗導論實戰測驗 (Q01 ~ Q03)' -->

<!-- _class: part-cover -->
# Part 1: 使用者體驗導論實戰測驗 (Q01 ~ Q03)
## 從 UX 基礎心法到使用者中心設計 (UCD) 雙鑽石架構

---
<!-- header: 'Part 1: 使用者體驗導論實戰測驗 (Q01 ~ Q03)' -->

## ❓ 第 01 題：【UX 與 UI 的核心界線】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">某新創團隊在開發一款智慧健康管理 App。前端工程師認為只要套用最時髦的 UI 視覺元件庫、漸層色與微動畫，就能保證使用者擁有極佳的產品體驗。</div>
      <div class="quiz-prompt">依據本課程對 UX (User Experience) 與 UI (User Interface) 的本質定義，下列哪一項敘述最為正確？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>UI 設計優美即等於卓越的 UX，兩者本質完全相同</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>UI 聚焦於外觀視覺與互動觸點，UX 則涵蓋使用者在使用全過程中的整體感受、易用性與價值實現</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>UX 僅屬於後端工程師與產品經理的責任，UI 設計師不必涉入</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>UX 只能透過大量的 A/B 測試來定義，無法在前期進行使用者研究</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">UI (User Interface) 是介面外觀、色彩、排版與按鈕樣式等具體視覺與互動觸點；而 UX (User Experience) 則是使用者在與系統互動全程所感受到的整體滿意度、認知摩擦與問題解決程度。漂亮的 UI 若流程繁瑣或無法解決使用者問題，仍是糟糕的 UX。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 1: 使用者體驗導論實戰測驗 (Q01 ~ Q03)' -->

## ❓ 第 02 題：【使用者中心設計 (UCD) 核心心法】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">傳統軟體工程中常發生的「溝通代溝」，多半源於工程團隊直接依據數十頁文字規格書 (PRD) 埋頭開發，數月後交付時才發現與客戶期望大相逕庭，修改成本極高。</div>
      <div class="quiz-prompt">使用者中心設計 (User-Centered Design, UCD) 主張的核心做法為何？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>嚴格禁止客戶在交付驗收前查看任何開發中的半成品與原型</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>盡可能在專案前期透過訪談、雛形 (Prototypes) 與可用性測試讓真實使用者參與，並進行快速迭代</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>全權交由資深軟體架構師憑工程直覺定義使用者的最佳操作流程</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>將所有心力放在後端資料庫的正規化，介面待上線後再交給外包修改</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">UCD 強調「以人為本」，主張在軟體生命週期早期就必須引進真實使用者的回饋，透過低保真 (Low-fi) 與高保真 (High-fi) 雛形走查驗證需求，早期發現問題，避免在後期付出高昂的修改成本。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 1: 使用者體驗導論實戰測驗 (Q01 ~ Q03)' -->

## ❓ 第 03 題：【雙鑽石設計模型 (Double Diamond)】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">英國設計委員會 (Design Council) 提出的雙鑽石設計模型 (Double Diamond) 是 UX 與軟體工程創新極為推崇的架構，強調「發散 (Diverge)」與「收斂 (Converge)」的交替運用。</div>
      <div class="quiz-prompt">請問雙鑽石模型的四個核心階段依序為何？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>發想 (Discover) ➔ 定義 (Define) ➔ 開發 (Develop) ➔ 交付 (Deliver)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>編碼 (Code) ➔ 測試 (Test) ➔ 部署 (Deploy) ➔ 監控 (Monitor)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>需求 (PRD) ➔ 繪製 (Figma) ➔ 切版 (HTML) ➔ 上線 (Launch)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>訪談 (Interview) ➔ 繪圖 (Sketch) ➔ 會議 (Meeting) ➔ 結案 (Close)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">雙鑽石由兩個鑽石組成：第一個鑽石「做對的事情」(Discover 發散探索問題領域 ➔ Define 收斂定義真實痛點)；第二個鑽石「把事情做好」(Develop 發散探索解決方案 ➔ Deliver 收斂交付測試驗證)。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

<!-- _class: part-cover -->
# Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)
## 啟發式評估十準則、AI 介面防呆與約束式提示工程

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 04 題：【NS01 系統狀態能見度 (Visibility of System Status)】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">某雲端硬碟在使用者上傳 100 張高清相片時，介面不僅顯示「已完成 42/100 張 (42%)」，還以微步進進度條即時提示預估剩餘時間與上傳速率，而非只有靜態的等待圖示。</div>
      <div class="quiz-prompt">請問這項設計最直接符合哪一項尼爾森原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>NS01 系統狀態能見度 (Visibility of System Status)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>NS02 真實世界與系統對應 (Match Between System and the Real World)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>NS04 一致性與標準 (Consistency and Standards)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>NS08 美學與簡約設計 (Aesthetic and Minimalist Design)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS01 要求系統應在合理時間內，透過適當的反饋（如進度條、完成百分比、剩餘時間），隨時讓使用者清楚掌握目前狀態，消除等待時「是否當機或斷線」的未知焦慮。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 05 題：【NS02 真實世界與系統對應 (Match Between System and Real World)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">電子書閱讀 App 在翻頁時模擬紙本書籍的翻頁動畫與紙張摩擦音效，並將收藏書籍的分類介面設計成木質書架，刪除檔案則使用「丟入桌面垃圾桶」的動作。</div>
      <div class="quiz-prompt">請問這項設計最能體現哪一項原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>NS01 系統狀態能見度 (Visibility of System Status)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>NS02 真實世界與系統對應 (Match Between System and the Real World)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>NS06 易於識別而非記憶 (Recognition Rather than Recall)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>NS07 彈性與使用效率 (Flexibility and Efficiency of Use)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS02 要求系統說使用者的日常語言，使用通俗熟悉詞彙，並遵循真實世界的物理習慣與邏輯隱喻（如木質書架、翻頁效果與實體垃圾桶），降低使用者的心智轉譯負擔。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 06 題：【NS03 使用者控制與自由 (User Control and Freedom)】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">使用者在郵件軟體中誤將 50 封重要信件整批選取並點擊「刪除」。系統立即在底部浮現橫幅：「已將 50 封郵件移至垃圾桶 [復原 (Undo)]」，並持續顯示 10 秒供隨時點擊復原。</div>
      <div class="quiz-prompt">請問這項設計符合哪一項原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>NS03 使用者控制與自由 (User Control and Freedom)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>NS05 錯誤預防 (Error Prevention)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>NS08 美學與簡約設計 (Aesthetic and Minimalist Design)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>NS10 說明文件與輔助 (Help and Documentation)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS03 指出使用者常會因誤觸功能而出錯，系統必須提供清晰標記的「緊急出口」（Emergency Exit）與支援 Undo/Redo 的反悔機制，讓使用者能自主掌控全局而不致恐慌。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 07 題：【NS04 一致性與標準 (Consistency and Standards)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">某跨平台系統在 iOS App 遵循蘋果 HIG 將主導覽列置於底部，在桌面 Web 遵循頂部 Header 導航；全站無論在哪個頁面，「加入購物車」一律是深橘色按鈕、「立即結帳」一律是綠色按鈕，危險操作一律是紅色文字。</div>
      <div class="quiz-prompt">請問這項設計主要符合哪一項原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>NS03 使用者控制與自由 (User Control and Freedom)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>NS04 一致性與標準 (Consistency and Standards)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>NS06 易於識別而非記憶 (Recognition Rather than Recall)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>NS09 協助辨識與復原錯誤 (Help Users Recover from Errors)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS04 要求系統遵循平台的既定慣例（如 iOS 與 Web 的標準）與全站統一的視覺規範（Design System）。相同的文字、色彩與按鈕在不同頁面具備一致意義，能有效降低使用者的學習門檻。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 08 題：【NS05 錯誤預防 (Error Prevention)】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">在訂房系統的表單中，當使用者選擇「入住日期：2026/10/15」後，系統會自動將「退房日期」選擇器中早於 10/15 的所有日期設為灰色反灰且不可點選狀態。</div>
      <div class="quiz-prompt">請問這項設計的核心價值為何？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>屬於 NS05 錯誤預防，防範不合理的輸入與操作於未然</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>屬於 NS09 錯誤復原，在使用者輸入錯誤後跳出警告視窗</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>屬於 NS10 說明文件，教導使用者如何正確看懂日曆</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>屬於 NS01 狀態能見度，告知使用者目前資料庫的空房數量</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS05 主張「預防勝於治療」。比起在使用者送出非法日期後拋出錯誤對話框，更好的設計是在輸入時直接透過介面約束 (Constraints) 將錯誤發生的機會消除於萌芽階段。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 09 題：【NS06 易於識別而非記憶 (Recognition Rather than Recall)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">在電商網站搜尋時，輸入框下方自動列出使用者「最近搜尋過的關鍵字」與「最近瀏覽過的 5 件商品」，且在比較多款筆電時提供並排規格比較表。</div>
      <div class="quiz-prompt">請問這項設計主要符合哪一項原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>NS02 真實世界與系統對應</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>NS06 易於識別而非記憶 (Recognition Rather than Recall)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>NS07 彈性與使用效率</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>NS04 一致性與標準</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">人類大腦擅長辨識 (Recognition) 而不擅長憑空回憶 (Recall)。將選項、動作與歷史紀錄直接呈現在眼前，使用者「看見就能點選」，可大幅減輕記憶負擔。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 10 題：【NS07 彈性與使用效率 (Flexibility and Efficiency of Use)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">圖形設計工具為新手提供視覺化圖示工具列與步驟指引精靈，同時為資深專家提供大量的單鍵快捷鍵（如 V 選擇、B 筆刷、Cmd+J 複製圖層）與自訂批次巨集功能。</div>
      <div class="quiz-prompt">請問這項設計符合哪一項原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>NS03 使用者控制與自由</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>NS07 彈性與使用效率 (Flexibility and Efficiency of Use)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>NS08 美學與簡約設計</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>NS05 錯誤預防</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS07 要求系統兼顧新手與專家的不同步調。新手可以循序漸進點選按鈕，而高頻資深專家則能透過快捷加速器 (Accelerators) 實現極致的操作效率。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 11 題：【NS08 美學與簡約設計 (Aesthetic and Minimalist Design)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">某資訊看板將數百條未分類的各類數據無差別全部堆砌在首頁，充斥五顏六色的圖表與閃爍字體，使用者難以找到重點。依據 NS08 原則，最佳改善方案為何？</div>
      <div class="quiz-prompt">下列哪一項改善策略最符合 NS08 美學與簡約設計？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>在頁面頂部加上一個搜尋框即可，首頁內容保持不變</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>建立明確的資訊層級，預設僅展示 3 個核心指標卡片與精簡摘要，其餘細節提供「展開查看完整推演」</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>增加更多跳轉連結與側邊欄廣告以塞滿留白空間</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>將字體全部改為超小字級以塞下更多圖表</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS08 指出介面不應包含無關或極少需要的資訊。每一個額外的雜訊都會與真正重要的資訊競爭注意力。適當留白、預設折疊與清楚的層級收納是簡約美學的核心。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 12 題：【NS09 協助辨識、診斷與從錯誤中復原】

<div class="quiz-grid" data-answer="C">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">使用者在註冊網站填寫密碼時若長度不足，下列哪一種介面反饋方式最符合 NS09 的優良設計實踐？</div>
      <div class="quiz-prompt">下列哪一種錯誤反饋方式最符合 NS09 原則？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>彈出警示對話框顯示：Error Code: 0x8004005 Validation Failure</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>僅在輸入框周圍亮紅框，但不給予任何文字說明</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>在密碼框下方即時以紅字清晰提示：「密碼長度不足，至少需包含 8 個字元與 1 個數字」，並標出尚缺條件</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>靜默重設整個表單，強迫使用者從姓名重新填寫</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(C) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">NS09 要求錯誤訊息必須以清楚淺白的日常語言呈現，嚴禁直接拋出底層錯誤碼；更重要的是必須精確指出問題所在，並建設性地給予復原指引，引導使用者完成正確操作。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 2: 尼爾森 10 大原則與 AI 提示工程 (Q04 ~ Q13)' -->

## ❓ 第 13 題：【1-10-100 法則與 RTCF 提示框架】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">軟體工程中的「1-10-100 品質成本法則」強調前期預防的重要性。而在運用 AI 生成符合 UX 規範的組件時，RTCF 框架能確保輸出品質。</div>
      <div class="quiz-prompt">關於 1-10-100 法則與 RTCF 提示詞架構，下列哪一項敘述正確？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>1-10-100 代表開發速度需提升 100 倍；RTCF 代表 Run, Test, Code, Fix</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>1-10-100 指在需求/UX 階段修正花 1 元，後期修改成本呈指數劇增；RTCF 為 Role（角色）、Task（任務）、Constraint（約束）、Few-shots（少樣本）</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>1-10-100 指預算分配比例；RTCF 指 React, TypeScript, CSS, Figma</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>1-10-100 指 A/B 測試人數；RTCF 代表 Return, Throw, Catch, Finally</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">1-10-100 法則證明了前期 UX 確認的極高價值（前期改花 1 元，上線後改花 100 元）；而在使用 AI 協同設計 UI 時，透過 RTCF 框架定義明確的約束 (Constraint) 能確保 AI 生成程式碼符合可用性標準。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)' -->

<!-- _class: part-cover -->
# Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)
## 從黑盒子走向透明人機協同，Agentic 閉環與優雅降級

---
<!-- header: 'Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)' -->

## ❓ 第 14 題：【傳統對話型 Prompting 的上下文孤島】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">在複雜軟體開發中，傳統「在網頁對話框 (Chat UI) 反覆複製貼上 Prompt」的協同模式，常讓開發者感到效率低落且繁瑣。</div>
      <div class="quiz-prompt">請問這最能說明傳統對話型 Prompting 的哪一項核心局限？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>大型語言模型的推理速度過慢</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>上下文孤島 (Context Silo) 與缺乏全專案視野，AI 無法主動調用工具驗證成果</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>模型欠缺基本的程式碼語法檢查能力</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>對話介面無法輸出超過 50 行的文字</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">傳統 Chat Prompting 的 AI 被困在單一對話框中，無法直接感知整個專案的目錄架構、相依性與執行環境，且無法自主驗證修改是否引發編譯報錯，迫使工程師成為人工搬運工。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)' -->

## ❓ 第 15 題：【Agent 規劃優先原則 (Planning Mode)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">Google Antigravity IDE 等現代 Agentic AI 開發環境在處理大型任務時，提倡「Planning Mode（規劃審查模式）」。</div>
      <div class="quiz-prompt">請問 Planning Mode 的核心人機協同優勢為何？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>讓 AI 在完全不通知使用者的情況下直接覆寫所有程式碼</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>在動手修改前，先梳理架構脈絡並生成多步驟實施藍圖供工程師審查審核，確保方向正確後再執行</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>強制將所有後端邏輯轉寫為 Python 腳本</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>限制 AI 每次只能修改一行程式碼以節省 Token</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">Planning Mode 體現了以人為本的人機協同：在進入破壞性執行前，先產出清晰的步驟藍圖與風險評估，讓人類具備充分的知情權與控制權（Approve/Reject/Edit），避免失控修改。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)' -->

## ❓ 第 16 題：【閉環驗證與自主走查 (Feedback Loop)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">Agentic 軟體工程強調 AI 的自主執行能力與自我修正機制。</div>
      <div class="quiz-prompt">下列哪一項行為最能說明 Agentic 模式的「閉環驗證 (Feedback Loop)」？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>AI 生成程式碼後直接向使用者宣布任務完成，不進行任何測試</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>AI 生成修改後，自主調用終端機執行編譯與單元測試，若遇錯誤則讀取堆疊日誌自我修正，直至測試全數通過</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>AI 隨機挑選檔案刪除以測試系統的容錯能力</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>遇到錯誤時直接終止任務並要求使用者重新開新對話</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">閉環驗證是 Agent 區別於傳統單向輸出的關鍵。 Agent 具備工具調用能力（Tool Use），能在沙盒中自動執行編譯指令或單元測試，遇到錯誤自主修復，形成「生成 ➔ 驗證 ➔ 診斷 ➔ 修正」的自治閉環。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)' -->

## ❓ 第 17 題：【AI 信心度 (Confidence Score) 與防呆信任】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">在醫療輔助診斷、財務風控或法律諮詢等高風險 AI 系統中，介面設計應如何處理 AI 的分析結果，以防範使用者「過度信任 (Over-reliance)」？</div>
      <div class="quiz-prompt">下列哪一項設計最符合 UX for AI 的防呆信任架構？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>一律以 100% 絕對篤定的語氣宣稱診斷無誤，以建立使用者無條件的信任</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>呈現結果時附帶信心度指標（如：信心度 72%）、備選方案與推論依據，並提醒使用者進行專業交叉核對</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>隱藏所有推論過程，只顯示最後的處方籤</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>強制使用者在 3 秒內接受 AI 的建議否則鎖定系統</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">過度信任是 AI 互動設計的重大隱憂。透過誠實揭露信心水準、列出替代解釋並提醒人類審查，能保持使用者批判性思維，避免因盲信 AI 幻覺而釀成重大事故。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 3: UX for AI 體驗設計與 Agent 轉移 (Q14 ~ Q18)' -->

## ❓ 第 18 題：【AI 服務異常的優雅降級 (Graceful Degradation)】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">當大型語言模型處理長文本發生網路連線超時 (Timeout) 或 API 額度過載時，介面應如何向使用者反饋？</div>
      <div class="quiz-prompt">下列哪一種設計最符合 UX for AI 的優雅降級 (Graceful Degradation)？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>畫面直接崩潰變白，並在控制台拋出 HTTP 504 Gateway Timeout</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>白話告知連線超時、自動暫存使用者已輸入的 Prompt 與上傳文件，並提供「一鍵重試」與「自動分段處理」建議按鈕</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>彈出警示框責備使用者的網路環境不佳</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>自動刪除所有對話紀錄以釋放記憶體</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">優雅降級在 AI 服務中至關重要。當底層 API 斷線或過載，系統應妥善保護使用者輸入的資料資產，並以建設性的行動選項協助復原，絕不可拋出未經包裝的底層狀態碼。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

<!-- _class: part-cover -->
# Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)
## 經典 UI 模式庫：導覽架構、多步驟表單與空間收納

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

## ❓ 第 19 題：【Wizard 步驟精靈模式】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">依據 Tidwell 介面設計模式，當使用者面對線上綜合所得稅申報、複雜帳號註冊等具備高認知負擔且具嚴格先後順序的多步驟任務時。</div>
      <div class="quiz-prompt">請問最推薦採用的模式為何？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>Accordion (手風琴)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>Wizard (步驟精靈模式)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>Deep Linking (深層連結)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>Infinite Scroll (無限滾動)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">Wizard 模式將複雜龐大的長表單拆解成數個邏輯連貫的線性步驟（如：身分驗證 ➔ 收入確認 ➔ 扣除額計算 ➔ 繳稅確認），並搭配進度步進器，大幅降低使用者的認知負荷與出錯率。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

## ❓ 第 20 題：【Deep Linking 深層連結模式】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">某企業知識庫系統包含數百篇長篇技術文件與多層級 API 規範。工程師希望能直接將文件中某個具體章節或特定程式碼區塊的 URL 複製分享給同事，點擊後頁面能自動精準滾動至該段落。</div>
      <div class="quiz-prompt">請問這體現了哪種 Tidwell 模式？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>Deep Linking (深層連結)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>Modal Dialog (強制對話框)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>Carousels (輪播卡片)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>Breadcrumbs (麵包屑)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">Deep Linking（深層連結）為頁面內的特定錨點、狀態或子內容提供唯一的 URL。使用者點擊後能直接精準抵達該特定內容，極大促進協同合作與知識分享效率。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

## ❓ 第 21 題：【Accordion 手風琴模式】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">在行動端或空間受限的設定頁面中，若有 10 個互不干擾的偏好設定項目（如：隱私設定、通知頻率、主題色彩等），設計師希望使用者能在單一視窗中瀏覽所有項目大綱，並僅在需要時就地展開細節。</div>
      <div class="quiz-prompt">請問最合適的模式為？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>Accordion (手風琴 / 折疊卡片)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>Wizard (步驟精靈)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>Splash Screen (啟動閃屏)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>Pagination (多頁分頁)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">Accordion 模式透過垂直堆疊的標題欄，允許使用者點擊「就地展開/收攏」感興趣的內容區塊，在極度節省垂直螢幕空間的同時，維持宏觀概覽與微觀細節的兼顧。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

## ❓ 第 22 題：【Breadcrumbs 麵包屑導航】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">在多層級大型電商網站（如：首頁 > 3C 數位 > 筆記型電腦 > 輕薄商務筆電）中，使用者常常在深層商品頁面迷失方向。在標題上方常駐提供階層路徑的模式稱為什麼？</div>
      <div class="quiz-prompt">請問這項設計模式稱為什麼？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>Breadcrumbs (麵包屑導航)</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>Tree View (樹狀目錄)</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>Hamburger Menu (漢堡選單)</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>Toast Notification (吐司提示)</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">Breadcrumbs（麵包屑導航，源自童話《糖果屋》灑麵包屑認路）清晰顯示使用者在全站階層樹狀架構中所處的精確位置，並提供各父層級的一鍵回溯路徑，是層級導航的經典模式。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

## ❓ 第 23 題：【Card List 卡片清單模式】

<div class="quiz-grid" data-answer="B">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">現代社群平台（如 Instagram、Pinterest、Facebook 動態消息）與專案看板（Trello），普遍採用「Card（卡片）」樣式來呈現單元內容。</div>
      <div class="quiz-prompt">請問卡片模式 (Card List) 廣受青睞的核心優勢為何？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>因為卡片樣式強制只能容納文字，不可放置圖片或影片</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>因為卡片將異質資訊（圖片、標題、作者、點讚數、留言）封裝成一個自給自足的獨立視覺單元，便於在不同螢幕尺寸間靈活重組排版</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>因為卡片樣式無法點擊，能防止使用者誤觸</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>因為卡片樣式只適用於橫向列印</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(B) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">Card（卡片）是現代響應式設計 (RWD) 的基石。它將異質且相關的資訊封裝為一體，具有極高的模組化特性，在多欄網格、單欄滾動或瀑布流中皆能完美適應。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: 'Part 4: Tidwell 介面設計模式精選測驗 (Q19 ~ Q24)' -->

## ❓ 第 24 題：【Time-Slot Picker / Data Sheet 數據表格模式】

<div class="quiz-grid" data-answer="A">
  <div class="quiz-card-left">
    <div>
      <span class="badge-topic">情境描述與題目</span>
      <div class="quiz-scenario">台灣高鐵購票系統在查詢某日車次時，呈現矩陣清單標明「車次、出發時間、抵達時間、自由座餘額、早鳥折扣」，並允許使用者直接點選切換前一班或後一班車次。</div>
      <div class="quiz-prompt">這最直接體現了 Tidwell 的哪種設計心法？</div>
    </div>
    <div class="quiz-options-group">
      <div class="quiz-option-btn" data-opt="A"><span class="opt-badge">A</span><span>透過直覺的數據表格 (Data Sheet) 與時間時段選擇器 (Time-Slot Picker) 消除認知負荷，讓使用者在單一脈絡下進行多維度方案比對與決策</span></div>
      <div class="quiz-option-btn" data-opt="B"><span class="opt-badge">B</span><span>強迫使用者記憶每一班車的列車編號才能輸入訂票</span></div>
      <div class="quiz-option-btn" data-opt="C"><span class="opt-badge">C</span><span>隱藏票價資訊，直到使用者輸入信用卡付款後才揭示</span></div>
      <div class="quiz-option-btn" data-opt="D"><span class="opt-badge">D</span><span>限制使用者每次查詢只能查看一班列車</span></div>
    </div>
  </div>
  <div class="quiz-card-right">
    <div class="quiz-status-pending">
      <div class="pending-icon">🎯</div>
      <div class="pending-title">請點擊左側選項作答</div>
      <div class="pending-desc">選錯可隨時換選再試，答對將立即揭曉深度解析！</div>
    </div>
    <div class="quiz-status-wrong">
      <div class="wrong-title"><span>❌</span><span class="wrong-msg">答案不太對喔！</span></div>
      <div class="wrong-desc">再仔細想一想題意，換個選項再試一次！💪</div>
    </div>
    <div class="quiz-status-correct">
      <div class="quiz-encourage-banner">
        <div class="encourage-title">🎉 太棒了，完全答對！👏</div>
        <div class="encourage-sub">🎯 正確答案：(A) | 觀念精確掌握！</div>
      </div>
      <div class="quiz-explanation-box">
        <span class="exp-tag">💡 核心解析與觀念釐清</span>
        <div class="exp-text">數據表格與時段選擇器將繁雜的多維度選項（班次、時間、票價、餘額）平鋪並置，使用者不必反覆跳出頁面，即可在同一個畫面上比較優劣並做出最佳決策，顯著提升操作效率與體驗。</div>
      </div>
      <button class="quiz-retry-btn" type="button">🔄 重新自我測驗</button>
    </div>
  </div>
</div>

---
<!-- header: '題庫完成與學習成效自我檢視' -->

## 🎓 題庫完成與學習成效自我檢視

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px;">
<div class="card" style="font-size: 20px;">

### 📊 自我測驗成效評估
- **21 ~ 24 題正確 (卓越 / 專家級)** ：
  - 徹底融會貫通 UX 原理、尼爾森 10 大原則與 AI 工具實務，具備優秀的軟體產品架構與評估能力！
- **16 ~ 20 題正確 (良好 / 穩健級)** ：
  - 掌握絕大多數核心觀念，建議複習答錯的題目並回顧 Unit 02 與 Unit 03 的案例對照。
- **15 題以下 (需加強 / 觀念釐清)** ：
  - 建議重溫 Unit 01 ~ Unit 04 投影片，加強體會「以人為本」的人機協同理念。

</div>
<div class="card" style="font-size: 20px;">

### 💡 學習三大關鍵要訣
1. **不要只看美觀 (UI)** ：時刻牢記 1-10-100 法則，前期做好 UX 規劃價值百倍。
2. **永遠給予控制權 (NS03/NS09)** ：AI 與系統充滿不確定性，緊急出口與白話復原是信任基石。
3. **動手實作閉環 (Agentic)** ：善用 Google Antigravity IDE、Planning Mode 與設計樣式庫，將理論落實於真實工程專案中！

</div>
</div>

<script>
(function() {
  // 1. Initialize Header Dropdown
  function initHeaderDropdown() {
    const slideSections = document.querySelectorAll('section[id]');
    const sections = [];
    const seenTitles = new Set();
    
    slideSections.forEach(sec => {
      const h2 = sec.querySelector('h2');
      const h1 = sec.querySelector('h1');
      let title = '';
      if (h2 && h2.textContent.trim()) {
        title = h2.textContent.trim();
      } else if (h1 && h1.textContent.trim()) {
        title = h1.textContent.trim();
      }
      
      title = title.replace(/^[#\s]+/, '')
                   .replace(/^[◄◀▶►\d\.\s]+/, '')
                   .replace(/^(Part\s*\d+[:：]|第\s*\d+\s*題[:：]|本題庫大綱|🎓\s*題庫完成與學習成效自我檢視)/, '$1')
                   .trim();
                   
      if (!title || seenTitles.has(title)) return;
      seenTitles.add(title);
      sections.push({
        id: sec.id,
        title: title
      });
    });

    if (sections.length === 0) return;

    function createDropdownWrapper(currentTitle) {
      const wrapper = document.createElement('span');
      wrapper.className = 'header-nav-wrapper';
      
      const titleSpan = document.createElement('span');
      titleSpan.className = 'header-nav-title';
      titleSpan.title = '點擊固定或懸停查看所有題目章節快速跳轉';
      titleSpan.innerHTML = currentTitle + '<span class="nav-caret"> ▾</span>';
      
      titleSpan.addEventListener('click', function(e) {
        e.stopPropagation();
        const wasOpen = wrapper.classList.contains('is-open');
        document.querySelectorAll('.header-nav-wrapper.is-open').forEach(w => w.classList.remove('is-open'));
        if (!wasOpen) {
          wrapper.classList.add('is-open');
        }
      });
      
      const dropdown = document.createElement('div');
      dropdown.className = 'nav-dropdown';
      
      dropdown.addEventListener('click', function(e) {
        e.stopPropagation();
      });
      
      const dropHeader = document.createElement('div');
      dropHeader.className = 'nav-dropdown-header';
      dropHeader.innerHTML = '<span>📑 快速跳轉測驗章節</span><span style="font-size:11px;font-weight:normal;color:#64748b;">共 ' + sections.length + ' 個章節</span>';
      dropdown.appendChild(dropHeader);
      
      const grid = document.createElement('div');
      grid.className = 'nav-dropdown-grid';
      
      sections.forEach(s => {
        const item = document.createElement('a');
        const isActive = (s.title === currentTitle);
        item.className = 'nav-dropdown-item' + (isActive ? ' active' : '');
        item.href = '#' + s.id;
        item.innerHTML = '<span class="badge">#' + s.id.padStart(2, '0') + '</span><span class="item-text" title="' + s.title + '">' + s.title + '</span>';
        
        item.addEventListener('click', function(e) {
          wrapper.classList.remove('is-open');
          dropdown.style.display = 'none';
          window.location.hash = '#' + s.id;
          setTimeout(() => { dropdown.style.display = ''; }, 350);
        });
        
        grid.appendChild(item);
      });
      
      dropdown.appendChild(grid);
      wrapper.appendChild(titleSpan);
      wrapper.appendChild(dropdown);
      return wrapper;
    }

    document.addEventListener('click', function(e) {
      if (!e.target.closest('.header-nav-wrapper')) {
        document.querySelectorAll('.header-nav-wrapper.is-open').forEach(w => w.classList.remove('is-open'));
      }
    });

    slideSections.forEach(sec => {
      const header = sec.querySelector('header');
      if (!header || header.dataset.navEnhanced) return;
      header.dataset.navEnhanced = 'true';
      
      let title = header.textContent.trim();
      title = title.replace(/^[◄◀]\s*/, '').replace(/\s*[►▶]$/, '').trim();
      if (!title) return;
      
      header.innerHTML = '';
      const wrapper = createDropdownWrapper(title);
      header.appendChild(wrapper);
    });
  }

  // 2. Initialize Interactive Quiz System
  function initQuizInteractions() {
    const quizGrids = document.querySelectorAll('.quiz-grid');
    quizGrids.forEach(grid => {
      if (grid.dataset.quizInit) return;
      grid.dataset.quizInit = 'true';
      
      const correctAns = grid.dataset.answer ? grid.dataset.answer.trim().toUpperCase() : '';
      const options = grid.querySelectorAll('.quiz-option-btn');
      const pending = grid.querySelector('.quiz-status-pending');
      const wrong = grid.querySelector('.quiz-status-wrong');
      const wrongMsg = grid.querySelector('.wrong-msg');
      const correct = grid.querySelector('.quiz-status-correct');
      const retryBtn = grid.querySelector('.quiz-retry-btn');
      
      // Mark key for print mode
      options.forEach(btn => {
        if (btn.dataset.opt === correctAns) {
          btn.classList.add('is-correct-key');
        }
      });

      options.forEach(btn => {
        btn.addEventListener('click', function(e) {
          e.stopPropagation();
          const selected = btn.dataset.opt ? btn.dataset.opt.trim().toUpperCase() : '';
          
          if (selected === correctAns) {
            // Correct answer chosen!
            options.forEach(b => {
              b.classList.remove('is-wrong');
              b.style.pointerEvents = 'none';
            });
            btn.classList.add('is-correct');
            
            if (pending) pending.style.display = 'none';
            if (wrong) wrong.style.display = 'none';
            if (correct) {
              correct.style.display = 'flex';
            }
          } else {
            // Wrong answer chosen!
            btn.classList.add('is-wrong');
            btn.style.animation = 'none';
            btn.offsetHeight; // trigger reflow
            btn.style.animation = 'quizShake 0.4s ease';
            
            if (pending) pending.style.display = 'none';
            if (wrong) {
              wrong.style.display = 'block';
              if (wrongMsg) {
                wrongMsg.textContent = '選項 (' + selected + ') 不太對喔！';
              }
            }
          }
        });
      });

      if (retryBtn) {
        retryBtn.addEventListener('click', function(e) {
          e.stopPropagation();
          options.forEach(b => {
            b.classList.remove('is-wrong', 'is-correct');
            b.style.pointerEvents = '';
            b.style.animation = '';
          });
          if (correct) correct.style.display = 'none';
          if (wrong) wrong.style.display = 'none';
          if (pending) pending.style.display = 'flex';
        });
      }
    });
  }

  function initAll() {
    initHeaderDropdown();
    initQuizInteractions();
  }

  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', initAll);
  } else {
    initAll();
  }
  setTimeout(initAll, 400);
  window.addEventListener('hashchange', () => setTimeout(initAll, 100));
})();
</script>
