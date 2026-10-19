# Assets

The portrait is powered by one file.

| File | Used by | Notes |
|------|---------|-------|
| `headshot.png` | Hero portrait | Optional transparent PNG of Gaurav. It sits on the themed frame with a soft accent glow and a bottom fade so it blends into the dark theme. Add a cutout with this exact name to show a photo. If it's missing, a "GM" monogram shows automatically. |

To generate a cutout from a source photo (requires `rembg`):

```bash
python3 -c "from rembg import remove; from PIL import Image; \
im=Image.open('source.png').convert('RGBA'); out=remove(im); \
out.crop(out.getbbox()).save('assets/headshot.png')"
```
