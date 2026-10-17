# ISO/IEC 27090:2026 全面研析與官方發行考據

> 專門針對 **AI 系統全生命週期資安威脅與處置** 的國際指引標準深度解析。

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-blue?style=flat-square&logo=github)](https://lushinshang.github.io/ISO-27090/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
[![ISO Status](https://img.shields.io/badge/ISO%20Status-Stage%2060.60%20Published-success?style=flat-square)](https://www.iso.org/obp/ui#iso:std:iso-iec:27090:ed-1:v1:en)

---

## 📖 專案簡介

**`ISO/IEC 27090:2026`**（題名：*Cybersecurity — Artificial intelligence — Addressing security threats and compromises to artificial intelligence systems*）於 **2026 年 10 月 14 日** 由 ISO/IEC JTC 1/SC 27 正式切換為 **Stage 60.60（已正式出版）**。

面對大語言模型（LLM）與代理式 AI（Agentic AI）大規模落地，傳統以防火牆、WAF 和端點防護為主的資安架構，在「提示詞注入」、「資料中毒」或「模型逆向竊取」面前幾乎完全致盲。本專案透過工程化情資檢索、多方權威標準交叉核實，以及頂尖 AI 模型的深度審查，整理出一部**手機直屏好讀、圖文並茂、因果鏈嚴謹**的繁體中文研析報告。

* 🌐 **線上完整研析報告**：[https://lushinshang.github.io/ISO-27090/](https://lushinshang.github.io/ISO-27090/)
* 📦 **GitHub 專案原始碼**：[https://github.com/lushinshang/ISO-27090](https://github.com/lushinshang/ISO-27090)

---

## 🎯 核心重點與特色

1. **嚴謹官方考據**：
   * 精準釐清官方於 2026-10-14 轉為 Stage 60.60 Published 之歷程，破除虛假日期。
   * 明確定位其為**實務指引（Informative Guidance）**，不可單獨發證，破除市面顧問認證話術。
2. **AI 資安治理三角架構**：
   * **ISO 42001 (AIMS)**：頂層組織治理方針與倫理風險。
   * **ISO 27001 / 27002 (ISMS)**：底層系統與網路基礎設施安全。
   * **ISO 27090**：專責 AI 系統生命週期技術控制項，並作為對應**歐盟 AI 法案（EU AI Act）第 15 條**資安強健性的技術佐證。
3. **完整六大威脅因果鏈**：
   * 深入剖析資料中毒、對抗性規避攻擊、模型竊取與逆向、推斷隱私攻擊（成員推斷／模型反轉）、提示詞注入與代理越權、模型供應鏈風險（含 Safetensors 與 AIBOM）。
4. **雙頂尖模型交叉審查（Peer Review）**：
   * **Claude Code 最佳模型**：審查專題因果深度，並導入 Claude Design 手機直屏閱讀人體工學（Sticky Chip 導覽、橫滑防擠壓容器）。
   * **Codex Exec 最佳模型**：審查六大攻擊向量覆蓋率、修正技術措辭，並精準對照歐盟 AI Act 第 15 條與第 40 條法律條款。
5. **Codex Exec 生成 16:9 高畫質 AI 資訊圖表**：
   * 內建 AI 資安治理三大支柱圖與五大威脅全景圖，支援點擊開大圖與無障礙文字替代。

---

## 📂 目錄結構

```text
.
├── index.html                  # GitHub Pages 預設首頁（與 iso_27090_overview.html 同步）
├── iso_27090_overview.html     # 完整研析報告原始 HTML
├── social_posts.txt            # LINE 社群版與 LinkedIn 專業社群版文案
├── README.md                   # 專案總覽與架構說明
├── history.md                  # 人機協作演進紀錄與除錯歷史
├── images/                     # 由 Codex Exec 生成的高解析 16:9 資訊圖表
│   ├── iso27090_governance_triangle.png   # 治理三大支柱圖 (1.7MB)
│   └── iso27090_threat_matrix.png          # 威脅矩陣全景圖 (1.6MB)
└── sdd/                        # 結構化軟體設計文件 (SDD) 歸檔庫
    └── archive/
        ├── 2026-10-17-iso-27090-html-report/     # 階段一初始報告歸檔
        └── 2026-10-17-upgrade-iso27090-report/   # 階段二雙模型審查與升級歸檔
```

---

## 🔗 權威參考來源

1. **[ISO 官方線上瀏覽平台 (OBP) 直達專頁](https://www.iso.org/obp/ui#iso:std:iso-iec:27090:ed-1:v1:en)**：可直接預覽 ISO/IEC 27090:2026 之目錄大綱、前言 (Foreword) 與範圍 (Scope)。
2. **[BSI 英國標準協會知識庫 (BSI Knowledge)](https://knowledge.bsigroup.com/)**
3. **[DIN Media 德國標準化學會平台](https://www.dinmedia.de/en)**
4. **[歐盟人工智慧法案官方導覽 (The EU AI Act Explorer)](https://artificialintelligenceact.eu/)**
5. **[OWASP AI Exchange (AI Security and Privacy Guide)](https://owaspai.org/)**
6. **[ITU-T Recommendation X.1457 (AI 推薦安全標準)](https://www.itu.int/rec/T-REC-X.1457)**
