# 專案協作與版本演進歷程（History）

> 本文件完整記錄 `ISO-27090` 專案在 2026 年 10 月 17 日的人機協作、技術考據、雙模型審查與除錯演進全貌。

---

## 🕒 演進時間軸

### 1. 探索與工程排查階段（11:00 - 11:08）
* **觸發情境**：嘗試存取 `https://www.iso.org/standard/27090#lifecycle` 探索發布狀態。
* **連線探測**：透過 `curl` 實測發現 `iso.org` 啟用了 Cloudflare WAF Managed Challenge（HTTP 403 Forbidden）。
* **版權性質核實**：
  * 確認 ISO 國際標準為付費版權文件（德國 DIN Media 報價約 €76，瑞士 ISO 官網約 160+ 瑞郎）。
  * 官方並無開放合法之免費完整 PDF 下載；決定轉向**多方公開權威情資搜集與結構化研析**。

---

### 2. SDD 階段一：建立基礎報告（11:10 - 11:59）
* **提案建立**：依照 SDD 工作流程建立 `sdd/iso-27090-html-report`。
* **架構梳理**：
  * 彙整 ISO 制定生命週期（2022 立案 -> 2025 DIS -> 2026/08 FDIS 投票通過）。
  * 整理治理三角（ISO 27001、ISO 42001、ISO 27090）與初期五大 AI 威脅。
  * 產出首版 `iso_27090_overview.html`，內建 Mermaid 流程圖與基礎 CSS。
* **驗收與歸檔**：將任務打勾後歸檔至 `sdd/archive/2026-10-17-iso-27090-html-report/`。

---

### 3. SDD 階段二：嚴謹度升級與雙頂尖模型交叉審查（12:00 - 12:14）
* **提案建立**：建立 `sdd/upgrade-iso27090-report`，設定三大目標：嚴謹發布日、Codex Exec 生圖、雙模型交叉審查。
* **Codex Exec 資訊圖表生成**：
  * 呼叫 `md_to_html` 核心腳本 `codex_imagegen.py`，調用 `codex exec` 繪製兩張 16:9 繁體中文 AI 專業資訊圖：
    1. `images/iso27090_governance_triangle.png`（治理三大支柱）
    2. `images/iso27090_threat_matrix.png`（威脅矩陣全景）
* **Claude Code 審查反饋（內容深度 ＋ Claude Design UI/UX）**：
  * **抓漏**：指出初版標題寫五大威脅卻只有四張卡，且 Clean-label 攻擊機制解釋過度簡化。
  * **UI/UX 重構**：指出五欄威脅圖在 390px 手機直屏上文字僅 5px 不可讀；建議增加橫向滾動容器（`.figure-scroll`）、左右滑動提示、置頂 Sticky Chip 導覽列。
* **Codex Exec 審查反饋（技術攻擊向量 ＋ 國際法規）**：
  * **考據校正**：從 ISO 官方目錄中精確定位出版日為 **2026 年 10 月 14 日（Stage 60.60 Published）**。
  * **攻擊向量補強**：補齊第六項「模型與套件供應鏈風險」（包含 pickle 反序列化攻擊與 AIBOM）。
  * **法規精準化**：釐清歐盟 AI Act 第 15 條要求與第 40 條調和標準「符合性推定」的嚴謹界線。
* **成果落地**：重構 `iso_27090_overview.html`，打勾任務後歸檔至 `sdd/archive/2026-10-17-upgrade-iso27090-report/`。

---

### 4. 發布與社群文案階段（12:15 - 12:20）
* **GitHub 公開倉庫建立**：
  * 複製首頁為 `index.html`。
  * 建立 GitHub 公開儲存庫 `lushinshang/ISO-27090` 並推送。
  * 啟用 GitHub Pages，正式上線：`https://lushinshang.github.io/ISO-27090/`。
* **社群文案產出**：
  * 撰寫 LINE 訊息版（好讀、短篇）與 LinkedIn 專業社群版文案。
  * 存檔為 `social_posts.txt` 並推播至 GitHub。

---

### 5. URL 除錯與官方 OBP 錨點直達（12:24 - 12:33）
* **發現問題**：使用者回報點擊 `https://www.iso.org/standard/27090.html` 顯示「沒有內容 / 空白」。
* **除錯破案**：
  * 查出 ISO 官網機制：`/standard/{id}.html` 裡的 `{id}` 為資料庫流水號而非標準號（例如 ISO 27001 其實是 `standard/82875.html`）。直接敲 `27090.html` 會連到數十年前廢棄的舊檔案。
* **永久解法**：
  * 採用 ISO Online Browsing Platform (OBP) 官方錨點直達網址：  
    `https://www.iso.org/obp/ui#iso:std:iso-iec:27090:ed-1:v1:en`
  * 全面測試並更新所有外部出處連結（BSI Knowledge、DIN Media、EU AI Act Explorer、OWASP、ITU-T）。
  * 同步推送至 GitHub 與 GitHub Pages。
