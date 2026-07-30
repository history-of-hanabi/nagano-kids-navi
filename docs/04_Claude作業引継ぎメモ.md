# 長野市キッズナビ｜04_Claude作業引継ぎメモ

**位置づけ**：正式なルールは `01_プロジェクト憲章.md`（理念・ブランド・禁止語彙）、
`02_サイト設計書.md`（IA・ページ構成・導線）、`03_制作ガイドライン.md`（実装ルール・
品質基準・テンプレート、v1.2で記事テンプレート等を追加）の3文書が最上位です。
本メモはそれらに含めるには変化が速すぎる「運用状況・実務メモ」を独立して管理する
ためのものです。内容が3文書と矛盾する場合は3文書を優先してください。

作成・更新：2026年7月時点。公開ページが増えるたびに9・10節を更新する。

---

## 1. サイト概要（要点）

- サイト名：長野市キッズナビ
- 運営：花火歴史家（長野市在住の保護者、個人運営、モバイル専業・PC/端末なし）
- ホスティング：GitHub Pages（アカウント/リポジトリ：`nagano-kids-navi`）
- 公開URL：`https://nagano-kids-navi.github.io/nagano-kids-navi/`
- ワークフロー：Claude＝HTML実装・修正・コード最適化、ChatGPT＝設計・レビュー・
  品質管理・ブランド管理（詳細な役割分担は7節）

詳細（ブランドコピー・禁止語彙・理念）は `01_プロジェクト憲章.md` を参照。

## 2. サイト構造（IA）参照

主カテゴリ＝独立ハブページ（4つ、これ以上増やさない）：
`worries/`（お悩み別ガイド）、`methods/`（学び方ガイド）、
`institutions/`（相談先・支援機関）、`glossary/`（教育の基礎知識）

横断条件（タグ、独立ハブではない）：`ages/`（学年・年齢）、`areas/`（地域）

詳細な役割分担・導線設計は `02_サイト設計書.md` を参照。記事テンプレート4種
（glossary型／worries型／methods型／institutions型）の具体的な構成は
`03_制作ガイドライン.md`（v1.2）を参照。

## 3. 現在の公開済みページ一覧（2026年7月時点、計18ページ）

**トップ・ハブ（5）**
- `index.html`
- `worries/index.html`
- `methods/index.html`
- `institutions/index.html`
- `glossary/index.html`

**個別記事（13）**

| ページ | ハブ | 型 |
|---|---|---|
| `glossary/futoukou.html`（不登校とは） | glossary | glossary型 |
| `worries/futoukou.html`（不登校） | worries | worries型 |
| `methods/gakkou.html`（学校での学び） | methods | methods型 |
| `institutions/kyouiku-shien-center.html`（教育支援センター：特徴・流れ） | institutions | institutions型 |
| `glossary/hattatsu-shougai.html`（発達障害とは） | glossary | glossary型 |
| `worries/hattatsu-gray.html`（発達障害・グレーゾーン） | worries | worries型 |
| `methods/katei.html`（家庭での学び） | methods | methods型 |
| `institutions/gakkou.html`（学校＝相談窓口として） | institutions | institutions型 |
| `glossary/tsushin-kyouiku.html`（通信教育とは） | glossary | glossary型 |
| `glossary/kyouiku-shien-center.html`（教育支援センターとは：用語・名称変遷） | glossary | glossary型 |
| `worries/katei-gakushu.html`（家庭学習） | worries | worries型 |
| `methods/minkan.html`（民間のサービスを活用した学び） | methods | methods型 |
| `institutions/minkan-soudan.html`（民間相談機関） | institutions | institutions型 |

## 4. 各ハブの空きスロット（次の優先候補）

各ハブのカード（`id`属性）は既にリンク先を確定済み。新しい個別記事は、必ずこの中から
選ぶこと（ハブに対応スロットのないテーマを書くと孤立記事になるため、新テーマを追加
したい場合はハブのカード構成自体の見直しを先に相談する）。

- **worries** 残り：`benkyou-tsuiteikenai`（勉強についていけない）、`koukou-juken`（高校受験）
- **methods** 残り：`chiiki`（地域での学び）
- **institutions** 残り：`gyousei`（行政機関）、`chiiki-soudan`（地域の相談先）
- **glossary** 残り：`katei-gakushu`（家庭学習とは）

上記6本を埋め終えると、4ハブ×5カードの構成が完全に埋まる（methodsのみ4カード）。
その後、サイトが育ってSearch Consoleのデータが集まった段階で、フリースクール・
オンライン学習・グレーゾーン単独記事などの新カテゴリ追加を検討する（現段階では見送り）。

## 5. 今後のToDo（サイト運営者側の作業）

- Search Console：sitemap.xml送信、公開記事のURL検査・インデックス登録リクエスト
- articles/index.html・diagnosis.htmlの実装（完了後、footerのリンク復帰。
  復帰手順は `03_制作ガイドライン.md` footer運用ルールを参照）
- ages/areasページの実装（横断タグとして。独立ハブにしないこと）
- 各ハブの空きスロット6本（4節参照）を埋め終えたら、プロジェクト憲章15節の
  「カテゴリ完成」の節目にあたるため、新規チャットへの移行を検討する

## 6. Claude実装時の細かい注意点（申し送りベース、まだ正式ルール化していないもの）

- 禁止語彙チェック時は活用形（例：「選ぶ」だけでなく「選べる」「選び方」）も
  漏れなく確認する。憲章6節のリストは終止形のみのため、機械チェック時は
  活用形も含めたリストを使うこと。
- 定義文（用語・機関の説明）は記事内で1箇所に統一し、summary-boxと本文で
  表現がずれないようにする。
- 「〇〇や相談先に相談」等、同一フレーズの反復をシリーズ全体で避ける。
  特に同じハブ内で複数記事を続けて書くときは、直前の記事と表現が重複していないか
  確認する。

## 7. 役割分担（運用実績ベース）

**設計担当（現時点ではChatGPT）**
- IA設計（サイト構造・ハブ設計）
- 新規記事の設計（構成案・切り口の提案）
- SEOレビュー（title・description・構造化データ・内部リンク設計）
- 品質管理（禁止語彙・YMYL配慮・表現の中立性）
- ブランドガイド管理（語彙・トーン・ブランドコピーの一貫性）
- 実装担当の成果物のレビュー・改善提案
- サイト全体との整合性確認（IA・テンプレート・既存記事との重複有無）

**実装担当（現時点ではClaude）**
- HTML実装（テンプレートに沿った新規記事・修正の実装）
- 機械チェック（FAQ完全一致・禁止語彙・内部リンク生存確認等）
- sitemap.xml・footer等の付随ファイルの同時更新
- 実装上の制約発見時の事前確認（例：未公開ページへのリンク、ハブに対応
  スロットのないテーマの検出）

担当するAIツール自体が将来変わる可能性があるため、この文書では固有名詞では
なく役割名で管理する。

## 8. 参照文書一覧

| 文書 | バージョン | 内容 |
|---|---|---|
| `01_プロジェクト憲章.md` | v1.1 | 理念・ブランド・禁止語彙 |
| `02_サイト設計書.md` | v1.1 | IA・ページ構成・導線 |
| `03_制作ガイドライン.md` | v1.2（更新予定） | 実装ルール・品質基準・記事テンプレート4種 |
| `04_Claude作業引継ぎメモ.md`（本書） | 随時更新 | 公開状況・実務メモ |

## 9. バージョン管理ルール

Version番号（v1.1、v1.2等）は、正式文書（01・02・03）のみに付与する。
本書（04）は運用メモのため、Version番号は付けず、内容を更新した際は
冒頭の「作成・更新」の日付のみを最新の更新日に書き換える。

## 10. 更新履歴（主要変更のみ）

Versionを振るほどではない変更を、日付とともに残す運用ログ。GitHubのコミット
履歴とは別に、人間が「いつ何が変わったか」を後から追うためのもの。

- **2026-07-23**
  - 優先5記事（glossary/futoukou・worries/futoukou・methods/gakkou・
    institutions/kyouiku-shien-center・glossary/hattatsu-shougai）公開完了
  - 追加4記事（worries/hattatsu-gray・methods/katei・institutions/gakkou・
    glossary/tsushin-kyouiku）公開完了
  - 追加4記事（glossary/kyouiku-shien-center・worries/katei-gakushu・
    methods/minkan・institutions/minkan-soudan）公開完了
  - FAQ本文とJSON-LDの完全一致チェック（機械チェック）を標準運用として確立
  - footer運用ルール（未公開ページリンクの一時除外・復帰コメント）を確立
  - `03_制作ガイドライン.md` v1.2へ、記事テンプレート4種・品質チェックリスト等を移管
  - 文書体系を01〜04の4層に整理
