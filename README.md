# git-flow の練習

## git-flow のインストール(windows)
コマンドを打ったら動いた。。。

## 参考サイト
- [git-flow cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html)
- [Git-flow ～Gitのブランチモデルを知る～](https://tracpath.com/bootcamp/learning_git_git_flow.html)

## 簡易な使い方
1. 初期化：git flow init
2. 
3. フィーチャーの開始：git flow feature start [feature-name]
4. 同一ブランチでの並行作業者へのpush：git flow feature publish [feature-name]
5. 同一ブランチで並行作業者からの修正の取り込み：git flow feature pull [feature-name]
6. フィーチャーの終了：git flow feature finish [feature-name]
7. 
8. リリースの開始：git flow release start [release-name]
9. リリースの終了：git flow release finish [release-name]
10. 
11. hot fixの開始：git flow hotfix start [hotfix-name]
12. hot fixの終了：git flow hotfix finish [hotfix-name]

## git-flow ブランチモデルの考え方
- master ブランチはリリース用。主にdevelop ブランチをマージしていく。
- develop ブランチがローカルリポジトリでの開発用のブランチ
- develop ブランチからさらに、featureブランチを作成して開発を進める。
- feature ブランチからpublishブランチを作成し、publishブランチをリモートリポジトリに push することで、並行開発者に開発中の機能をpushする。
- feature ブランチからpullすることで、他の開発者のコードをpullできる。
- release ブランチを作成し、最終版を作成したら、master ブランチの統合する。
- hotfix ブランチで、バグフィックスをする