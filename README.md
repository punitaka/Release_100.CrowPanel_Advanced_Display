# CrowPanel Advanced 7inch（ESP32-P4）開発資料集
[![YouTube](https://img.shields.io/badge/YouTube-regional--engineer-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@regional-engineer)
[![Target](https://img.shields.io/badge/Target-CrowPanel%20Advanced%207inch%20V1.1-00695C)](#対象製品)
[![Development](https://img.shields.io/badge/Development-Arduino%20IDE%20%2F%20ESP--IDF%20%2B%20VS%20Code-007ACC)](#収録資料)

[Elecrow社「CrowPanel Advanced 7inch | ESP32-P4 HMI AI Display 1024×600」](https://www.elecrow.com/crowpanel-advanced-7inch-esp32-p4-hmi-ai-display-1024x600-ips-touch-screen-with-wifi-6-compatible-with-arduino-lvgl-micropython.html)の開発情報をまとめたリポジトリです。Elecrow社公式のLesson資料（英語）の日本語訳や、開発環境構築の手順書などを公開しています。

あわせて、著者のYouTubeチャンネルでも本製品の解説動画を公開しています。

- 🎥 YouTubeチャンネル：[@regional-engineer](https://www.youtube.com/@regional-engineer)

> [!NOTE]
> 本リポジトリはElecrow社公式のLesson資料・コース資料を参考に、個人が非公式に翻訳・作成したものです。Elecrow社の公式ドキュメントではありません。内容の正確性については可能な限り注意していますが、製品仕様やソフトウェアのバージョンアップにより実際の画面表示やメニュー名等が変更される場合があります。最新の一次情報は必ず[Elecrow公式サイト](https://www.elecrow.com/)・[Elecrow公式Wiki](https://www.elecrow.com/wiki/)・各ソフトウェアの公式ドキュメントをご確認ください。

## 対象製品

| 項目 | 仕様 |
|---|---|
| 製品名 | CrowPanel Advanced 7inch \| ESP32-P4 HMI AI Display 1024×600 |
| メインチップ | ESP32-P4（RISC-V デュアルコア） |
| 無線通信 | ESP32-C6-MINI-1モジュール搭載（Wi-Fi 6 / Bluetooth 5.3） |
| Flash / PSRAM | 16MB / 32MB |
| ディスプレイ | 7.0インチ IPS、1024×600、静電容量式タッチ |
| メーカー公式ページ | https://www.elecrow.com/crowpanel-advanced-7inch-esp32-p4-hmi-ai-display-1024x600-ips-touch-screen-with-wifi-6-compatible-with-arduino-lvgl-micropython.html |

## 公開済みの動画

紹介・解説動画はYouTubeチャンネル「[@regional-engineer](https://www.youtube.com/@regional-engineer)」で公開しています。動画は今後も追加していく予定です。

| No. | タイトル | リンク |
|---|---|---|
| 1 | 【初心者向け】ESP32-P4搭載 CrowPanel Advanced 7インチをArduino IDEで動かす｜環境構築 | https://youtu.be/JwU0RU6vOWA |
| 2 | ESP32の最強進化形「P4」搭載！ELECROW 7インチ タッチディスプレイ開封＆スペック解説 | https://youtu.be/J4xz2Tut6aU |

> 新しい動画を公開次第、この表に追記していきます。最新の動画一覧は[チャンネルページ](https://www.youtube.com/@regional-engineer)でもご確認いただけます。

## リポジトリ構成

```
Release_100.CrowPanel_Advanced_Display/
├─ 1. 【arduino】Lesson資料+日本語版/
├─ 2. 【ESP-IDF+VSCode】Lesson資料+日本語版/
├─ 2. 【ESP-IDF+VSCode】導入手順書_AI作成版/
└─ 20.v1.1のlibrariesフォルダ/
```

### 1. 【arduino】Lesson資料+日本語版

Elecrow社公式のArduino IDE向けLesson資料（英語原文PDF）と、その日本語訳版（4分冊）を収録しています。Arduino IDEでCrowPanel Advanced 7inchを動かしたい方はまずこちらをご覧ください。

| ファイル | 内容 |
|---|---|
| `V1.1__CrowPanel_Advanced_7inch_ESP32-P4_HMI.pdf` | Elecrow公式Lesson資料（英語原文） |
| `日本語_..._part1_p01-10.pdf` 〜 `part4_p163-248.pdf` | 上記の日本語訳（全248ページを4分冊） |

### 2. 【ESP-IDF+VSCode】Lesson資料+日本語版

Elecrow社公式のESP-IDF向けコース資料「Advance HMI P4 7inch Course V1.1」（英語原文PDF）と、その日本語訳版（Lesson01〜17、全12分冊）を収録しています。

| ファイル | 内容 |
|---|---|
| `Advance_HMI_P4_7inch_Course_V1.1.pdf` | Elecrow公式コース資料（英語原文） |
| `【日本語版】..._Part_01_Lessons_01-03_pages_001-029.pdf` 〜 `Part_12_Lesson_17_pages_318-342.pdf` | 上記の日本語訳（Lesson01〜17を12分冊） |

### 2. 【ESP-IDF+VSCode】導入手順書_AI作成版

ESP-IDF＋VS Codeの開発環境構築手順を、AIエージェントに作成させた手順書・スライドです。作成に使用したAIごとにファイルを分けています（内容の比較・参考用）。

| ファイル | 作成AI | 内容 |
|---|---|---|
| `【claude作成】ESP-IDF_VSCode_setup_CrowPanel_ESP32-P4.pdf` | Claude | 導入手順書（PDF、全16ページ） |
| `【claude作成】ESP-IDF_VSCode_overview_slides.pptx` | Claude | 手順の全体像を示す解説スライド（PPTX、全11枚） |
| `【manus作成】ESP-IDF_導入手順書_CrowPanel_Advanced_7inch_V1.1.pdf` | Manus | 導入手順書（PDF） |
| `【manus作成】CrowPanel_Advanced_7inch_V1.1_ESP-IDF導入ガイド.pptx` | Manus | 導入ガイド（PPTX） |

> [!IMPORTANT]
> このフォルダ内の資料はAIが作成したものです。内容には誤りが含まれる可能性があるため、実機で操作しながら内容をご確認ください。

### 20.v1.1のlibrariesフォルダ

Arduino IDEでのビルドに使用するライブラリ一式です（詳細説明省略）。

## 免責事項

- 本リポジトリの内容は、Elecrow社公式のLesson資料・コース資料を参考に個人が作成した**非公式**のコンテンツです。Elecrow社および関連企業とは関係がありません。
- 日本語訳資料は原文（英語）を参考に翻訳したものであり、翻訳の正確性を保証するものではありません。内容に相違がある場合は英語の原文を正としてください。
- AIが作成した手順書・スライドについても内容の正確性を保証するものではありません。実際の作業は自己責任で行い、必要に応じて公式ドキュメントもあわせてご確認ください。
- 本リポジトリの内容によって生じたいかなる損害についても、作成者は責任を負いかねます。

## 参考リンク

- [Elecrow公式サイト（製品ページ）](https://www.elecrow.com/crowpanel-advanced-7inch-esp32-p4-hmi-ai-display-1024x600-ips-touch-screen-with-wifi-6-compatible-with-arduino-lvgl-micropython.html)
- [Elecrow公式Wiki](https://www.elecrow.com/wiki/)
- [ESP-IDF VS Code拡張機能 公式ドキュメント](https://docs.espressif.com/projects/vscode-esp-idf-extension/)
- [ESP-IDF公式ドキュメント（ESP32-P4）](https://docs.espressif.com/projects/esp-idf/en/stable/esp32p4/)

## クレジット

- 資料翻訳・手順書作成：[@regional-engineer](https://www.youtube.com/@regional-engineer)
- 参考元：Elecrow社公式Lesson資料・コース資料
