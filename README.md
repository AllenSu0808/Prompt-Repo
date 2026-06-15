# Prompt Repo

針對不同工程技術領域，提供一套標準化的 AI 助手指令集（System Prompt / Instructions），讓 ChatGPT、Claude 等 LLM 能以特定專業語氣、規範與格式回覆，提升開發效率與輸出品質。

---

## 目錄結構

```
Prompt-Repo/
├── C#_Instructions.md            # C# / .NET 軟體工程師指令集
├── Ignition_SCADA_Instructions.md  # Ignition SCADA 工程師指令集
└── LICENSE
```

---

## 指令集說明

### C#_Instructions.md

適用對象：使用 ChatGPT / Claude 進行 **C# / .NET** 開發的工程師。

主要特性：
- 角色：軟體工程師，全程繁體中文（台灣用語）
- 預設目標框架：**.NET Framework 4.8**
- 程式碼規範：XML Documentation、`#region / #endregion` 折疊
- 多語言支援：C#、C++17、Python 3.10、JavaScript/React（附對應註解規範）
- 命名規則：Pascal Case（類別/方法）、camelCase（區域變數）、`_camelCase`（私有欄位）
- 輸出結構：需求理解 → 解法步驟 → 程式範例 → 測試驗證 → 效能/常見坑 → 延伸
- 視覺化：Mermaid v11.8.0，`flowchart TD`
- 地域預設：台灣、`yyyy/MM/dd`、zh-TW

---

### Ignition_SCADA_Instructions.md

適用對象：使用 ChatGPT / Claude 進行 **Ignition SCADA** 系統開發的工程師。

主要特性：
- 角色：Ignition SCADA 工程師，全程繁體中文（台灣用語）
- 優先使用 **Perspective** 模組
- Scripting 規範：**Jython 2.7**，禁止 f-string / type hints，必須包含 `try/except`、`system.util.getLogger()`、scope 標示
- Tag 架構：`Enterprise/Site/Area/Line/Equipment/Tag`，搭配 UDT 標準化
- 資料庫：PostgreSQL + Named Query
- HMI 設計：HPHMI 風格（灰階背景、顏色僅用於警報）
- 效能建議：Tag Group 分級（1s/5s/60s）、`invokeAsynchronous()`、避免 UI 大量讀寫 Tag
- 輸出結構：摘要 → 步驟 → 範例 → 驗證 → 常見坑 → 延伸

---

## 使用方式

1. 開啟對應的 `*_Instructions.md` 檔案。
2. 複製全部內容。
3. 貼入 ChatGPT「自訂指令（Custom Instructions）」或 Claude「System Prompt」欄位。
4. 即可開始以對應工程師角色與規範進行對話。

---

## 授權

本專案採用 [MIT License](LICENSE)。

© 2026 JiaHongSu
