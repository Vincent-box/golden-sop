# 💡 AI 結對編程黃金 SOP 隨身指令卡 (Cheat Sheet)

把這份指令卡存在 Obsidian、Notion 或桌面，隨時複製使用！

---

## 🎯 階段對話卡（5 張 Prompt 卡片）

### 🃏 卡片 1：Phase 1 啟動（意圖錨定）
```markdown
「我想實作【功能名稱】。
目的：【預期解決的問題或達成的效果】
請依據黃金 SOP Phase 1 啟動對話訪談，主動向我提問以釐清需求、邊界與限制。
注意：請先不要提供代碼或方案，直到我們完成意圖對齊並獲得我的確認許可。」
```

---

### 🃏 卡片 2：Phase 2 推進（方案發散與選型）
```markdown
「意圖已確認無誤，請進入 Phase 2。
請提供 3 個業界主流的最佳實踐架構方案，並列出：
1. 核心實作思路與架構模式
2. Trade-off 矩陣（複雜度、依賴性、擴展彈性 vs YAGNI）
3. 你的推薦方案與具體理由」
```

---

### 🃏 卡片 3：Phase 3 啟動（雙維度 Double Grill 對抗獵殺）
```markdown
「我選定【方案 X】。現在請啟動 Phase 3 對抗獵殺模式：
1. Round 1 (Grill Yourself)：針對維度 A（數據與邏輯邊界）與維度 B（系統併發、網路重試、爆炸半徑與相容性）全面施壓。
2. Round 2 (Grill Yourself Again)：假設第一輪防禦已就緒，再次以極端刁鑽角度發起二次拷問。
3. 輸出完整的 Edge Cases 清單、Gap 分析與優雅降級策略。
等待我確認防禦完備後，方可進入 Phase 4。」
```

---

### 🃏 卡片 4：Phase 4 推進（TDD 閉環實作）
```markdown
「防禦完備，確認進入 Phase 4。
請將剛才討論出的所有 Edge Cases 與防禦規格整合：
1. 建立行為導向的 Test Matrix（S1~S6 等級）。
2. 嚴格遵守 Red（紅燈確認）-> Green（最簡通過）-> Refactor（重構優化）實作。
3. 執行測試與覆蓋率驗收。」
```

---

### 🃏 卡片 5：Phase 5 收尾（ADR 決策存檔）
```markdown
「實作與測試已全數通過。
請輸出簡明標準的 ADR（架構決策記錄）存檔：
包含：Context（背景）、Decision（決策與放棄方案）、Edge Cases & Defenses（防禦關鍵與代碼位置）、Consequences（後續影響與維護備忘）。」
```

---

## ⚡ 一鍵全流程指令（One-Shot Prompt）
```markdown
「需求：【XXX】，目的：【YYY】。
請按 AI 結對編程黃金 SOP 進行：
- Step 1：透過提問梳理需求，待我確認；
- Step 2：提供 3 種最佳實踐 Trade-off 選型；
- Step 3：選定後執行 Double Grill（Grill Yourself + Grill Yourself Again）獵殺邊界，待我確認；
- Step 4：交由 TDD 閉環（Test Matrix -> Red -> Green -> Refactor -> Gate）；
- Step 5：交付完成後輸出 ADR 決策存檔。」
```
