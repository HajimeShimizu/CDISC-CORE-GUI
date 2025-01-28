# CDISC-CORE-GUI

## 概要
CDISCはCDISC Open Rules Engine (CORE)を開発していますが、コマンドライン版のみが提供されています。CDISC CORE GUI は、COREにGUIを搭載したものです。本ツールは、ユーザーがテストしやすいCOREを用意し、CORE開発者へのフィードバックを促すことを目的としています。

## 使い方
core_gui.exeをダブルクリックします。**起動まで時間がかかる**ケースがあるので、しばらくお待ちください。環境によっては40秒程度かかることが報告されています。大規模データセット（1GB超え）をバリデーションする場合、ローカルにデータを保存して実行することを推奨します。

起動に成功すると、以下の画面が表示されます。パッケージのバリデーションを実行するには、
1. 必要なパラメータを指定し、
2. 「実行」ボタンを押します

<img width="500" alt="GUI image" src="gui_image.png">

### パラメータの指定
基本設定
- 標準: Specify Implematation Guide. All standards supported by CORE show up.\
-Version: Specify version of Standard.\
-CT: Specify version of controlled terminology. Terminology should be placed in 'resources/cache' folder.\
\
External Dictionaries\
-MedDRA: Optional. Specify version.\
-WHODD: Optional. Specify version.\
-MED-RT: Optional. Specify version.\
-LOINC: Optional. Specify version.\
\
Define.xml\
-Either 'path of define.xml' or 'expected version of define.xml' must be specified. 'Expcted version' is ignored when both parameters are specified.\
-define.xml v1.0 is not supported\
\
Data files\
-Specify dataset file(s). XPT, JSON, Parquet, USDM are acceptable file formats.\
\
Output\
-Specify report folder. '/report' is recommended.

## How to prepare external dictionaries
-Under preparation.
