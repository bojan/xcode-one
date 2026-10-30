# One Dark & One Light themes for Xcode

A port of the original [Atom One Dark](https://github.com/atom/one-dark-syntax) and [Atom One Light](https://github.com/atom/one-light-syntax) syntax themes (MIT) for Xcode, with fresh gradient variants for Xcode 27.

Each Xcode version gets its own set. Install only the set for your version.

> [!NOTE]
> This repository provides both dark and light themes, but Xcode does not switch between them automatically. To change, set Appearance to Light or Dark in Settings → Appearance, then choose the matching theme under Theme → Choose….

## Xcode 27 (Modern)

Install the `.xcworkspacecolortheme` files:

| Dark | Light |
| --- | --- |
| One Dark | One Light |
| One Dark Plum | One Light Plum |
| One Dark Indigo | One Light Indigo |
| One Dark Aurora | One Light Aurora |

One Dark and One Light are the ports of the Atom themes, with a flat background. Plum, Indigo and Aurora are new variants, not from Atom: the same colors on a gradient background. For slides and screen sharing, use Presentation mode in Settings → Fonts.

Xcode 27 themes do not contain fonts. The themes were designed with SF Mono Regular and italic comments, which you can set in Settings → Fonts.

## Xcode 26 and earlier (Classic)

Install the `.xccolortheme` files:

- One (Dark)
- One (Light)
- One Presentation (Dark)
- One Presentation (Light)

They use SF Mono Regular (Italic for comments), which ships with macOS and Xcode.

## Installation

Copy the files for your version (see above) to:

```sh
~/Library/Developer/Xcode/UserData/FontAndColorThemes
```

If the folder doesn't exist, create it manually. Xcode 27 picks the files up right away. Xcode 26 and earlier need a restart. Then choose the theme in Settings → Themes.

## License

[WTFPL](LICENSE)
