# scratch-buf

A simple plugin to provide a scratch buffer for jotting down random notes in NeoVim while you're doing other things. The plugin will open a new vertical or horizontal split with a buffer named `*scratch-buffer*`, and a `txt` filetype.

Written in Lua for Neovim.

## Features

- Opens a new buffer in a new vertical or horizontal split window.
- Automatically switch to an existing scratch buffer if it's already open.
- Scratch buffers are ephemeral, and not backed up to a file.

## Installation

Install as you would any other plugin NeoVim.

### [lazy](https://github.com/folke/lazy.nvim)

```lua
{
  "adudenamedruby/scratch-buf",
  lazy = true,
  keys = {
    { "<leader>bs", "<cmd>ScratchVSplit<cr>", desc = "scratch buffer (vertical)", mode = "n" },
    { "<leader>bS", "<cmd>ScratchHSplit<cr>", desc = "scratch buffer (horizontal)", mode = "n" },
  },
  cmd = {
    "ScratchVSplit",
    "ScratchHSplit",
  },
  opts = {},
}
```

## Usage

### Commands

The plugin provides two commands:

- `:ScratchVSplit` — Opens or switches to the scratch buffer in a vertical window.
- `:ScratchHSplit` — Opens or switches to the scratch buffer in a horizontal window.

### Lua Functions

You can also use the plugin's Lua functions directly:

- `require('scratch-buf').vertical()` — Equivalent to `:ScratchVSplit`.
- `require('scratch-buf').horizontal()` — Equivalent to `:ScratchHSplit`.

## License

[MIT License](LICENSE)

## Contributing

Contributions are always welcome! Feel free to open issues or submit pull requests.
