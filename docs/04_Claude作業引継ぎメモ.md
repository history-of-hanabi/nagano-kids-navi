長野市キッズナビ｜04_Claude作業引継ぎメモ

位置づけ：正式なルールは 01_プロジェクト憲章.md（理念・ブランド・禁止語彙）、
02_サイト設計書.md（IA・ページ構成・導線）、03_制作ガイドライン.md（実装ルール・
品質基準・テンプレート、v1.2で記事テンプレート等を追加）の3文書が最上位です。
本メモはそれらに含めるには変化が速すぎる「運用状況・実務メモ」を独立して管理する
ためのものです。内容が3文書と矛盾する場合は3文書を優先してください。

作成・更新：2026年8月2日時点。公開ページが増えるたびに9・10節を更新する。

1. サイト概要（要点）
サイト名：長野市キッズナビ
運営：花火歴史家（長野市在住の保護者、個人運営、モバイル専業・PC/端末なし）
ホスティング：GitHub Pages（アカウント/リポジトリ：nagano-kids-navi）
公開URL：https://nagano-kids-navi.github.io/nagano-kids-navi/
ワークフロー：Claude＝HTML実装・修正・コード最適化、ChatGPT＝設計・レビュー・
品質管理・ブランド管理（詳細な役割分担は7節）
詳細（ブランドコピー・禁止語彙・理念）は 01_プロジェクト憲章.md を参照。

2. サイト構造（IA）参照
主カテゴリ＝独立ハブページ（4つ、これ以上増やさない）：
worries/（お悩み別ガイド）、methods/（学び方ガイド）、
institutions/（相談先・支援機関）、glossary/（教育の基礎知識）

横断条件（タグ、独立ハブではない）：ages/（学年・年齢）、areas/（地域）

詳細な役割分担・導線設計は 02_サイト設計書.md を参照。記事テンプレート4種
（glossary型／worries型／methods型／institutions型）の具体的な構成は
03_制作ガイドライン.md（v1.2）を参照。

3. 現在の公開済みページ一覧（2026年8月2日時点、計26ページ）
トップ・ハブ（5）

index.html
worries/index.html
methods/index.html
institutions/index.html
glossary/index.html

補助導線（2）

articles/index.html（記事一覧。カテゴリ別に19記事へのリンクを整理。
  記事本文の代替にはしない位置づけ／サイト設計書11節）
diagnosis.html（学び方診断。Q1悩み→Q2学び方→Q3相談先の3問構成、
  結果画面下にglossary5記事を常設。診断ではなく考えるヒントを示す位置づけ
  ／サイト設計書10節）

個別記事（19）

ページ	ハブ	型
glossary/futoukou.html（不登校とは）	glossary	glossary型
worries/futoukou.html（不登校）	worries	worries型
methods/gakkou.html（学校での学び）	methods	methods型
institutions/kyouiku-shien-center.html（教育支援センター：特徴・流れ）	institutions	institutions型
glossary/hattatsu-shougai.html（発達障害とは）	glossary	glossary型
worries/hattatsu-gray.html（発達障害・グレーゾーン）	worries	worries型
methods/katei.html（家庭での学び）	methods	methods型
institutions/gakkou.html（学校＝相談窓口として）	institutions	institutions型
glossary/tsushin-kyouiku.html（通信教育とは）	glossary	glossary型
glossary/kyouiku-shien-center.html（教育支援センターとは：用語・名称変遷）	glossary	glossary型
worries/katei-gakushu.html（家庭学習）	worries	worries型
methods/minkan.html（民間のサービスを活用した学び）	methods	methods型
institutions/minkan-soudan.html（民間相談機関）	institutions	institutions型
worries/benkyou-tsuiteikenai.html（勉強についていけない）	worries	worries型
worries/koukou-juken.html（高校受験）	worries	worries型
glossary/katei-gakushu.html（家庭学習とは）	glossary	glossary型
methods/chiiki.html（地域での学び）	methods	methods型
institutions/gyousei.html（行政機関）	institutions	institutions型
institutions/chiiki-soudan.html（地域の相談先）	institutions	institutions型

4. 各ハブの空きスロット
空きスロットなし。4ハブ×5カード（methodsのみ4カード）構成が2026年7月31日時点で
完成した。

カテゴリ構成確定：
worries（5カード）：futoukou／hattatsu-gray／katei-gakushu／
  benkyou-tsuiteikenai／koukou-juken
methods（4カード）：gakkou／katei／minkan／chiiki
institutions（5カード）：kyouiku-shien-center／gakkou／minkan-soudan／
  gyousei／chiiki-soudan
glossary（5カード）：futoukou／hattatsu-shougai／tsushin-kyouiku／
  kyouiku-shien-center／katei-gakushu

今後、サイトが育ってSearch Consoleのデータが集まった段階で、フリースクール・
オンライン学習・グレーゾーン単独記事などの新カテゴリ追加を検討する（現段階では
見送り）。

5. 今後のToDo（サイト運営者側の作業、優先順位順）
Search Console：sitemap.xml送信、公開記事のURL検査・インデックス登録リクエスト
記事一覧（articles/index.html）の実装
学び方診断（diagnosis.html）の実装
footer復帰ルール（v1.0で確立、ここで明文化）：articles/index.html単体の完成
  時点ではfooterのリンクは復帰させない。diagnosis.htmlが完成し、両方が揃った
  タイミングで、全ページのfooterを一括で復帰させる（復帰手順は
  03_制作ガイドライン.md footer運用ルールを参照）。
ages/areasページの実装（横断タグとして。独立ハブにしないこと）
E-E-A-T強化（出典表記・運営者情報・監修方針・更新履歴等）の各記事への追加
Search Consoleのデータを見ながらのリライト・内部リンク改善

6. Claude実装時の細かい注意点（申し送りベース、まだ正式ルール化していないもの）
禁止語彙チェック時は活用形（例：「選ぶ」だけでなく「選べる」「選び方」）も
漏れなく確認する。憲章6節のリストは終止形のみのため、機械チェック時は
活用形も含めたリストを使うこと。
定義文（用語・機関の説明）は記事内で1箇所に統一し、summary-boxと本文で
表現がずれないようにする。
「〇〇や相談先に相談」等、同一フレーズの反復をシリーズ全体で避ける。
特に同じハブ内で複数記事を続けて書くときは、直前の記事と表現が重複していないか
確認する。CTA文言も同一ハブ内で使い回さない（例：institutionsは記事ごとに
「他の相談先も見てみる」「相談先・支援機関に戻る」「相談先・支援機関の一覧を
見る」と変えている）。
info-box等のcard-labelは、直上のh2見出しと同一文言にしない（見出しと
card-labelは役割が異なるため、別表現にする）。
「大切です」「必要です」「おすすめします」等の断定的な結び表現は、サイトの
「一緒に考える」思想と衝突しやすいため、「〜考えていくとよいでしょう」
「〜方法もあります」「〜一つです」等に置き換える方針とする（2026-07-30の
編集レビューで確立）。

7. 役割分担（運用実績ベース）
設計担当（現時点ではChatGPT）

IA設計（サイト構造・ハブ設計）
新規記事の設計（構成案・切り口の提案）
SEOレビュー（title・description・構造化データ・内部リンク設計）
品質管理（禁止語彙・YMYL配慮・表現の中立性）
ブランドガイド管理（語彙・トーン・ブランドコピーの一貫性）
実装担当の成果物のレビュー・改善提案
サイト全体との整合性確認（IA・テンプレート・既存記事との重複有無）

実装担当（現時点ではClaude）

HTML実装（テンプレートに沿った新規記事・修正の実装）
機械チェック（FAQ完全一致・禁止語彙・内部リンク生存確認等）
sitemap.xml・footer等の付随ファイルの同時更新
実装上の制約発見時の事前確認（例：未公開ページへのリンク、ハブに対応
スロットのないテーマの検出）

担当するAIツール自体が将来変わる可能性があるため、この文書では固有名詞では
なく役割名で管理する。

8. 参照文書一覧
文書	バージョン	内容
01_プロジェクト憲章.md	v1.1	理念・ブランド・禁止語彙
02_サイト設計書.md	v1.1	IA・ページ構成・導線
03_制作ガイドライン.md	v1.2	実装ルール・品質基準・記事テンプレート4種
04_Claude作業引継ぎメモ.md（本書）	随時更新	公開状況・実務メモ

9. バージョン管理ルール
Version番号（v1.1、v1.2等）は、正式文書（01・02・03）のみに付与する。
本書（04）は運用メモのため、Version番号は付けず、内容を更新した際は
冒頭の「作成・更新」の日付のみを最新の更新日に書き換える。

9.5. 第2フェーズ改善候補（メモ）
第1フェーズでは実装を見送り、Search Consoleなどの利用状況を見ながら
第2フェーズで検討する項目。

改善候補：診断結果と連動したglossary記事の提示
現在はdiagnosis.htmlの結果画面下にglossary5記事を常設表示している。
将来的には診断結果（特にQ1の回答）に応じて関連するglossary記事を1件
優先表示し、常設一覧との併用方法（重複表示・表示順・UI）を再設計する。

10. 更新履歴（主要変更のみ）
Versionを振るほどではない変更を、日付とともに残す運用ログ。GitHubのコミット
履歴とは別に、人間が「いつ何が変わったか」を後から追うためのもの。

2026-08-02
design-system.cssの記述漏れを発見・対処法を記録：`.about__list`内の`<a>`に
  色指定がなく、related-link-box等の「次に読みたい記事」リンクがグレーの
  地の文と同化して見える不具合。サイト全体（公開済み全記事）に影響。
  design-system.cssへ`.about__list a`・`.about__text a`にブランドブルー
  （--color-blue-deep）を指定するルールを追加することで、個別HTMLを
  変更せず一括解決できることを確認・提案
diagnosis.html（学び方診断）公開完了。第一フェーズの全ページ（26ページ）が
  出揃い、footer復帰ルールに基づき全ページのfooterを一括復帰
diagnosis.htmlはQ1（悩み・worries、6択）→Q2（学び方・methods、5択）→
  Q3（相談先・institutions、6択）の3問構成。結果画面下にglossary5記事を
  常設リンクとして掲載し、公開済み19記事のほぼ全てに直接導線を確保
Q1・Q3の「困りごと／相談先が特にない」選択肢がどちらもmethods/index.htmlを
  指すケースで結果が重複表示される不具合を修正（href基準の重複除去ロジックを
  追加）
sitemap.xmlにdiagnosis.htmlを追加し、コメントを「全ページ公開済み」の状態に
  更新。全26URL
第2フェーズ改善候補（診断結果連動glossary表示）を9.5節に記録
articles/index.html（記事一覧）公開完了。カテゴリ別に19記事へのリンクを整理
sitemap.xmlにarticles/index.htmlを追加（lastmod 2026-08-02、
  changefreq weekly、priority 0.6）。全25URLに更新
sitemap.xmlの冒頭コメントを実態（個別記事19本・articles/index.html公開済み、
  diagnosis.htmlのみ未公開）に合わせて修正
footer復帰ルールを明文化：articles/index.html単体では復帰させず、
  diagnosis.html完成と同時に全ページ一括で復帰する

2026-07-31
worries残り2記事（benkyou-tsuiteikenai・koukou-juken）公開完了、
  worriesカテゴリ完成（5カード）
glossary残り1記事（katei-gakushu）公開完了、glossaryカテゴリ完成（5カード）
methods残り1記事（chiiki）公開完了、methodsカテゴリ完成（4カード）
institutions残り2記事（gyousei・chiiki-soudan）公開完了、institutions
  カテゴリ完成（5カード）
4ハブ×19個別記事（トップ・ハブ含め計24ページ）の第一フェーズが完成
sitemap.xml、24URLに更新（重複なし・lastmod整合済み）
「家庭学習」というテーマで worries／methods／glossary の3方向リンクを構築
「地域の相談先」で institutions の役割分担（学校／教育支援センター／行政機関／
  民間相談機関／地域の相談先）が完成
編集レビューを経て、断定表現（大切です／必要です／おすすめします）を避ける
  方針、card-labelと見出しの重複回避、CTA文言のハブ内使い回し回避を確立
次フェーズ優先順位を確定：①記事一覧 ②学び方診断 ③E-E-A-T強化
  ④Search Consoleを見ながらのリライト

2026-07-23
優先5記事（glossary/futoukou・worries/futoukou・methods/gakkou・
institutions/kyouiku-shien-center・glossary/hattatsu-shougai）公開完了
追加4記事（worries/hattatsu-gray・methods/katei・institutions/gakkou・
glossary/tsushin-kyouiku）公開完了
追加4記事（glossary/kyouiku-shien-center・worries/katei-gakushu・
methods/minkan・institutions/minkan-soudan）公開完了
FAQ本文とJSON-LDの完全一致チェック（機械チェック）を標準運用として確立
footer運用ルール（未公開ページリンクの一時除外・復帰コメント）を確立
03_制作ガイドライン.md v1.2へ、記事テンプレート4種・品質チェックリスト等を移管
文書体系を01〜04の4層に整理
