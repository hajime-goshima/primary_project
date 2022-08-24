## Git subtree の動作確認

`subtree add`で外部リポジトリを取り込む

```
$ git subtree add --prefix secondary https://github.com/hajime-goshima/secondary_project.git main
git fetch https://github.com/hajime-goshima/secondary_project.git main
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 244 bytes | 244.00 KiB/s, done.
From https://github.com/hajime-goshima/secondary_project
 * branch            main       -> FETCH_HEAD
Added dir 'secondary'
```

`subtree pull`で外部リポジトリの最新の変更を取り込む

```
$ git subtree pull --prefix secondary https://github.com/hajime-goshima/secondary_project.git main
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 284 bytes | 284.00 KiB/s, done.
From https://github.com/hajime-goshima/secondary_project
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.
 secondary/main2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 secondary/main2.txt
```
