verdict: PUBLIC_REVIEW_APPROVED

# JA-01 / Ameba Blog — 独立公開R-P 001

public_url: `https://ameblo.jp/videowebai/entry-12978310398.html`  
human_acceptance_status: MISSING

## 読み取り方法と境界

2026-09-10T04:06:41.521506Z に、認証なし・読み取り専用のHTTPS GETで読者HTMLを独立取得した。HTTP 200、raw SHA-256は `d820bc5362717dba3a7dc7a60395f0e92891eff0db86aa36e7435283f8bd8ab3`、ETagは `W/"1a9b2-PjlRQ9/opGHR+Wrje9wOQLBIem8"` である。完全な再現用の比較値とDOM抽出は `evidence/public-reader-001.json` に保存した。ログイン、ブラウザ/CU/CDP、editor、アップロード、削除、再投稿その他の外部書込みは行っていない。

これはpublisher receiptではなく、現在の匿名読者応答に基づく技術的R-Pである。ただし人手による `HUMAN_ACCEPTED` は渡されておらず、公開完了、`PUBLIC_QA_PASSED`、又は人手受諾を意味しない。

## canonicalとの読者面照合

- `html[lang]` は `ja`。読者H1はcanonical titleと完全一致し、document titleは同じ題名にAmebaブログ接尾辞を加えたものだった。
- 公開 `#entryBody` は、canonical本文からH1と画像を除く既定の構造正規化で同じSHA-256 `5f9aa553618fde2b016e114bbc34c989768e0c437f85a0cc5ab61457be96c74d` になった。本文順・日本語・founder開示・非テスト/非品質比較/非推奨開示に差異はない。
- H2は6、H3は3で、全ての見出し文言と順序はcanonical mapに一致する。
- 読者本文のVideoWeb宛hrefは次の2本だけで、説明的アンカーと各1回の配置を確認した：`VideoWebのSeedance 2.5提供ページ` → `https://videoweb.ai/model/seedance-2-5/`、`VideoWebのMiniMax H3提供ページ` → `https://videoweb.ai/model/minimax-h3/`。画像CDNへの空アンカーは編集リンクではない。Flyne、FLAQ、UGCMaker、BestImageその他の旧ブランド/リンクは本文にない。
- 読者HTML（noscript fallbackを除外）にはLEAD、MIDDLE、CLOSINGの順に3画像があり、各ALTはfingerprintの完全な日本語ALTと一致する。3つの「AI生成の編集用イラスト…」図注も本文順に存在する。HTMLにおける画像要素の表示属性は各420×236で、16:9のサムネイル表示と整合する。

公開HTMLは各画像のnoscript fallbackを重複して含むが、通常のreader-source要素は3件であり、公開本文の画像重複を示す証拠ではない。今回の認証なしHTTPスコープでは、リモート画像バイト/最終描画ピクセルを再取得していない。そのため、公開sourceにおける画像URL・順序・ALT・図注は確認済みだが、ブラウザでの最終painted pixelsはこのR-Pの未確認限界として残す。

## native tags・コメント

`AI動画生成`、`商品紹介動画`、`参考写真`、`動画プロンプト` の4タグ、および空白を含む2 rawタグの非代替省略は、controller承認済みの `APPROVED_NATIVE_FIELD_ADAPTATION` として受け入れる。これはcanonical metadataの改変や失敗ではない。この匿名読者HTMLにはタグ表示を確認できなかったため、public tag visibilityは **UNVERIFIED**。同じく、コメントの表示/可否はこの読者HTMLからは **UNVERIFIED** であり、publisher記録を独立の証明にはしていない。

## findingと次段階

公開読者sourceとcanonicalの技術照合にはOPEN findingがない。`human_acceptance_status: MISSING` は別の明示的な手渡し条件として残る。人手が `HUMAN_ACCEPTED` を明示して初めて、fresh G-Pがその受諾と公開reader結果を別途評価できる。
