# Pallet Stacking Calculator (棧板堆疊計算器)

![Version](https://img.shields.io/badge/version-v1.5-blue.svg)
![Status](https://img.shields.io/badge/status-stable-success.svg)

這是一個基於 Web 的輕量級棧板堆疊與材積計算工具，專為業務與倉儲人員設計。
無需安裝、無需後端伺服器，支援 Excel 與 PDF 報表匯出功能。

## 🚀 線上使用 (Live Demo)
[點擊此處開啟應用程式](https://neriakto.github.io/Pallet-Calc/)

## 🌟 v1.5 更新
- **📏 強制 A4 排版**：解決 PDF 內容右側被截斷的問題，現在匯出時會強制將內容縮放至 200mm 寬度，完美符合 A4 紙張。
- **✂️ 移除上方留白**：修正 PDF 輸出時上方出現大片空白的問題，直接從「訂單合計」開始列印。
- **📝 極致緊湊模式**：大幅壓縮卡片間距與內距，解決分頁造成的巨大空白，單頁可容納更多資訊。

## 🌟 歷史功能亮點
- **PDF 報表輸出** (v1.3)：一鍵產出高解析度圖文報表。
- **容許誤差設定** (v1.2)：支援棧板長寬高「容許超出範圍 (Overhang)」設定。
- **多單位支援** (v1.2)：輸入台分自動換算公分。

## 📖 專案背景與目標
業務在面對多 SKU 訂單時，需要快速產出「可實際執行」的棧板堆疊方案。本工具解決了傳統 Excel 計算耗時、易出錯且難以指導現場堆疊的問題。

### 核心功能
1.  **參數化設定**：
    - 支援自定義棧板尺寸 (L/W)。
    - 可設定最大堆高、棧板高度及 **容許超出範圍**。
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
  - [SheetJS (xlsx)](https://sheetjs.com/) - Excel 匯出
  - [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) - PDF 匯出
- **Deployment**: GitHub Pages

## 📦 離線使用指南
若需在無網路環境（如工廠內部）使用，請下載以下檔案並置於同一目錄：
1. `index.html`
2. `xlsx.full.min.js`
3. `html2pdf.bundle.min.js`

## 📝 版本紀錄 (Changelog)
- **v1.5 (Current)**: PDF A4 寬度強制適配，解決截斷與留白問題。
- **v1.4**: PDF 基礎緊湊排版優化。
- **v1.3**: 新增 PDF 匯出功能。
- **v1.2**: 新增台分單位、容許超出範圍設定。
- **v1.1**: 基礎單位換算。
- **v1.0**: 初始發布。

---
© 2026 Chang-ching Enterprise Co., Ltd. Internal Tool.