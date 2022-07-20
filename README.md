# pymail

## NAME

pymail -- メール送信スクリプト

## SYNOPSIS

pymail contents

## DESCRIPTION

送信先・件名・メール内容など (contents) を読み込み、メールを送信する。
contents は

- - -

To: hogehoge@mail
Cc: hogetmp@mail
Subject: 件名
File: filepath

本文

- - -

などのように記載する。To: などの指示と本文との間には 1 行の空白行を入れておく。

メールアカウント等の設定ファイルは
~/controls/setting/mutt/pass/.pymailconf.json.gpg
に設置する。

To, Cc, Bcc, Path については、メールアドレスをコンマで区切ることによって複数アドレスを対象にすることができる。
