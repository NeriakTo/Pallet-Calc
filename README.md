# Pallet Stacking Calculator (棧板堆疊計算器)

![Version](https://img.shields.io/badge/version-v1.4-blue.svg)
![Status](https://img.shields.io/badge/status-stable-success.svg)

這是一個基於 Web 的輕量級棧板堆疊與材積計算工具，專為業務與倉儲人員設計。
無需安裝、無需後端伺服器，支援 Excel 與 PDF 報表匯出功能。

## 🚀 線上使用 (Live Demo)
[點擊此處開啟應用程式](https://neriakto.github.io/Pallet-Calc/)

## 🌟 v1.4 版面優化
- **📄 PDF 緊湊排版 (Compact Layout)**：大幅縮減 PDF 匯出時的留白與間距，移除不必要的標題，最大化 A4 版面利用率。
- **邊距調整**：將 PDF 邊距縮減至 5mm，讓內容顯示更完整。

## 🌟 v1.3 功能回顧
- **PDF 報表輸出**：整合 `html2pdf.js`，可一鍵將計算結果匯出為高解析度文件。
- **雙重匯出**：同時支援 Excel (.xlsx) 與 PDF (.pdf)。

## 📖 專案背景與目標
業務在面對多 SKU 訂單時，需要快速產出「可實際執行」的棧板堆疊方案。本工具解決了傳統 Excel 計算耗時、易出錯且難以指導現場堆疊的問題。

### 核心功能
1.  **參數化設定**：
    - 支援自定義棧板尺寸 (L/W)。
    - 可設定最大堆高、棧板高度及 **容許超出範圍 (Overhang)**。
2.  **自動計算**：
    - 自動判斷最佳平面排列方向 (Dir1 vs Dir2)。
    - 計算每棧板最大箱數、滿棧板數與餘數。
3.  **智慧混棧 (Heuristic Level 1)**：
    - 針對餘數箱進行「層級」混棧。
    - 採用 First-Fit Descending 演算法，優先處理高度較高的貨物以確保穩定。
4.  **視覺化輸出**：
    - 提供「由下往上」的堆疊層序指示，與現場作業一致。
    - 計算貨物 CBM/CUFT 及含棧板總材積。

## 🛠️ 技術架構
- **Frontend**: 純 HTML5 / CSS3 / JavaScript (ES6+)
- **Dependencies**:
  - [SheetJS (xlsx)](https://sheetjs.com/) - 用於 Excel 匯出
  - [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) - 用於 PDF 匯出
- **Deployment**: GitHub Pages
- **Privacy**: 所有計算皆在瀏覽器端 (Client-side) 完成，資料不回傳伺服器。

## 📦 離線使用指南
若需在無網路環境（如工廠內部）使用，請下載以下檔案並置於同一目錄：
1. `index.html` (本專案主程式)
2. `xlsx.full.min.js` (Excel 功能庫)
3. `html2pdf.bundle.min.js` (PDF 功能庫)

*下載後請記得修改 index.html 內的 `<script>` 來源路徑。*

## 📝 版本紀錄 (Changelog)
- **v1.4 (Current)**: PDF 排版優化，移除冗餘標題並實作緊湊模式 (Compact Mode)。
- **v1.3**: 新增 PDF 匯出功能。
- **v1.2**: 新增台分/公分單位切換、新增棧板容許超出範圍設定。
- **v1.1**: 基礎單位換算功能試行。
- **v1.0**: 初始發布。

---
© 2026 Chang-ching Enterprise Co., Ltd. Internal Tool.