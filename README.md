# Vim Dotfiles

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

Two `.vimrc` configurations that cover most environments:

- **Enhanced** — feature-rich for flexible systems (plugins/themes OK).
- **Lite** — minimal, plugin-free for restricted or secure hosts (great over SSH).

---

## Quick Install

### Enhanced (flexible systems)

```bash
curl -fsSL https://robert.bumgarner.org/vimrc/enhanced -o ~/.vimrc
````

### Lite (restricted systems)

```bash
curl -fsSL https://robert.bumgarner.org/vimrc/lite -o ~/.vimrc
```

---

## Keep Both & Switch

```bash
curl -fsSL https://robert.bumgarner.org/vimrc/enhanced -o ~/.vimrc_enhanced
curl -fsSL https://robert.bumgarner.org/vimrc/lite      -o ~/.vimrc_lite

ln -sf ~/.vimrc_enhanced ~/.vimrc   # use enhanced
ln -sf ~/.vimrc_lite ~/.vimrc       # use lite
```

---

## What’s Inside

### Enhanced

* Sensible defaults (UTF-8, relative numbers, 4-space soft tabs).
* Window management mappings and quality-of-life tweaks.
* Guarded plugin integrations (fzf/Rg/NERDTree).
* **Colorscheme:** tries `gruvbox`; falls back to Vim’s `default`.

### Lite

* Same ergonomics but **no plugin assumptions**.
* File browsing via built-in **netrw**.
* Grep using **ripgrep** when available, else pure `:vimgrep`.

---

## Shared Key Mappings (Leader = `<Space>`)

| Mapping                 | Action                            |
| ----------------------- | --------------------------------- |
| `<Space>w`              | Write file (`:w`)                 |
| `<Space>q`              | Quit (`:q`)                       |
| `<Space><Space>`        | Clear search highlight            |
| `<Space>e`              | Open file explorer                |
| `<Space>p`              | Open file (fzf or `:find`)        |
| `<Space>g`              | Project grep (`:Rg` / `:vimgrep`) |
| `<Space>v` / `<Space>s` | Vertical / horizontal split       |
| `<Space>h/j/k/l`        | Move between windows              |
| `<Space>=`              | Equalize windows                  |
| `<Space>-`              | Maximize height                   |
| `<Space>\`              | Maximize width                    |
| `<Space>co`             | Quickfix open                     |
| `<Space>cc`             | Quickfix close                    |
| `<Space>cn`             | Quickfix next                     |
| `<Space>cp`             | Quickfix prev                     |

---

## Troubleshooting

* **Colorscheme not found**: Enhanced config traps errors and falls back to `default`.
* **Reload config**: Run `:source $MYVIMRC` inside Vim.

---

## License

[MIT](./LICENSE) – feel free to adapt for your own use.
