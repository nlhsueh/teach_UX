# Chapter 3: AI for UX — 運用 AI 進行體驗設計與原型打造

## 3.1 AI 輔助生成組件與介面感知錯誤處理

在透過 AI 提示詞生成前端程式碼時，除了程式層面的例外捕捉，必須在 UI 層面符合 NS09 的友善引導原則。

<!-- id: ux-ch03-ccq1 -->
### 🙋 **概念核對問答 (CCQ 1)**


**問題**

在要求 AI 生成前端資料請求組件時，提示詞明確要求「當 API 發生 500 伺服器錯誤時，必須使用 `try...catch` 捕捉並在控制台輸出 `console.error(err)`」，在軟體工程與 UX 層面上已完整滿足了 NS09（協助辨識與復原錯誤）的要求？

A) 正確 (True)
B) 錯誤 (False)

<details>
<summary>點擊查看【概念核對問答】答案與解析</summary>

**正確答案：B**

* **解析**：
  * `console.error` 是開發者除錯工具，對終端使用者完全不可見，使用者只會看到按鈕無反應或畫面卡住。
  * NS09 要求介面層級應呈現白話錯誤說明，並提供重試按鈕或指引。

</details>

---

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch03-ccq1)

## 3.2 Master Prompt 的多維度 UX 約束設計

撰寫給 AI 的 Master Prompt 時，透過精準定義多項易用性約束，能大幅提升生成原型的品質與實用性。

<!-- id: ux-ch03-ccq2 -->
### 🙋 **概念核對問答 (CCQ 2)**


**問題**

在要求 AI 生成「多步驟註冊表單」時，以下哪一段提示詞最能同時滿足 NS01 (狀態)、NS03 (控制權) 與 NS05 (錯誤預防)？

A) 「請用 React + Tailwind 寫一個美觀的註冊表單，支援深色模式。」
B) 「提供步驟進度條；每步均有『上一步』且保留資料；欄位 blur 時即時驗證並禁用未過關的『下一步』按鈕。」
C) 「表單最後提供送出按鈕，送出失敗時彈出 Toast `Submission failed`。」
D) 「使用 LocalStorage 快取所有欄位，並提供一鍵重設按鈕。」

<details>
<summary>點擊查看【概念核對問答】答案與解析</summary>

**正確答案：B**

* **解析**：
  * NS01 系統狀態能見度：頂部步驟進度條清楚標示當前與整體進度。
  * NS03 使用者控制與自由：隨時提供上一步且保留已填資料，支援自由回溯。
  * NS05 錯誤預防：blur 時即時校驗，未填完必填項時主動禁用下一步按鈕，防止無效送出。

</details>

---

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch03-ccq2)

<!-- id: ux-ch03-qa1 -->
### 🙋 **問答討論 (QA 1)：用 AI 設計辦公室 Web 點餐系統**


> * **任務與挑戰**：請使用 AI 輔助設計辦公室 Web 點餐系統，並分享你的提示詞與生成觀察：
>   1. **初版生成 vs. UX 優化**：比較「無 Prompt 限制」與「加入尼爾森原則約束」後的程式碼與介面差異。
>   2. **滿足哪些易用性原則**：你的 Master Prompt 中加入了哪些 UX 約束（如 NS01 狀態、NS03 控制權、NS05 錯誤預防）？
>   3. **心得與發現**：AI 生成的 UX 細節是否符合預期？有哪些值得注意的盲點？

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch03-qa1)
