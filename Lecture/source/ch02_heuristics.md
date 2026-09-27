# Chapter 2: 尼爾森 10 大易用性原則 (Nielsen's 10 Usability Heuristics)

## 2.1 錯誤預防 (NS05) 與警示疲勞

防呆機制必須兼顧使用者的控制自由與操作效率，避免過度的阻斷確認造成使用者的警示疲勞。

<!-- id: ux-ch02-ccq1 -->
### 🙋 **概念核對問答 (CCQ 1)**

**問題**

為了徹底落實錯誤預防，系統在使用者執行「任何」可能修改資料的操作（包括編輯個人暱稱、切換深色模式）時，都強制彈出確認視窗要求點擊「確定修改」，這是兼顧安全性與可用性的最佳實踐？

A) 正確 (True)
B) 錯誤 (False)

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch02-ccq1)

<details>
<summary>點擊查看【概念核對問答】答案與解析</summary>

**正確答案：B**

* **解析**：
  * 無差別的確認彈窗會誘發「警示疲勞 (Alert Fatigue)」，嚴重破壞 NS03 (使用者控制權) 與 NS07 (使用效率)，讓用戶養成不看內容直接按確定的麻木習慣。
  * 最佳實踐為風險分級：低風險操作採用自動儲存 + Undo 復原機制；唯有高風險、不可逆操作才需二次阻斷確認。

</details>

---

## 2.2 簡潔設計 (NS08) 與跨裝置識別性 (NS06)

追求視覺極簡時，不可忽略跨裝置的可發現性與可用性限制。

<!-- id: ux-ch02-ccq2 -->
### 🙋 **概念核對問答 (CCQ 2)**

**問題**

為了實現極致簡潔的視覺體驗，將資料表格中的操作按鈕（編輯/刪除/下載）全數隱藏，改為僅在使用者將滑鼠 Hover 懸停於該列時才浮現，這在所有裝置與情境下都是最推薦的做法？

A) 正確 (True)
B) 錯誤 (False)

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch02-ccq2)

<details>
<summary>點擊查看【概念核對問答】答案與解析</summary>

**正確答案：B**

* **解析**：
  * 在觸控螢幕或行動裝置上缺乏滑鼠 Hover 懸停機制，隱藏按鈕將導致功能無法被觸發。
  * 過度隱藏核心操作違反了 NS06 (易於識別而非記憶)，降低了系統的可發現性 (Discoverability)。

</details>

---

## 2.3 尼爾森原則綜合交叉應用案例

在真實系統中，往往需要結合多個易用性原則來設計流暢且安全的使用者體驗。

<!-- id: ux-ch02-ccq3 -->
### 🙋 **概念核對問答 (CCQ 3)**

**問題**

電商結帳頁在輸入信用卡時，自動依卡號長度在每 4 碼插入空格（`4111 2222 3333 4444`），並在辨識出卡別後即時於右側點亮 Visa 圖示。這項設計最直接體現了哪兩項原則的結合？

A) NS05 (錯誤預防) 與 NS06 (易於識別而非記憶)
B) NS03 (控制權) 與 NS07 (彈性與使用效率)
C) NS04 (一致性) 與 NS09 (清楚的錯誤處理)
D) NS08 (優雅簡潔的設計) 與 NS10 (適當的說明與文件)

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch02-ccq3)

<details>
<summary>點擊查看【概念核對問答】答案與解析</summary>

**正確答案：A**

* **解析**：
  * NS05 錯誤預防：利用格式化分塊 (Chunking) 將 16 位數字拆解為 4 位一組，降低抄寫與輸錯機率。
  * NS06 易於識別而非記憶：系統自動辨識並點亮卡片 Logo，使用者一眼即可確認是否拿對卡片，無需回憶卡種規則。

</details>

---

<!-- id: ux-ch02-ccq4 -->
### 🙋 **概念核對問答 (CCQ 4)**

**問題**

使用者在 Gmail 內文提及「如附件企劃書」，但在未附加檔案時點擊「傳送」，系統即時攔截並提示：「您提及了附件但未附加檔案，是否仍要傳送？」，並提供「取消」與「直接傳送」。這最直接體現了哪兩項原則的結合？

A) NS05 (錯誤預防) 與 NS03 (使用者控制與自由)
B) NS01 (系統狀態能見度) 與 NS08 (優雅簡潔的設計)
C) NS02 (與真實世界對應) 與 NS06 (易於識別而非記憶)
D) NS04 (一致性與標準) 與 NS10 (適當的說明與文件)

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch02-ccq4)

<details>
<summary>點擊查看【概念核對問答】答案與解析</summary>

**正確答案：A**

* **解析**：
  * NS05 錯誤預防：透過內文語意分析在不可逆操作前主動攔截遺漏附件。
  * NS03 使用者控制與自由：提供「取消」與「直接傳送」兩個出口，尊重使用者的最終自主權。

</details>

---

## 2.4 課堂互動遊戲：尼爾森 10 大原則闖關大挑戰

<!-- id: ux-ch02-game1 -->
### 🙋 課堂遊戲：尼爾森 10 大原則闖關大挑戰 (Game)

**第 1 題：【大檔案上傳與即時回饋】**
使用者在雲端硬碟上傳 1GB 的影片檔，系統在右下角以浮動視窗顯示圓形百分比進度、已上傳容量（如 450MB / 1GB）、即時傳輸速度與預估剩餘時間。這項設計最直接落實了哪一項易用性原則？
A) NS01 清楚的系統狀態能見度 (Visibility of System Status)
B) NS03 使用者控制與自由 (User Control and Freedom)
C) NS07 彈性與使用效率 (Flexibility and Efficiency of Use)
D) NS08 優雅簡潔的設計 (Aesthetic and Minimalist Design)

[課堂互動](https://nlhsueh.github.io/nickedupocket/#/student/ux-ch02-game1)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：A
**解析**：系統在合理時間內提供即時、精確的狀態回饋（進度百分比、剩餘時間），消除使用者的等待焦慮與系統是否凍結的疑慮，完全符合 NS01 (系統狀態能見度)。
</details>

---

**第 2 題：【實體閱讀隱喻與書架設計】**
電子書閱讀 App 在使用者翻頁時提供紙張翻摺陰影與沙沙紙張翻頁聲，並使用「書籤」、「螢光筆劃記」與「書架」來組織收藏，介面詞彙亦使用讀者熟悉的「章節」、「目錄」而非底層工程術語。這項設計最直接體現了哪一項易用性原則？
A) NS01 清楚的系統狀態能見度 (Visibility of System Status)
B) NS02 與真實世界對應 (Match Between System and Real World)
C) NS04 一致性與標準 (Consistency and Standards)
D) NS06 易於識別而非記憶 (Recognition Rather Than Recall)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：B
**解析**：使用真實實體世界的物件（書架、書籤、紙張質感）與日常概念作為隱喻，使用使用者熟悉的領域語言而非系統工程術語，符合 NS02 (與真實世界對應)。
</details>

---

**第 3 題：【批次操作的緊急出口】**
使用者在照片管理工具中勾選了 50 張照片並點擊「全數封存」，畫面底部立即彈出 SnackBar 提示：「已封存 50 張照片」，並在旁邊提供明顯的「復原 (Undo)」按鈕，且提供 10 秒的反悔猶豫期。這項設計最直接符合哪一項易用性原則？
A) NS02 與真實世界對應 (Match Between System and Real World)
B) NS03 使用者控制與自由 (User Control and Freedom)
C) NS05 錯誤預防 (Error Prevention)
D) NS08 優雅簡潔的設計 (Aesthetic and Minimalist Design)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：B
**解析**：使用者在誤操作時需要一個清楚標記的「緊急出口 (Emergency Exit)」以撤銷操作返回先前狀態，Undo 復原機制賦予使用者充分的操作安全感，符合 NS03 (使用者控制與自由)。
</details>

---

**第 4 題：【全站按鈕規範與平台標準】**
某跨平台購物系統在 iOS App 遵循蘋果 HIG 規範將導覽標籤放在底部，在 Web 則遵循常見的頂部 Header 導航；全站無論在哪個頁面，「加入購物車」一律是深橘色按鈕、「立即結帳」一律是綠色按鈕，危險操作一律是紅色文字。這項設計最直接符合哪一項易用性原則？
A) NS03 使用者控制與自由 (User Control and Freedom)
B) NS04 一致性與標準 (Consistency and Standards)
C) NS06 易於識別而非記憶 (Recognition Rather Than Recall)
D) NS07 彈性與使用效率 (Flexibility and Efficiency of Use)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：B
**解析**：兼顧了「外部一致性」（適配平台既有慣例）與「內部一致性」（全站統一顏色編碼與按鈕意圖），讓使用者不需猜測不同文字或按鈕代表的含義，符合 NS04 (一致性與標準)。
</details>

---

**第 5 題：【表單格式約束與不可逆確認】**
銀行跨行轉帳頁面中，系統在使用者輸入帳號時只允許輸入數字，並在輸滿 14 碼前自動禁用「下一步」按鈕；當使用者欲執行「結清並註銷帳戶」不可逆重大操作時，系統強制彈出視窗要求使用者親自輸入「我確認註銷」字樣才允許送出。這項設計最直接體現了哪一項易用性原則？
A) NS01 清楚的系統狀態能見度 (Visibility of System Status)
B) NS04 一致性與標準 (Consistency and Standards)
C) NS05 錯誤預防 (Error Prevention)
D) NS09 清楚的錯誤處理 (Help Users Recognize, Diagnose, and Recover from Errors)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：C
**解析**：預防勝於治療。透過輸入約束（防呆校驗、禁用無效按鈕）與不可逆高風險操作的刻意阻斷（輸入確認字串），在使用者犯錯前就先消除發生錯誤的條件，符合 NS05 (錯誤預防)。
</details>

---

**第 6 題：【搜尋歷程與多商品規格對照】**
使用者在線上選購筆記型電腦時，搜尋列在點擊時主動列出「最近搜尋過之關鍵字」，在瀏覽商品時提供浮動按鈕讓使用者勾選 3 款筆電展開「規格橫向對照表」，各項規格一覽無遺，使用者不必自行反覆切換頁面抄寫記憶。這項設計最直接體現了哪一項易用性原則？
A) NS02 與真實世界對應 (Match Between System and Real World)
B) NS06 易於識別而非記憶 (Recognition Rather Than Recall)
C) NS08 優雅簡潔的設計 (Aesthetic and Minimalist Design)
D) NS10 適當的說明與文件 (Help and Documentation)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：B
**解析**：人類的「識別 (Recognition)」遠比「回憶 (Recall)」容易。將歷史紀錄與比較資訊直接外顯於畫面上，使物件與選項清晰可見，大幅降低短暫記憶的認知負擔，符合 NS06 (易於識別而非記憶)。
</details>

---

**第 7 題：【新手視覺按鈕與專家快捷鍵】**
現代程式碼編輯器（如 VS Code）為新手提供視覺化的功能選單與側邊欄按鈕，同時為資深工程師提供強大的快捷鍵（如 `Cmd + P` 快速開檔、`Cmd + Shift + L` 多游標編輯），並允許自訂程式碼片段 (Snippets) 與巨集。這項設計最直接符合哪一項易用性原則？
A) NS03 使用者控制與自由 (User Control and Freedom)
B) NS05 錯誤預防 (Error Prevention)
C) NS07 彈性與使用效率 (Flexibility and Efficiency of Use)
D) NS09 清楚的錯誤處理 (Help Users Recognize, Diagnose, and Recover from Errors)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：C
**解析**：系統提供加速鍵 (Accelerators) 與客製化捷徑，同時包容無經驗新手與追求極致速度的高頻率資深用戶，提升操作效率，符合 NS07 (彈性與使用效率)。
</details>

---

**第 8 題：【極簡搜尋首頁與視覺降噪】**
Google 搜尋引擎首頁中央僅保留一個搜尋輸入框、兩個按鈕與簡約商標，將所有進階篩選、搜尋歷史與廣告內容完全排除於首頁之外，避免不相干或極少使用的資訊干擾視覺。這項設計最符合哪一項易用性原則？
A) NS01 清楚的系統狀態能見度 (Visibility of System Status)
B) NS04 一致性與標準 (Consistency and Standards)
C) NS08 優雅簡潔的設計 (Aesthetic and Minimalist Design)
D) NS10 適當的說明與文件 (Help and Documentation)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：C
**解析**：遵循 80/20 法則，移除任何不必要的視覺噪訊與冗餘資訊，凸顯唯一的核心任務，符合 NS08 (優雅簡潔的設計)。
</details>

---

**第 9 題：【白話錯誤提示與修復指引】**
使用者在網頁註冊輸入 Email 時，系統沒有顯示冷冰冰的「錯誤碼：ERR_4021」，而是在欄位下方以紅字清楚標示：「信箱格式有誤：請檢查是否漏打了『@』符號，例如：user@example.com」，並將游標自動聚焦於該欄位方便直接修改。這項設計最符合哪一項易用性原則？
A) NS02 與真實世界對應 (Match Between System and Real World)
B) NS05 錯誤預防 (Error Prevention)
C) NS07 彈性與使用效率 (Flexibility and Efficiency of Use)
D) NS09 清楚的錯誤處理 (Help Users Recognize, Diagnose, and Recover from Errors)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：D
**解析**：使用易懂的純人類語言精確指出問題所在，不拋出技術錯誤碼，並主動提供具體、建設性的修復動作建議，符合 NS09 (清楚的錯誤處理)。
</details>

---

**第 10 題：【情境式引導與微教學 Tooltip】**
使用者首次開啟線上心智圖軟體時，畫面並非跳出長達 30 頁的 PDF 說明書，而是透過 3 個簡短的輕量級步驟氣泡（Tooltip）引導：「1. 拖曳此處新增節點、2. 點擊此處邀請成員、3. 按空白鍵平移畫布」，並在右上角提供隨時可搜尋的範本問答庫。這項設計最符合哪一項易用性原則？
A) NS01 清楚的系統狀態能見度 (Visibility of System Status)
B) NS06 易於識別而非記憶 (Recognition Rather Than Recall)
C) NS08 優雅簡潔的設計 (Aesthetic and Minimalist Design)
D) NS10 適當的說明與文件 (Help and Documentation)

<details>
<summary>點擊查看答案與解析</summary>

**正確答案**：D
**解析**：提供情境化 (Contextual)、任務導向且容易檢索的新手引導與說明資訊，避免拋給使用者整本厚重的操作手冊，符合 NS10 (適當的說明與文件)。
</details>
