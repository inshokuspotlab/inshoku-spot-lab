# 飲食スポットlab. ランディングページ

飲食店向け「スポットワーカー受入診断」サービスのランディングページです。
HTML / CSS / JavaScript を 1 ファイル（`index.html`）に内包しており、外部ビルド不要でそのまま公開できます。

## 公開方法（GitHub Pages）

1. このリポジトリを GitHub に push
2. リポジトリの **Settings → Pages** を開く
3. **Source** を `Deploy from a branch` にし、Branch を `main` / フォルダを `/ (root)` に設定
4. 数十秒後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます

## 編集ポイント

| 内容 | 場所 |
|---|---|
| 予約フォームURL | `index.html` 末尾の `<script>` 内 `YOUR_GOOGLE_FORM_URL` を書き換え |
| ブランドカラー | `<style>` 冒頭の `:root`（`--navy` / `--blue` など） |
| 料金 | `<!-- 料金 -->` セクション内、各カードの `<span class="val">` の数字 |
| キャッチコピー・各文言 | 該当セクションのテキストを直接編集 |

## 予約フォームURLの設定

`index.html` の最下部にある以下を、実際の Google フォーム等の URL に書き換えてください。

```js
var YOUR_GOOGLE_FORM_URL = "YOUR_GOOGLE_FORM_URL";
```

未設定のままでも、CTA ボタンはページ内の相談セクションへスクロールするフォールバックが効きます。

## 特徴

- 青・紺基調 / 白背景 / 余白広め のコンサルティング会社風デザイン
- スマホファースト・レスポンシブ対応
- 写真ゼロ・インラインSVGアイコン中心で高速表示（外部リクエストなし）
- SEO対策（title / meta description / OGP / 構造化データ JSON-LD）
- アニメーションは控えめ（`prefers-reduced-motion` 対応）
- 複数箇所に問い合わせ導線（ヘッダー・ヒーロー・流れ・最終CTA・フッター・モバイル固定ボタン）
