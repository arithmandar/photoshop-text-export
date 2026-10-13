# Photoshop Text Export

A collection of Photoshop (ExtendScript `.jsx`) scripts for extracting text from PSD files.

| Folder | Description |
|--------|-------------|
| [TextExport](./TextExport) | `Text Export.jsx` exports all visible text layers of the open PSD(s) to a text file, including layer path, content and basic font styles (capitalization, color, faux bold/italic, font, size, tracking). Based on `PS_BRAMUS.TextExport`. See its [README](./TextExport/README.md) and [revision history](./TextExport/Revision.md). |
| [TextConvert](./TextConvert) | `PS_BRAMUS.TextConvert` Export/Import scripts: export text to a TXT file (PSD2TXT), edit or translate it, then import it back into the PSD (TXT2PSD). See its [README](./TextConvert/Readme.md). |
| [wow-tool](./wow-tool) | `psd_text_extract.jsx` exports visible text layers as a Lua table of map markers (text, sequence number, X/Y position) for the Atlas addon. See its [README](./wow-tool/Readme.md). |

## Requirements

Adobe Photoshop (the scripts target CS2 and up, including Photoshop CC).

## Installation

1. Copy the `.jsx` script(s) you need to the `Presets/Scripts` folder of your Photoshop installation (e.g. `C:\Program Files\Adobe\Adobe Photoshop <version>\Presets\Scripts`).
2. Restart Photoshop.
3. Run them from *File* > *Scripts*.

Alternatively, run a script without installing via *File* > *Scripts* > *Browse...*.

## Credits

- [PS_BRAMUS.TextExport / TextConvert](https://github.com/bramus/PS_BRAMUS.TextConvert) by Bramus (MIT license)
- [photoshop-scripts](https://github.com/pivanov/photoshop-scripts) by pivanov
