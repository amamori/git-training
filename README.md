# Git Training 実施事項

## 初期登録例

1. `git add -A`
1. `git commit -m`
1. `git push origin master`

## 「add」オプション

- `git add .` : 新規作成、また変更があったファイルを登録する。rmで削除したファイルはaddされない。

- `git add -u` : 1つ前の最新ステージと更新があったファイルを登録する。また新規作成したファイルは登録されない。

- `git add -A` : `「.」`と`「-u」`のオプションを合わせたもの。

## 「commit」オプション

※ commitするときにaddしていないファイルはコミットされない。

- `git commit -m` : `「-m」`コミットコメントを入力する。

- `git commit .` : `「.」`currentディレクトリで変更があったものをコミットする。

- `git commit -a` : `「-a」`git管理ディレクトリ上で変更があったものをコミットする。

## 「push」オプション

- `git push <repository> <branch>`

- 例：`git push origin master`

    - origin: レポジトリの場所(URL)の別名
        - `git remote -v`コマンドで確認できる
    - master: ブランチの名前

- `git push -f origin master` : コンフリクトしていて強制的にpushする

## Gitで使うときの標準エディタを変更する

- `git config --global core.editor '○○'`

    - 〇〇のところは'vim'のような感じで指定する。
    - ※初期はemacsとかになっていると思います。(未確認・・・)

## ブランチの切り方

- `git branch` : 現在のブランチを確認する
- `git branch <新しいbranch名>` : 新しいローカルブランチを作成する

## ブランチの変更方法

- `git checkout <branch名>` : ブランチを切り替える

## ブランチのマージ

- `git merge <branch>` : 
    - ※mergeする時はマージするbranchに移動しておくこと※

## ブランチの削除

### ローカルブランチ

- `git branch --delete <branch名>`

### リモートブランチ

- `git push --delete origin <branch名>`

## commitのキャンセル

- `git reset --hard HEAD^` : 1つ前のコミットをキャンセルし、ファイルも最新コミット時のファイルまで戻す
- `git reset --soft HEAD^` : 1つ前のコミットをキャンセルし、ファイルの変更はそのまま。

https://qiita.com/shuntaro_tamura/items/06281261d893acf049ed

## logの整理方法

- `git rebase -i`
