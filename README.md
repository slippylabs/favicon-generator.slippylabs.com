# Favicon Generator

Build a real multi-resolution favicon.ico from any image, entirely in the browser — hand-written ICO container, per-size previews, PNG export.

**Live:** <https://favicon-generator.slippylabs.com/>

## What it does

- Turn any image into a real multi-resolution `favicon.ico`.
- Fit modes — contain, cover, stretch — plus keep-transparency or fill with a colour.
- Previews every size at actual pixel dimensions, so you see the 16px one honestly.
- Also exports a 512px PNG for manifests.

## How it works

The ICO container is written byte by byte in the browser: an `ICONDIR` header, one `ICONDIRENTRY` per size, and PNG-compressed images packed in at the recorded offsets. No encoder library involved.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/favicon-generator.slippylabs.com.git
cd favicon-generator.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
