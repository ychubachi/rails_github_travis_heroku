## 概要
Railsアプリを作成し，GitHub，Travis CI，Herokuと連携する設定を行い，Deployします．

## 前提

- Vagrant - Ubuntu 12.04
- Ruby 2.0.0，Rails 4.0がインストールされていること
- rbenvを使っていること
- [Heroku Toolbelt](https://toolbelt.heroku.com/)がインストールされていること
- [github/hub](https://github.com/github/hub)がインストールされていること

## GitHubへのSSH公開鍵

GitHubへSSH公開鍵を登録していない場合は下記のコマンドを実行してください．

```bash
$ wget https://gist.github.com/acoulton/1969779/raw/5b24fc88fb978f6fec89196903432a94aa1c209b/github-connect.sh
$ chmod 755 github-connect.sh
$ ./github-connect.sh
```

（このscriptは[Create and register an SSH key for your github account](https://gist.github.com/acoulton/1969779)から一部を改変したものです．）

## Railsアプリの自動生成

下記のコマンドを実行してください．

```
$ mkdir -p /vagrant/work
$ cd /vagrant/work
$ git clone git@github.com:ychubachi/rails_github_travis_heroku.git
$ cd rails_github_travis_heroku
$ ./generate_rails.sh <app_name>
```

Heroku，Travis CIへのログインの後，アプリの生成が始まります．
