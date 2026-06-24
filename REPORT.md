# Creative Project 93 — Moebius Tiny Model 互動式 Inpainting 模擬器

## 🎯 專案目標
打造一個互動式 HTML Canvas 模擬器，體驗 Moebius Tiny Model 的影像修復（Inpainting）能力，整合 HuggingFace API 進行真實推理。

## 🚀 已實現功能

### ✅ 1. 多場景支援
- **自然風景**：山水風景場景，含山巒、水面元素
- **人像**：人像輪廓場景，含頭部、肩部輪廓
- **建築**：建築輪廓場景，含屋頂、牆體結構
- 用戶可即時切換場景，觀察不同場景的 inpainting 效果

### ✅ 2. HuggingFace API 整合
- **API 端點**：`https://mike0021-moebius.hf.space`（Moebius Inpainting 空間）
- **連接狀態監測**：即時顯示 API 連線狀態（就緒/讀取中）
- **參數傳遞**：
  - `seed`：隨機種子值（0-999999）
  - `strength`：推理強度（0.00-1.00）
  - `prompt`：自然語言提示詞
- **進度條**：即時顯示生成進度（0-100%）
- **日誌系統**：記錄 API 請求參數與回應

### ✅ 3. 多人比較模式
- **四欄位並排比較**：
  - 原始圖像
  - Moebius Tiny 修復結果
  - HF 模型 A（模擬）
  - HF 模型 B（模擬）
- **切換模式**：單一模式 / 比較模式
- **自訂圖像上傳**：支援拖曳或點擊上傳圖像

### ✅ 4. 互動工具
- **筆刷工具**：繪製修復區域（紅半透明遮罩）
- **橡皮擦工具**：清除遮罩
- **筆刷大小**：5-100px 可調
- **網格顯示**：輔助繪製定位
- **遮罩清除**：一鍵重置遮罩
- **畫布重置**：恢復原始場景

## 🛠️ 技術架構

### 前端
- **單一 HTML 文件**：所有功能整合於單一檔案
- **Canvas API**：用於場景渲染、遮罩繪製、修復效果
- **CSS Grid/Flexbox**：響應式佈局設計
- **漸層主題**：深色主題，紫色調（#6366f1）

### 後端
- **HuggingFace Gradio API**：Mike0021/Moebius 空間
- **Fetch API**：非同步 API 請求
- **本地模擬**：當 API 不可用時，提供 Canvas 繪製模擬效果

## 📊 部署狀態
- **GitHub 儲存庫**：https://github.com/Mavisy75106/creative-project-93-moebius-tiny-model
- **GitHub Pages**：https://mavisy75106.github.io/creative-project-93-moebius-tiny-model/
- **部署狀態**：✅ 已構建完成（status: built）
- **HTTPS**：已啟用
- **訪問狀態**：HTTP 200 OK

## 🎨 UI/UX 特色
- **深色主題**：保護眼睛，適合長時間使用
- **漸層按鈕**：紫色調，提升視覺吸引力
- **即時回饋**：按鈕 hover 效果、進度條動畫
- **響應式設計**：支援桌面與行動裝置
- **工具提示**：清晰的圖示與文字說明

## 📈 效能優化
- **單一檔案部署**：無外部依賴，載入快速
- **Canvas 優化**：使用 requestAnimationFrame 避免不必要的重繪
- **API 超時處理**：5 秒超時機制，避免無回應等待
- **遮罩緩衝**：使用獨立 Canvas 儲存遮罩狀態

## 🔮 未來擴展方向
1. **更多場景**：室內、海洋、城市夜景
2. **模型選擇**：支援多個 Moebius 變體模型
3. **歷史記錄**：儲存生成歷史，支援回溯
4. **分享功能**：生成 URL 分享修復結果
5. **批量處理**：支援多區域同時 inpainting

## 📝 開發日期
- **開始**：2026-06-24
- **完成**：2026-06-24
- **作者**：Mavisy75106

---
*專案連結*：https://github.com/Mavisy75106/creative-project-93-moebius-tiny-model
*線上體驗*：https://mavisy75106.github.io/creative-project-93-moebius-tiny-model/
