# Predawn - Quick Start Guide

Get up and running with the Predawn color scheme in under 5 minutes!

## 🚀 Installation

### Option 1: Manual Install (Recommended for first-time users)

**For Vim:**
```bash
mkdir -p ~/.vim/colors
cd ~/.vim/colors
curl -O https://raw.githubusercontent.com/cellsummer/vim-predawn/main/colors/predawn.vim
```

**For Neovim:**
```bash
mkdir -p ~/.config/nvim/colors
cd ~/.config/nvim/colors
curl -O https://raw.githubusercontent.com/cellsummer/vim-predawn/main/colors/predawn.vim
```

### Option 2: Using vim-plug

Add to your `~/.vimrc` or `~/.config/nvim/init.vim`:

```vim
Plug 'cellsummer/vim-predawn'
```

Then run:
```vim
:PlugInstall
```

### Option 3: Using the Install Script

```bash
git clone https://github.com/cellsummer/vim-predawn.git
cd vim-predawn
chmod +x install.sh
./install.sh
```

## ⚙️ Configuration

### For Vim

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

### For Neovim (VimScript)

Add to your `~/.config/nvim/init.vim`:

```vim
" Enable 24-bit color support
set termguicolors

" Set dark background
set background=dark

" Activate Predawn color scheme
colorscheme predawn
```

### For Neovim (Lua)

Add to your `~/.config/nvim/init.lua`:

```lua
-- Enable 24-bit color support
vim.opt.termguicolors = true

-- Set dark background
vim.cmd('set background=dark')

-- Activate Predawn color scheme
vim.cmd('colorscheme predawn')
```

## ✅ Verify Installation

1. **Restart Vim/Neovim** or source your config:
   ```vim
   :source ~/.vimrc    " For Vim
   :source ~/.config/nvim/init.vim    " For Neovim
   ```

2. **Check the color scheme**:
   ```vim
   :colorscheme
   ```
   Should display: `predawn`

3. **Test the colors** - Open any source file and verify:
   - Comments appear in gray italic
   - Strings appear in pale blue
   - Keywords appear in orange
   - Functions appear in blue

## 🎨 Quick Test

Create a test file to see the colors in action:

```vim
:edit ~/test.py
```

Paste this Python code:

```python
# This is a comment (gray, italic)
def hello_world(name):
    """A simple function (gray, italic)"""
    message = f"Hello, {name}!"  # String (pale blue)
    return message

if __name__ == "__main__":
    result = hello_world("Predawn")
    print(result)
```

You should see:
- 🟦 **Blue**: `hello_world`, `print`
- 🟧 **Orange**: `def`, `if`, `return`
- 🟦 **Pale Blue**: `"Hello, {name}!"`, `"Predawn"`
- 🟨 **Yellow**: `__name__`, `__main__`
- ⚪ **Gray italic**: Comments and docstrings

## 🔧 Optional: nvim-coc Integration

If you use coc.nvim for auto-completion and LSP:

1. **Install coc.nvim** (if not already installed):
   ```vim
   Plug 'neoclide/coc.nvim', {'branch': 'release'}
   ```

2. **Configure diagnostic signs** - Run `:CocConfig` and add:
   ```json
   {
     "diagnostic.errorSign": "✗",
     "diagnostic.warningSign": "⚠",
     "diagnostic.infoSign": "ℹ",
     "diagnostic.hintSign": "➤"
   }
   ```

3. **See the full guide**: [COC_GUIDE.md](COC_GUIDE.md)

## 📚 Next Steps

- **Customize colors**: See [FEATURES.md](FEATURES.md#customization)
- **Language-specific features**: See [README.md](README.md#language-support)
- **Advanced configuration**: See [COC_GUIDE.md](COC_GUIDE.md)
- **View examples**: Check the `examples/` directory

## 🐛 Troubleshooting

### Colors look wrong or washed out

**Solution**: Enable true color support in your terminal and Vim/Neovim.

```vim
" Add to your .vimrc or init.vim
set termguicolors
```

**Check your terminal**: Most modern terminals support true colors. Recommended:
- **Windows**: Windows Terminal, Alacritty
- **macOS**: iTerm2, Alacritty, kitty
- **Linux**: Alacritty, kitty, gnome-terminal 3.20+

### Color scheme not loading

**Solution**: Verify the file is in the correct location:

```vim
" Check if Vim can find the color scheme
:echo globpath(&rtp, 'colors/predawn.vim')
```

Should return the path to `predawn.vim`. If empty, the file is not in your runtime path.

### Colors don't match the screenshots

**Solution**: 
1. Ensure `termguicolors` is enabled
2. Check terminal color settings (disable any overrides)
3. Verify you're using the latest version of Predawn

### Comments not showing italic

**Solution**: Your terminal might not support italic text.

Test with:
```vim
:highlight Comment
```

Try a different terminal emulator or font that supports italics.

## 📖 Learn More

- Full documentation: [README.md](README.md)
- Feature list: [FEATURES.md](FEATURES.md)
- coc.nvim setup: [COC_GUIDE.md](COC_GUIDE.md)
- Report issues: [GitHub Issues](https://github.com/cellsummer/vim-predawn/issues)

---

**Enjoy coding with Predawn!** 🌅

If you like this color scheme, please ⭐ star the repository!
