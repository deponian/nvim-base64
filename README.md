### Description

Encodes/decodes base64 strings using [lbase64](https://github.com/iskolbin/lbase64) Lua library by Ilya Kolbin.

It doesn't require `base64` utility to be installed on the system.

### Installation

Install via your preferred package manager:
- `deponian/nvim-base64`

You can check current version in [changelog](./CHANGELOG.md) or on [releases page](https://github.com/deponian/nvim-base64/releases).

Example for [lazy](https://github.com/folke/lazy.nvim) package manager:

Import file below or directory it is contained on lazy setup.

```lua
return {
  "deponian/nvim-base64",
  version = "*",
  keys = {
    -- Decode/encode selected sequence from/to base64
    -- (mnemonic: [b]ase64)
    { "<Leader>b", "<Plug>(FromBase64)", mode = "x" },
    { "<Leader>B", "<Plug>(ToBase64)", mode = "x" },
  },
  config = function()
    require("nvim-base64").setup()
  end,
}
```

### Usage

Map `<Plug>(FromBase64)` to decode selected string from base64 and `<Plug>(ToBase64)` to encode it.

```lua
vim.keymap.set('x', "<leader>b", "<Plug>(FromBase64)")
vim.keymap.set('x', "<leader>B", "<Plug>(ToBase64)")
```

or

```vim
vmap <Leader>b <Plug>(FromBase64)
vmap <Leader>B <Plug>(ToBase64)
```

### Acknowledgements

Thanks to Christian Rondeau and his [vim-base64](https://github.com/christianrondeau/vim-base64) plugin that I've been using for the past few years.

Thanks to Ilya Kolbin and his great [lbase64](https://github.com/iskolbin/lbase64) library.
