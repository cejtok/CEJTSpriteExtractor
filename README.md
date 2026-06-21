# CEJTSpriteExtractor

Static web application for detecting sprites inside a transparent spritesheet, organizing them into groups, and exporting them as PNG images inside a ZIP file.

## Features

- Load spritesheets from a local image.
- Automatically detect sprites using non-transparent pixels.
- Display the spritesheet with rectangles over the detected sprites.
- Create, edit, and delete sprite groups.
- Select sprites by clicking their detected rectangles.
- Animated preview of the selected group.
- Global export options.
- Custom export options per group:
  - Target width.
  - Target height.
  - Horizontal padding.
  - Vertical padding.
  - Rotation or flipping.
- ZIP export for created groups only.
- Language selector: Spanish and English.

## Usage

1. Open `index.html` in a browser.
2. In the **Spritesheet** section, click **Select file** and load an image.
3. Review the detected rectangles over the spritesheet.
4. In **Groups**, select sprites by clicking their rectangles.
5. Enter a group name.
6. Configure the group's export settings:
   - Use the global options, or
   - Define custom options.
7. Click **Create group**.
8. Repeat the process for additional groups.
9. In **Global export**, adjust the general options if needed.
10. Click **Export groups ZIP**.

## Exported File Names

Each exported sprite uses this format:

```text
groupname_x.png
```

Where `x` is the sprite number within the group's selection.

Example:

```text
walk_1.png
walk_2.png
jump_1.png
```

## Notes

- Detection works best with separated sprites on a transparent background.
- If two sprites touch through opaque pixels, they may be detected as a single sprite.
- If the image contains noise or semi-transparent pixels, extra sprites may be detected.
- The app uses JSZip from a CDN, so ZIP export requires an internet connection unless the library is included locally.

## Author

Carlos Ernesto Jimenez Torres
cejtok@gmail.com
