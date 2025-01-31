# CDISC-CORE-GUI

README in English [README.md](https://github.com/HajimeShimizu/CDISC-CORE-GUI/blob/main/README.md).


## 概要
CDISCはCDISC Open Rules Engine (CORE)を開発していますが、コマンドライン版のみが提供されています。CDISC CORE GUI は、COREにGUIを搭載したものです。本ツールは、ユーザーがテストしやすいCORE環境を用意し、CORE開発者へのフィードバックを促すことを目的としています。


## ダウンロード
[こちらのページ](https://github.com/HajimeShimizu/CDISC-CORE-GUI/releases/tag/v0.1.3)からダウンロードできます\
<img width="200" alt="GUI image" src="files.png">

### 注意事項
1. 上記ファイルをすべてダウンロードします
2. exeファイルをダブルクリックすると、ファイルが結合されます
3. 圧縮ファイルを解凍します


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
### MedDRA
config/meddraフォルダに辞書データを配置します。バージョンごとにフォルダを作成します。次のファイルが必須です：
- pt.asc
- hlt.asc
- llt.asc
- soc.asc
- hlgt.asc
- soc_hlgt.asc
- hlgt_hlt.asc
- hlt_pt.asc
- meddra_release.asc

### WHODD
config/whoフォルダに辞書データを配置します。バージョンごとにフォルダを作成します。次のファイルが必須です：
- DD.txt
- INA.txt
- DDA.txt
- version.txt [*]

[*]: UMCから公式に配布されているパッケージでは 'Version.txt' です。ファイル名の変更が必要ないか、確認してください

### MEDRT
config/medrtフォルダに辞書データを配置します。バージョンごとにフォルダを作成し、core DTSファイルを保存します。ファイル名は Core_MEDRT_[日付]_DTS.xmlとします

### LOINC
config/loincフォルダに辞書データを配置します。バージョンごとにフォルダを作成し、LOINCにて配布されているファイルを保存します。ファイル名は Loinc.csvである必要があります
