# Cross Stitch

A browser-based image tool that turns pictures into soft, raised cross stitches. The interface is in English and adapts to desktop, tablet, and mobile screens.

## Getting started

Open `index.html` in a modern browser. No installation, build step, server, or API key is required. Images are processed locally in your browser.

1. Click **Upload image** or drag an image onto the upload area.
2. Adjust stitch size, thread thickness, and yarn softness.
3. Fine-tune the natural texture settings.
4. Optionally remove a plain background.
5. Choose an export format and resolution, then download the result.

## Controls

| Control | Effect |
| --- | --- |
| Stitch size | Smaller values preserve more image detail; larger values create a coarser pattern. |
| Thread thickness | Changes the width of the yarn strokes. |
| Yarn softness | Adds fine fibers and softer edges. |
| Handmade variation | Adds subtle differences in stitch position and thickness. |
| Thread tone variation | Adds small color differences between stitches. |
| Thread depth | Changes shading and the raised appearance of the yarn. |
| Matte finish | Reduces highlights for a softer finish. |
| Remove background | Removes the selected background color and leaves transparent gaps between stitches. |
| Background | Choose a color using the swatch or enter a six-digit HEX code. |
| Removal tolerance | Controls how closely colors must match the selected background color to be removed. |

Background removal is color-based, not AI subject segmentation. Matching colors inside the subject can also be removed. It works best with plain backgrounds.

## Preview navigation

- Use **+** and **−**, or the mouse wheel, to zoom from 100% to 800%.
- Drag the image while zoomed in to pan.
- Double-click to switch between the fitted view and 200% zoom.
- Select **Fit** to return to the fitted view.

The zoom toolbar sits at the bottom-right of the canvas. Desktop settings scroll independently; mobile settings appear below the canvas.

## Export

- **PNG:** lossless output with transparency.
- **JPEG:** compressed output with a white background.
- **WebP:** compressed output with transparency, where supported by the browser.
- **Resolution:** choose 1×, 2×, 3×, or 4×. Stitches are redrawn at the selected resolution.
- **Quality:** controls JPEG and WebP compression; it does not affect PNG.

Input images are resized to at most 1,600 pixels on the longest side for processing. Exports are limited to 8,192 pixels per side and 32 megapixels. Higher export resolutions improve the rendered thread detail; they do not restore detail absent from the source image. Browser format support and memory limits may vary.

## Implementation

The application uses plain HTML, CSS, JavaScript, and Canvas 2D. All application code is bundled in `index.html`. There are no external runtime dependencies. Uploaded images are held in memory and are not uploaded to a server. Reloading the page clears the uploaded image.
