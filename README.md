# One Dark & One Light themes for Xcode

A port of the original [Atom One Dark](https://github.com/atom/one-dark-syntax) and [Atom One Light](https://github.com/atom/one-light-syntax) syntax themes (MIT) for Xcode, with fresh gradient variants for Xcode 27.

The themes come in two file formats: one for Xcode 27 and one for Xcode 26 and earlier. Use the files that match your Xcode.

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

Xcode 27 themes cannot contain fonts. Set SF Mono Regular with italic comments in Settings → Fonts.

## Xcode 26 and earlier (Classic)

Install the `.xccolortheme` files:

- One (Dark)
- One (Light)
- One Presentation (Dark)
- One Presentation (Light)

They use SF Mono Regular with italic comments. SF Mono ships with macOS and Xcode.

## Installation

Copy the files for your version (see above) to:

```sh
~/Library/Developer/Xcode/UserData/FontAndColorThemes
```

If the folder doesn't exist, create it manually. Xcode 27 picks the files up right away. Xcode 26 and earlier need a restart. Then choose the theme in Settings → Themes.

## Original themes

The colors come from the original themes (MIT):

- Atom syntax themes: [One Dark](https://github.com/atom/one-dark-syntax) and [One Light](https://github.com/atom/one-light-syntax)
- Atom UI themes: [One Dark UI](https://github.com/atom/one-dark-ui) and [One Light UI](https://github.com/atom/one-light-ui)
- VS Code ports: [One Dark](https://github.com/akamud/vscode-theme-onedark) and [One Light](https://github.com/akamud/vscode-theme-onelight)

## License

[WTFPL](LICENSE)
