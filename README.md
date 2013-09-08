## 概要
Railsアプリを作成し，GitHub，Travis CI，Herokuと連携する設定を行い，Deployします．

## 前提

- Ruby 2.0.0，Rails 4.0がインストールされていること
- rbenvを使っていること
- git configの設定ができていること
- SSHの公開鍵をGitHubとHerokuに登録してあること
- [Heroku Toolbelt](https://toolbelt.heroku.com/)がインストールされていること
- [github/hub](https://github.com/github/hub)がインストールされていること

## 使い方

```
$ source generate_rails.sh <app_name>
```
