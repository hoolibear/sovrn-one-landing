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

`token/` holds the SVO token icon: Solomon's head with the LED mouth lit, as on the Talk to Solomon page, on a white
disc with a black border, on a black square (`#000`, the page background of explorer.imd.fun).

| File | Use |
| --- | --- |
| `svo-icon-1024.png`, `-512`, `-256`, `-128` | The icon. Square; the disc is centred in it and the head is centred in the disc. |
| `solomon-head.png` | The head alone, transparent background, 771 px. |
| `icon-source.html` | What the icon is rendered from. |

Measurements at 1024 px: the disc is 920 px across (52 px of black on every side, its outer 12 px a black border), and
the head's visible pixels are centred on the square's centre, 130 px from the left and right edges and 139 px from the
top and bottom.

To render again, with Chrome:

```sh
chrome --headless=new --force-device-scale-factor=1 --window-size=1024,1024 --screenshot=svo-icon-1024.png token/icon-source.html
```
