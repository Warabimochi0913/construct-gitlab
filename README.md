# construct-gitlab
## 概要
Ansibleを用いてgitlabを自動で構築します。

## 使用技術一覧
<img src="https://img.shields.io/badge/-Ansible-000000.svg?logo=ansible&style=ansible&logoColor=#EE0000"><img src="https://img.shields.io/badge/-docker-1488C6.svg?logo=docker&style=docker&logoColor=#2496ED"><img src="https://img.shields.io/badge/-Ubuntu-E95420?logo=ubuntu&logoColor=white&style=flat">

## 環境構築
1. Ansibleを実行可能な環境(control node)を準備します。
2. **deploy先の準備**<br>
  `target`: Ubuntu Serverをインストールし、SSH鍵認証でアクセスできるように設定。<br>
3. **リポジトリのクローン**:<br>
  control nodeにリポジトリをクローンします。
4.  **`hosts_vars` の設定**:<br>
  `develop.yml.example`から`develop.yml`を作成し、自身の環境に合わせて修正してください。
## 環境構築の実行
control nodeで以下のコマンドを実行します。
1. **実行**:<br>
   docker composeを用いてgitlabが立ち上がります。
  `--ask-become-pass`は必要な場合につけます。
  ```bash
  ansible-playbook playbook.yml --ask-become-pass
  ```