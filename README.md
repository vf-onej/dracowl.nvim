<h1 align="center" >dracowl.nvim</h1>

<h2> NOTE: This is very much a work in progress currently, and at the moment is heavily pulled from <a href="http://github.com/Mofiqul/dracula.nvim">Dracula.nvim</a> by Mofiqul. You'll probably be happier with his. :)</h2>

<p align="center">A theme for <a href="https://neovim.io/">NEOVIM</a> based on a combination of Dracula and NightOwl</p>

## ✔️ Requirements

- Neovim >= 0.9.2
- Treesitter (optional)


## #️ Supported Plugins

- [LSP](https://github.com/neovim/nvim-lspconfig)
- [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-compe](https://github.com/hrsh7th/nvim-compe)
- [nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [blink.cmp](https://github.com/Saghen/blink.cmp/)
- [Telescope](https://github.com/nvim-telescope/telescope.nvim)
- [NvimTree](https://github.com/kyazdani42/nvim-tree.lua)
- [NeoTree](https://github.com/nvim-neo-tree/neo-tree.nvim)
- [BufferLine](https://github.com/akinsho/nvim-bufferline.lua)
- [Git Signs](https://github.com/lewis6991/gitsigns.nvim)
- [Lualine](https://github.com/hoob3rt/lualine.nvim)
- [LSPSaga](https://github.com/glepnir/lspsaga.nvim)
- [indent-blankline](https://github.com/lukas-reineke/indent-blankline.nvim)
- [nvim-ts-rainbow](https://github.com/p00f/nvim-ts-rainbow)
- [nvim-dap-ui](https://github.com/rcarriga/nvim-dap-ui)
- [mini.indentcope](https://github.com/echasnovski/mini.indentcope)
- [mini.icons](https://github.com/echasnovski/mini.icons)
- [mini.statusline](https://github.com/echasnovski/mini.statusline)

## ⬇️ Installation

Install via package manager

```lua
-- Using Packer:
use 'vf-onej/dracowl.nvim'
```

```vim
" Using Vim-Plug:
Plug 'vf-onej/dracowl.nvim'
```

## 🚀 Usage

```lua
-- Lua:
vim.cmd[[colorscheme dracowl]]
```

```vim
" Vim-Script:
colorscheme dracowl
```

If you are using [`lualine`](https://github.com/hoob3rt/lualine.nvim), you can also enable the provided theme:


```lua
require('lualine').setup {
  options = {
    -- ...
    theme = 'dracowl'
    -- ...
  }
}
```

If you are using [LazyVim](https://github.com/LazyVim/LazyVim), you can add this to your plugins/colorscheme.lua file:
```lua
return {
  -- add dracowl
  { "vf-onej/dracowl.nvim" },

  -- Configure LazyVim to load dracowl
  {
    "LazyVim/LazyVim",
    opts = {
      colorscheme = "dracowl",
    },
  },
}
```

## 🔧 Configuration

The configuration must be run before `colorscheme` command to take effect.

If you're using Lua:

```lua
local dracowl = require("dracowl")
dracowl.setup({
  -- customize dracowl color palette
  colors = {
    bg = "#282A36",
    fg = "#F8F8F2",
    selection = "#44475A",
    comment = "#6272A4",
    red = "#FF5555",
    orange = "#FFB86C",
    yellow = "#F1FA8C",
    green = "#50fa7b",
    purple = "#BD93F9",
    cyan = "#8BE9FD",
    pink = "#FF79C6",
    bright_red = "#FF6E6E",
    bright_green = "#69FF94",
    bright_yellow = "#FFFFA5",
    bright_blue = "#D6ACFF",
    bright_magenta = "#FF92DF",
    bright_cyan = "#A4FFFF",
    bright_white = "#FFFFFF",
    menu = "#21222C",
    visual = "#3E4452",
    gutter_fg = "#4B5263",
    nontext = "#3B4048",
    white = "#ABB2BF",
    black = "#191A21",
  },
  -- show the '~' characters after the end of buffers
  show_end_of_buffer = true, -- default false
  -- use transparent background
  transparent_bg = true, -- default false
  -- set custom lualine background color
  lualine_bg_color = "#44475a", -- default nil
  -- set italic comment
  italic_comment = true, -- default false
  -- overrides the default highlights with table see `:h synIDattr`
  overrides = {},
  -- You can use overrides as table like this
  -- overrides = {
  --   NonText = { fg = "white" }, -- set NonText fg to white
  --   NvimTreeIndentMarker = { link = "NonText" }, -- link to NonText highlight
  --   Nothing = {} -- clear highlight of Nothing
  -- },
  -- Or you can also use it like a function to get color from theme
  -- overrides = function (colors)
  --   return {
  --     NonText = { fg = colors.white }, -- set NonText fg to white of theme
  --   }
  -- end,
})
```

## 🎨 Importing colors for other usage

```lua
local colors = require('dracowl').colors()
```

This will return the following table (`dracowl` palette shown):

![colors](./assets/colors.png)
