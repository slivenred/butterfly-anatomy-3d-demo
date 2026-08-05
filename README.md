<div align="center">

# Butterfly Atelier 3D

### 互動式藍閃蝶解剖、飛行力學與結構色視覺化

以原生 **WebGL 2** 打造的博物館級 3D 科學展示 Demo。  
旋轉標本、探索構造熱點、觀察四翼拍動、拆解翅脈與翅膜，並從微觀尺度理解藍閃蝶的結構色。

<p>
  <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/"><img alt="Open Live Demo" src="https://img.shields.io/badge/LIVE_DEMO-OPEN_NOW-1677ff?style=for-the-badge&logo=githubpages&logoColor=white"></a>
  <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/demo.html"><img alt="Open Fullscreen Viewer" src="https://img.shields.io/badge/3D_VIEWER-FULLSCREEN-6547d8?style=for-the-badge&logo=webgl&logoColor=white"></a>
  <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/assets/video/feature-tour.mp4"><img alt="Watch Demo Video" src="https://img.shields.io/badge/DEMO_VIDEO-WATCH-ec6f5e?style=for-the-badge&logo=youtube&logoColor=white"></a>
</p>

<p>
  <img alt="MIT License" src="https://img.shields.io/badge/License-MIT-2f2a27?style=flat-square">
  <img alt="WebGL 2" src="https://img.shields.io/badge/WebGL-2.0-990000?style=flat-square&logo=webgl&logoColor=white">
  <img alt="Zero runtime dependencies" src="https://img.shields.io/badge/runtime_dependencies-0-769d74?style=flat-square">
  <img alt="GitHub Pages" src="https://img.shields.io/badge/deploy-GitHub_Pages-222222?style=flat-square&logo=github">
</p>

[![Butterfly Atelier 3D overview](assets/images/preview.png)](https://slivenred.github.io/butterfly-anatomy-3d-demo/)

**點擊上方畫面，直接進入 GitHub Pages Live Demo。**

</div>

---

## 專案概覽

Butterfly Atelier 3D 將藍閃蝶呈現為一件可以自由探索的數位標本，而不是固定角度的 3D 模型。

中央 Viewer 是整個體驗的主角；左側提供觀察模式，右側整理當前主題的科學資訊，畫面中的發光熱點則會跟著標本旋轉並連結到對應構造。使用者可以在同一套介面中，從外部形態一路深入到翅面材料、飛行運動與生命週期。

本專案沒有 runtime 套件依賴，核心幾何、動畫、相機、材質、光照與互動皆以原生 WebGL 2 與 JavaScript 實作。

### 快速入口

| 項目 | 連結 |
|---|---|
| 完整 Demo Site | [開啟專案首頁](https://slivenred.github.io/butterfly-anatomy-3d-demo/) |
| 全螢幕 3D Viewer | [開啟互動標本](https://slivenred.github.io/butterfly-anatomy-3d-demo/demo.html) |
| 完整功能展示影片 | [播放 H.264 MP4](https://slivenred.github.io/butterfly-anatomy-3d-demo/assets/video/feature-tour.mp4) |
| 概念來源與歸屬 | [閱讀 ATTRIBUTION.md](ATTRIBUTION.md) |
| 技術實作說明 | [閱讀 TECHNICAL_NOTES.md](docs/TECHNICAL_NOTES.md) |
| 影片與功能驗證 | [閱讀 VIDEO_QA.md](docs/VIDEO_QA.md) |

---

## 功能展示

### 1. 互動式 3D 科學標本

- 拖曳旋轉並從任意角度觀察標本
- 滾輪或觸控手勢縮放
- 窄視角鏡頭降低廣角變形，保留標本攝影感
- 暖、冷主光與輪廓光共同塑造翅面和身體體積
- 柔和展示底座、接觸陰影與環境光暈
- 依畫面可見性與互動狀態調整更新，避免不必要渲染

### 2. 跟隨標本的構造熱點

熱點存在於 3D 座標中，而不是固定在網頁上的裝飾標籤。旋轉標本時，標記與說明卡會跟著觸角、前翅、後翅、胸部、腹部、足與翅鱗位置移動。

- 固定螢幕閱讀尺寸
- 前後面可見度判斷
- 點擊、懸停與脈衝提示
- 說明卡自動選擇左右展開方向

### 3. 四翼飛行力學

前翅與後翅不是共用一個整體旋轉，而是四個獨立翼面。飛行模式會呈現不同相位、拍動幅度與翼面扭轉，同時加入氣流路徑，讓動作更接近真正的飛行展示。

### 4. 藍閃蝶結構色

藍閃蝶的亮藍並非單純塗上一層藍色。Viewer 透過自訂 Shader，讓翅面顏色依視線、表面法線與光線角度，在深藍、青藍、靛藍與微量紫色之間變化，模擬結構色的觀看感受。

### 5. 分層觀察

使用者可以逐步切換：

1. **完整翅面**：觀察結構色與整體標本。
2. **翅脈網路**：凸顯翅脈分布與支撐關係。
3. **半透明翅膜**：降低表面遮蔽，理解翅面層次。
4. **翅鱗剖面**：將屋瓦狀翅鱗與微觀支撐構造放大展示。

### 6. 背面、腹面與生命週期

- 一鍵翻轉整個標本，比較背面結構色與腹面棕褐色保護性外觀
- 隔離模式弱化展台與環境元素
- 完全變態模式依序呈現卵、幼蟲、蛹與成蝶
- 一鍵重設相機、圖層與所有 Viewer 狀態

---

## 擷圖畫廊

<table>
  <tr>
    <td width="50%" align="center">
      <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/demo.html">
        <img src="assets/images/preview.png" alt="完整 3D 藍閃蝶標本" width="100%">
      </a>
      <br><strong>完整 3D 標本</strong><br>
      <sub>中央標本、解剖熱點與博物館式工作區</sub>
    </td>
    <td width="50%" align="center">
      <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/demo.html">
        <img src="assets/images/preview-flight.png" alt="蝴蝶飛行力學模式" width="100%">
      </a>
      <br><strong>飛行力學</strong><br>
      <sub>四翼獨立拍動、翼面扭轉與氣流路徑</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" align="center">
      <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/demo.html">
        <img src="assets/images/preview-micro.png" alt="蝴蝶翅鱗微觀剖面" width="100%">
      </a>
      <br><strong>翅鱗微觀剖面</strong><br>
      <sub>放大屋瓦狀翅鱗、支撐脊與翅膜結構</sub>
    </td>
    <td width="50%" align="center">
      <a href="https://slivenred.github.io/butterfly-anatomy-3d-demo/">
        <img src="assets/images/preview-mobile.png" alt="行動裝置響應式畫面" width="100%">
      </a>
      <br><strong>行動裝置</strong><br>
      <sub>針對窄螢幕、觸控與 Pixel Ratio 調整</sub>
    </td>
  </tr>
</table>

> 所有圖片皆可點擊開啟公開 Demo。完整解析度檔案位於 [`assets/images`](assets/images)。

---

## Demo 影片

<div align="center">

[![觀看 Butterfly Atelier 3D 完整功能展示](assets/images/feature-tour-contact-sheet.jpg)](https://slivenred.github.io/butterfly-anatomy-3d-demo/assets/video/feature-tour.mp4)

### [▶ 播放完整功能展示影片](https://slivenred.github.io/butterfly-anatomy-3d-demo/assets/video/feature-tour.mp4)

約 **2 分 21 秒｜1280 × 800｜H.264／AVC｜30 fps**

</div>

影片依序展示：

- 3D 標本旋轉與縮放
- 構造熱點與跟隨式說明卡
- 四翼飛行動畫與氣流視覺化
- 角度依賴的藍色結構色
- 完整翅面、翅脈與半透明翅膜
- 翅鱗微觀剖面
- 標本隔離與背腹面比較
- 卵、幼蟲、蛹、成蝶的完全變態
- 一鍵重設與概念來源說明

> GitHub README 不會穩定保留 HTML `<video>` 播放器，因此此處採用可點擊的影片封面與 MP4 直連。影片會由 GitHub Pages 直接開啟播放。

---

## 操作方式

| 操作 | 桌機 | 行動裝置 |
|---|---|---|
| 旋轉標本 | 按住滑鼠左鍵拖曳 | 單指拖曳 |
| 縮放 | 滑鼠滾輪 | 雙指縮放或使用工具按鈕 |
| 查看構造 | 點擊發光熱點 | 點按發光熱點 |
| 切換主題 | 左側模式選單 | 響應式模式選單 |
| 切換工具 | Viewer 左側工具列 | Viewer 工具控制區 |
| 關閉說明 | 點擊關閉或其他熱點 | 點按關閉或其他熱點 |

---

## 設計與技術方法

### 視覺系統

- 暖白、低對比、博物館標本式介面
- 大面積留白與中央單一視覺焦點
- 34° 窄視角標本鏡頭
- 冷暖攝影棚布光與輪廓光
- 柔和接觸陰影取代高成本即時陰影
- 半透明工具面板、低對比邊框與細緻內陰影

### WebGL 2 實作

- 高密度程序化四翼曲面
- 原創翅面紋理與背腹面材質
- 自訂 Vertex／Fragment Shader
- 角度依賴的結構色色相與高光
- 深度測試、Alpha 混合與分層顯示
- 獨立翼面樞紐與時間軸動畫
- 3D 座標投影式熱點
- 依裝置能力限制 Pixel Ratio
- 頁面隱藏或 Viewer 離開視窗時暫停更新

### 為什麼沒有使用大型框架

這是一個專注於視覺原理與互動方法的 Demo，因此選擇原生 WebGL 2，讓核心渲染、Shader、動畫與互動邏輯都可以直接閱讀。專案無需安裝 runtime 依賴，也適合直接部署至 GitHub Pages。

---

## 概念來源與原創邊界

本專案的互動標本展示方法與介面概念，受到以下作品啟發：

- 原始專案：[`thebuggeddev/anatomy`](https://github.com/thebuggeddev/anatomy)
- 概念作者：GitHub 使用者 [`@thebuggeddev`](https://github.com/thebuggeddev)
- 公開展示：`anatomy-livid.vercel.app`

主要參考的是：

- 以中央大型 3D 標本作為畫面主角
- 暖白色、低對比、博物館式工作區
- 窄視角鏡頭與攝影棚式冷暖布光
- 展示底座與接觸陰影
- 垂直工具列
- Isolate、Section、Layers、Compare 等探索工具
- 跟隨標本的 3D 熱點和說明卡
- 只在畫面或狀態改變時持續更新的效能策略

本 repository **沒有包含或重新散布**參考專案的程式碼、器官模型、貼圖、圖像或內容資料。蝴蝶幾何、WebGL 2 引擎、Shader、動畫、翅面資產、介面、文件、擷圖與展示影片，均為本專案重新實作或製作。

完整說明請閱讀 [`ATTRIBUTION.md`](ATTRIBUTION.md)。

---

## 專案結構

```text
.
├── index.html                         # Demo Site 專案首頁
├── demo.html                          # 全螢幕、自包含 WebGL 2 Viewer
├── assets/
│   ├── images/
│   │   ├── preview.png                # 主要展示畫面
│   │   ├── preview-flight.png         # 飛行力學模式
│   │   ├── preview-micro.png          # 翅鱗剖面模式
│   │   ├── preview-mobile.png         # 行動裝置畫面
│   │   └── feature-tour-contact-sheet.jpg
│   ├── textures/                      # 原創翅面紋理
│   └── video/
│       └── feature-tour.mp4           # 完整功能展示影片
├── docs/
│   ├── TECHNICAL_NOTES.md
│   └── VIDEO_QA.md
├── ATTRIBUTION.md
├── LICENSE
└── .github/workflows/pages.yml        # GitHub Pages 自動部署
```

---

## 本機執行

不需要安裝 npm 套件。Clone 後啟動任何靜態伺服器即可：

```bash
git clone https://github.com/slivenred/butterfly-anatomy-3d-demo.git
cd butterfly-anatomy-3d-demo
python3 -m http.server 4173
```

瀏覽器開啟：

```text
http://localhost:4173/
```

全螢幕 Viewer：

```text
http://localhost:4173/demo.html
```

> 不建議直接用 `file://` 開啟，部分瀏覽器會限制本機資產與媒體載入。

---

## 部署

專案包含 GitHub Pages workflow。推送至 `main` 後，GitHub Actions 會自動部署靜態網站：

```text
https://slivenred.github.io/butterfly-anatomy-3d-demo/
```

---

## 瀏覽器與效能

建議使用支援 WebGL 2 的近期版本：

- Chrome／Edge
- Safari
- Firefox

Viewer 會依裝置效能限制最高 Pixel Ratio，低效能或行動裝置不會盲目以完整 Retina 倍率渲染。當分頁被隱藏或 Viewer 離開可視範圍時，也會降低不必要的更新。

---

## 授權

本專案的原創程式碼、文件與隨附資產採用 [MIT License](LICENSE)。

參考專案的名稱、內容與權利仍分別屬於其原始權利人。本專案的 MIT 授權不延伸至 `thebuggeddev/anatomy` 或其他第三方內容。

---

<div align="center">

### Explore the butterfly as a living system, not a static object.

[Live Demo](https://slivenred.github.io/butterfly-anatomy-3d-demo/) · [3D Viewer](https://slivenred.github.io/butterfly-anatomy-3d-demo/demo.html) · [Demo Video](https://slivenred.github.io/butterfly-anatomy-3d-demo/assets/video/feature-tour.mp4) · [Attribution](ATTRIBUTION.md) · [MIT License](LICENSE)

</div>
