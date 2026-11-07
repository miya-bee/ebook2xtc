# ebook2xtc（β版）

ebook2xtc は、電子書籍リーダーアプリの読書画面を Android エミュレーター（AVD）から取得し、XTEINK X4 / X3 向けの XTC / XTCH ファイルに変換する Windows アプリです。

このリポジトリには、マニュアルと導入説明を置いています。アプリ本体はここでは配布していません。

## 入手方法

ebook2xtc（exe 版）は、日本語XTC GUI Studio をご購入いただいた方向けに限定配布しています。入手方法は、noteでご購入時いただいた有料部分を案内をご覧ください。

入手した ZIP を展開したら、`ebook2xtc` フォルダーの `README.txt` をお読みください（同じ内容: [docs/README_FIRST.txt](docs/README_FIRST.txt)）。

## 必要な環境

- Windows 11
- Android Studio と AVD（Android 仮想デバイス）のインストール
- 相応のマシンパワー。目安: Intel Core i5 第11世代 / Ryzen 5 4000番台相当以上、メモリ16GB推奨、BIOS で仮想化が有効で WHPX を使えること、十数GBの空き容量

## ご利用にあたって

- DRM や画面保護は回避しません。画面に表示された内容を取得する方式です。
- 私的使用の範囲に限ってご利用ください。
- 生成したファイルを第三者に配布しないでください。
- 各ストア・サービスの利用規約は、利用者ご自身でご確認ください。

## マニュアル

- [操作マニュアル（Markdown）](docs/manual/index.md)
- 配布 ZIP の `manual\index.html` にも同じ内容が入っています。
- 依存ライブラリのライセンス: [docs/dependency-licenses.md](docs/dependency-licenses.md)
