# Memo

## 行終端文字の調整

Windows と Linux や Mac では行終端文字が異なるので、```.gitattributes``` を追加して調整する。

[Resolving Git line ending issues in containers (resulting in many modified files)](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files)

## コンテナ内からのGit操作

既定では Git リポジトリのルートがマウントされた状態で開く。
コンテナイメージ内に Git がインストールされていれば、VSCodeのTerminalから操作可能。

## 非 Root ユーザーでの開発作業

Dockerfile でイメージをビルドする際に Non Root ユーザーを追加する。
devcontainer.json からはその ```remoteUser``` プロパティでユーザー名を指定しておく。
Dev Container が起動されたときは指定したユーザーで処理が行われることになる。

## Docker from Docker
https://github.com/microsoft/vscode-dev-containers/tree/master/containers/docker-from-docker