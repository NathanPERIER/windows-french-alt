
# Windows French alternative keyboard

If you are French and you use the default AZERTY keyboard layout featured in most Windows installations, you might have noticed this it is quite minimalist. You do get quick access to almost all the letters you need on a day-to-day basis, but there are exceptions. The most notable ones are accented capital letters (É, È, À, ...) and ligatures (œ, æ, ...), although these are required in some contexts and the spell checker will blame you if you substitute them for other characters available by default.

The next best option is to use alt-codes, like `Alt + 144` which prints an `É`. This sure does work but is arguably not a very good interface for humans...

This situation is kind of a shame because Windows does support `Ctrl + AltGr` key combinations, but these are literally not used at all on the default French AZERTY layout. This is why we made this simple custom layout, based on the default one.

## Additions

### Accented letters

| Key combination   | Character |
|-------------------|-----------|
| Shift + AltGr + é | `É`       |
| Shift + AltGr + è | `È`       |
| Shift + AltGr + ç | `Ç`       |
| Shift + AltGr + à | `À`       |
| Shift + AltGr + ù | `Ù`       |

### Ligatures

| Key combination   | Character |
|-------------------|-----------|
| AltGr + A         | `æ`       |
| Shift + AltGr + A | `Æ`       |
| AltGr + O         | `œ`       |
| Shift + AltGr + O | `Œ`       |

## Requirements

In order to make this into an actual keyboard configuration, you must use [Miscrosoft Keyboard Layout Creator (MSKLC)](https://www.microsoft.com/en-us/download/details.aspx?id=102134).

Note that this is quite an old software, which requires [.NET 3.5](https://www.microsoft.com/en-us/download/details.aspx?id=21) to work.

## Build and install

In KLMC, click on `File > Load Source File` and select `fr-alt.klc`. Then, use `Project > Build DLL and Setup Package` to generate the layout.

This will create a folder named `fr-altNN` (`NN` being the version number) in Documents. Inside, you will find an installer named `setup.exe` that you can run to install the layout. This will only add the keyboard as an option to the fr-FR locale, which means you should probably remove the default French keyboard from the options if you don't want to risk switching by accident (`Settings` > `Time & Language` > `Language & Regions`).

