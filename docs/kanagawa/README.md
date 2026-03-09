# Kanagawa Color Scheme

A dark, elegant color scheme for Vim 9.1+ inspired by the famous painting "The Great Wave off Kanagawa" by Katsushika Hokusai. This theme features a beautiful palette of deep blues, soft greens, and warm orange-yellow accents that create a serene and focused coding environment.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Status](https://img.shields.io/badge/status-stable-green.svg)

## Overview

Kanagawa brings the tranquility and beauty of traditional Japanese art to your editor, with carefully selected colors that provide excellent readability and aesthetic appeal.

## Color Palette

### Primary Colors

| Element | Color Name | Hex | Usage |
|---------|------------|-----|-------|
| **Background** | sumiInk1 | `#1F1F28` | Default background |
| **Foreground** | fujiWhite | `#DCD7BA` | Default text |
| **Functions** | crystalBlue | `#7E9CD8` | Function names, titles |
| **Keywords** | roninYellow | `#FF9E3B` | Keywords, statements |
| **Strings** | springGreen | `#98BB6C` | String literals |
| **Types** | waveAqua2 | `#7AA89F` | Type definitions |
| **Numbers** | sakuraPink | `#D27E99` | Numeric values |
| **Operators** | boatYellow2 | `#C0A36E` | Operators, regex |
| **Comments** | fujiGray | `#727169` | Comments (italic) |
| **Constants** | surimiOrange | `#FFA066` | Constants, imports, booleans |
| **Errors** | samuraiRed | `#E82424` | Errors, diagnostics |
| **Warnings** | roninYellow | `#FF9E3B` | Warnings |

### Accent Colors

- **Identifiers**: carpYellow (`#E6C384`)
- **Built-ins**: springBlue (`#7FB4CA`)
- **Special**: peachRed (`#FF5D62`)
- **Decorators**: waveRed (`#E46876`)

## Installation

Installation is identical to Predawn. See the [main README](../../README.md) for detailed instructions.

### Quick Install

```bash
# Manual installation
mkdir -p ~/.vim/colors
cp colors/kanagawa.vim ~/.vim/colors/

# Or use the installer
./install.sh
# Select Kanagawa from the menu
```

## Configuration

Add to your `.vimrc` or `init.vim`:

```vim
set termguicolors
set background=dark
colorscheme kanagawa
```

For Neovim with Lua (`init.lua`):

```lua
vim.opt.termguicolors = true
vim.cmd('set background=dark')
vim.cmd('colorscheme kanagawa')
```

## Features

- ✅ **350+ highlight groups** - Comprehensive coverage
- ✅ **Language support** - Python, SQL, Markdown, VB.NET
- ✅ **nvim-coc integration** - Full LSP/diagnostic support (70+ groups)
- ✅ **Semantic highlighting** - Enhanced code comprehension
- ✅ **GitGutter support** - Git diff indicators
- ✅ **Terminal colors** - Consistent palette in `:terminal`
- ✅ **Aesthetic design** - Inspired by Japanese art
- ✅ **WCAG AA compliant** - Accessible contrast ratios
- ✅ **Zero dependencies** - Pure VimScript

## Language Support

### Python
- Functions, classes, decorators highlighted in crystalBlue
- Keywords and statements in roninYellow (warm orange)
- Strings in springGreen
- Built-in functions in springBlue (italic)
- Special variables (self) in waveRed (italic)

### SQL
- Keywords in roninYellow (warm orange)
- Functions in crystalBlue (italic)
- Types in waveAqua2 (italic)
- Strings in springGreen

### Markdown
- Headers in crystalBlue and springBlue
- Code blocks in springGreen
- Links in waveAqua1 and springBlue

### VB.NET
- Full support with Kanagawa color palette

## Design Philosophy

Kanagawa embodies the spirit of traditional Japanese aesthetics:
- **Wabi-sabi**: Beauty in imperfection and subtlety
- **Ma**: Thoughtful use of negative space
- **Shibui**: Simple, subtle, and unobtrusive beauty

The color palette creates a calm, focused environment perfect for long coding sessions while maintaining excellent readability and visual hierarchy.

## Customization

Override specific colors after loading the scheme:

```vim
colorscheme kanagawa

" Example: Adjust comment brightness
highlight Comment guifg=#8A8980

" Example: Transparent background
highlight Normal guibg=NONE
highlight SignColumn guibg=NONE
```

## Comparison with Predawn

| Aspect | Kanagawa | Predawn |
|--------|----------|---------|
| Background | Deep blue-gray | Warm gray |
| Temperature | Cool with warm accents | Neutral-warm |
| Inspiration | Japanese art | Sublime theme |
| Functions | Crystal blue | Pale yellow |
| Keywords | Orange-yellow | Orange |
| Overall Feel | Serene, artistic | Warm, comfortable |

## Credits

- **Inspiration**: "The Great Wave off Kanagawa" by Katsushika Hokusai
- **Original Theme**: Kanagawa.nvim by [rebelot](https://github.com/rebelot)
  - Repository: https://github.com/rebelot/kanagawa.nvim
- **Vim Port**: Adapted for Vim 9.1 with enhancements (violet colors replaced with warm orange-yellow)
- **License**: MIT

## License

MIT License - See [../../LICENSE](../../LICENSE)

---

**Version**: 1.0.0  
**Last Updated**: 2024-01-15  
**Status**: Stable

**Experience the beauty of Kanagawa!** 🌊✨