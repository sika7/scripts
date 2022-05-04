# dotfilesを簡単に作成するシェルスクリプト

## 使い方

コマンドのように使用できます。

例
```
$ dotfiles -h
```
ヘルプを表示します。

追加
```
$ dotfiles add {file name}
```
dotfileに追加しシンボリックリンクを貼ります。

一覧表示
```
$ dotfiles list
```
dotfileのファイル一覧

削除
```
$ dotfiles remove {file name}
```
シンボリックリンクを削除しdotfileからファイルを移動します。

デプロイ
```
$ dotfiles deploy
```
dotfiles一覧のシンボリックリンクをすべて貼ります。

## 設置

パスを通したフォルダに設置し、実行権限を追加してください。

設定例
```
mkdir ~/bin
echo '~/bin' >> ~/.bash_profile
git clone repository ~/your/path
cp ~/your/path/dotfiles ~/bin/dotfiles
chmod 755 ~/bin/dotfiles
```

## 設定

shell scriptをEditorで開き12~14行目を編集してください。

変更できるもの
```
DOTPATH=~/.dotfiles # dotfilesのパス
HOSTPATH=work # DOTPATHからみた実態ファイルのディレクトリ
LINKFILE=work # dotfile一覧が書き込まれるファイル
```

## 動作確認環境

* ubuntu 16.04 LTS
* ubuntu 18.04 LTS

## 注意事項

* 変更・改変は自己責任で行ってください。

