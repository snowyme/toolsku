[English](README.md) | **简体中文** | [繁體中文](README_zh-Hant.md) | [日本語](README_ja.md)

---

## 高频工具直达

官网入口：[Toolsku 在线工具箱](https://www.toolsku.com/)

以下是用户搜索频率较高、适合作为外链入口的工具：

| 分类 | 工具 |
|---|---|
| 图片工具 | [图片压缩](https://www.toolsku.com/zh-CN/image/compress) |
| 图片工具 | [PNG 压缩](https://www.toolsku.com/zh-CN/image/png-compress) |
| 图片工具 | [JPG 压缩](https://www.toolsku.com/zh-CN/image/jpg-compress) |
| 图片工具 | [图片格式互转](https://www.toolsku.com/zh-CN/image/convert) |
| PDF 工具 | [PDF 转 Word](https://www.toolsku.com/zh-CN/pdf/to-word) |
| PDF 工具 | [PDF 转 Excel](https://www.toolsku.com/zh-CN/pdf/to-excel) |
| PDF 工具 | [PDF 转图片](https://www.toolsku.com/zh-CN/pdf/pdf-to-images) |
| JSON 工具 | [JSON 格式化](https://www.toolsku.com/zh-CN/json/format) |
| 实用工具 | [银行卡 BIN 查询](https://www.toolsku.com/zh-CN/utils/bankcard-bin) |
| 实用工具 | [二维码生成](https://www.toolsku.com/zh-CN/encode/qr) |
| 实用工具 | [二维码识别](https://www.toolsku.com/zh-CN/encode/qr-decode) |
| 实用工具 | [Wi-Fi 二维码生成](https://www.toolsku.com/zh-CN/encode/wifi-qr) |
| 视频工具 | [视频压缩](https://www.toolsku.com/zh-CN/video/compress) |
| 实用工具 | [工时计算器](https://www.toolsku.com/zh-CN/utils/work-hours) |
| 实用工具 | [UUID 生成器](https://www.toolsku.com/zh-CN/utils/uuid) |
| 实用工具 | [条形码生成器](https://www.toolsku.com/zh-CN/utils/barcode) |
| 实用工具 | [汇率换算](https://www.toolsku.com/zh-CN/utils/exchange-rate) |
| 实用工具 | [贷款计算器](https://www.toolsku.com/zh-CN/utils/loan-calc) |
| 实用工具 | [房贷计算器](https://www.toolsku.com/zh-CN/utils/mortgage-calc) |
| 实用工具 | [BMI 计算器](https://www.toolsku.com/zh-CN/utils/bmi) |
| 实用工具 | [番茄钟](https://www.toolsku.com/zh-CN/utils/pomodoro) |

---

## 欢迎贡献

欢迎大家给工具库 **toolsku** 提问题或优化意见，我会第一时间跟进并优化解决！无论是功能需求、Bug 反馈还是使用体验上的建议，都欢迎通过 Issue 提交交流。

---

# 功能简介

**toolsku** 是一个基于 **Next.js 15 + React 19** 构建的现代在线工具箱，采用纯前端（浏览器本地）处理为主的设计，覆盖图片、PDF、视频、文本、JSON、编码加密、Web/SEO、开发接口、文档效率等数百个实用工具。数据处理优先在本地完成，无需上传即可保护隐私；少数重计算场景（如 PDF 转 Word/Excel）通过阿里云文档智能（DocMind）代理完成。

### 核心技术

- **Next.js 15（App Router）+ React 19 + TypeScript**，静态导出（SSG），可部署到任意静态托管 / 阿里云函数计算。
- **国际化**：`next-intl` 支持 **简体中文、繁体中文、English、日本語** 四语种（`localePrefix: always`）。
- **本地运算**：利用 WebAssembly（ffmpeg.wasm、PDF 解析）、Web Crypto API、Canvas、Web Audio 等在浏览器端完成转换与计算。
- **搜索索引自动生成**：构建期脚本生成多语种工具搜索索引与 SEO 页面。

### 主要功能分类

#### 1. PDF 工具（26+）

合并/拆分/旋转/删除页、PDF 转图片（PNG/JPG）、图片转 PDF、压缩、加密/解密、文字水印、图章/Logo、页码、页眉页脚模板、文本提取、反转页序、元数据读写、签名检查、PDF 转 Word/Excel（DocMind）等。

#### 2. 图片工具（30+）

格式互转（PNG/JPG/WebP/ICO/SVG/HEIC/GIF）、批量压缩、改尺寸、裁剪、等比例缩放、水印、拼接、九宫格裁剪、翻转/旋转/滤镜、灰度化、EXIF 查看与清除、OCR 文字识别、电子签名、截图美化、GIF 逐帧提取等。

#### 3. 视频工具（12+）

格式转换（MP4/WebM/MKV/MOV/AVI/GIF）、剪切、压缩、转 GIF、提取音频（ffmpeg.wasm 纯浏览器本地转码）。

#### 4. JSON 工具（14+）

格式化/压缩/最小化、YAML ↔ JSON、TOML ↔ JSON、JSON ↔ CSV、XML ↔ JSON、JSONPath 查询、JMESPath 查询、JSON 结构对比（Diff）、JSON → TypeScript/Go/Java/SQL 类型生成、JSON 深度合并。

#### 5. 文本处理（40+）

大小写与命名转换（camelCase/kebab/snake/CONSTANT 等）、行整理排序去重、字数统计、正则试验台、文本对比（Diff）、Markdown 在线预览、HTML 转纯文本、缩进/反缩进、行号、固定宽度换行、拼音、简繁转换、字符串脱敏、Emoji 选择器、近反义词、Numeronym、ASCII 文字画、盘古之白、模板填充、URL 安美化、违禁词检测、提词器、中文拆字、URL 批量生成、文本行长度过滤、文本转语音、标点符号转换、逆序、文本转 HTML 表格、特殊符号大全等。

#### 6. 加密解密（30+）

Base64/Base32/Base58 编解码、URL/Hex 编解码、HTML 实体与 JSON 转义、哈希摘要（MD5/SHA-256 等）、HMAC、AES-256-GCM、RSA-OAEP、Bcrypt、SM2/SM3/SM4 国密、DES/3DES、RC4、XOR、维吉尼亚密码、凯撒密码、RIPEMD-160、CRC32/BCC/LRC 校验、随机密码/Token 生成、二维码生成与识别、Wi-Fi 二维码、BIP39 助记词、RSA 密钥对生成、密码强度分析、ISO-8859-1 乱码修复、Emoji 加密等。

#### 7. Web / SEO 工具

Open Graph 预览、robots.txt 生成、Sitemap 生成、CSP（内容安全策略）拼装、Permissions-Policy 拼装、.env 解析、安全响应头速查、Whois 查询、DNS 查询、ICP 备案查询、公网 IP 查询、浏览器指纹检测、端口开放检测、DNS over HTTPS、URL 解析、Punycode、Data URL、MIME 速查、文件类型嗅探、HTTP 状态码速查、User-Agent 解析、颜色转换/对比度等。

#### 8. 开发与接口（40+）

GraphQL 格式化、OpenAPI（Swagger）浏览、Properties ↔ JSON、.editorconfig 生成、XML 格式化、SemVer 比较、Mermaid 预览、Nginx 格式化、Docker Run → Compose、正则大全、假数据生成、代码反混淆、cURL 转代码、CSS 生成器（Box Shadow、Border Radius、Flexbox、渐变、动画）、色盲模拟器、Protobuf 解码、htpasswd 生成、代码截图、CSR 生成、在线代码运行（HTML/CSS/JS）、目录树生成器、键值对转代码、文件 Hash 计算、大端/小端转换、原码/反码/补码、SSL 证书生成、PFX 转 PEM、HTTP 模拟请求、通用代码格式化器等。

#### 9. 文档与效率（12+）

CSV ↔ Markdown 表格、全角/半角转换、人民币大写、iCalendar（.ics）预览、vCard 解析、邮件头解析、身份证校验、中国传统色彩、亲戚关系计算、元素周期表、格子纸生成、化学方程式配平。

#### 10. 小工具 / 实用工具（60+）

时间戳转换、UUID/ULID/NanoID 生成、日期计算/年龄计算、随机数/百分比、温度转换、罗马数字、单位换算、进制换算、ASCII 表、IBAN/Luhn 校验、电话号码解析、北约/摩尔斯/盲文编码、条形码/艺术二维码生成、OTP/TOTP、HTTP Basic Auth、Cookie 解析、JWT 生成/解码、SVG 占位符、秒表计时、MAC 地址查询/生成、IPv4/IPv6 网络工具、端口速查、数学表达式计算、ETA 计算器、设备信息、AI Token 计数器、宽高比计算、贷款/房贷/BMI/个税计算器、工时计算、坐标转换、字幕格式转换、GCD/LCM、手持弹幕、批量重命名、银行卡 Bin、汇率换算、音频剪辑、种子分析、占位图片生成、隐私政策生成器、番茄钟、屏幕 PPI 计算、GB2312/GBK 编码表、公历农历转换、世界时钟、麦克风/键盘/屏幕测试、涂鸦画板、模幂计算、二进制逆序、闰年查询、字体预览、剪切板查看、SVG 编辑器、反应时间测试、IPv4↔IPv6 转换、网页定时刷新等。

### 设计亮点

- **隐私优先**：绝大多数工具在浏览器本地运行，文件不上传到任何服务器。
- **多语种 SEO**：每个工具均生成 4 语言静态页与 `hreflang` 标签，搜索引擎友好。
- **零后端依赖（默认）**：静态站点开箱即用；仅在需要 PDF→Word/Excel 转换时才需部署 DocMind 代理。
- **响应式设计**：适配桌面与移动端。

---

## 工具数量概览

| 分类 | 数量 |
|---|---|
| PDF 工具 | 26+ |
| JSON 工具 | 14+ |
| 文本处理 | 40+ |
| 图片工具 | 30+ |
| 视频工具 | 12+ |
| 加密解密 | 30+ |
| Web / SEO | 20+ |
| 开发与接口 | 40+ |
| 文档与效率 | 12+ |
| 小工具 | 60+ |
| **合计** | **约 300+** |
