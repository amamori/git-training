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

※ commitするときにaddしていないファイルはコミットされない。

- `git commit -m` : `「-m」`コミットコメントを入力する。

- `git commit .` : `「.」`currentディレクトリで変更があったものをコミットする。

- `git commit -a` : `「-a」`git管理ディレクトリ上で変更があったものをコミットする。

