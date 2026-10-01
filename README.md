# NJU Academic — HorseMD / Typora theme

A calm, paper-first academic theme for Typora/Horse, built around Nanjing University's official purple `#6A005F`.

- Light theme: **NJU Academic**
- Dark theme: **NJU Academic Dark**
- Serif body, sans headings, restrained purple accents
- Academic title page treatment, blockquotes, tables, code, TOC, and print rules
- Includes the official NJU seal as the title ornament

## Install

Download the theme package from the [latest release](https://github.com/zephyrq-z/typora-theme-nju/releases/latest), then:

1. Unzip it and copy the `nju-academic` folder into your Typora/Horse themes directory:
   - HorseMD (macOS): `/Users/<you>/Library/Application Support/horse/themes/`
   - Typora (macOS): `/Users/<you>/Library/Application Support/abnerworks.Typora/themes/`
   - Typora (Windows): `%APPDATA%\Typora\themes\`
   - Typora (Linux): `~/.config/Typora/themes/`
2. Restart Typora/Horse.
3. Select **NJU Academic** or **NJU Academic Dark** from the theme menu.

For local development, keep the folder in this repository and symlink or copy it into the themes directory.

## Follow the system theme

HorseMD does not load custom theme files when its appearance mode is set to **Follow System**. For that mode, use the generated custom CSS snippet instead:

```bash
pbcopy < nju-academic-system.css
```

Then paste it into **Settings → Appearance → Custom CSS** while theme mode is set to **Follow System**.

`nju-academic-system.css` is self-contained:

- base rules provide the light `#EBE7E0` paper;
- `@media (prefers-color-scheme: dark)` re-tunes the same rules for the `#1D1915` night paper;
- the official logo and motto are embedded as data URLs, because custom snippets cannot rely on relative URLs from the themes folder;
- print/export remains light.

Keep `nju-academic.css` and `nju-academic-dark.css` for manual theme selection. Do not put `nju-academic-system.css` inside the HorseMD themes folder; it is intended for the custom CSS editor, not the theme picker.

## Files

- `nju-academic.css` — light theme
- `nju-academic-dark.css` — dark theme
- `nju-academic-system.css` — self-contained custom CSS snippet for Follow System mode
- `assets/nju-logo-combined.png` — combined NJU logo and wordmark
- `assets/nju-motto-purple.png` — purple NJU motto ornament

## Notes

- The body uses serif typography for a paper-like academic feel.
- Headings are sans-serif for clear hierarchy.
- Code, tables, and blockquotes are muted so prose remains the focus.
- Print/export rules strip shadows and decorative chrome.
