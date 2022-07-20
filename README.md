# pymail

## NAME

pymail -- メール送信スクリプト

## USAGE

```
usage: pymail [-h] [--file FILE] [--config CONFIG]

optional arguments:
  -h, --help            show this help message and exit
  --file FILE, -f FILE  メールの情報 (宛先など) および本文に関するファイルを指定する
  --config CONFIG, -c CONFIG
                        config ファイル (gnupg で暗号化された json ファイル) を指定する (デフォルトは
                        ~/.pymailconf)
```


## DESCRIPTION

送信先・件名・メール内容など (contents) を読み込み、メールを送信する。
contents は

```
To: hogehoge@mail
Cc: hogetmp@mail
Subject: 件名
File: filepath

本文
```

などのように記載する。To: などの指示と本文との間には 1 行の空白行を入れておく。

メールアカウント等の設定ファイルは
~/controls/setting/mutt/pass/.pymailconf.json.gpg
に設置する。

To, Cc, Bcc, File については、コンマで区切ることによって複数の要素を対象にすることができる。
