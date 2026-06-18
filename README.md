# td-color-picker

ブラウザで完結するカラーピッカー。

- **スタンドアロン版**(GitHub Pages 公開): https://tsumikiroom.github.io/td-color-picker/
- TouchDesigner 連動版: `td.html`(WebSocket で TD に色を送る、TD 側のサーバー必要)

## スタンドアロン版の機能

- SV 平面 + Hue スライダーで HSV 選択
- HEX / RGB (0-255, 0-1) / HSV (度%, 0-1 TD用) を表示、**クリックでクリップボードコピー**
- **画面スポイト**(Chrome / Edge の EyeDropper API)
- **画像スポイト**: ドロップ または Ctrl+V → クリックで吸う
- パレット保存(localStorage、右クリックで削除)

## ローカルで開く

```
index.html をブラウザで開くだけ
```

## TD 連動版(td.html)

`color_picker.toe` を起動して、WebServer DAT が立てた URL から `td.html` を開く想定。
ローカル運用前提のため Pages では使えない(WebSocket は wss / 同ホスト制約あり)。

## ファイル構成

- `index.html` — スタンドアロン版(picker.html と同じ内容、Pages のデフォルト)
- `picker.html` — スタンドアロン版(同上、明示的なファイル名)
- `td.html` — TouchDesigner 連動版
- `color_picker.toe` — TouchDesigner プロジェクト本体(.gitignore で除外)
