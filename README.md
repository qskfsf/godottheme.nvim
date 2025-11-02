---

# GodotTheme.nvim

<p align="center">
  <img src="./demo3.png" alt="Preview" />

  <br>

  <img src="https://img.shields.io/badge/Neovim-0.8+-green.svg" />
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" />
  <img src="https://img.shields.io/badge/Lua-5.1%2B-blue.svg" />
  <img src="https://img.shields.io/badge/Maintained-Yes-success.svg" />

  <img src="https://img.shields.io/github/stars/Rehd0/godottheme.nvim?style=social" />
  <img src="https://img.shields.io/github/forks/Rehd0/godottheme.nvim?style=social" />
  <img src="https://img.shields.io/github/issues/Rehd0/godottheme.nvim.svg" />
  <img src="https://img.shields.io/github/issues-pr/Rehd0/godottheme.nvim.svg" />
  <img src="https://img.shields.io/github/last-commit/Rehd0/godottheme.nvim.svg" />

  <img src="https://img.shields.io/badge/packer.nvim-supported-brightgreen.svg" />
  <img src="https://img.shields.io/badge/lazy.nvim-supported-brightgreen.svg" />
  <img src="https://img.shields.io/badge/Tree--sitter-supported-brightgreen.svg" />
  <img src="https://img.shields.io/badge/LSP-highlights-blue.svg" />

  <img src="https://img.shields.io/badge/Code%20Style-LuaFormatter-lightgrey.svg" />
  <img src="https://img.shields.io/badge/Contributions-welcome-orange.svg" />
  <img src="https://badges.frapsoft.com/os/v3/open-source.svg?v=103" />
</p>

---


A **modern, Godot-inspired Neovim color theme** written in Lua.  
This theme emphasizes readability, clear syntax highlighting, and deep integration with **Treesitter**, **CMP popup menus**, and **Coc.nvim** for a polished coding experience.

---

## Features

- Fully designed for **Neovim 0.8+** with Lua configuration.
- **Godot-inspired color palette** with rich contrasts and soft backgrounds.
- Deep **Treesitter support** for syntax highlighting.
- Highlighting for:
  - Strings, numbers, booleans, keywords, operators, functions, and types.
  - HTML, CSS, PHP, JS, and other front-end languages.
- **Autocomplete / Popup menu (CMP & Coc.nvim) support**.
- **Cursor line, Visual selection, TabLine, WinSeparator, StatusLine** styling.
- Support for **indent guides** and **Treesitter context**.

---

### Screenhots
![Preview](./demo1.png)
![Preview](./demo4.png)

---

## Installation

### Using [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
{
  "yourusername/godottheme.nvim",
  config = function()
    require('godot').setup()
  end
}
```

Using packer.nvim
```lua
use {
  "yourusername/godottheme.nvim",
  config = function()
    require('godot').setup()
  end
}
```
Using vim-plug
```vim
Plug 'Rehd0/godottheme.nvim'
```


Manual Installation

Clone the repository into your ~/.config/nvim/lua folder:

git clone https://github.com/Rehd0/godottheme.nvim.git

Then add this to your init.lua or colors/godot.lua:

```lua
require('godot').setup()
```

---

Usage

After setup, set your colorscheme:

```vim
:colorscheme godot
```
---


Customization

You can customize the theme by overriding colors or highlight groups in your setup() call.

```lua
require('godot').setup({
    colors = {
        bg = "#1D2229",
        fg = "#DDDFE7",
        yellow = "#F4E39A",
        red = "#FF7A9F",
        green = "#9AEED7",
        -- ... override any color
    },
    highlights = {
        Normal = { fg = "#DDDFE7", bg = "#1D2229" },
        Comment = { fg = "#51545A", italic = true },
        -- ... override any highlight
    }
})
```

> Tip: Only override the colors or groups you want to change; the rest will use the default Godot palette.




---

Supported Highlight Groups


Core groups:

Normal, Comment, Keyword, String, Number, Boolean, Function, Type, Operator, Delimiter, Statement, Conditional, Exception, Call


Treesitter:

@function.call, @function.builtin, @keyword.conditional, @keyword.exception, @type.builtin, @string.special.url


UI / Plugins:

CMP: Pmenu, PmenuSel, PmenuSbar, PmenuThumb, PmenuKind, PmenuExtra

Coc.nvim: CocMenuSel, CocFloating, CocPumMenu, CocSearch

Status line: StatusLine, TabLine, TabLineSel

Visual / Cursor: Visual, CursorLine

Treesitter context: TreesitterContext, TreesitterContextLineNumber

Indent guides: IblScope

---



<h2 align="center">Color Palette</h2>

<p align="center">
  <table align="center">
    <tr>
      <th>Name</th>
      <th>Color</th>
      <th>Hex</th>
      <th>Usage</th>
    </tr>
    <tr><td>bg</td><td><span style="background-color:#1D2229; color:#1D2229;">███</span></td><td>#1D2229</td><td>Background</td></tr>
    <tr><td>fg</td><td><span style="background-color:#DDDFE7; color:#DDDFE7;">███</span></td><td>#DDDFE7</td><td>Foreground / Text</td></tr>
    <tr><td>yellow</td><td><span style="background-color:#F4E39A; color:#F4E39A;">███</span></td><td>#F4E39A</td><td>Strings, highlights</td></tr>
    <tr><td>red</td><td><span style="background-color:#FF7A9F; color:#FF7A9F;">███</span></td><td>#FF7A9F</td><td>Keywords, booleans</td></tr>
    <tr><td>green</td><td><span style="background-color:#9AEED7; color:#9AEED7;">███</span></td><td>#9AEED7</td><td>Numbers, types</td></tr>
    <tr><td>darkGreen</td><td><span style="background-color:#6CC068; color:#6CC068;">███</span></td><td>#6CC068</td><td>Preprocessor, accents</td></tr>
    <tr><td>typeGreen</td><td><span style="background-color:#5EF5CA; color:#5EF5CA;">███</span></td><td>#5EF5CA</td><td>Built-in types</td></tr>
    <tr><td>blue</td><td><span style="background-color:#AAC9FE; color:#AAC9FE;">███</span></td><td>#AAC9FE</td><td>Operators, delimiters</td></tr>
    <tr><td>flowerBlue</td><td><span style="background-color:#A3A3F5; color:#A3A3F5;">███</span></td><td>#A3A3F5</td><td>Built-in functions</td></tr>
    <tr><td>funcCallBlue</td><td><span style="background-color:#1E90FF; color:#1E90FF;">███</span></td><td>#1E90FF</td><td>Function calls</td></tr>
    <tr><td>pink</td><td><span style="background-color:#FF8CCC; color:#FF8CCC;">███</span></td><td>#FF8CCC</td><td>Conditionals, exceptions</td></tr>
    <tr><td>gray</td><td><span style="background-color:#51545A; color:#51545A;">███</span></td><td>#51545A</td><td>Comments</td></tr>
    <tr><td>lightGray</td><td><span style="background-color:#2D3238; color:#2D3238;">███</span></td><td>#2D3238</td><td>Cursor line, context</td></tr>
    <tr><td>cyan</td><td><span style="background-color:#5ECFE7; color:#5ECFE7;">███</span></td><td>#5ECFE7</td><td>Functions</td></tr>
    <tr><td>errorRed</td><td><span style="background-color:#613C3D; color:#613C3D;">███</span></td><td>#613C3D</td><td>Error background</td></tr>
    <tr><td>errorYellow</td><td><span style="background-color:#3E3E32; color:#3E3E32;">███</span></td><td>#3E3E32</td><td>Warning background</td></tr>
    <tr><td>transparentBlue</td><td><span style="background-color:#3F5E7C; color:#3F5E7C;">███</span></td><td>#3F5E7C</td><td>Visual / Search</td></tr>
    <tr><td>lightTheme</td><td><span style="background-color:#353D4A; color:#353D4A;">███</span></td><td>#353D4A</td><td>TabLine / StatusLine</td></tr>
  </table>
</p>

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.  
© Rehd0

---


