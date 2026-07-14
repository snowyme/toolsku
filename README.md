**English** | [简体中文](README_zh.md) | [繁體中文](README_zh-Hant.md) | [日本語](README_ja.md)

---

## Welcome to Contribute

Welcome to submit issues or feedback for **toolsku**! I will follow up and resolve them as soon as possible. Whether it's feature requests, bug reports, or UX suggestions, all kinds of input are highly appreciated.

---

# Feature Overview

**toolsku** is a modern online toolbox built with **Next.js 15 + React 19**, designed around client-side (in-browser) processing. It bundles **hundreds of utilities** across images, PDF, video, text, JSON, encoding/crypto, Web/SEO, developer tools, and documents. Most operations run locally in the browser to protect privacy; a few compute-heavy tasks (e.g. PDF→Word/Excel) are handled via an Alibaba Cloud DocMind proxy.

### Tech Stack

- **Next.js 15 (App Router) + React 19 + TypeScript**, statically exported (SSG), deployable to any static host or Alibaba Cloud Function Compute.
- **i18n**: `next-intl` with **Simplified Chinese, Traditional Chinese, English, Japanese** (`localePrefix: always`).
- **Local computation**: WebAssembly (ffmpeg.wasm, PDF parsing), Web Crypto API, Canvas, Web Audio for in-browser processing.
- **Build-time tooling**: Scripts generate per-locale search indexes, tool client metadata, and SEO pages.

### Feature Categories

#### 1. PDF Tools (26+)

Merge / Split / Rotate / Delete pages, PDF → PNG/JPG, images → PDF, compress, encrypt / decrypt, text watermark, stamp / logo, page numbers, header / footer templates, text extraction, reverse page order, metadata read / write, signature inspection, PDF → Word / Excel (DocMind).

#### 2. Image Tools (30+)

Format conversion (PNG / JPG / WebP / ICO / SVG / HEIC / GIF), batch compress, resize, crop, proportional scale, watermark, collage, nine-grid crop, flip / rotate / filter, grayscale, EXIF view & clear, OCR (Tesseract.js), signature, screenshot beautify, GIF frame extraction.

#### 3. Video Tools (12+)

Format conversion (MP4 / WebM / MKV / MOV / AVI / GIF), trim, compress, convert to GIF, extract audio (ffmpeg.wasm — in-browser transcoding).

#### 4. JSON Tools (14+)

Format / minify, YAML ↔ JSON, TOML ↔ JSON, JSON ↔ CSV, XML ↔ JSON, JSONPath, JMESPath, diff, JSON → TypeScript / Go / Java / SQL type generation, deep merge.

#### 5. Text Tools (40+)

Case & naming conversion (camelCase / kebab / snake / CONSTANT etc.), line sorting & dedup, word count, regex playground, text diff, Markdown preview, HTML → plain text, indent / unindent, line numbers, fixed-width wrapping, Pinyin, Simplified ↔ Traditional Chinese, masking, Emoji picker, synonyms / antonyms, numeronym, ASCII art, Pangu spacing, template filler, URL defang / refang, sensitive words detection, teleprompter, Chinese character decomposition, URL batch generator, line-length filter, TTS, punctuation conversion, reverse, text → HTML table, special symbols.

#### 6. Encode / Crypto (30+)

Base64 / Base32 / Base58, URL / Hex encoding, HTML entities & JSON escaping, hash (MD5 / SHA-256 etc.), HMAC, AES-256-GCM, RSA-OAEP, Bcrypt, SM2 / SM3 / SM4 (Chinese national standard), DES / 3DES, RC4, XOR, Vigenère, Caesar cipher, RIPEMD-160, CRC32 / BCC / LRC, random password / token, QR encode & decode, Wi-Fi QR, BIP39 mnemonic, RSA keypair, password strength, ISO-8859-1 garbled fix, Emoji encrypt.

#### 7. Web / SEO Tools

Open Graph preview, robots.txt & sitemap generators, CSP builder, Permissions-Policy builder, .env parser, security headers reference, Whois / DNS / ICP lookup, public IP, browser fingerprint, port checker, DNS over HTTPS, URL parser, Punycode, Data URL, MIME cheatsheet, file type sniffing, HTTP status codes reference, User-Agent parser, color converter / contrast checker.

#### 8. Developer Tools (40+)

GraphQL / XML / Nginx formatters, OpenAPI (Swagger) viewer, Properties ↔ JSON, .editorconfig generator, SemVer comparator, Mermaid preview, Docker Run → Compose, regex cheatsheet, fake data generator, code deobfuscation, cURL → code, CSS generators (Box Shadow, Border Radius, Flexbox, Gradient, Animation), color blindness simulator, Protobuf decoder, htpasswd generator, code screenshot, CSR generator, online code playground (HTML / CSS / JS), directory tree generator, KV → code, file hash, endianness converter, ones' complement, SSL certificate generator, PFX → PEM, HTTP request simulator, code formatter.

#### 9. Docs & Productivity (12+)

CSV ↔ Markdown, full-width / half-width, RMB amount in words, iCalendar (.ics) preview, vCard parser, email header parser, Chinese ID-card validation, traditional Chinese colors, kinship calculator, periodic table, grid paper generator, chemical equation balancer.

#### 10. Mini / Utility Tools (60+)

Timestamp converter, UUID / ULID / NanoID generator, date / age calculator, random number / percentage, temperature converter, Roman numerals, unit converter, number base converter, ASCII table, IBAN / Luhn validator, phone number parser, NATO / Morse / Braille codes, barcode / art-QR generator, OTP / TOTP, HTTP Basic Auth, cookie parser, JWT generator / decoder, SVG placeholder, stopwatch, MAC lookup / generator, IPv4 / IPv6 subnet tools, port reference, math expression evaluator, ETA calculator, device info, AI token counter, aspect ratio calculator, loan / mortgage / BMI / tax calculators, work hours calculator, coordinate converter, subtitle format converter, GCD / LCM, scrolling danmaku, batch rename, bankcard BIN, exchange rates, audio editor, torrent analyzer, placeholder image generator, privacy policy generator, pomodoro timer, screen PPI calculator, GB2312 / GBK encoding table, solar-lunar calendar, world clock, mic / keyboard / screen test, doodle board, modular exponentiation, binary reverse, leap year, font preview, clipboard viewer, SVG editor, reaction time test, IPv4↔IPv6 conversion, auto-refresh.

### Highlights

- **Privacy-first**: most tools run entirely in the browser — no file upload required.
- **Multilingual SEO**: every tool ships static pages per language with `hreflang` tags, fully search-engine friendly.
- **Zero backend by default**: the static site works out of the box; only the DocMind proxy is needed for PDF→Word/Excel conversion.
- **Responsive design**: works on desktop and mobile.

---

## Tool Count Overview

| Category | Count |
|---|---|
| PDF Tools | 26+ |
| JSON Tools | 14+ |
| Text Tools | 40+ |
| Image Tools | 30+ |
| Video Tools | 12+ |
| Encode / Crypto | 30+ |
| Web / SEO | 20+ |
| Developer Tools | 40+ |
| Docs & Productivity | 12+ |
| Utility Tools | 60+ |
| **Total** | **~300+** |
