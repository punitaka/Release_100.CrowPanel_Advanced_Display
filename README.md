# CrowPanel Advanced 7inch 開発資料・日本語Lesson集

[![YouTube](https://img.shields.io/badge/YouTube-regional--engineer-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@regional-engineer)
[![Target](https://img.shields.io/badge/Target-CrowPanel%20Advanced%207inch%20V1.1-00695C)](#対象製品)
[![Development](https://img.shields.io/badge/Development-Arduino%20IDE%20%2F%20ESP--IDF%20%2B%20VS%20Code-007ACC)](#収録資料)

# CrowPanel Advanced 7inch 開発資料・日本語Lesson集

[![YouTube](https://img.shields.io/badge/YouTube-regional--engineer-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@regional-engineer)
[![Target](https://img.shields.io/badge/Target-CrowPanel%20Advanced%207inch%20V1.1-00695C)](#対象製品)
[![Development](https://img.shields.io/badge/Development-Arduino%20IDE%20%2F%20ESP--IDF%20%2B%20VS%20Code-007ACC)](#収録資料)

CrowPanel Advanced 7inch（ESP32-P4搭載、1024×600タッチディスプレイ）の開発に必要な**日本語のLesson資料**、**ESP-IDF × Visual Studio Codeの導入手順書**、および関連するArduinoライブラリを整理して公開するリポジトリです。

Elecrow公式資料・公式サンプルを日本語で理解しやすくすることを目的としています。まずは対象基板のバージョンと利用する開発環境を確認し、公式サンプルを小さく検証してから、ご自身のアプリケーションへ発展させてください。

> **本リポジトリはElecrow社およびEspressif社の公式サポートサイトではありません。** 公式資料と公式ソースを優先し、本リポジトリの日本語資料は理解補助・開発支援として利用してください。

---

## 目次

- [対象製品](#対象製品)
- [このリポジトリでできること](#このリポジトリでできること)
- [収録資料](#収録資料)
- [おすすめの利用順序](#おすすめの利用順序)
- [YouTube動画](#youtube動画)
- [利用上の重要な注意](#利用上の重要な注意)
- [質問・改善提案](#質問改善提案)
- [公式資料](#公式資料)

---

## 対象製品

本リポジトリの主な対象は、以下の製品です。

| 項目 | 内容 |
| --- | --- |
| 製品名 | CrowPanel Advanced 7inch ESP32-P4 HMI AI Display |
| 対象版 | **Hardware & Software V1.1** |
| 主な構成 | ESP32-P4、ESP32-C6、1024×600 IPSタッチディスプレイ |
| 開発環境 | Arduino IDE、ESP-IDF、Visual Studio Code |

> **重要:** 実機がV1.1の場合は、V1.1向けの公式サンプル、`sdkconfig`、配線・初期化前提を使用してください。V1.2向けの設定を混在させると、LCD、タッチ、Wi-Fiなどの問題を切り分けにくくなります。

---

## このリポジトリでできること

このリポジトリでは、英語中心の公式資料やサンプルを読む際の負担を下げ、CrowPanelの開発を段階的に進めるための情報を提供します。

| 開発したいこと | 参照する資料 | 最初の到達点 |
| --- | --- | --- |
| Arduino IDEで基板を動かしたい | Arduino向けLesson資料・日本語版 | 公式サンプルのビルドと書込み |
| ESP-IDFで画面・タッチを確認したい | ESP-IDF向けLesson資料・日本語版 | Lesson09のLCD・GT911タッチ確認 |
| VS CodeでESP-IDFを使い始めたい | ESP-IDF + VS Code導入手順書 | Visual Studio Codeでビルド・書込み・モニタ |
| Wi-FiやAI会話表示へ発展させたい | V1.1公式Lessonと導入手順書 | Lesson17 stationのIP取得後に統合へ進む |

---

## 収録資料

リポジトリ直下の主なフォルダと用途は以下のとおりです。資料を追加・改訂する場合も、この構成を基準に整理します。

| フォルダ | 内容 | 主な対象者 |
| --- | --- | --- |
| [`1. 【arduino】Lesson資料+日本語版`](./1.%20【arduino】Lesson資料+日本語版/) | Arduino IDE向けのLesson資料と日本語版 | Arduino IDEから始めたい方 |
| [`2. 【ESP-IDF+VSCode】Lesson資料+日本語版`](./2.%20【ESP-IDF+VSCode】Lesson資料+日本語版/) | ESP-IDF / Visual Studio Code向けのLesson資料と日本語版 | ESP-IDFの公式Lessonを学びたい方 |
| [`2. 【ESP-IDF+VSCode】導入手順書_AI作成版`](./2.%20【ESP-IDF+VSCode】導入手順書_AI作成版/) | V1.1でESP-IDFを導入するための実践手順書 | VS Codeで書込み・ログ確認まで進めたい方 |
| [`20.v1.1のlibrariesフォルダ/V1.1/Arduino_Code`](./20.v1.1のlibrariesフォルダ/V1.1/Arduino_Code/) | V1.1向けArduinoコードとライブラリ | Arduinoサンプルをビルドする方 |

---

## おすすめの利用順序

初めてCrowPanel Advanced 7inchを扱う場合は、画面、タッチ、Wi-Fiを同時に実装しようとせず、公式サンプルを利用して一つずつ確認することをおすすめします。

| 手順 | 実施内容 | 合格条件 |
| --- | --- | --- |
| 1 | 基板のハードウェア／ソフトウェア版が**V1.1**であることを確認します。 | 対象版に対応した資料を選べる。 |
| 2 | Arduino IDEまたはESP-IDF + VS Codeの、どちらで始めるか選びます。 | 開発環境と資料の対応関係が明確になる。 |
| 3 | ESP-IDFの場合は、導入手順書に従ってVisual Studio CodeとESP-IDF拡張を設定します。 | `Doctor Command`が正常に完了する。 |
| 4 | V1.1のLesson09を改変せずに書き込みます。 | LCD・バックライト・タッチが動作する。 |
| 5 | V1.1のLesson17 stationを単独で確認します。 | シリアルログに`got ip:`が表示される。 |
| 6 | 個別検証が成功してから、画面とWi-Fiの統合や独自アプリケーションへ進みます。 | 問題発生時に原因を切り分けられる。 |

---

## YouTube動画

CrowPanel、ESP32-P4、Arduino IDE、ESP-IDFに関する動画を公開しています。**新しい動画はこの表の先頭へ追加**することで、最新情報を追いやすくなります。

| 公開日 | 動画 | 内容 | リンク |
| --- | --- | --- | --- |
| 公開済み | 【初心者向け】ESP32-P4搭載 CrowPanel Advanced 7インチをArduino IDEで動かす｜環境構築 | Arduino IDEでCrowPanel Advanced 7inchを動かすための環境構築を解説 | [YouTubeで視聴](https://youtu.be/JwU0RU6vOWA) |
| 公開済み | ESP32の最強進化形「P4」搭載！ELECROW 7インチ タッチディスプレイ開封＆スペック解説 | CrowPanel Advanced 7inchの開封と主要仕様を紹介 | [YouTubeで視聴](https://youtu.be/J4xz2Tut6aU) |
| 今後追加 | 新しい動画はここへ追加 | ESP-IDF、Wi-Fi、Raspberry Pi連携、AI会話表示などの検証動画を追加予定 | [チャンネルを見る](https://www.youtube.com/@regional-engineer) |

動画で扱ったソースコード・資料・補足情報は、必要に応じて本リポジトリへ追加します。動画の説明欄と本READMEをあわせて確認してください。

### 動画を追加するときの更新テンプレート

新しい動画を公開したら、上の表の先頭に次の1行を追加してください。

```markdown
| YYYY-MM-DD | [動画タイトル](https://youtu.be/VIDEO_ID) | 動画で扱う内容を1文で記載 | [YouTubeで視聴](https://youtu.be/VIDEO_ID) |
```

---

## 利用上の重要な注意

### V1.1とV1.2を混在させない

CrowPanel Advanced 7inchはハードウェア／ソフトウェア版ごとにサンプルや設定が異なります。本リポジトリでV1.1を対象とする資料は、Elecrow公式リポジトリの`example/V1.1/`を基準にしています。実機の版と異なる資料を使用する場合は、事前に差分を確認してください。[1]

### Wi-Fiの資格情報を公開しない

ESP-IDFのWi-Fiサンプルでは、SSIDやパスワードが` sdkconfig`に保存され、シリアルログに表示される場合があります。GitHubへのコミット、Issueへのログ貼り付け、YouTubeでの画面収録を行う前に、SSID、パスワード、IPアドレス、アクセストークンを必ず伏せてください。

### APIキーをCrowPanelへ置かない

Raspberry PiとCrowPanelを連携するAI会話表示システムへ発展させる場合、Manus APIやOpenAI APIなどのクラウドAPIキー、会話履歴、ログ管理はRaspberry Pi側へ集約する構成を推奨します。CrowPanelは、Wi-FiによるLAN通信、LVGL表示、タッチ操作、接続状態表示に専念させてください。

### 公式資料を優先する

本リポジトリに収録・紹介する日本語資料は理解補助を目的としたものです。仕様変更、不具合、ライセンス、配線、C6ファームウェアの扱いなどの最終判断は、必ずElecrowおよびEspressifの公式資料で確認してください。[1] [2] [3]

---

## 質問・改善提案

資料の誤記、分かりにくい表現、動作環境との差異、追加してほしいLessonがあれば、[Issues](../../issues)でお知らせください。再現条件を確認できるよう、次の情報を添えていただけると助かります。

| 項目 | 記載例 |
| --- | --- |
| 基板の版 | Hardware & Software V1.1 |
| 開発環境 | Arduino IDEの版、ESP-IDFの版、Visual Studio Codeの版 |
| 使用したサンプル | `Lesson09-LVGL_Lighting_Control` など |
| 期待した結果と実際の結果 | 画面表示の有無、`got ip:`の有無など |
| ログ | 秘密情報を削除・マスクしたシリアルログ |

Pull Requestによる誤記修正、手順の改善、資料追加も歓迎します。追加する資料については、元となる公式情報の出典と、対象ハードウェア版を明記してください。

---

## 公式資料

| 資料 | 用途 |
| --- | --- |
| [Elecrow公式Wiki](https://www.elecrow.com/wiki/CrowPanel_Advanced_7inch_ESP32-P4_HMI_AI_Display_1024x600_IPS_Touch_Screen_with_WiFi6_Compatible_with_ArduinoLVGL.html) | 製品概要、接続・利用上の注意、公式資料への入口 |
| [Elecrow公式GitHub](https://github.com/Elecrow-RD/CrowPanel-Advanced-7inch-ESP32-P4-HMI-AI-Display-1024x600-IPS-Touch-Screen) | V1.1を含む公式サンプル、ライブラリ、回路関連資料 |
| [CrowPanel Advanced 7inch Course V1.1](https://www.elecrow.com/download/product/DHE04107D/Advance_HMI_P4_7inch_Course_V1.1.pdf) | V1.1向け公式コース資料 |
| [Espressif: ESP-IDF Extension for VS Code](https://docs.espressif.com/projects/vscode-esp-idf-extension/en/latest/) | Visual Studio Code上でのESP-IDF導入、ビルド、書込み、モニタの公式手順 |

---

## ライセンス・権利について

ElecrowおよびEspressifに帰属するソースコード、ライブラリ、画像、資料を利用する場合は、それぞれに付属するライセンス、著作権表示、利用条件を確認してください。本リポジトリにおける日本語解説・手順書の利用条件を追加・変更する場合は、リポジトリ直下のライセンスファイルまたは本節へ明記してください。

---

CrowPanel Advanced 7inchの開発を、日本語で一歩ずつ確実に進めるための情報を整理しています。  
[regional-engineer YouTube Channel](https://www.youtube.com/@regional-engineer)
