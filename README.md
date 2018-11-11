# Git Training 実施事項

## 初期登録例

1. `git add -A`
1. `git commit -m`
1. `git push origin master`

## 「add」オプション

- `git add .` : 新規作成、また変更があったファイルを登録する。rmで削除したファイルはaddされない。

- `git add -u` : 1つ前の最新ステージと更新があったファイルを登録する。また新規作成したファイルは登録されない。

- `git add -A` : `「.」`と`「-u」`のオプションを合わせたもの。

