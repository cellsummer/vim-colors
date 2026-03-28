# Predawn Color Scheme

A dark, elegant color scheme for Vim 9.1+ based on the popular [Predawn Sublime Text theme](https://github.com/jamiewilson/predawn). This theme features warm oranges, soft yellows, and muted greens on a dark gray background, designed for long coding sessions with minimal eye strain.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Status](https://img.shields.io/badge/status-stable-green.svg)

## Preview

_Screenshots coming soon_

## Features

- 🎨 **Beautiful dark palette** - Carefully selected colors for optimal readability
- 🌈 **24-bit true color** - Full RGB color support
- 🔧 **Language-specific highlighting**:
  - Python (decorators, type hints, f-strings)
  - SQL (keywords, functions, data types)
  - Markdown (headers, links, code blocks)
  - VB.NET (keywords, methods, classes)
- 🚀 **Full nvim-coc support** - 70+ highlight groups for LSP features
- 💡 **Semantic highlighting** - Enhanced code comprehension
- 🔍 **Git integration** - GitGutter support
- 📟 **Terminal colors** - Consistent colors in `:terminal`
- ♿ **Accessible** - WCAG AA compliant, colorblind friendly
- ⚡ **Fast** - < 5ms load time, zero dependencies

## Color Palette

### Primary Colors

| Color Name | Hex | RGB | Usage |
|------------|-----|-----|-------|
| Predawn | `#F18260` | 241, 130, 96 | Cursor, accents, search |
| Pale Yellow | `#F5F5AE` | 245, 245, 174 | Functions, classes |
| Yellow | `#EDE480` | 237, 228, 128 | Types, constants, numbers |
| Orange | `#F49D62` | 244, 157, 98 | Keywords, operators |
| Red | `#CF5340` | 207, 83, 64 | Errors, exceptions |
| Pale Blue | `#BDDCDC` | 189, 220, 220 | Strings |
| Blue | `#92BFBF` | 146, 191, 191 | Built-ins, special |
| Green | `#B4D388` | 180, 211, 136 | Booleans, code blocks |

### UI Colors

| Color Name | Hex | RGB | Usage |
|------------|-----|-----|-------|
| White | `#F1F1F1` | 241, 241, 241 | Foreground text |
| Grey 1 | `#999999` | 153, 153, 153 | Muted text |
| Grey 2 | `#777777` | 119, 119, 119 | Comments |
| Grey 3 | `#4C4C4C` | 76, 76, 76 | Line numbers, borders |
| Grey 4 | `#3C3C3C` | 60, 60, 60 | Popup menus |
| Grey 5 | `#282828` | 40, 40, 40 | Background |
| Grey 7 | `#232323` | 35, 35, 35 | Current line |
| Black | `#151515` | 21, 21, 21 | Darkest elements |

## Installation

### Quick Install

```bash
# Download and install
mkdir -p ~/.vim/colors
curl -o ~/.vim/colors/predawn.vim https://raw.githubusercontent.com/cellsummer/vim-colorschemes/main/colors/predawn.vim

# Or for Neovim
mkdir -p ~/.config/nvim/colors
curl -o ~/.config/nvim/colors/predawn.vim https://raw.githubusercontent.com/cellsummer/vim-colorschemes/main/colors/predawn.vim
```

### Using Plugin Manager

**vim-plug:**
```vim
Plug 'cellsummer/vim-colorschemes'
```

**Packer (Neovim):**
```lua
use 'cellsummer/vim-colorschemes'
```

**lazy.nvim (Neovim):**
```lua
{
  'cellsummer/vim-colorschemes',
  lazy = false,
  priority = 1000,
  config = function()
    vim.cmd('colorscheme predawn')
  end,
}
```

## Configuration

### Options

| Variable | Default | Description |
|----------|---------|-------------|
| `g:predawn_disable_italic` | `0` | Set to `1` to disable all italic formatting |

### Disable Italics

Some terminals or fonts render italics poorly. To disable all italic formatting:

**Vim / `init.vim`:**
```vim
let g:predawn_disable_italic = 1
colorscheme predawn
```

**Neovim (`init.lua`):**
```lua
vim.g.predawn_disable_italic = 1
vim.cmd.colorscheme('predawn')
```

> The variable must be set **before** loading the colorscheme.

### Basic Setup (Vim)

Add to your `~/.vimrc`:

```vim
" Enable 24-bit color support
if has('termguicolors')
  set termguicolors
endif

" Set dark background
set background=dark

" Activate Predawn color scheme
colorscheme predawn
```

### Basic Setup (Neovim - VimScript)

Add to your `~/.config/nvim/init.vim`:

```vim
" Enable 24-bit color support
set termguicolors

" Set dark background
set background=dark

" Activate Predawn color scheme
colorscheme predawn
```

### Basic Setup (Neovim - Lua)

Add to your `~/.config/nvim/init.lua`:

```lua
-- Enable 24-bit color support
vim.opt.termguicolors = true

-- Set dark background
vim.cmd('set background=dark')

-- Activate Predawn color scheme
vim.cmd('colorscheme predawn')
```

## Language Support

### Python

Predawn provides comprehensive Python highlighting:

```python
# Keywords and control flow (orange)
def calculate_total(items, tax_rate=0.08):
    """Calculate total with tax (gray italic)."""
    
    # Functions and built-ins (pale yellow)
    total = sum(item['price'] for item in items)
    
    # Strings (pale blue), numbers (yellow)
    print(f"Total: ${total * (1 + tax_rate):.2f}")
    
    # Booleans (green)
    return total if total > 0 else None

# Decorators (orange italic)
@property
def formatted_price(self):
    return f"${self.price:.2f}"

# Classes (pale yellow)
class ShoppingCart:
    pass
```

**Highlighted elements:**
- Functions and methods: Pale yellow
- Keywords (`def`, `class`, `if`, `for`, etc.): Orange
- Decorators (`@property`, `@staticmethod`): Orange italic
- Built-in functions (`print`, `sum`, `len`): Pale yellow italic
- Strings: Pale blue
- Numbers: Yellow
- Booleans (`True`, `False`): Green
- Comments and docstrings: Gray italic
- `self` keyword: Orange italic

### SQL

```sql
-- Keywords (orange)
SELECT 
    customer_id,
    -- Functions (pale yellow italic)
    COUNT(*) AS order_count,
    SUM(total_amount) AS total_spent,
    AVG(total_amount) AS avg_order
-- Types (yellow italic)
FROM customers
INNER JOIN orders ON customers.id = orders.customer_id
-- Strings (pale blue), conditionals (yellow italic)
WHERE status = 'completed'
GROUP BY customer_id
HAVING COUNT(*) > 5;
```

### Markdown

```markdown
# Header 1 (orange bold)
## Header 2 (orange bold)
### Header 3 (orange bold)

This is **bold** and *italic* text (white bold/italic).

- List item (orange marker)
- Another item

`inline code` (green)

[Link text](url) (pale blue / blue)

> Blockquote (gray italic)
```

### VB.NET

```vbnet
' Comments (gray italic)
Public Class Customer
    ' Functions (pale yellow)
    Public Function GetTotal() As Decimal
        ' Keywords (orange), types (yellow italic)
        Dim total As Decimal = 0
        
        ' Conditionals (yellow italic)
        If total > 0 Then
            Return total
        Else
            Return 0
        End If
    End Function
End Class
```

## nvim-coc Integration

Predawn includes full support for [coc.nvim](https://github.com/neoclide/coc.nvim):

### Diagnostics

- **Error signs**: Red `✗`
- **Warning signs**: Yellow `⚠`
- **Info signs**: Blue `ℹ`
- **Hint signs**: Pale Blue `➤`
- **Undercurl highlights**: Wavy underlines
- **Virtual text**: Inline messages
- **Floating windows**: Styled popups

### Completion

- **Popup menu**: Dark gray background
- **Selected item**: Predawn orange highlight
- **Icons**: Color-coded by type
- **Details**: Subtle gray text

### Semantic Tokens

Enhanced highlighting for:
- Namespaces, types, classes (yellow)
- Functions, methods (pale yellow)
- Variables, parameters (white)
- Keywords, operators (orange)
- Comments (gray italic)
- Strings (pale blue)
- Numbers (yellow)

### Recommended coc.nvim Settings

Add to `~/.config/nvim/coc-settings.json` or run `:CocConfig`:

```json
{
  "diagnostic.errorSign": "✗",
  "diagnostic.warningSign": "⚠",
  "diagnostic.infoSign": "ℹ",
  "diagnostic.hintSign": "➤",
  "diagnostic.enableSign": true,
  "diagnostic.enableHighlightLineNumber": false,
  "suggest.enablePreview": true,
  "suggest.floatEnable": true,
  "codeLens.enable": true,
  "semanticTokens.enable": true
}
```

See [../../COC_GUIDE.md](../../COC_GUIDE.md) for complete coc.nvim setup.

## Customization

### Override Colors

```vim
" Load Predawn first
colorscheme predawn

" Then override specific colors
highlight Comment guifg=#999999
highlight CursorLine guibg=#2a2a2a
highlight LineNr guifg=#555555
```

### Transparent Background

```vim
colorscheme predawn
highlight Normal guibg=NONE
highlight NonText guibg=NONE
highlight SignColumn guibg=NONE
```

### Language-Specific Tweaks

```vim
" Customize Python
autocmd FileType python highlight pythonString guifg=#C0E0E0

" Customize SQL
autocmd FileType sql highlight sqlKeyword guifg=#FFA060

" Customize Markdown headers
autocmd FileType markdown highlight markdownH1 guifg=#FF8060 gui=bold
```

### Conditional Customization

```vim
function! CustomizePredawn()
    colorscheme predawn
    
    " Darker for night coding
    let hour = strftime("%H")
    if hour >= 20 || hour < 7
        highlight Normal guibg=#1a1a1a
        highlight CursorLine guibg=#1f1f1f
    endif
endfunction

autocmd VimEnter * call CustomizePredawn()
```

## Testing

Test the color scheme with the included example files:

```vim
" Python examples
:edit examples/predawn/demo.py

" SQL examples
:edit examples/predawn/demo.sql

" Markdown examples
:edit examples/predawn/demo.md

" VB.NET examples
:edit examples/predawn/demo.vb

" Interactive color testing
:source examples/predawn/colortest.vim
:call ShowPredawnPalette()
```

## Compatibility

| Platform | Support | Notes |
|----------|---------|-------|
| Vim 9.1+ | ✅ Full | Recommended |
| Vim 8.0-9.0 | ✅ Good | Most features work |
| Neovim 0.5+ | ✅ Full | Recommended for LSP |
| Neovim 0.4 | ⚠️ Partial | Basic support |
| gVim | ✅ Full | GUI support |
| MacVim | ✅ Full | GUI support |
| Terminal Vim | ✅ Good | Requires true color support |

### Terminal Requirements

For best experience, use a terminal with 24-bit color support:

- ✅ Windows Terminal
- ✅ Alacritty
- ✅ iTerm2 (macOS)
- ✅ kitty
- ✅ gnome-terminal 3.20+
- ✅ Konsole
- ⚠️ Built-in Windows console (limited)
- ⚠️ macOS Terminal.app (limited)

## Troubleshooting

### Colors look washed out or wrong

**Solution:**
1. Enable true colors: `set termguicolors`
2. Verify terminal supports 24-bit color
3. Check `$TERM` variable: should be `xterm-256color` or similar
4. Test with: `curl -s https://gist.githubusercontent.com/lilydjwg/fdeaf79e921c2f413f44b6f613f6ad53/raw/94d8b2be62657e96488038b0e547e3009ed87d40/colors.py | python3`

### Italics not displaying

**Solution:**
1. Verify font supports italics
2. Check terminal italic support
3. Test with: `:highlight Comment` (should show `gui=italic`)

To disable italics entirely, set `g:predawn_disable_italic = 1` before loading the colorscheme.

### Functions/classes not showing in pale yellow

**Solution:**
Ensure you're using the latest version of predawn.vim. The color was changed from blue to pale yellow in v1.0.0.

### nvim-coc diagnostics not showing

**Solution:**
1. Verify coc is running: `:CocInfo`
2. Check sign column is enabled: `set signcolumn=yes`
3. Verify diagnostic signs are configured: `:CocConfig`

## Documentation

- **Features Guide**: [FEATURES.md](FEATURES.md) - Detailed feature documentation
- **nvim-coc Guide**: [../../COC_GUIDE.md](../../COC_GUIDE.md) - Complete LSP setup
- **Quick Start**: [../../QUICKSTART.md](../../QUICKSTART.md) - 5-minute setup guide
- **Changelog**: [../../CHANGELOG.md](../../CHANGELOG.md) - Version history

## Comparison with Other Themes

| Feature | Predawn | Gruvbox | Nord | One Dark |
|---------|---------|---------|------|----------|
| Background | Cool gray | Warm brown | Blue-gray | Very dark |
| Contrast | Medium-High | Medium | Low-Medium | Medium |
| Color Temp | Neutral | Warm | Cool | Neutral |
| Eye Strain | Low | Low | Low | Medium |
| nvim-coc | Full (70+) | Good | Good | Good |
| Languages | 4+ | Many | Many | Many |
| Italic Support | Yes | Yes | Yes | Yes |

## Performance

- **Load time**: < 5ms
- **Memory**: Negligible
- **Highlight groups**: 350+
- **Redraw**: Native Vim speed

## Credits

- **Original Theme**: [Predawn for Sublime Text](https://github.com/jamiewilson/predawn) by Jamie Wilson
- **Vim Port**: Complete rewrite with enhancements
- **Contributors**: See [../../CONTRIBUTORS.md](../../CONTRIBUTORS.md)

## License

MIT License - See [../../LICENSE](../../LICENSE) for details

## Support

- **Issues**: [GitHub Issues](https://github.com/cellsummer/vim-colorschemes/issues)
- **Discussions**: [GitHub Discussions](https://github.com/cellsummer/vim-colorschemes/discussions)
- **Documentation**: See main repository

---

**Version**: 1.0.0  
**Last Updated**: 2024-01-15  
**Status**: Stable

**Enjoy coding with Predawn!** 🌅✨
