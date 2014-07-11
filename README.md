# macの基本設定(個人メモ)

## Xcodeのインストール
- AppStore経由でOK
- CommandLineToolsをDeveloperセンターから取得

## Homebrewのインストール
[http://brew.sh/index_ja.html](http://brew.sh/index_ja.html)
```
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
```

## Dockを左寄せに
- システム環境設定 => dockより選択
- 自動で消えるように設定

## Fnキーを標準のファンクションキーとして使用
- システム環境設定を変更

## .で始まるファイルを可視化する
```
defaults write com.apple.finder AppleShowAllFiles -boolean true
killall Finder
```

## [homesick](https://github.com/technicalpickles/homesick)のダウンロード
```
 gem install homesick
```
## github
### 公開鍵設定
[https://help.github.com/articles/generating-ssh-keys](https://help.github.com/articles/generating-ssh-keys)
リンクの通りに設定すれば問題ない


## homesickの設定
```
homesick clone HAKASHUN/dotfiles
cd ~ 
homesick symlink dotfiles 
```
# コマンドライン

## iTerm2をダウンロードする
[http://www.iterm2.com/](http://www.iterm2.com/)

## zsh
### zshモードをデフォルトにする
```
chsh -s /bin/zsh
```
を実行するとzshをデフォルトで使えるようになる。

## `brew bundle`を実行する

アプリケーションの落とす場所を設定
[http://waka.github.io/2014/1/19/homebrew_cask.html](http://waka.github.io/2014/1/19/homebrew_cask.html)
```
 export HOMEBREW_CASK_OPTS="--appdir=/Applications"
```
Brewfileの定義をマシンに反映

```
brew bundle
```

### .zshenvを作成する

```
# path settings
export PATH="/usr/local/bin:$PATH"
```
### .zshrcを作成する
.zshrcファイルに必要な設定を記述する

Ex. .zshrcにnvmの設定がされている場合
```
# nvm source setting
source ~/.nvm/nvm.sh
```
## nvm
### nvmを入れる
以下を実行する
```
curl https://raw.github.com/creationix/nvm/master/install.sh | sh
```
### nodeのバージョン
```
nvm install v0.10.26
nvm use v0.10.26
```

## npm

### npmのインストール
```
curl -L https://npmjs.org/install.sh | sh
```
### node-gyp入れる
```
npm install -g node-gyp
```
### bower 入れる
```
npm install bower -g
```

### grunt入れる
```
npm install grunt-cli -g
```

### stylus入れる
```
npm install stylus -g
```
## トラブルシューティング

1. brew updateでエラー
[http://qiita.com/harapeko_wktk/items/f4f44ddb5d3912e15ea2]()
