# Nape firmware

`main`は従来のNape／ZMK Studio向け設定です。過去にこのリポジトリをforkした方のビルドを急に変えないため、Nape Console対応のβ版は`console-beta`ブランチに分けています。

## Nape Console β版

`console-beta`のGitHub Actionsは`nape-console.uf2`をビルドします。ファームウェアのZMK fork、トラックボールドライバー、RGBドライバーは`config/west.yml`のコミットSHAで固定しています。設定画面は[Nape Console](https://menbou0202.github.io/nape-console/)です。デスクトップ版Chrome／Edgeで開き、対応UF2を書き込んだNapeをUSB接続してください。

既存の`nape.uf2`や`nape-studio.uf2`にはConsole専用のCombo・ランタイム設定RPCがありません。従来版を使い続ける場合、`main`のままで構いません。

### 自分のforkでビルドする場合

自分のforkに`console-beta`ブランチを取り込み、Actionsを有効にしてください。既存forkを`main`で同期するだけでは、新しい別ブランチは自動的には追加されません。GitHub Actionsの「Build ZMK firmware」から`console-beta`を選んで手動実行するか、そのブランチへpushします。完成した`nape-console.uf2`は実行結果の`firmware`成果物に入ります。

ファームウェアを書き込むだけなら、自分でビルドする必要はありません。βリリースに添付された`nape-console.uf2`を使えます。

### 保存設定と復旧

ConsoleのSaveはキーマップ・Combo・ランタイム設定を本体に保存します。通常のUF2書き込みでは保存データは消えません。起動に問題が出たときは、動作を確認済みの従来版UF2に戻してください。設定の全消去はBluetoothペアリングなども消えるため、先にIssueで状況をご連絡ください。

## 開発元

Nape Consoleは[ZMK Studio](https://github.com/zmkfirmware/zmk-studio)を基にしています。Console版ZMKの変更は[menbou0202/zmk](https://github.com/menbou0202/zmk)の`console-beta`ブランチにあります。
