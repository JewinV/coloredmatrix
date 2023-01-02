# Colored Matrix
![GitHub](https://img.shields.io/github/license/JewinV/colored-console)

A Python library for changing the colors in the terminal using ANSI escape codes.

## Installation
To install Colored Matrix, use **`pip`**:
```bash
pip install coloredmatrix
```

## Usage
To use Colored Matrix, import the Stylize class and the Color constants, and call the desired methods on a Stylize object:
```py
from coloredmatrix import Stylize, Color

# Set the background color to green
print(Stylize("hello").bg_color(Color.Green))

# Set the background color to red
print(Stylize("hello").bg_color(Color.Red))

# Set the background color to green and the foreground color to red
print(Stylize("hello").bg_color(Color.Green).fg_color(Color.Red))

# Set the text to bold and underlined
print(Stylize("hello").bold().underline())

```
You can also pass an RGB color tuple to the bg_color and fg_color methods:
```py
from coloredmatrix import Stylize

# Set the background color to red using an RGB color tuple
print(Stylize("hello").bg_color((255, 0, 0)))

# Set the background color to green using an RGB color tuple
print(Stylize("hello").bg_color((0, 255, 0)))

# Set the background color to red and the foreground color to green using RGB color tuples
print(Stylize("hello").bg_color((255, 0, 0)).fg_color((0, 255, 0)))
```

## Text Styling

The `Stylize` class provides the following methods for styling text:

- `bold`: Makes the text bold
- `italic`: Makes the text italic
- `underline`: Underlines the text
- `blink`: Makes the text blink
- `strike`: Strikes through the text

You can chain these methods to apply multiple styles to the same text. For example:

```python
from coloredmatrix import Stylize

# Set the text to bold, italic, and underlined
print(Stylize("hello").bold().italic().underline())

# Set the text to blink and struck through
print(Stylize("hello").blink().strike())
```

## Troubleshooting

If you are having trouble using coloredmatrix in Windows, there are a few things you can try to troubleshoot the issue:
- Make sure that your system supports ANSI escape codes. Some older versions of Windows may not support ANSI escape codes, which are used by coloredmatrix to change the colors in the terminal.
- Enable virtual terminal processing. In some versions of Windows, you may need to enable virtual terminal processing in order for ANSI escape codes to work. To do this, you can try adding the VirtualTerminalLevel registry key under the `HKEY_CURRENT_USER\console` key.

To do this, open the command prompt or PowerShell with administrative privileges and run the following command:
```cmd
reg add "HKEY_CURRENT_USER\console" /v "VirtualTerminalLevel" /t REG_DWORD /d 1
```


## Supported Colors
You can also use RGB color tuples to specify any other color.
<br>The `Color` constants define the following colors:
| Color Name          | Color Name          | Color Name          | Color Name          | Color Name          |
| ------------------- | ------------------- | ------------------- | ------------------- | ------------------- |
| MediumVioletRed     | DeepPink            | PaleVioletRed       | HotPink             | LightPink           |
| Pink                | DarkRed             | Red                 | Firebrick           | Crimson             |
| IndianRed           | LightCoral          | Salmon              | DarkSalmon          | LightSalmon         |
| OrangeRed           | Tomato              | DarkOrange          | Coral               | Orange              |
| DarkKhaki           | Gold                | Khaki               | PeachPuff           | Yellow              |
| PaleGoldenrod       | Moccasin            | PapayaWhip          | LightGoldenrodYellow| LemonChiffon        |
| LightYellow         | Maroon              | Brown               | SaddleBrown         | Sienna              |
| Chocolate           | DarkGoldenrod       | Peru                | RosyBrown           | Goldenrod           |
| SandyBrown          | Tan                 | Burlywood           | Wheat               | NavajoWhite         |
| Bisque              | BlanchedAlmond      | Cornsilk            | Indigo              | Purple              |
| DarkMagenta         | DarkViolet          | DarkSlateBlue       | BlueViolet          | DarkOrchid          |
| Fuchsia             | Magenta             | SlateBlue           | MediumSlateBlue     | MediumOrchid        |
| MediumPurple        | Orchid              | Violet              | Plum                | Thistle             |
| Lavender            | MidnightBlue        | Navy                | DarkBlue            | MediumBlue          |
| Blue                | RoyalBlue           | SteelBlue           | DodgerBlue          | DeepSkyBlue         |
| CornflowerBlue      | SkyBlue             | LightSkyBlue        | LightSteelBlue      | LightBlue           |
| PowderBlue          | Teal                | DarkCyan            | LightSeaGreen       | CadetBlue           |
| DarkTurquoise       | MediumTurquoise     | Turquoise           | Aqua                | Cyan                |
| Aquamarine          | PaleTurquoise       | LightCyan           | DarkGreen           | Green               |
| DarkOliveGreen      | ForestGreen         | SeaGreen            | Olive               | OliveDrab           |
| MediumSeaGreen      | LimeGreen           | Lime                | SpringGreen         | MediumSpringGreen   |
| DarkSeaGreen        | MediumAquamarine    | YellowGreen         | LawnGreen           | Chartreuse          |
| LightGreen          | GreenYellow         | PaleGreen           | MistyRose           | AntiqueWhite        |
| Linen               | Beige               | WhiteSmoke          | LavenderBlush       | OldLace             |
| AliceBlue           | Seashell            | GhostWhite          | Honeydew            | FloralWhite         |
| Azure               | MintCream           | Snow                | Ivory               | White               |
| Black               | DarkSlateGray       | DimGray             | SlateGray           | Gray                |
| LightSlateGray      | DarkGray            | Silver              | LightGray           | Gainsboro           |


## License
License
Colored Matrix is released under the MIT License. See the **LICENSE** file for more information.
