# Nape Console β1 — リリース文案

Nape Console対応ファームウェアのβ版です。Napeのキーマップ、Combo、Hold-Tapのタイミング、トラックボールのDPI、起動時の角度レイヤーをUSB接続で変更できます。

## 使い方

1. このリリースの`nape-console.uf2`をNapeに書き込みます。
2. デスクトップ版Chrome／Edgeで[Nape Console](https://menbou0202.github.io/nape-console/)を開き、NapeをUSB接続します。
3. Unlockして編集します。電源を切った後も変更を残す場合は画面右上のSaveを押します。

従来版`nape.uf2`はそのまま使えます。Consoleを使わない利用者は更新不要です。自分でビルドする場合は`console-beta`ブランチのGitHub Actionsを使用してください。

## 対応するソース

- Firmware build source: `menbou0202/zmk-config-nape` `console-beta` — `362f899420d14cae4a66f5c05ca7f021a4bca61e`（[Actionsの成功した実行](https://github.com/menbou0202/zmk-config-nape/actions/runs/36231883233)）
- ZMK fork: `menbou0202/zmk` `console-beta` — `b3544e343c28580a2f5e68c23e83d6f175b8595f`
- Trackball driver: `menbou0202/zmk-pmw3610-driver-nape` `console-beta` — `4be9979b9ff008b209de8c523ab2665da1adc28e`
- Web UI: `menbou0202/nape-console` — `64fcd9f5e1265118d5d3f5a19d8fc123f803b483`

この文案で配布を想定しているローカルビルドUF2のSHA-256: `4b003fb2d793901d46de5afbb4b505aa566cf812ead8dbcb59a54b399d54513b`。Actionsの`firmware`成果物内のUF2とはハッシュが異なる可能性があるため、実際に添付するファイルを確認してください。

## β版の注意

- 対応ブラウザーはデスクトップ版Chrome／Edge。設定時の接続はUSBです。
- 通常のUF2再書き込みでは本体の保存設定は消えません。起動できない場合は動作確認済みの従来版UF2へ戻し、Issueでご連絡ください。全設定消去はBluetoothペアリングなども消します。
- 公開URLでの実機接続とActions生成UF2の実機書き込みは、公開前の最終確認項目です。
