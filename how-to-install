# Minecraft 材質包完整教學

適用Java版1.20.2 ~ 26.x。基岩版的資源包結構完全不同，不適用本文。

---

## 一、安裝前先搞懂三件事

**1. 材質包可以不解壓縮**
Minecraft 可以直接讀取 `.zip`。只有在你想整理成資料夾、編輯 `pack.mcmeta`，或使用資料夾分類模組時，才需要解壓縮。

**2. 判斷材質包是否可用**
根目錄必須直接看到 `pack.mcmeta` 和 `assets` 資料夾。

### ✅ 正確
```
Material Expressive v5/
 ┣━━ pack.mcmeta
 ┣━━ pack.png
 ┗━━ assets/
```

### ❌ 錯誤（多包了一層，遊戲會認不出來）
```
Material Expressive v5/
 ┗━━ Material Expressive v5/
     ┣━━ pack.mcmeta
     ┗━━ assets/
```

**3. 版本相容性**  
版本不符時，遊戲只會顯示紅色警告，多半仍可載入。(Material Expressive v5適用於1.20.2及以後版本，IceCool UI v31適用於1.16.5~1.20.1，1.20.2前後的材質包幾乎不可互通)

---

## 二、下載與解壓縮

1. 從官方來源下載（[https://icecoolbw.vercel.app/games#minecraft](https://icecoolbw.vercel.app/games#minecraft)）。
2. Material Expressive v5包含多個檔案（核心 + 配色變體 + 字體擴充），請依需求或全部下載。
3. 需要解壓縮時：
    - **Windows**：右鍵 → 全部解壓縮（或用7-Zip、NanoZip）
    - **macOS**：雙擊 zip
    - **Linux**：`unzip 檔名.zip`
4. 解壓縮後檢查根目錄是否直接有 `pack.mcmeta`。若多了一層，把內層資料夾拿出來即可。

> 注意：不要用「解壓縮到同名資料夾」的選項，這很容易造成上述雙層資料夾問題。
> 本材質包(Material Expressive v5) 請使用「解壓縮至此」。

---

## 三、放進資源包資料夾

### 開啟資料夾的方法

遊戲內：**選項 → 資源包 → 開啟資源包資料夾**

### 手動路徑

|系統|路徑|
|---|---|
|Windows|`%appdata%\.minecraft\resourcepacks`|
|macOS|`~/Library/Application Support/minecraft/resourcepacks`|
|Linux|`~/.minecraft/resourcepacks`|

使用 Prism、MultiMC、CurseForge等啟動器時，路徑會在各自的實例資料夾內：`實例資料夾/minecraft/resourcepacks`（或 `.minecraft/resourcepacks`）。可從啟動器的「開啟資料夾」按鈕進入。

---

## 四、你的資料夾結構怎麼擺

原生 Minecraft 的資源包畫面**只掃描 `resourcepacks` 資料夾第一層**，不會自動進入子資料夾尋找。[網站](https://material-3e-pack.vercel.app/)中的分類結構，需要搭配模組才會顯示。

建議結構如下：

```
resourcepacks/
 ┣━━ Material Expressive 系列/           ← 分類資料夾（需模組支援）
 ┃   ┣━━ Material Expressive v5/           核心版本
 ┃   ┣━━ Material Expressive v5 - ReColor Ver./   配色變體
 ┃   ┗━━ Material Expressive Addon - Roboto v1/   字體擴充
 ┗━━ 其他材質類型資源包...
```

**沒有管理模組時**，請把各個資料夾（或 zip）直接放在 `resourcepacks` 第一層，並用檔名區分，例如：

```
resourcepacks/
 ┣━━ Material Expressive v5.zip
 ┣━━ Material Expressive v5 - ReColor Ver.zip
 ┗━━ Material Expressive Addon - Roboto v1.zip
```

---

## 五、在遊戲內啟用

1. 進入 **選項 → 資源包**。
2. 左側「可用」清單會出現你的資源包。
3. 點資源包上的 **箭頭 ▶** 移到右側「已選擇」。
4. 按 **完成**，遊戲會重新載入。

### 載入順序（重要）

右側清單中，**越上面的優先度越高，會覆蓋下面的**。

針對Material Expressive v5，建議順序（由上到下）：

```
資源包根目錄
 ┣━━ Material Expressive 系列 (如果有資源包管理模組推薦使用資料夾)
 ┃   ┣━━ Material Expressive Addon - Roboto v1 (字體擴充)
 ┃   ┣━━ 其他擴充 (如：模組支援、選單背景等)
 ┃   ┣━━ Material Expressive v5 - ReColor Ver. (配色變體)
 ┃   ┗━━ Material Expressive v5 (核心版本)
 ┗━━ 其他材質類型資源包...
```

原因：擴充與變體只覆蓋少數檔案，必須放在核心之上才會生效。

---

## 六、處理版本警告

### 常見訊息

- 「為舊版 Minecraft 製作」或「為新版 Minecraft 製作」：屬於警告，按「是」即可載入，通常能用，但新版新增的GUI可能沒有對應貼圖。(材質包5.0.0版本支援到Minecraft 26.3)

---

## 七、字體擴充的注意事項

- 如果與其他字體類資源包同時使用，只有排在最上面的字體設定會生效。

---

## 八、疑難排解

| 問題                    | 解決方法                                                           |
| --------------------- | -------------------------------------------------------------- |
| 資源包清單裡看不到             | 檢查是否多包一層資料夾，確認 `pack.mcmeta` 在根目錄，確認副檔名是 `.zip` 而不是 `.zip.zip` |
| 啟用後畫面沒變化              | 載入順序錯誤，按 F3 + T 重新載入                                           |
| 配色變體沒效果               | 確認它排在核心版本上方                                                    |
