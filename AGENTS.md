# Workspace Coding Rules and Best Practices

Welcome to the `gTeachUX` project! When modifying or editing files in this workspace (including lecture handbooks in `Lecture/source/` and presentation slide decks in `Slide/source/`), you must strictly adhere to the following rules:

## 1. Markdown Formatting for Slides (Marp & Markdown-it)

### Chinese Bold Spacing Rule
* **Problem**: In the Markdown-it parser (which Marp uses), bold markers (`**`) placed directly adjacent to Chinese characters or full-width punctuation/brackets (e.g., `，。！？、「」（）［］【】` etc.) without spaces will fail to render as bold and instead output raw asterisks.
* **Rule**: You **MUST** insert a single whitespace character before and after any bold markdown block (`**text**`) if it is adjacent to a Chinese character or full-width punctuation outside the block.
* **Example**:
  * ❌ *Incorrect*: `改用**打字機效果（Streaming）**即時輸出`
  * ✅ *Correct*: `改用 **打字機效果（Streaming）** 即時輸出`
  * ❌ *Incorrect*: `在**合理的時間內**給予反饋`
  * ✅ *Correct*: `在 **合理的時間內** 給予反饋`

### 表格全域置中規範 (Table Centering Rule)
* **Problem**: Marp 的預設主題會將 Markdown 表格設定為 `display: block; width: max-content;`，導致表格無法透過 `margin: auto` 水平置中，排版會靠左偏斜且右側大片留白。
* **Rule**: 投影片中所有表格（包括對照表、總結表等）必須一律維持水平置中。全域樣式必須強制指定 `display: table !important` 與 `align-self: center !important`：
  ```css
  table {
    display: table !important;
    width: 95%;
    max-width: 1100px;
    border-collapse: collapse;
    margin: 16px auto !important;
    align-self: center !important;
  }
  ```

---

## 2. 互動題目 (CCQ) 生命週期與同步標準程序 (CCQ Lifecycle & Sync Workflow)

* **階段 1 (初創無 QR 狀態)**：
  * AI 撰寫新互動題目時，一律按照標準格式撰寫題目文字、選項與答案解析。
  * **初創時一律為「無 QR」狀態**，不需要手動繪製或插入 QR Code 圖片，也不需要手動放置 `[線上作答]` 連結。
  * 題目上方可保留或由系統產生 `<!-- id: ux-chXX-ccqN -->` 註解。
* **階段 2 (執行同步)**：
  * 題目撰寫完成後，執行統一同步指令：
    ```bash
    python3 scripts/sync_iActivity.py --course gTeachUX
    ```
  * 同步腳本會自動完成：
    1. 解析 `Lecture/source/` 與 `Slide/source/` 中的互動題目。
    2. 匯出題庫至 `nickedupocket/public/courses/gTeachUX.md`。
    3. 自動生成各題 QR Code 圖檔至 `img/chXX/<act_id>.png`（供簡報使用）。
    4. 自動在講義手冊嵌入 `<!-- id: ... -->` 與 `[課堂互動]` 連結（講義不放 QR Code），簡報投影片中則同時嵌入 `[課堂互動]` 連結與 QR Code 圖檔。
* **階段 3 (題目修改重同步)**：
  * 若題目文字、選項或解析修改，直接修改 Markdown（保留原有 `<!-- id: ... -->`），再次執行 `sync_iActivity.py` 即可自動冪等更新。
* **階段 4 (編譯 PDF)**：
  * 同步完成後再執行 PDF 編譯：
    - 講義 PDF：`node scripts/generate_lecture_pdf.js Lecture/source/ch01_intro.md`
    - 投影片 PDF：`npx @marp-team/marp-cli Slide/source/UX_AI.md --pdf --allow-local-files --no-stdin -o Slide/UX_AI.pdf`

---

## 3. 繁體中文與軟體工程專業用語守則 (Terminology Consistency)

* **程式碼用語規範**：
  * ❌ *嚴禁使用*：`代碼`、`前端代碼`、`代碼塊`、`寫代碼`
  * ✅ *必須使用*：`程式碼`、`前端程式碼`、`程式碼區塊`、`撰寫程式碼`
* **錯誤碼／狀態碼用語**：
  * ❌ *避免使用*：`錯誤代碼`、`系統代碼`
  * ✅ *推薦使用*：`錯誤碼`、`錯誤代號`、`狀態碼`（如 HTTP 狀態碼）
* **原則**：本教材為逢甲大學資工系之授課教材，全面遵循臺灣資訊科技教育之繁體中文標準軟體工程術語。

