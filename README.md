# Qollie Terminal Viewer

> 在終端機中優雅瀏覽 Qollie (求職天眼通) 公司評論與心得的現代化 TUI 應用程式。

[![Release](https://img.shields.io/github/v/release/sonnytf/qollie-terminal-viewer?color=brightgreen&label=Latest%20Release)](https://github.com/sonnytf/qollie-terminal-viewer/releases)
[![Platform](https://img.shields.io/badge/Platform-macOS%20|%20Linux%20|%20Windows-lightgrey)](#下載二進位檔)
[![Binary Size](https://img.shields.io/badge/Size-~7MB-blue)](#下載二進位檔)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## ✨ 功能特色

- ⚡ **超輕量單一靜態二進位**：僅 ~7MB，無相依依賴，下載即用。
- 🖥️ **雙欄 Master-Detail 自適應佈局**：
  - **頂部大盤**：即時統計星級評分、推薦率分佈與評論總數。
  - **左欄清單**：直覺瀏覽評論標題、作者身份與發布日期；支援 `Tab` 切換「心得 / 討論 / 提問」。
  - **右欄詳情**：對齊閱讀優缺點與留言回覆，智慧折行、零字元斷詞截斷。
- ⌨️ **Vim 風格鍵盤導航**：完全免按 Shift，支援 `j` / `k`、`d` / `u`、`g` / `G` 高效穿梭。
- 🔍 **即時公司搜尋**：內建搜尋引導，支援中文公司名稱或 ID 快速檢索。
- 🎨 **護眼暗色調終端配色**：柔和 Slate 灰藍基調，長時間閱讀不眩光。

---

## 🚀 下載與安裝

從 **[GitHub Releases](https://github.com/sonnytf/qollie-terminal-viewer/releases)** 下載適合你作業系統與架構的執行檔（**純單一執行檔，免解壓縮**）：

| 作業系統 / 架構 | 檔案名稱 | 說明 |
| :--- | :--- | :--- |
| **macOS Apple Silicon** | `qollie-macos-arm64` | M1 / M2 / M3 / M4 晶片 |
| **macOS Intel** | `qollie-macos-amd64` | x86_64 架構 |
| **Linux 64-bit** | `qollie-linux-amd64` | 一般 x86_64 伺服器 / PC |
| **Linux ARM64** | `qollie-linux-arm64` | aarch64 / 樹莓派 / 雲端 ARM |
| **Windows 64-bit** | `qollie-windows-amd64.exe` | 一般 Windows x64 架構 |
| **Windows ARM64** | `qollie-windows-arm64.exe` | Windows on ARM (Snapdragon / Surface 等) |

### 快速安裝範例 (macOS / Linux)

```bash
# 1. 賦予下載的檔案執行權限
chmod +x qollie-macos-arm64

# 2. (選用) 重新命名並移動至系統 PATH 方便隨處輸入 qollie 執行
sudo mv qollie-macos-arm64 /usr/local/bin/qollie
```

---

## 📖 使用方式

```bash
# 1. 直接啟動互動式介面 (進入搜尋畫面)
qollie

# 2. 帶入關鍵字直接搜尋公司
qollie 台積電
qollie 聯發科

# 3. 指定精準公司全名或 Qollie 公司 ID
qollie -n 台灣積體電路製造股份有限公司
qollie --id 5860c66430162b7e4c17de29

# 4. 指定評論擷取筆數上限 (預設 50 筆)
qollie 台積電 --limit 100
```

---

## ⌨️ 鍵盤快捷鍵指南

| 按鍵 | 動作說明 |
| :--- | :--- |
| `↓` 或 `j` | 評論清單向下移動 |
| `↑` 或 `k` | 評論清單向上移動 |
| `Tab` | 切換評論分類（心得 / 討論 / 提問） |
| `→` 或 `d` | 評論內容向下滾動（半頁） |
| `←` 或 `u` | 評論內容向上滾動（半頁） |
| `g` | 跳至第一筆評論 |
| `G` | 跳至最後一筆評論 |
| `/` 或 `s` | 重新開啟搜尋公司畫面 |
| `r` | 重新整理當前公司評論 |
| `q` 或 `Ctrl+C` | 退出程式 |

---

## 📄 授權條款

本專案基於 [MIT License](LICENSE) 釋出。
所有評論數據版權屬於 [Qollie (求職天眼通)](https://www.qollie.com) 及原發文作者所有。
