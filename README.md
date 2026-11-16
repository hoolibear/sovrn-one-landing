# Sovrn.One landing page

A static, single-file copy of the top section of [sovrn.one](https://sovrn.one): the SVO hero.

- `index.html`: the whole page, styles inline, no build step and no JavaScript.
- `banner.jpg`: the hero background.
- `icon.png`, `apple-icon.png`: favicons.

The buttons link to the live site:

| Button | Goes to |
| --- | --- |
| Stake | https://sovrn.one/stake |
| Buy / Swap | https://sovrn.one/swap |
| Talk to Solomon | https://sovrn.one/ai/coach |

Open `index.html` in a browser, or host the folder on any static host (GitHub Pages, Netlify, Vercel, S3).
Fonts (Audiowide, Rubik) load from Google Fonts. Light and dark follow the visitor's system setting.

## Token icon

`token/` holds the SVO token icon: Solomon's head with the LED mouth lit, as on the Talk to Solomon page, on the brand navy.

| File | Use |
| --- | --- |
| `svo-icon-1024.png`, `-512`, `-256`, `-128` | Square, full-bleed background. For token lists and explorers that crop to a circle themselves. The head sits inside the circle, so nothing is cut off. |
| `svo-icon-round-1024.png`, `-512`, `-256`, `-128` | Already cropped to a circle, transparent corners. |
| `solomon-head.png` | The head alone, transparent background, 771 px. |
| `icon-source.html` | What the icons are rendered from. |

To render again, with Chrome:

```sh
chrome --headless=new --force-device-scale-factor=1 --window-size=1024,1024 --screenshot=svo-icon-1024.png token/icon-source.html
chrome --headless=new --force-device-scale-factor=1 --window-size=1024,1024 --default-background-color=00000000 --screenshot=svo-icon-round-1024.png "token/icon-source.html?round"
```
