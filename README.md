# Gapminder PivotUI 線上版

此版本是建立在金融大數據課程分析 `gapminder` 資料的`pivotUI` 互動式資料分析頁面之上，加上透過 GitHub Pages 分享已操作完成的 Pivot Table / Regression 結果的功能。

## 重要聲明

原始 `pivotUI` 程式由 **鍾經樊老師** 製作。

本專案只是課堂作業用途的線上版。原始 `pivotUI` 程式由 **鍾經樊老師** 製作，小的沒有重新開發或主張此工具為本人作品；此網頁版只是為了方便同學不需依賴本機路徑，憑網址即可查看其他同學的pivotUI結果，做了一些與 GitHub Pages 分享、URL 狀態保存、snapshot 下載相關的小修改。

主要修改方向是：

- 讓 pivotUI 可以部署到 GitHub Pages
- 讓同學不需要依賴本機路徑或 RStudio Viewer，透過網址即可查看其他同學已經操作好的 pivotUI 結果
- 新增複製目前狀態網址的功能
- 新增下載 snapshot 的功能，方便保留分析結果

簡單來說，這個版本只是把原本只能在本機查看的互動結果，改成可以透過網頁連結分享。

## 功能說明

這個版本的 pivotUI 支援：
> (1~5 均為鍾經樊老師開發)
1. 互動式 Pivot Table
2. 分組統計，例如平均值、中位數、標準差等
3. 圖表視覺化
4. Regression 頁面
5. 分箱功能，例如 Domain Breaks  
6. 複製目前操作狀態網址
7. 下載目前結果或整頁快照

## 如何查看互動結果

本專案可透過 GitHub Pages 開啟：

```text
https://hizakurakuma.github.io/gapminder-pivot-ui/
```

如果網址後面帶有 `#...`，表示該網址包含目前 pivotUI 的操作狀態。

例如：

```text
https://hizakurakuma.github.io/gapminder-pivot-ui/#pvgapminder_hw6=...
```

打開這種網址時，pivotUI 會自動還原成分享者當時設定好的結果。

## 如何分享自己的結果

1. 打開 GitHub Pages 上的 pivotUI 頁面。
2. 在頁面中完成 Pivot Table、圖表或 Regression 設定。
3. 點選 `Copy current state URL` (按鈕在Regression按鈕右邊的區塊)。
4. 將複製下來的網址分享給其他同學。

其他人打開這個網址後，就可以看到相同的操作結果，且仍然可以繼續互動調整。

## Snapshot 功能

本版本也新增了 snapshot 下載功能：

| 功能                         | 說明                             |
| -------------------------- | ------------------------------ |
| Save interactive full page | 儲存可互動的完整頁面，但仍需搭配 `pivot_libs/` |
| Save static full page      | 儲存靜態完整頁面，不依賴 `pivot_libs/`     |
| Save result snapshot       | 只儲存目前表格、圖表或 regression 結果      |

其中，`static full page` 和 `result snapshot` 比較適合用來繳交或保留畫面結果；
`interactive full page` 則比較適合之後繼續操作。

## 檔案結構

如果其他同學要部署到 GitHub Pages 時，建議維持以下結構：

```text
gapminder-pivot-ui/
├── index.html
└── pivot_libs/
    ├── jquery-3.6.0.min.js
    ├── jquery-ui.min.js
    ├── pivot.min.js
    ├── pivot.min.css
    ├── chart.min.js
    └── ...
```

其中：

* `index.html` 是 GitHub Pages 的首頁
* `pivot_libs/` 是互動式 pivotUI 所需的 JavaScript / CSS 檔案

如果缺少 `pivot_libs/`，互動版頁面可能無法正常運作。

## 修改目的

這次修改的主要目的不是改變老師原本設計的分析功能，而是改善分享方式。

原本同學如果想看彼此的結果，可能需要：

* 傳整個 HTML 檔案
* 擔心本機路徑不同
* 擔心 `pivot_libs/` 找不到
* 無法直接還原對方操作後的狀態

因此，這個版本加入了「複製目前狀態網址」的功能，讓大家只要分享一個 GitHub Pages URL，就可以看到相同的 pivotUI 結果。

## Attribution

Original pivotUI program by Professor 鍾經樊.
This version only makes small adjustments for easier sharing through GitHub Pages and state URLs.

All core pivotUI functionality and original design belong to the original course-provided program.
