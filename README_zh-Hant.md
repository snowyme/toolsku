[English](README.md) | [简体中文](README_zh.md) | **繁體中文** | [日本語](README_ja.md)

---

## 熱門工具直達

官網入口：[Toolsku 線上工具箱](https://www.toolsku.com/)

以下是使用者搜尋頻率較高、適合作為外部入口的工具：

| 分類 | 工具 |
|---|---|
| 圖片工具 | [圖片壓縮](https://www.toolsku.com/zh-TW/image/compress) |
| 圖片工具 | [PNG 壓縮](https://www.toolsku.com/zh-TW/image/png-compress) |
| 圖片工具 | [JPG 壓縮](https://www.toolsku.com/zh-TW/image/jpg-compress) |
| 圖片工具 | [圖片格式互轉](https://www.toolsku.com/zh-TW/image/convert) |
| PDF 工具 | [PDF 轉 Word](https://www.toolsku.com/zh-TW/pdf/to-word) |
| PDF 工具 | [PDF 轉 Excel](https://www.toolsku.com/zh-TW/pdf/to-excel) |
| PDF 工具 | [PDF 轉圖片](https://www.toolsku.com/zh-TW/pdf/pdf-to-images) |
| JSON 工具 | [JSON 格式化](https://www.toolsku.com/zh-TW/json/format) |
| 實用工具 | [銀行卡 BIN 查詢](https://www.toolsku.com/zh-TW/utils/bankcard-bin) |
| 實用工具 | [QR 碼生成](https://www.toolsku.com/zh-TW/encode/qr) |
| 實用工具 | [QR 碼辨識](https://www.toolsku.com/zh-TW/encode/qr-decode) |
| 實用工具 | [Wi-Fi QR 碼生成](https://www.toolsku.com/zh-TW/encode/wifi-qr) |
| 影片工具 | [影片壓縮](https://www.toolsku.com/zh-TW/video/compress) |
| 實用工具 | [工時計算器](https://www.toolsku.com/zh-TW/utils/work-hours) |
| 實用工具 | [UUID 產生器](https://www.toolsku.com/zh-TW/utils/uuid) |
| 實用工具 | [條碼產生器](https://www.toolsku.com/zh-TW/utils/barcode) |
| 實用工具 | [匯率換算](https://www.toolsku.com/zh-TW/utils/exchange-rate) |
| 實用工具 | [貸款計算器](https://www.toolsku.com/zh-TW/utils/loan-calc) |
| 實用工具 | [房貸計算器](https://www.toolsku.com/zh-TW/utils/mortgage-calc) |
| 實用工具 | [BMI 計算器](https://www.toolsku.com/zh-TW/utils/bmi) |
| 實用工具 | [番茄鐘](https://www.toolsku.com/zh-TW/utils/pomodoro) |

---

## 歡迎貢獻

歡迎大家給工具庫 **toolsku** 提問題或優化意見，我會第一時間跟進並優化解決！無論是功能需求、Bug 回饋還是使用體驗上的建議，都歡迎透過 Issue 提交交流。

---

# 功能簡介

**toolsku** 是一個基於 **Next.js 15 + React 19** 構建的現代線上工具箱，採用純前端（瀏覽器本地）處理為主的設計，涵蓋圖片、PDF、影片、文字、JSON、編碼加密、Web/SEO、開發介面、文件效率等數百個實用工具。資料處理優先在本機完成，無需上傳即可保護隱私；少數重計算場景（如 PDF 轉 Word/Excel）透過阿里雲檔案智能（DocMind）代理完成。

### 核心技術

- **Next.js 15（App Router）+ React 19 + TypeScript**，靜態匯出（SSG），可部署到任意靜態託管 / 阿里雲函式計算。
- **國際化**：`next-intl` 支援 **簡體中文、繁體中文、English、日本語** 四語種（`localePrefix: always`）。
- **本機運算**：利用 WebAssembly（ffmpeg.wasm、PDF 解析）、Web Crypto API、Canvas、Web Audio 等在瀏覽器端完成轉換與計算。
- **搜尋索引自動生成**：建置期腳本生成多語種工具搜尋索引與 SEO 頁面。

### 主要功能分類

#### 1. PDF 工具（26+）

合併/拆分/旋轉/刪除頁、PDF 轉圖片（PNG/JPG）、圖片轉 PDF、壓縮、加密/解密、文字浮水印、圖章/Logo、頁碼、頁首頁尾範本、文字提取、反轉頁序、中繼資料讀寫、簽名檢查、PDF 轉 Word/Excel（DocMind）等。

#### 2. 圖片工具（30+）

格式互轉（PNG/JPG/WebP/ICO/SVG/HEIC/GIF）、批量壓縮、改尺寸、裁剪、等比例縮放、浮水印、拼接、九宮格裁剪、翻轉/旋轉/濾鏡、灰階化、EXIF 檢視與清除、OCR 文字辨識、電子簽名、截圖美化、GIF 逐幀提取等。

#### 3. 影片工具（12+）

格式轉換（MP4/WebM/MKV/MOV/AVI/GIF）、剪輯、壓縮、轉 GIF、提取音訊（ffmpeg.wasm 純瀏覽器本機轉碼）。

#### 4. JSON 工具（14+）

格式化/壓縮/最小化、YAML ↔ JSON、TOML ↔ JSON、JSON ↔ CSV、XML ↔ JSON、JSONPath 查詢、JMESPath 查詢、JSON 結構對比（Diff）、JSON → TypeScript/Go/Java/SQL 型別生成、JSON 深度合併。

#### 5. 文字處理（40+）

大小寫與命名轉換（camelCase/kebab/snake/CONSTANT 等）、行整理排序去重、字數統計、正則試驗台、文字對比（Diff）、Markdown 即時預覽、HTML 轉純文字、縮排/反縮排、行號、固定寬度換行、拼音、簡繁轉換、字串脫敏、Emoji 選擇器、近反義詞、Numeronym、ASCII 文字畫、盤古之白、範本填充、URL 安美化、違禁詞檢測、提詞器、中文拆字、URL 批量生成、文字行長度過濾、文字轉語音、標點符號轉換、逆序、文字轉 HTML 表格、特殊符號大全等。

#### 6. 加密解密（30+）

Base64/Base32/Base58 編解碼、URL/Hex 編解碼、HTML 實體與 JSON 轉義、雜湊摘要（MD5/SHA-256 等）、HMAC、AES-256-GCM、RSA-OAEP、Bcrypt、SM2/SM3/SM4 國密、DES/3DES、RC4、XOR、維吉尼亞密碼、凱撒密碼、RIPEMD-160、CRC32/BCC/LRC 校驗、隨機密碼/Token 生成、QR 碼生成與辨識、Wi-Fi QR 碼、BIP39 助記詞、RSA 金鑰對產生、密碼強度分析、ISO-8859-1 亂碼修復、Emoji 加密等。

#### 7. Web / SEO 工具

Open Graph 預覽、robots.txt 生成、Sitemap 產生、CSP（內容安全策略）組裝、Permissions-Policy 組裝、.env 解析、安全回應標頭速查、Whois 查詢、DNS 查詢、ICP 備案查詢、公網 IP 查詢、瀏覽器指紋檢測、連接埠開放檢測、DNS over HTTPS、URL 解析、Punycode、Data URL、MIME 速查、檔案類型嗅探、HTTP 狀態碼速查、User-Agent 解析、顏色轉換/對比度等。

#### 8. 開發與介面（40+）

GraphQL 格式化、OpenAPI（Swagger）瀏覽、Properties ↔ JSON、.editorconfig 生成、XML 格式化、SemVer 比較、Mermaid 預覽、Nginx 格式化、Docker Run → Compose、正則大全、假資料生成、程式碼反混淆、cURL 轉程式碼、CSS 產生器（Box Shadow、Border Radius、Flexbox、漸層、動畫）、色盲模擬器、Protobuf 解碼、htpasswd 生成、程式碼截圖、CSR 生成、線上程式碼執行（HTML/CSS/JS）、目錄樹產生器、鍵值對轉程式碼、檔案雜湊計算、大端/小端轉換、原碼/反碼/補碼、SSL 憑證生成、PFX 轉 PEM、HTTP 模擬請求、通用程式碼格式化器等。

#### 9. 文件與效率（12+）

CSV ↔ Markdown 表格、全形/半形轉換、人民幣大寫、iCalendar（.ics）預覽、vCard 解析、郵件標頭解析、身分證校驗、中國傳統色彩、親戚關係計算、元素週期表、格子紙生成、化學方程式配平。

#### 10. 小工具 / 實用工具（60+）

時間戳轉換、UUID/ULID/NanoID 生成、日期計算/年齡計算、亂數/百分比、溫度轉換、羅馬數字、單位換算、進制換算、ASCII 表、IBAN/Luhn 校驗、電話號碼解析、北約/摩斯/盲文編碼、條碼/藝術 QR 碼生成、OTP/TOTP、HTTP Basic Auth、Cookie 解析、JWT 生成/解碼、SVG 佔位符、碼錶計時、MAC 位址查詢/生成、IPv4/IPv6 網路工具、連接埠速查、數學表達式計算、ETA 計算器、裝置資訊、AI Token 計數器、寬高比計算、貸款/房貸/BMI/個稅計算器、工時計算、座標轉換、字幕格式轉換、GCD/LCM、手持彈幕、批量重新命名、銀行卡 Bin、匯率換算、音訊剪輯、種子分析、佔位圖片生成、隱私政策產生器、番茄鐘、螢幕 PPI 計算、GB2312/GBK 編碼表、公曆農曆轉換、世界時鐘、麥克風/鍵盤/螢幕測試、塗鴉畫板、模冪計算、二進位逆序、閏年查詢、字型預覽、剪貼簿檢視、SVG 編輯器、反應時間測試、IPv4↔IPv6 轉換、網頁定時重新整理等。

### 設計亮點

- **隱私優先**：絕大多數工具在瀏覽器本機執行，檔案不上傳到任何伺服器。
- **多語種 SEO**：每個工具均生成 4 語言靜態頁與 `hreflang` 標籤，搜尋引擎友善。
- **零後端相依（預設）**：靜態網站開箱即用；僅在需要 PDF→Word/Excel 轉換時才需部署 DocMind 代理。
- **響應式設計**：適配桌面與行動端。

---

## 工具數量概覽

| 分類 | 數量 |
|---|---|
| PDF 工具 | 26+ |
| JSON 工具 | 14+ |
| 文字處理 | 40+ |
| 圖片工具 | 30+ |
| 影片工具 | 12+ |
| 加密解密 | 30+ |
| Web / SEO | 20+ |
| 開發與介面 | 40+ |
| 文件與效率 | 12+ |
| 小工具 | 60+ |
| **合計** | **約 300+** |
