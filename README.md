# MD3 Palette Comparator

A one-page tool for generating and fine-tuning color palettes in Google's Material Design 3 (MD3) system.

## 🚀 [Launch MD3 Palette Tool](https://jsethcreates.github.io/web-tool-md3-palette-lab/)
![MD3 Palette Tool Screenshot](https://raw.githubusercontent.com/JSethCreates/web-tool-md3-palette-lab/main/assets/demo.PNG)

---

## 🎨 Purpose

This tool allows you to explore and compare how MD3 color logic behaves when generated **manually using HCT rules** versus **automatically via Google's Material Color Utilities (MCU)**.



## 🧠 Google's Light and Dark Color Generation - Material Color Utilities (MCU)

Google's MCU uses your source ARGB color to generate a full **101-tone HCT palette** for that hue (tones 0–100). This tonal palette:
- Maintains **consistent hue**
- Dynamically adjusts **chroma per tone**
- Ensures **contrast/legibility**

### Example Tone Assignments in MD3 (Light Scheme):
- `primary` = tone 40 from accent
- `onPrimary` = tone 100
- `primaryContainer` = tone 90
- `onPrimaryContainer` = tone 10
- `secondary` = tone 40 from secondary accent
- `tertiary` = tone 40 from a tertiary accent
- `surface` = tone 99
- `onSurface` = tone 10

Google provides a system-wide mapping table assigning tones to every `md-sys-color-*` role, sometimes with adjusted hues (e.g., for neutral-variant tones).

---

🧪 Material Design Schemes (MCU Presets)  
Material Design 3 offers multiple dynamic color schemes — each a strategy for how to use your seed color to generate themed palettes. These schemes determine not just tones and chroma, but how neutral or expressive the result feels.

#### 🔁 Available Schemes

| **Scheme Name** | **Description** |
|-----------------|-----------------|
| `Custom HCT`    | Uses your local manual logic based on HCT hue/chroma/tone settings. Great for exploring alternative interpretations. |
| `Tonal Spot`    | Google’s default scheme, used on Pixel devices. Balanced and elegant. |
| `Expressive`    | Injects bold, vibrant color choices into the UI. Higher chroma and lively contrast. |
| `Vibrant`       | Even more saturated than Expressive — ideal for colorful UIs or branding-heavy designs. |
| `Fidelity`      | Stays extremely close to the seed color — prioritizing hue accuracy over balance. |
| `Content`       | Optimized for content-rich UIs like media or reading apps — focuses on legibility and neutrality. |
| `Monochrome`    | Uses tone-only variation with almost no chroma — excellent for minimalist, grayscale designs. |
| `Rainbow`       | For experimental or playful use: assigns different hues across roles to maximize diversity. |
| `Fruit Salad`   | Another fun, thematic option with playful chromatic shifts (as the name implies). |

Each of these schemes interprets the seed color differently — whether to preserve hue fidelity, amp up saturation, reduce visual noise, or add vibrancy.

---

## 🔍 HCT Color Generation Scheme- Local Logic

### Primary
Generated using the seed hue with **high chroma (e.g. 48)** and a **mid-dark tone (e.g. 40)**. This produces a vivid, deep version of the base color.

### Secondary
Uses the **same hue** but with **lower chroma (e.g. 16)** at the **same tone (40)**, yielding a more muted companion.

### Tertiary
Shifts the hue by **+60°** (moving one “segment” on the color wheel), with **moderate chroma (e.g. 24)** at **tone 40**. This provides a harmonizing accent.

### Neutral & Neutral-Variant
Generated using low-chroma HCT colors at tone 40:
- **Neutral**: chroma ≈ 4
- **Neutral-variant**: chroma ≈ 8
- Includes a very dark neutral for "on-surface" tokens

These serve as grayish supporting tones.

---

## ✅ Contrast Assurance

The MCU algorithm adjusts chroma dynamically to ensure each tone passes WCAG contrast ratios, creating **accessible, balanced palettes** by design.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
