# setup

Setup Knowledge

## 一般設定

- 言語を英語にする
- 地域を日本にする
- hostname の変更
  - SystemPreferrence>共有
- 日付と時刻の表示設定
- バッテリーの設置
  - パーセンテージ表示
  - ディスプレイオフまでの時間設定
- ディスプレイ解像度設定
- キーストローク設定
- トラックパッド設定
- 3本指ドラッグ設定
- Keyboard > Input Sources で以下を無効化(そのkeybindをneovimで使いたいため)
  - x Select the previous input source
  - x Select next soruce in input menu
- 操作スペースの自動入れ替わりを無効化
- Finder設定
  - Finder>環境設定 隠しファイル表示、その他諸々
  - Host配下を、 表示オプション >常にカラム表示で開く・カラム表示でブラウズ
  - 表示>パスバーを表示
  - 表示>タブバーを表示
  - 表示>ステータスバーを表示
- ユーザー辞書
  - OFF 英字入力中にスペルを自動変換
  - OFF 文頭を自動的に大文字にする
  - OFF スペースバーを2回押してピリオドを入力
  - OFF スマート引用符とスマートダッシュを使用
- Chrome インストール
- IME設定
  - Google日本語入力 インストール
  - ことえり アンインストール
- BetterSnapTool設定
  - ON Start BetterSnapTool everytime your Mac starts up
  - border width 3px
- vim設定

## 開発環境構築 - 全般

- Homebrew
- Git設定
  - gitconfig
    ```sh
    $ git config --global user.name my_name
    $ git config --global user.email myname@example.com
    ```
  - github SSH 設定
    - `$ ssh-keygen -t ed25519 -N "" -f ~/.ssh/github -C myname@example.com`
    - github の settingsから新しい SSH Key を作成
      - `$ pbcopy < ~/.ssh/github.pub` してクリップボードに公開鍵をコピーすると楽
      - key名にはマシン名をつけるのが管理しやすい
    - ```sh
      $ vi ~/.ssh/config
      Host github.com
        IdentityFile ~/.ssh/github
        User git
      ```
      - User は git にしないとうまく行かない
    - ssh -T github.com
      - yes -> success!

## Dotfiles

[dotfilesリポジトリ](https://github.com/hahnah/dotfiles の内容でセットする。  
その内容に各種ツールインストール時にセットされたりする。

## CLI Tools

次のサイトを参考に設定する。  
https://www.josean.com/posts/how-to-setup-alacritty-terminal

- Alacritty
- alacritty-theme
- powerlevel10k
- zsh-autosuggestions
- zsh-syntax-highlighting
- eza
- zoxide
- ~~tmux~~ tmuxではなくzellijを使うことにする

### zellij のインストール・設定

```bash
brew install zellij
mkdir ~/.config/zellij
zellij setup --dump-config > ~/.config/zellij/config.kdl
```

### ripgrep コマンドのインストール

```
brew install ripgrep
```

### fd コマンドのインストール

```
brew install fd
```

### tree コマンドのインストール

```
brew install tree
```

### AeroSpace のインストール

```
brew install --cask nikitabobko/tap/aerospace
```

## Neovim

```
brew install neovim
```

設定は[dotfiles](https://github.com/hahnah/dotfiles)の内容にする。

Neovimを使う上での [Requirements](https://github.com/hahnah/dotfiles/blob/main/.config/nvim/README.md#requirements) を用意する。

Lazy.nvimでプラグインのインストールを実行する。

```
:Lazy
```

Mason で LSP, Formatter, Linter などをインストールする。

```
:Mason
```

## 開発環境構築 - iOS

- XCode
- CocoaPods

## 開発環境構築 - Web

- ~~nodenv~~ (一部のプロジェクトのために必要な場合あり)
- volta
- node.js (npm inside)

## SNSアプリ

- Slack
- Discord
