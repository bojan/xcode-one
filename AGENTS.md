# Agent notes

Color themes for Xcode, ported from Atom's One Dark and One Light. There is no build step: the theme files in the repository root are edited directly.

## Layout

- `*.xccolortheme`: Classic themes for Xcode 26 and earlier. Named in Apple's pattern, `One (Dark)`, `One (Light)`, `One Presentation (Dark)`, `One Presentation (Light)`.
- `*.xcworkspacecolortheme`: Modern themes for Xcode 27. `One Dark`, `One Light`, and the gradient variants `Plum`, `Indigo`, `Aurora` in both schemes (`One Dark Plum`, `One Light Aurora`, and so on).
- One file holds one color scheme. A file cannot contain both dark and light, and Xcode does not switch themes automatically. Do not try `colorScheme: "adaptive"` or a combined file: Xcode ignores or rejects both.

## Colors

- The base colors are Atom's originals. One Light's are verified against `atom/one-light-syntax` and `akamud/vscode-theme-onelight`. Do not darken or "improve" them without being asked.
- Hex values are the source of truth. One Dark: background `282c34`, text `abb2bf`, keyword `c678dd`, string `98c379`, number `d19a66`, function `61afef`, type `e5c07b`, variable `e06c75`, cyan `56b6c2`, comment `5c6370`. One Light: background `fafafa`, text `383a42`, keyword `a626a4`, string `50a14f`, number `986801`, function `4078f2`, type `c18401`, variable `e45649`, cyan `0184bc`, comment `a0a1a7`.

## Classic format

- Colors are `"r g b a"` floats and are plain sRGB (hex ÷ 255). Apple's own Default (Dark) keyword is `0.988394 0.37355 0.638329`, which is `#FC5FA3`.
- A theme must keep every key of Apple's built-in Default theme (`DVTFontAndColorVersion`, the scrollbar markers, `declaration.*`, `mark` and `markup.*` syntax keys). Missing keys fall back to Apple's colors. `Exectuable` in the console keys is Apple's own spelling.
- One font scheme for all four: SF Mono Regular 13 (console 12, Presentation 18), Semibold keywords, Bold marks and doc keywords, Regular Italic comments, Light Italic doc comments.

## Modern format

- JSON recipe. Colors are OKLCH (`lightness`, `chroma`, `hue.radians`, `gamut: "P3"`). To convert a hex color: sRGB to linear, then to OKLab with Björn Ottosson's matrices, then to polar.
- `recipe.background` is `gradient`. Xcode derives the background from `palette.primary` and `palette.secondary` (a hue in radians and an intensity from 0 to 1). The mapping from hue to rendered color is not predictable, so judge in Xcode. A custom background color renders solid.
- Below about 0.3 intensity the background is plain gray; Plum is 0.5, Indigo 0.6. Light Aurora is 0.3 because stronger cyan clips and shows no gradient.
- The current line and selection on gradient themes are translucent overlays (dark: `#99bbff` at 6% and white at 14.5%; light: the text color at 5% and 12%), so the gradient shows through. The flat themes use flat colors.
- Modern themes contain no fonts or italics. Those live in Xcode's `DVTWorkspaceGlobalFontRecipe` preference. There are no Presentation themes: Xcode 27 has a Presentation mode toggle.

## Testing

- Themes load from `~/Library/Developer/Xcode/UserData/FontAndColorThemes`. Xcode 27 reloads them immediately. Xcode 26 needs a restart, and macOS may block opening it by double-click: run `Contents/MacOS/Xcode` directly.
- Do not delete files in that folder that you did not put there.
- Compare colors by sampling screenshots, not by eye. Xcode's picker only shows themes of the current appearance's scheme.
