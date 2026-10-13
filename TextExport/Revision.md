# 2026/10/13

Photoshop throws error 8800 when a script reads `textItem.capitalization` (and sometimes `color`, `font` or `size`) on certain layers, such as ones with mixed styles. The old check also compared the value to the string "TextCase.NORMAL", which never matched because the value is an enum.

## Changes:

- Each style property is now read inside a try/catch, so one layer with an unreadable property no longer stops the export. An unreadable property is written as an empty value.
- Capitalization is compared against `TextCase.NORMAL`, `TextCase.ALLCAPS` and `TextCase.SMALLCAPS`, and the output is normal, uppercase or smallcaps.
- I also fixed a bug I noticed: `tracking` was printing the `fauxItalic` value. It now prints the real tracking.