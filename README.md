# Vesper Themes

Community ports of the [Vesper](https://github.com/raunofreiberg/vesper) dark theme by [Rauno Freiberg](https://github.com/raunofreiberg) for terminal tools.

Peppermint and orange flavored.

## Ports

| Tool | Repository |
| ---- | ---------- |
| [bat](https://github.com/sharkdp/bat) | [vesper-bat](https://github.com/adriandlam/vesper-bat) |
| [fzf](https://github.com/junegunn/fzf) | [vesper-fzf](https://github.com/adriandlam/vesper-fzf) |
| [delta](https://github.com/dandavison/delta) | [vesper-delta](https://github.com/adriandlam/vesper-delta) |
| [eza](https://github.com/eza-community/eza) | [vesper-eza](https://github.com/adriandlam/vesper-eza) |
| [atuin](https://github.com/atuinsh/atuin) | [vesper-atuin](https://github.com/adriandlam/vesper-atuin) |

## bat

TextMate theme (`.tmTheme`) for bat and Sublime Text.

![bat](https://raw.githubusercontent.com/adriandlam/vesper-bat/main/preview.png)

And with fzf:

![bat + fzf](https://raw.githubusercontent.com/adriandlam/vesper-bat/main/preview-fzf.png)

```sh
# Copy theme and rebuild cache
cp Vesper.tmTheme "$(bat --config-dir)/themes/"
bat cache --build

# Use it
bat --theme=Vesper file.txt
```

Or add to your bat config (`bat --config-file`):

```
--theme="Vesper"
```

## fzf

Sourceable `--color` config for fzf.

![fzf](https://raw.githubusercontent.com/adriandlam/vesper-fzf/main/preview.png)

```sh
# Source it
source /path/to/vesper-fzf/vesper.sh
```

Or copy the `--color` string directly into your `FZF_DEFAULT_OPTS`:

```sh
export FZF_DEFAULT_OPTS="$FZF_DEFAULT_OPTS \
  --color=bg+:#2a2a2a,bg:#101010,spinner:#99ffe4,hl:#ffc799 \
  --color=fg:#ffffff,header:#505050,info:#505050,pointer:#99ffe4 \
  --color=marker:#99ffe4,fg+:#ffffff,prompt:#ffc799,hl+:#ffc799 \
  --color=selected-bg:#2a2a2a,border:#2a2a2a,gutter:#101010"
```

## delta

Includable gitconfig for the delta diff viewer.

![delta](https://raw.githubusercontent.com/adriandlam/vesper-delta/main/preview.png)

```gitconfig
[include]
  path = /path/to/vesper-delta/vesper.gitconfig
```

Or copy the `[delta]` section from [`vesper.gitconfig`](https://github.com/adriandlam/vesper-delta/blob/main/vesper.gitconfig) into your `~/.gitconfig`.

## eza

Full `theme.yml` with file type, permission, and git colors.

![eza](https://raw.githubusercontent.com/adriandlam/vesper-eza/main/preview.png)

```sh
mkdir -p ~/.config/eza
cp theme.yml ~/.config/eza/theme.yml
```

## atuin

Theme TOML for the atuin shell history TUI.

![atuin](https://raw.githubusercontent.com/adriandlam/vesper-atuin/main/preview.png)

```sh
mkdir -p ~/.config/atuin/themes
cp vesper.toml ~/.config/atuin/themes/vesper.toml
```

Add to `~/.config/atuin/config.toml`:

```toml
[theme]
name = "vesper"
```

## Color Palette

| Role        | Hex       | Preview |
| ----------- | --------- | ------- |
| Background  | `#101010` | ![#101010](https://via.placeholder.com/12/101010/101010.png) |
| Foreground  | `#CCCCCC` | ![#CCCCCC](https://via.placeholder.com/12/CCCCCC/CCCCCC.png) |
| Strings     | `#99FFE4` | ![#99FFE4](https://via.placeholder.com/12/99FFE4/99FFE4.png) |
| Keywords    | `#FFC799` | ![#FFC799](https://via.placeholder.com/12/FFC799/FFC799.png) |
| Comments    | `#7D7D7D` | ![#7D7D7D](https://via.placeholder.com/12/7D7D7D/7D7D7D.png) |
| Errors      | `#FF8080` | ![#FF8080](https://via.placeholder.com/12/FF8080/FF8080.png) |
| Operators   | `#65737E` | ![#65737E](https://via.placeholder.com/12/65737E/65737E.png) |
| Functions   | `#FFFFFF` | ![#FFFFFF](https://via.placeholder.com/12/FFFFFF/FFFFFF.png) |

## Credits

Based on the [Vesper](https://github.com/raunofreiberg/vesper) VS Code theme by [Rauno Freiberg](https://github.com/raunofreiberg).

## License

[MIT](LICENSE)
