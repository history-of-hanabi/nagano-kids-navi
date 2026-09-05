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

2026-08-02（追記21）
トップページを2点修正：
  - H1を「長野市で、お子さまに合った学びを、一緒に考える。」から
    「長野市の子どもの学び・教育情報」に変更。旧コピーはサブコピー
    （hero__lead）に移動し、「お子さまに合った学びを、一緒に考える。」
    「学び方から相談先まで、子どもの教育について考えるヒントを
    お届けします。」の2文構成にした。初見の訪問者が3秒でサイトの
    正体を判断できるようにする狙い（運営者・設計担当との協議）
  - 「体験談・コラム」のトップページカードを、related-link-box
    （補助的な見た目）からnav-card構造に変更。主要4カテゴリ・ages
    カードと同じ余白・枠・タイトル・説明文の構造に統一し、視覚的な
    不統一感を解消。ただし情報設計上は主要4カテゴリと別系統のまま
    維持（「情報設計は別、デザインシステムは共通」という方針）。
    絵文字は使わず、「談」という文字アイコンを使用

2026-08-02（追記20）
「体験談・コラム」をサイト全体へ正式統合。
  - column/shiteikou-henkou.html：「指定校変更を希望していると伝えたので
    その後の相談もスムーズだった」という評価表現を、事実ベース
    （「そのときは指定校変更を希望していると伝えました」）に修正。
    体験談としての評価と、ノウハウ的な助言に読める記述を切り分けた
  - 既存29ページ＋column配下2ページ、計31ページのfooterに「体験談・コラム」
    リンクを一括追加（改行フォーマットも整形）
  - sitemap.xmlは追記17で追加済み（31URL）
  - トップページのcanonical等について運営者から指摘があったが、実ファイル
    確認の結果、通常のHTML形式で問題なし（チャット上の表示のみの見え方
    だったことを運営者と確認済み）
  - 02サイト設計書・03制作ガイドラインへの正式追記は、記事が増えるまで
    引き続き見送り

2026-08-02（追記19）
column/index.htmlの導入文に「制度や施設を実際に利用して分かったことなど、
  公式情報だけでは分からない『その後』の体験も記録していきます。」を追加し、
  やや具体性を持たせた（h1・HTMLコメントの設計思想・「断定的に
  おすすめするものではなく」の一文は変更せず維持）。
  column/index.html・column/shiteikou-henkou.htmlともに公開可能な品質と
  最終確認。
「体験談・コラム」カテゴリの統合作業（sitemap.xml追加・トップページへの
  独立導線追加）は追記17で完了済み。残る手順：
  ⑤GitHubへアップロード ⑥実際にページを開いて表示確認
  ⑦Search Consoleでインデックス登録をリクエスト
  footer全ページ変更・03制作ガイドラインの正式改訂は、記事が増えて
  「正式カテゴリ」と判断できる段階まで見送る

2026-08-02（追記18）
column/shiteikou-henkou.htmlの最終レビューで2点を修正：
  - 「現在の制度については、長野市の公式情報をご確認のうえ、学校教育課へ
    ご相談ください」→「制度の確認」と「自分の状況が対象かどうか」を
    分離し、「長野市の公式情報をご確認ください。ご自身の状況が対象になる
    かどうかは、学校教育課へご相談ください」に修正
  - 体験談としての正確性のため、「すぐに迎えに行ける」→「迎えに行き
    やすい」に修正（学校から職場まで45分という前段の記述と整合させる）
  それ以外の文章・出典リンク・「我が家が利用した当時の手続きと、現在の
  手続きが完全に同じとは限りません」の一文は、意図的に変更せず維持。
  体験談記事は「一次情報をそのまま残す」ことを優先し、SEO目的の一般論
  追加や過度な整文は行わない方針を確認
column/shiteikou-henkou.htmlは公開可能な品質と判断。次はSearch Console
  でのインデックス確認

2026-08-02（追記17）
新カテゴリ「体験談・コラム」を新設。第1号記事
  column/shiteikou-henkou.html（長野市の指定校変更・区域外通学の体験談）と
  ハブページcolumn/index.htmlを公開。
  運営者との協議により、今回は段階的に進める方針を確認：
  今回やる：①sitemap.xml追加 ②トップページに独立導線を追加
    （主要4カテゴリのnav-cardとは別に、related-link-boxで補助的に配置）
  今回見送る：既存28ページのfooterへの追加（記事が増えて「正式カテゴリ」
    と判断できてから）、02サイト設計書・03制作ガイドラインへの正式な
    テンプレート追記（現状はHTMLコメントに設計意図を記録）
  編集面：公式情報に基づく記述（指定校変更制度の許可事由「共働き等」）には
    長野市公式ページ（2026年2月27日更新分で内容確認済み）への出典リンクを
    追加。「体験談部分」と「公式情報部分」を明確に線引きする方針を確立
  sitemap.xmlを31URLに更新
次のステップ：④公開・表示確認 ⑤内部リンク確認（完了）⑥Search Console
  インデックス確認 ⑦しばらく運用 ⑧記事が増えたらfooter・設計書を正式更新

2026-08-02（追記16）
glossary/hattatsu-shougai.htmlを3点修正：
  - 告知バー（他4ページと同様、全用語記事完成に伴い削除）
  - 比較表「個性・特性」セルがスマホ表示で改行し、行の高さが崩れる問題を
    発見。該当セルにwhite-space: nowrapをインラインで指定し解消（同様の
    「・」を含む短い用語が他記事の比較表にもある場合、同じ崩れが起きうる
    ため、今後同種の指摘があれば同じ対処を行う）
  - FAQ「きょうだい」表記を「兄弟姉妹」に統一（worries/hattatsu-gray.html・
    worries/katei-gakushu.htmlと同じ表記ルールに合わせた）

2026-08-02（追記15）
運営者判断により、5ページ（index.html・worries/index.html・
  methods/index.html・institutions/index.html・glossary/index.html）から
  「現在、（テーマ別／用語別の）記事を順次公開中です。一部のページは近日
  公開予定です。」という告知バー（info-box site-notice）をコメントごと削除。
  4ハブすべて（worries5／methods4／institutions5／glossary5）が完成して
  いるため、元のHTMLコメントに記載されていた「将来：全テーマ記事が揃い
  次第、このブロックごと削除する」という設計意図どおりの対応

2026-08-02（追記14）
運営者判断により、index.htmlの「条件から探す」セクションから地域(areas)の
  nav-cardを削除。学年・年齢(ages)カードのみとなったため
  category-grid--singleを付与しレイアウトを統一。復帰用のコメントを残し、
  将来areasページ実装時にnav-cardを戻せるようにしている。
  これによりサイト全体でareas/index.htmlへの実リンクはゼロになった
  （未実装ページへの404導線を解消）

2026-08-02（追記13）
第二フェーズ③として ages/index.html（学年・年齢から探す）を公開。
  小学生（7本）／中学生（7本）／高校生（6本）、静的キュレーション方式で
  19記事から関連度の高いものを手動選定（タグシステムは将来の発展形として
  設計書に残し、19記事本体への学年タグ付与は行わない）。「通信教育とは」
  「行政機関」「地域の相談先」「教育支援センターとは」「家庭学習とは」は
  agesでは扱わず、各ハブ・記事一覧からの導線を維持する方針を確認
全29ページのfooterに「学年・年齢から探す」を一括追加。footerは「ホーム／
  学年・年齢から探す／記事一覧／学び方診断／プライバシーポリシー／
  運営者情報／お問い合わせ・掲載のご相談」の7項目構成で最終確定
sitemap.xmlにages/index.htmlを追加。全29URLに更新
areas（地域）は12節の方針どおり見送り。地域に紐づく記事が10〜20本程度
  増えた段階で着手する
第二フェーズ③agesが完了。次は④Search Console登録

2026-08-02（追記12）
ages/index.html公開直後、404（GitHub Pages標準）が表示される問題が発生。
  ワークフロー設定ファイル（.github/workflows）を確認したところ、
  ages/areasフォルダを除外する特別な記述は存在せず、GitHub Pages標準の
  「存在しないページは404にフォールバックする」挙動であることを確認。
  一時的にデプロイのキューが滞留していた可能性があり、削除→再アップロード
  および後続のデプロイ完了（#223等）を経て解消。運営者がGitHub Actionsの
  実行ログ・Pages公開状況を確認し、トップページ含め正常に表示されることを
  確認済み。以後、新規ページ公開後に404が出た場合は、まず数分待って
  再アクセス→解消しなければActionsタブでビルド状況を確認する、という
  対応フローとする

2026-08-02（追記11）
運営者確認により、privacy.html・about.html公開時にsitemap.xmlへの追加が
  漏れていたことが判明。両ページを追加し、全28URLに更新
  （privacy.html: priority 0.3・changefreq yearly、
  about.html: priority 0.4・changefreq yearly。更新頻度が低いページのため
  他ページより優先度・頻度を下げて設定）
  以後、新規ページ公開時はfooter更新だけでなくsitemap.xml更新も
  セットで確認するチェック項目とする（6節に追記済みの内部リンク・FAQ確認
  フローと合わせて運用する）

2026-08-02（追記10）
about.htmlの「サイトの目的」文言をレビュー・修正。
  「安心して考えられる情報サイトを目指しています」は、①「安心」の対象が
  曖昧（サイトが安心を提供するように読める）②2文目の「お届けします」と
  重複する、という2点の指摘を受け、以下に変更：
  「学び方や相談先などを考えるための情報をまとめています」／
  「（略）お子さまに合った学びを考えるためのヒントを紹介しています」。
  「安心」「正しい」「最適」等の自己評価的な語を使わず、サイトが何を
  しているかを淡々と説明する方針を確認（今後の文言判断の参考にする）

2026-08-02（追記9）
about.html公開後のレビューで3点を確認・対応：
  - 運営開始（2026年8月）・お問い合わせフォームURLは既存のままで問題なし
  - 全28ページ（第一フェーズ26ページ＋privacy.html＋about.html）のfooter先頭に
    「ホーム」リンクを一括追加。footerは「ホーム／記事一覧／学び方診断／
    プライバシーポリシー／運営者情報／お問い合わせ・掲載のご相談」の6項目構成で
    最終確定
  - about.htmlの「サイト運営者」表記を「長野市キッズナビ運営事務局（個人運営）」
    に修正（個人運営であることを明示）
第二フェーズ②運営者情報が完了。次は③ages（学年別、静的キュレーション）→
  ④Search Console登録

2026-08-02（追記8）
第二フェーズ②として about.html（運営者情報）を作成・公開。
  運営者名：長野市キッズナビ運営事務局／運営開始：2026年8月。
  目的文の原案に「比較・検討」という禁止語彙が含まれていたため、
  ブランド方針（一緒に考える）に沿って「安心して考えられる情報サイト」に修正。
  お問い合わせ窓口は既存のGoogleフォームを共通利用
全27ページ（第一フェーズ26ページ＋privacy.html）のfooterに「運営者情報」
  リンクを一括追加。footerは「記事一覧／学び方診断／プライバシーポリシー／
  運営者情報／お問い合わせ・掲載のご相談」の構成で統一
第二フェーズの次のステップは③ages（学年別、静的キュレーション）→
  ④Search Console登録

2026-08-02（追記7）
第二フェーズ①として privacy.html（プライバシーポリシー）を作成・公開。
  記載内容：個人情報の取り扱い／GA4によるアクセス解析／Googleフォームの利用／
  第三者提供／開示等の請求／免責事項／ポリシー変更／お問い合わせ窓口。
  問い合わせ窓口は既存のGoogleフォームを共通利用する方針を確認。
  GA4以外のツール導入予定は現時点でなし（将来追加時はポリシー改訂が必要）
全26ページ（トップ・4ハブindex・個別記事19本・articles/index.html・
  diagnosis.html・privacy.html）のfooterに一括対応：
  - 「プライバシーポリシー」リンクを追加
  - フォームのリンク文言を「掲載をご希望の教育機関様はこちら」→
    「お問い合わせ・掲載のご相談」に統一（運営者提案。掲載依頼以外の
    問い合わせもしやすくする目的）
第二フェーズの次のステップは②運営者情報 → ③ages（静的キュレーション）→
  ④Search Console登録

2026-08-02（追記6）
運営者確認により、404.htmlのfooterは今回のfooter一括復帰の対象外とし、
  現状（「掲載をご希望の教育機関様はこちら」リンクのみのシンプルな構成）を
  維持する方針を確認。articles/index.html・sitemap.xmlの最終版も運営者側で
  確認済み（差分なし）
  これにより、footer復帰・内部リンク整合・FAQ整合性チェックの一連の作業が
  正式に完了

2026-08-02（追記5）
運営者からアップロードされた既存17ページ（4ハブindex＋個別記事13本）すべての
  footer復帰作業が完了。今回の作業の中で、footer以外にも以下の問題を発見・修正：
  - 暫定リンクの残存：glossary/futoukou.html・worries/futoukou.html・
    worries/hattatsu-gray.html・methods/gakkou.htmlで、個別記事公開前に設置した
    ハブページアンカー（例：worries/index.html#futoukou）が、対象記事の公開後も
    更新されずに残っていた。すべて個別記事への直接リンクに更新
  - FAQ本文とJSON-LDの不一致：glossary/futoukou.html（1問目）・
    glossary/kyouiku-shien-center.html（6問目）・worries/hattatsu-gray.html
    （6問目）・worries/katei-gakushu.html（4問目、「きょうだい」/「兄弟姉妹」の
    表記ゆれ）で発見。いずれも運営者確認のうえ、本文側の表現にJSON-LDを統一
  - 禁止語彙の残存：methods/gakkou.html FAQ5問目に「選ぶ」が残存。
    「限定する」に修正（運営者提案）
  - これにより第一フェーズの全26ページ（トップ・4ハブindex・個別記事19本・
    articles/index.html・diagnosis.html）が、footer・内部リンク・FAQ整合性の
    すべてにおいて公開基準を満たした状態になった

2026-08-02（追記4）
運営者からのアップロードを受け、既存記事のfooter復帰作業を開始（17ページ中、
  順次対応）。あわせて以下の問題を発見・修正：
  - glossary/futoukou.html：「次に読みたい記事」・CTAが、個別記事公開前の
    暫定リンク（worries/index.html#futoukou 等のハブページアンカー）の
    ままだった。worries/futoukou.html・methods/gakkou.html・
    institutions/kyouiku-shien-center.htmlへの直接リンクに更新
  - glossary/futoukou.html：FAQ 1問目でJSON-LDと本文（faq__a）の文言が
    不一致だった（「心理面や生活環境などの背景により」と
    「心理的・情緒的・身体的・社会的な要因により」）。運営者確認のうえ、
    本文側の表現にJSON-LDを統一
  - 同様の「公開前の暫定リンクが残っていないか」「FAQ本文とJSON-LDの
    完全一致」は、他の既存記事（2026-07-23公開分）でも同時期に作られた
    ものであるため、footer復帰作業とあわせて全ページ確認する方針とする

2026-08-02（追記3）
運営者確認により、index.htmlの「条件から探す」セクションから
  ages/index.html・areas/index.htmlへのリンクが404（GitHub Pages標準の
  404ページ、noindex設定済み）になっていることが判明。404ページ自体は
  適切に作られており（トップページへの導線あり）、運営者の判断により
  当面はこのまま許容し、ages/areasページ実装（5節ToDo）まで一時的な
  リンク除外などの対応は行わない方針を確認

2026-08-02（追記2）
運営者確認により、index.html（トップページ）のfooterがまだ復帰されていない
  ことが判明。articles/index.html・diagnosis.htmlへのリンクを追加する
  置換スニペットを提供済み（ルート階層のため../プレフィックスなし）。
  4ハブindex.html・既存記事13本を含む残り17ページも同様に未反映の可能性が
  高く、要確認
design-system.cssの`.tag-link`（トップページ「よくあるお悩みから探す」の
  タグボタン）について、文字色が`--color-text`（黒系）のままクリック可能と
  分かりにくいとの指摘を受け、`color: var(--color-blue-deep)`への変更案を
  提供。枠線・背景によるボタン型デザインは維持したまま文字色のみ変更

2026-08-02
design-system.cssの記述漏れを発見・対処法を記録：`.about__list`内の`<a>`に
  色指定がなく、related-link-box等の「次に読みたい記事」リンクがグレーの
  地の文と同化して見える不具合。サイト全体（公開済み全記事）に影響。
  design-system.cssへ`.about__list a`・`.about__text a`にブランドブルー
  （--color-blue-deep）を指定するルールを追加することで、個別HTMLを
  変更せず一括解決できることを確認・提案
diagnosis.html（学び方診断）公開完了。第一フェーズの全ページ（25ページ）が
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

11. 公開前チェックリスト（第一フェーズ完了時点で申し送り）
push前に5〜10分で確認できる項目。運営者提案（2026-08-02）。

①リンク切れ最終チェック
  すべての内部リンク／画像・favicon／canonical／CSS／Google Fonts
②Search Console登録前チェック
  robots.txt／sitemap.xml／canonicalの自己参照／noindexの付け忘れ
③モバイル表示確認
  iPhone幅／Android幅／タブレット幅／CTAボタンの押しやすさ
④Lighthouse確認
  Accessibility／Best Practices／SEO／Performance

12. 第二フェーズの方向性（サイトを「作る」から「育てる」へ）
第一フェーズ（サイト基盤構築）完了後、運営者との協議により以下の順番を
第二フェーズの実行計画として確定（2026-08-02）。

①プライバシーポリシー（GA4・Google Forms利用のため、Search Console登録前に
  必須。優先度は最も高い）
②運営者情報
③ages（学年別、静的キュレーション方式。小学生／中学生／高校生の3セクション、
  タグシステムは将来の発展形として設計書に残すが、v1では手動選定リンクで
  十分とする）
④Search Console登録
⑤公開・インデックス確認
⑥areas（地域）は今回見送り。現状19記事はいずれも地域に紐づく内容がなく、
  無理に実装すると「該当記事なし」のページになるため、地域紐づけの記事
  （〇〇地区のフリースクール等）が10〜20本程度増えてから着手する。
  サイト設計書には「将来実装予定」として残す

その他、優先順位が確定するまでの参考項目：
Search Console・Analyticsで実データを確認
diagnosis.htmlの利用状況・クリック率の分析（9.5節の改善候補と合わせて検討）
glossaryの追加（保留中の改善案含む）
新規記事の拡充
E-E-A-T強化（運営者情報・監修方針・出典表記等、②と重複するため②実施時に統合）

13. 第一フェーズ完了宣言
2026-08-02、上記11節のチェックリスト実施を残すのみの状態で、
サイト基盤構築（第一フェーズ）の完了を確認。次回セッションは、
公開前チェックリストの実施、またはSearch Console登録後の第二フェーズ
（12節）のいずれかから開始する想定。
