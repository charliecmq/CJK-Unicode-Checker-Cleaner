# CJK Unicode Checker & Cleaner

🔗 **Live App:** [charliecmq.github.io/CJK-Unicode-Checker-Cleaner](https://charliecmq.github.io/CJK-Unicode-Checker-Cleaner/)

## 📌 Overview

CJK Unicode Checker & Cleaner is a single, fully self-contained static web tool for inspecting and cleaning CJK (Chinese, Japanese, Korean) and mixed text that contains problematic or invisible Unicode characters. Paste text into the browser, review what the tool detects, apply the cleaning rules you need, and copy or download the cleaned result.

The entire app runs in the browser from one HTML file. There is no backend, no build step, no external dependencies, and no network calls, so your text never leaves your device.

## 🎯 Features

### Detection & Analysis

- **Unique Anomalies Summary** — a quick overview of the problematic characters detected in the input.
- **Visual Character Inspector** — see each character rendered so hidden or unusual ones become obvious.
- **Character Breakdown Table** — a per-character breakdown with filters for *All*, *CJK / Native*, *Invisible & Spaces*, and *Issues Only*, plus *Show All Rows* and *Clear Highlight* controls.
- **Normalization reference** — shows the **NFC Equivalent** and **NFKC Equivalent** for characters that have a code point.

### Cleaner Rules & Normalization

Each rule is toggleable, and a **Reset Defaults** button restores the standard configuration:

- **Remove Invisible & Zero-Width Chars** — strips ZWSP, ZWNJ, ZWJ, BOM (U+FEFF), Soft Hyphen, and control characters, while keeping `\n`, `\r`, and `\t`.
- **Normalize Unusual Spaces** — converts NBSP (U+00A0) and Ideographic Space (U+3000) to a standard ASCII space.
- **Full-width ASCII & Punctuation → Half-width** — converts full-width ASCII and punctuation to their half-width forms.
- **Half-width Kana** — handles half-width kana characters.
- **Fix Kangxi Radicals & CJK Compatibility** — maps Kangxi radicals and CJK compatibility forms to their normal CJK equivalents.
- **Unicode Normalization** — choose **NFC** or **NFKC**.

### Input & Output

- An **Input Text** box and a **Cleaned Output** box side by side.
- Output actions: **Copy Cleaned**, **Download .txt**, and **Replace Input**.

## 🛠️ Tools & Technologies

- **HTML, CSS & JavaScript** — a single self-contained static page
- **Unicode normalization** — NFC and NFKC equivalence via the browser's built-in support
- **Client-side only** — no backend, no build step, no external dependencies, and no network calls

## 🚀 How to Use

1. Open the [live app](https://charliecmq.github.io/CJK-Unicode-Checker-Cleaner/) in any modern browser, or open the HTML file locally.
2. Paste or type your text into the **Input Text** box.
3. Review the **Unique Anomalies Summary**, **Visual Character Inspector**, and **Character Breakdown Table** to see what was detected. Use the table filters to focus on invisible characters, CJK characters, or issues only.
4. Toggle the **Cleaner Rules & Normalization** options you need, and pick NFC or NFKC normalization. Use **Reset Defaults** to return to the standard configuration.
5. Read the result in the **Cleaned Output** box, then **Copy Cleaned**, **Download .txt**, or **Replace Input** to continue cleaning.

## ⚠️ Limitations

The tool runs entirely in the browser and relies on the browser's Unicode support, so results can vary slightly between browsers. It is intended for inspecting and cleaning text rather than validating language-specific orthography, and it does not store or transmit any of the text you enter.

## 🗄️ Repository Contents

- `index.html` — the single self-contained static page that is the entire app (served as the site root by the live URL).
- `README.md` — project documentation.
- `LICENSE` — license terms for this repository (MIT-style).

## 👤 Author

**Chin Mun Qin**

Developed as a client-side web tool for inspecting and cleaning CJK and mixed Unicode text.
