# 4. キーボード入力と画面消灯の設定

ログイン欄への入力と、長時間のキャプチャに備えて、AVDの2つの設定を確認します。

## PCのキーボードで入力する

- AVDを作るときに「Enable Keyboard Input」を有効にします。作成済みのAVDなら、Device ManagerでAVDの編集（鉛筆）→「Show Advanced Settings」→「Keyboard」→「Enable Keyboard Input」を確認して保存し、AVDを再起動します。
- AVDのウィンドウを前面にしてから入力欄をクリックし、PCのキーボードで入力します。AVDのウィンドウにフォーカスがないと入力されません。
- 組み合わせキーがエミュレーター側のショートカットとして扱われる場合は、エミュレーターの「…」→「Settings」→「General」→「Send keyboard shortcuts to」を見直します。
- ソフトウェアキーボードを使う場合は、入力欄をタップします。キーボードが出ない場合でも、まずPCキーボードの入力が有効かを確認してください。

AVDの詳細設定とキーボード入力の説明は、[AVD公式ガイド](https://developer.android.com/studio/run/managing-avds)にあります。

## リーダーアプリのログイン欄でかな入力から英数字へ切り替える

リーダーアプリのID・パスワード欄にかな文字しか入らない場合は、**AVD画面内のキーボード**と**Windows側の日本語IME**のどちらがかな入力になっているかを確認します。Androidやリーダーアプリの表示言語を日本語のままにして、入力方法だけを切り替えられます。

**AVD画面にかなキーボードが表示されている場合（Gboard）**

1. リーダーアプリの入力欄をタップし、AVD画面にキーボードを表示します。
2. キーボードの**スペースキーを長押し**し、言語の一覧から **English (US)** などの英語キーボードを選びます。地球儀キーが表示されていれば、それでも言語を切り替えられます。
3. 英語が一覧にない場合は、キーボードの歯車からGboardの設定を開き、**言語 → キーボードを追加 → English (US) → QWERTY** を追加してから手順2を行います。表示名はGboardの版によって多少異なります。

参考：[Gboard公式ヘルプ：別の言語で入力する](https://support.google.com/gboard/answer/7068494?hl=ja)

**PCのキーボードで入力する場合**

1. AVDの外で、Windowsのタスクバーにある入力言語を確認します。日本語IMEが「**あ**」なら「**A**」（英数字入力）へ切り替えます。英語キーボードをWindowsに追加済みなら、**Windowsキー＋Space** で「ENG」を選ぶこともできます。
2. AVDのウィンドウを前面にし、リーダーアプリの入力欄をクリックしてPCのキーボードで入力します。入力されなければ、この章の「Enable Keyboard Input」とAVDへのフォーカスを確認します。

参考：[Microsoft 日本語IME](https://support.microsoft.com/ja-jp/windows/hardware/input-devices/microsoft-japanese-ime)、[Windowsの入力言語切り替え](https://support.microsoft.com/en-us/windows/hardware/input-devices/advanced-input-methods-for-east-asian-languages)

> 🔑 ID・パスワード・認証コードはAVDへ直接入力してください。ebook2xtcやサポートのチャットへ送らないでください。

## キャプチャ中にAVDの画面が消えないようにする

1. AVDの「Settings（設定）」→「About phone（デバイス情報）」または「About emulated device（エミュレートされたデバイス情報）」→「Build number（ビルド番号）」を開き、ビルド番号を7回タップします。画面ロックの確認が出たら、AVDの設定に従います。これで「Developer options」が表示されます。
2. 「Settings（設定）」→「System（システム）」→「Developer options（開発者向けオプション）」→「Stay awake（充電中は画面をスリープにしない）」をオンにします。
3. Windows PC自体がスリープすると、キャプチャは止まります。連続取得の間は、ebook2xtcがWindowsにスリープしないよう求めるので、電源設定を変えなくても、操作しないまま取得を続けられます。止めると元に戻ります。
   - 画面の消灯は止めません。画面が消えても取得は続きます。
   - ノートPCのふたを閉じたとき、電源ボタンを押したとき、バッテリー残量が少なくなったときは、設定どおりにスリープします。長時間の取得では、電源につないで、ふたを開けたままにしてください。
   - 連続取得を止めて⑥でリーダーアプリを調整している間などは、通常の電源設定でスリープします。

> 🔋 **「Stay awake」は充電中に働きます**: 通常、AVDは充電状態ですが、それでも消灯する場合は、エミュレーター右側の「…」→「Battery」で「Charger connection」を「AC charger」、「Battery status」を「Charging」にします。

作業が終わったら、必要に応じて設定を元へ戻します。参考：[Android公式の開発者向けオプションの説明](https://developer.android.com/studio/debug/dev-options)、[エミュレーターの拡張コントロール](https://developer.android.com/studio/run/emulator-extended-controls)
