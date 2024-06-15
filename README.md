# My python projects

## 開発

[Context: "https://rye.astral.sh/guide/basics/"]

### Ryeの導入

```sh
curl -sSf https://rye.astral.sh/get | bash

// for fish
set -Ua fish_user_paths "$HOME/.rye/shims"

rye self completion -s fish > ~/.config/fish/completions/rye.fish

```

Ryeの更新

```sh
rye self update
```

### プロジェクト作成

```sh
rye init --script {project_name}
```

### パッケージ追加

```sh
rye add {package_name}

// for dev
rye add --dev {package_name}
```

ライブラリ追加後に実行

```sh
rye sync
```

.venv/,requirements.lock,requirements-dev.lockが生成される

### 実行

```sh
rye sync
rye run {project_name}
```

### lazyvimの設定

追加したパッケージがimportで呼べないことがあった以下をcode.luaに記述して解決

[Context: "https://github.com/LazyVim/LazyVim/issues/1386#issuecomment-1720957273"]
