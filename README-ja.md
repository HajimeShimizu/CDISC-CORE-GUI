# CDISC-CORE-GUI

README in English [README-ja.md](https://github.com/HajimeShimizu/CDISC-CORE-GUI/blob/main/README.md).

## 概要
CDISCはCDISC Open Rules Engine (CORE)を開発していますが、コマンドライン版のみが提供されています。CDISC CORE GUI は、COREにGUIを搭載したものです。本ツールは、ユーザーがテストしやすいCORE環境を用意し、CORE開発者へのフィードバックを促すことを目的としています。

## 使い方
core_gui.exeをダブルクリックします。**起動まで時間がかかる**ケースがあるので、しばらくお待ちください。環境によっては40秒程度かかることが報告されています。大規模データセット（1GB超え）をバリデーションする場合、ローカルにデータを保存して実行することを推奨します。

起動に成功すると、以下の画面が表示されます。パッケージのバリデーションを実行するには、
1. 必要なパラメータを指定し、
2. 「実行」ボタンを押します

<img width="500" alt="GUI image" src="gui_image.png">

### パラメータの指定
基本設定
- 標準：標準を指定します。COREでサポートされている標準のみ表示されます
- バージョン：標準のバージョンを選択します
- CT：Controlled Terminologyのバージョンを選びます。'resources/cache'フォルダ内にある用語がリストで表示されます

外部辞書
- MedDRA：任意指定。バージョンを指定してください
- WHODD：任意指定。バージョンを指定してください
- MED-RT：任意指定。バージョンを指定してください
- LOINC：任意指定。バージョンを指定してください

Define.xml
- define.xmlのパス　または　想定されるdefine.xmlのバージョン　のいずれかを指定します。両方のパラメータを設定した場合、指定されたdefine.xmlのコンテンツが優先されます（仮想のdefine.xmlバージョンは無視されます）

データセット
- バリデーションの対象となるデータセットを指定します。XPT・JSON・PARQUET・USDM形式のデータを指定できます

出力先
- レポートの出力先フォルダを指定します。’/report’フォルダを推奨します

## 辞書のセットアップ
-Under preparation.
