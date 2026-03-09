# Vim Color Schemes Collection

A curated collection of beautiful, carefully crafted color schemes for Vim 9.1+ and Neovim, optimized for modern development workflows with full LSP and nvim-coc support.

![Vim Version](https://img.shields.io/badge/vim-9.1%2B-green.svg)
![Neovim Version](https://img.shields.io/badge/neovim-0.5%2B-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🎨 Available Color Schemes

### Predawn
A dark, elegant theme based on the popular Sublime Text Predawn theme. Features warm oranges, cool blues, and muted greens on a dark gray background.

- **Style**: Dark, warm
- **Best for**: Long coding sessions, low eye strain
- **Accent**: Predawn orange (`#F18260`)
- **Language Support**: Python, SQL, Markdown, VB.NET
- **Special Features**: Full nvim-coc integration, semantic highlighting
- **Status**: ✅ Stable (v1.0.0)

[View Predawn Details →](docs/predawn/README.md)

---

### Kanagawa

A dark, elegant theme inspired by the famous painting "The Great Wave off Kanagawa". Features a beautiful palette of deep blues, soft greens, and warm orange-yellow accents on a dark background.

- **Style**: Dark, cool blues with warm orange-yellow accents
- **Best for**: Aesthetic appeal, balanced contrast, focused coding
- **Accent**: Crystal blue (`#7E9CD8`) and Ronin yellow (`#FF9E3B`)
- **Language Support**: Python, SQL, Markdown, VB.NET
- **Special Features**: Full nvim-coc integration, semantic highlighting, distinctive warm and cool color balance
- **Status**: ✅ Stable (v1.0.0)

[View Kanagawa Details →](docs/kanagawa/README.md)

---

### Coming Soon
- **Predawn Light** - Light variant of Predawn
- **Additional themes** - More color schemes in development

## 📦 Quick Installation

### Option 1: Install All Schemes

```bash
# Clone the repository
git clone https://github.com/cellsummer/vim-colorschemes.git

# Run the installation script
cd vim-colorschemes
chmod +x install.sh
./install.sh
```

### Option 2: Manual Installation (Single Scheme)

**For Vim:**
```bash
mkdir -p ~/.vim/colors
cp colors/predawn.vim ~/.vim/colors/
```

**For Neovim:**
```bash
mkdir -p ~/.config/nvim/colors
cp colors/predawn.vim ~/.config/nvim/colors/
```

### Option 3: Plugin Manager

#### vim-plug
```vim
Plug 'cellsummer/vim-colorschemes'
```

#### Packer (Neovim)
```lua
use 'cellsummer/vim-colorschemes'
```

#### lazy.nvim (Neovim)
```lua
{
  'cellsummer/vim-colorschemes',
  lazy = false,
  priority = 1000,
}
```

## ⚙️ Configuration

Add to your `.vimrc` or `init.vim`:

```vim
" Enable 24-bit color support
if has('termguicolors')
  set termguicolors
endif

" Set background
set background=dark

" Choose your color scheme
colorscheme predawn
```

For Neovim with Lua (`init.lua`):

```lua
-- Enable 24-bit color support
vim.opt.termguicolors = true

-- Set background
vim.cmd('set background=dark')

-- Choose your color scheme
vim.cmd('colorscheme predawn')
```

## 🚀 Features

### Common Features (All Schemes)

- ✅ **24-bit true color support** - 16.7 million colors
- ✅ **Zero dependencies** - Pure VimScript implementation
- ✅ **Fast loading** - < 5ms load time
- ✅ **LSP/nvim-coc support** - Full diagnostic and semantic highlighting
- ✅ **Extensive language support** - Python, SQL, Markdown, VB.NET, and more
- ✅ **Git integration** - GitGutter support
- ✅ **Terminal colors** - Consistent colors in `:terminal`
- ✅ **Accessibility** - WCAG AA compliant, colorblind friendly
- ✅ **Comprehensive docs** - Detailed guides and examples

### Scheme-Specific Features

Each color scheme includes:
- 350+ highlight groups
- Language-specific optimizations
- Semantic token highlighting
- Complete nvim-coc integration
- Example files for testing
- Customization guides

## 📚 Documentation

### General Documentation
- [Quick Start Guide](QUICKSTART.md) - Get started in 5 minutes
- [Installation Guide](INSTALL.md) - Detailed installation instructions
- [nvim-coc Setup](COC_GUIDE.md) - Complete LSP configuration guide
- [Contributing](CONTRIBUTING.md) - How to contribute new schemes

### Scheme-Specific Documentation
- [Predawn Guide](docs/predawn/README.md)
- [Predawn Features](docs/predawn/FEATURES.md)
- [Predawn Examples](examples/predawn/)

## 🎯 Language Support

All color schemes support:
- **Python** - Full syntax highlighting, decorators, type hints
- **SQL** - All keywords, functions, data types
- **Markdown** - Headers, links, code blocks, tables
- **VB.NET** - Keywords, methods, classes, operators
- **JavaScript/TypeScript** - Modern syntax support
- **And many more...**

## 🔧 Customization

Each color scheme can be customized to your preferences:

```vim
" Load your preferred scheme
colorscheme predawn

" Override specific colors
highlight Comment guifg=#999999
highlight CursorLine guibg=#2a2a2a

" Language-specific customization
autocmd FileType python highlight pythonString guifg=#add8e6
```

See individual scheme documentation for detailed customization options.

## 🧪 Testing

Each color scheme includes comprehensive test files:

```vim
" Open test files to preview colors
:edit examples/predawn/demo.py
:edit examples/predawn/demo.sql
:edit examples/predawn/demo.md
:edit examples/predawn/demo.vb

" Interactive color testing
:source examples/predawn/colortest.vim
```

## 📊 Comparison

| Feature | Predawn | Predawn Light |
|---------|---------|---------------|
| Background | Dark | Light |
| Contrast | Medium-High | Medium |
| Eye Strain | Low | Low |
| nvim-coc | Full | Full |
| Languages | 4+ | 4+ |
| Status | Stable | Coming Soon |

## 🤝 Contributing

We welcome contributions! You can help by:

- 🎨 **Adding new color schemes**
- 🌍 **Adding language support**
- 📝 **Improving documentation**
- 🐛 **Reporting bugs**
- ⭐ **Sharing feedback**

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding new color schemes.

## 📋 Requirements

- **Vim**: 9.1+ (recommended), 8.0+ (compatible)
- **Neovim**: 0.5+ (recommended for full features)
- **Terminal**: 24-bit color support recommended
- **Optional**: nvim-coc for LSP features

### Recommended Terminal Emulators

- **Windows**: Windows Terminal, Alacritty
- **macOS**: iTerm2, Alacritty, kitty
- **Linux**: Alacritty, kitty, gnome-terminal 3.20+

## 🐛 Troubleshooting

### Colors look wrong
1. Enable true color support: `set termguicolors`
2. Verify terminal supports 24-bit color
3. Check `:highlight` output

### Scheme not loading
1. Verify file location: `:echo globpath(&rtp, 'colors/*.vim')`
2. Check for errors: `:messages`
3. Reload: `:colorscheme predawn`

See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for more help.

## 📜 License

MIT License - See [LICENSE](LICENSE) file for details.

Each color scheme may have additional attributions listed in its specific documentation.

## 🙏 Credits

### Color Schemes

- **Predawn**: Based on [Predawn for Sublime Text](https://github.com/jamiewilson/predawn) by Jamie Wilson
  - Vim port with enhancements for Vim 9.1+
- **Kanagawa**: Based on [Kanagawa.nvim](https://github.com/rebelot/kanagawa.nvim) by rebelot
  - Inspired by "The Great Wave off Kanagawa" by Katsushika Hokusai
  - Vim port with warm color enhancements (violet replaced with orange-yellow)

### Project

- **Project Maintainers**: See [CONTRIBUTORS.md](CONTRIBUTORS.md)
- **Community**: Thanks to all contributors and users!

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/cellsummer/vim-colorschemes/issues)
- **Discussions**: [GitHub Discussions](https://github.com/cellsummer/vim-colorschemes/discussions)
- **Documentation**: See `docs/` directory

## 🗺️ Roadmap

- [ ] Predawn Light variant
- [ ] Additional color schemes (Nord-inspired, Gruvbox-inspired, etc.)
- [ ] Treesitter integration
- [ ] vim-airline themes
- [ ] lightline.vim themes
- [ ] More language support (Rust, Go, Java, TypeScript, C/C++)
- [ ] Interactive theme customizer
- [ ] Color palette generator

## ⭐ Star History

If you find these color schemes useful, please star the repository!

---

**Current Version**: 1.0.0  
**Last Updated**: 2024-01-15  
**Status**: Active Development

**Enjoy beautiful syntax highlighting!** 🎨✨
