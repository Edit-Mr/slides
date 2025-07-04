# 2024 中電會幹部訓練

網址: <https://g.scaict.org/112-workshop>

# 2024 中電會幹部訓練 課程簡報

這是一份使用 reveal.js 製作的課程簡報，涵蓋了幹部訓練所需的多個主題。原始 Markdown 簡報檔案位於 `slides` 資料夾。本文件將介紹課程內容、原理以及如何在本地開發。

## 課程內容

### 課程連結

- [Github](https://g.scaict.org/112-workshop/course/?course=Github)
- [基本平面設計](https://www.figma.com/slides/NDArIhpWCTFdm7keSRjIkb/基本平面設計---中電幹訓?node-id=1-34&t=Nh718iEOrXyokRd3-1)
- [Linux](https://g.scaict.org/112-workshop/course/?course=Linux)
- [Linux 應用](https://g.scaict.org/112-workshop/course/?course=LinuxApplication)
- [Web Security (Canva)](https://www.canva.com/design/DAGHsWC56XM/o_I1i2F38aRMv815f1Mlvg/edit?utm_content=DAGHsWC56XM&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
- [HTML](https://g.scaict.org/112-workshop/course/?course=HTML)
- [CSS](https://g.scaict.org/112-workshop/course/?course=CSS)

## reveal.js 簡介

reveal.js 是一個基於 HTML 的開源框架，用於創建精美的演示文稿。它支持 Markdown 格式的簡報內容，並且可以通過多種插件擴展功能，如動畫、互動性和多媒體支持。

### 主要功能

- **簡單的 Markdown 支持**：可以輕鬆地使用 Markdown 語法來編寫簡報內容。
- **可擴展的插件系統**：提供多種插件，增強簡報功能。
- **多種過渡效果**：提供多種過渡動畫效果，使簡報更具吸引力。
- **全屏支持**：支持全屏模式，適合各種屏幕尺寸。
- **內建高亮顯示**：內建語法高亮顯示，適合技術性演示。

## 本地開發指南

1. 克隆專案到本地：

    ```bash
    git clone https://github.com/SCAICT/112-workshop.git
    ```

2. 進入專案目錄：

    ```bash
    cd 112-workshop
    ```

### 啟動本地伺服器

網頁全是靜態資源，撰寫時可使用任意 HTTP 伺服器。如 VSCode Live Server、Python SimpleHTTPServer、Node.js http-server 等。或是直接點開 HTML 檔案，如果你恨你自己。

### 編輯簡報
所有的簡報內容都存放在 `slides` 資料夾中，撰寫方式與 hackmd 相同。詳細完整使用方式請參考 [reveal.js 官方文件](https://revealjs.com/zh-hant/)。使用 Markdown 格式編寫。編輯這些文件後，刷新瀏覽器即可看到更新內容。

### 部署簡報

當您準備好部署簡報時，push 到此 repo 即可。

@2024 SCAICT  
[Discord](https://dc.scaict.org) · [GitHub](https://github.com/SCAICT)
