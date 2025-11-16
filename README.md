# 姫路獨協大学 Debian Liveシステム

これは、姫路獨協大学の授業などで利用するためのLinuxライブシステムです。インストーラーもあるので、LiveシステムそのままをSSDにインストールして常用のLinuxシステムとして利用もできます。

## ビルド方法

このシステムは、Debian Liveのlive-buildを使って作られています。Debian GNU/Linux上からlive-buildパッケージをインストールしてください。

```console
sudo apt install -U live-build
```

ビルドをするには、このリポジトリを`git clone`したのち、`make`を実行するだけです。ビルドには管理者権限が必要になるので、パスワードを尋ねられたら入力してください。

ビルドをした後に不要なファイルを削除するには、`make clean`を実行します。また、設定だけする場合は、`make config`を実行します。

## カスタマイズ方法

独自で設定を追加する場合は、設定を参照するためにドキュメントをインストールします。[マニュアル](https://live-team.pages.debian.net/live-manual/html/live-manual/index.ja.html)はオンラインから参照できますが、起動時のオプション詳細については、`live-config-doc`と`live-boot-doc`に記載があるのでインストールしておきましょう。

```console
sudo apt install -U live-config-doc live-boot-doc live-manual
```

このシステムの基本設定は、リポジトリの`auto/config`にオプションの形で設定してあります。
それ以外については、`config`ディレクトリ以下にあります。
