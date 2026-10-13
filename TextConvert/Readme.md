# History

Codes copied from https://github.com/bramus/PS_BRAMUS.TextConvert

Original instruction and guideline can be found here:
https://www.bram.us/2008/10/30/ps_bramustextconvert-psd2txt-and-txt2psd-for-the-masses/

# PS_BRAMUS.TextConvert

Export all text strings from a PSD file into a TXT file (PSD2TXT) and import them back (TXT2PSD). It is the successor of `PS_BRAMUS.TextExport` and consists of two scripts:

1. `PS_BRAMUS.TextConvert.Export` (PSD2TXT): scans the PSD for text layers and saves the strings to a TXT file in your Documents folder.
2. `PS_BRAMUS.TextConvert.Import` (TXT2PSD): reads a TXT file previously created by the Export script and replaces the text layer contents in the PSD.

## Use cases

Ideal for translating Photoshop mockups: export the text, send the TXT file to a translation agency, then import the translated file back into the PSD. The Export script can also be used for (speed)slicing.

## Requirements

Tested with Photoshop CS2 and up (Photoshop CC also supported).

## License

MIT license.

## Installation

1. Download from https://github.com/bramus/PS_BRAMUS.TextConvert/releases
2. Extract to the `Presets/Scripts` folder of your Photoshop installation (e.g. `C:\Program Files\Adobe\Adobe Photoshop CS3\Presets\Scripts` on Windows).
3. Restart Photoshop if it was running (important!).

## Usage

### 1. Export text (PSD2TXT)

- In Photoshop go to *File* > *Scripts* and select `PS_BRAMUS.TextConvert.Export-1.0`.
- For each open PSD, a `TextConvert-[NAME_OF_YOUR_PSD_FILE].txt` file is created in your Documents folder. If multiple files are open, you can run it on the active file only or on all files.
- A notification is shown when done (with a single file, the TXT file is opened instead).

### 2. Rework text

- Open the exported TXT file in a text editor and translate the strings.
- Leave the `[BEGIN /XXXX ]` and `[END /XXXX ]` lines untouched, otherwise importing will fail.
- Save the file with the same name in the same location.

### 3. Import text (TXT2PSD)

- In Photoshop go to *File* > *Scripts* and select `PS_BRAMUS.TextConvert.Import-1.0`.
- For each open PSD, the script looks for `TextConvert-[NAME_OF_YOUR_PSD_FILE].txt` in your Documents folder and updates the text layers. If multiple files are open, you can run it on the active file only or on all files.
- A notification shows the number of files updated (0 if no TXT files were found).

## Warnings

- `PS_BRAMUS.TextConvert.Import` is not compatible with any version of `PS_BRAMUS.TextExport`.
- Make **no changes to the PSD file** between running Export and Import.

