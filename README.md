# 心律圖譜｜心臟傳導系統與心電圖

## 開啟

在此資料夾開啟終端機，執行：

```powershell
npm install
npm run dev
```

用瀏覽器開啟終端機顯示的 Local 網址。若要查看正式建置：

```powershell
npm run build
npm run preview
```

請透過本機伺服器開啟，不要直接雙擊 dist/index.html。

## 教學操作

- 心臟拆解：向下捲動拆開、繼續捲動合體；向上捲動可倒播。也能使用「拆解／合體」。使用捲動時會接回捲動進度。
- 點構造面板可聚焦部件；「顯示全部」解除。
- 傳導：播放、暫停、速度與逐步操作；點波形說明可重播該段。
- 練習：拖曳配對，或先點標籤再點圖上的字母。
- 測驗：答錯時回到傳導段重播，答對可繼續。
- 減少動態效果：顯示合體後的靜態圖；可用逐步模式理解傳導。

## 技術與範圍

Vite + vanilla JavaScript，固定 animejs@4.5.0。所有解剖插圖為手繪 inline SVG。沒有外部圖片或其他動畫套件。

這是解剖與電活動的教學示意；不是依病人資料重建的模型。心電圖不呈現時間、電壓或心跳數值。傳導動畫的速度為教學節奏。

教學內容參考：[OpenStax Anatomy and Physiology — Cardiac Muscle and Electrical Activity](https://openstax.org/books/anatomy-and-physiology-2e/pages/19-2-cardiac-muscle-and-electrical-activity)。


## GitHub Pages

原始碼儲存庫：https://github.com/pigcharles06/cardiac-atlas

發布來源設定為 `main` 分支的 `/docs`。`vite.config.js` 使用相對資產路徑，適用 GitHub Pages 的專案子路徑。

修改後執行 `npm run build:pages`，再提交原始碼及 `docs/`，GitHub Pages 就會更新。`public/.nojekyll` 用於停用 Jekyll 處理。
