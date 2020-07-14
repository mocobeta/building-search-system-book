# [PoC][書籍] 仕事ではじめる検索システム

## これは何？

一連のツイートに触発されて， @mocobeta がこんな本あったらいいな，という妄想を書き下した備忘録です。ご自由にお使いください。

- https://twitter.com/shiumachi/status/1282978358867812352
- https://twitter.com/moco_beta/status/1283014397628043264
- https://twitter.com/chezou/status/1283021918044446720
- https://twitter.com/icoxfog417/status/1283026877678940164

特定のソフトウェア／プロダクトの使い方に限定せず，かつ実用的な（全文）検索システムをゼロから作る，ことをテーマにした日本語の書籍は，私の知る限りではありません（たぶん）。

以下の章立てはあくまで想像の産物なので，形になる予定はいまのところありませんが，目次だけでも誰かの役に立つといいなと思って書きました（興味のある出版社の方，もしもいらっしゃいましたら[ご連絡ください](https://medium.com/@mocobeta/about-me-b28838ba631f) 😊）。思いつくトピックを短時間で詰め込んでみたので，クォリティはご容赦ください...あと，これ全部カバーしたら軽く1000ページ越えそう。改善を思いついたら PR/Issue をください＆このテーマについては任せろ／勉強しながら書きたいという方はぜひ執筆者欄を埋めてくださいませ :)

## 章立て

## 目次

### 1章 なんのために検索システムをつくるのか

執筆者: TBA

情報システムの中で，「検索」が果たしてきた役割，歴史，など。イントロダクション。

### 2章 検索システムプロジェクトのはじめかた

執筆者: TBA (または @mocobeta)

実務で検索システムを作るには，当然ですが技術以外の要素もたくさん絡んできます。プロジェクト管理を学ぶ章。

- 検索案件の立ち上げ方
- ファーストスコープに何を含めるべきか
- 人員配置やステークホルダー
- プロジェクト管理，リスク管理
- 立ち上げフェーズ以降

### 3章 検索エンジンのしくみ

執筆者: TBA (または @mocobeta)

検索システムのコアは，なんといっても検索エンジンです。検索エンジンの仕組みを学ぶ章。

- grep コマンドと検索エンジンの違い
- インデックスデータ構造いろいろ
- 転置インデックスと文書類似度
- 分散検索システム（レプリケーションやシャーディング）のしくみ

### 4章 データのインデクシング

執筆者: TBA

検索システムは，大まかに分けてインデクシング（オフライン処理）と検索クエリ処理（オンライン処理）に分けられます。インデクシングについて学ぶ章。

- テキストのインデクシング: 形態素解析，類義語
- テキスト以外のインデクシング（数値や地理情報など）
- 情報抽出: 効果的なナビゲーション（絞り込み）のための技術
- 外部データソース（RDBなど）との連携
- Web クローリング

### 5章 検索クエリの処理とランキング

執筆者: TBA

ユーザーからの入力クエリを受け付けて，ヒットしたドキュメントをランキングして検索結果を作るまでを学ぶ章。検索システムの華形ともいえる？

- 検索精度とは: 適合率と再現率
- 文書類似度によるランキング
- 検索クエリのパラメータチューニング
- 検索結果の良さの測り方: オフライン指標，オンライン指標
- ランキング学習 (Learning to Rank)
- 検索クエリ補完やサジェスチョン，Query Understanding について

### 6章 ユーザーインターフェース

執筆者: TBA

検索システムは，ユーザーとのインタラクションがとても重要なシステムです。心地良い検索 UI/UX について学ぶ章。

- Web ブラウザインタフェース
- モバイルインタフェース
- 音声入力インタフェース
- インタラクティブ性について

### 7章 検索システム事例

執筆者: TBA

商用サービスとして運用されている検索システムの事例から学ぶ章。

- toC 検索システム事例 A
- toC 検索システム事例 B
- toB 検索システム事例 C
- toB 検索システム事例 D
- 大規模/高トラフィック検索システムの設計と運用

### 8章 応用トピック

執筆者: TBA

関連の深い周辺システムや，最先端の研究に学ぶ章。

- 推薦システムとの関わり
- QAシステム（自然文検索）との関わり
- 画像検索，マルチモーダル検索
- Online Learning to Rank
- Personalized Search
- Semantic Search
- Knowledge Graph
- Dense vector search / approximate knn search
- Neural Networks for IR
- プライバシーと情報検索 (Privacy-preserving IR)

## 参考文献

### 書籍

Information Retrieval の教科書:

- [Introduction to Information Retrieval](https://nlp.stanford.edu/IR-book/information-retrieval-book.html)
  - 今ではだいぶ古くなっている内容もあるが，いわゆる古典と言われる本なので，検索に深く関わる人は一度は読んでおいて損はないと思う。少し高いが [邦訳](https://www.kyoritsu-pub.co.jp/bookdetail/9784320123229) もある。
- [Information Retrieval: Implementing and Evaluating Search Engines](https://www.amazon.co.jp/Information-Retrieval-Implementing-Evaluating-Engines/dp/0262026511/)
  - モダンなサーチエンジンの実装やアルゴリズムについて書かれた本。アルゴリズム好きなら面白いと思います。
- [Modern Information Retrieval](https://www.amazon.co.jp/Modern-Information-Retrieval-Concepts-Technology/dp/0321416910)
  - IR系論文集という感じ。鈍器系。。。
- [Learning to Rank for Information Retrieval](https://link.springer.com/book/10.1007/978-3-642-14267-3)
  - ランキング学習についての古典。サーベイ集にもなっている。
- [情報検索と言語処理 (言語と計算)](https://www.amazon.co.jp/dp/4130654055/)
  - 古いが，数少ない日本語で書かれた本。
- [情報検索アルゴリズム](https://www.amazon.co.jp/%E6%83%85%E5%A0%B1%E6%A4%9C%E7%B4%A2%E3%82%A2%E3%83%AB%E3%82%B4%E3%83%AA%E3%82%BA%E3%83%A0-%E5%8C%97-%E7%A0%94%E4%BA%8C/dp/4320120361)
  - こちらはアルゴリズム寄りの日本語で書かれた書籍。文字列パターンマッチもカバーされている。

(番外編) IRの教科書がたくさん紹介されているありがたいブログ記事:

- [情報検索ことはじめ〜教科書編〜](https://sleepy-yoshi.hatenablog.com/entry/20081212/p1)
  - [その2](https://sleepy-yoshi.hatenablog.com/entry/20110118/p1) もあります

Lucene 系で，いくつか実システム寄りでトピックを絞った書籍がいくつか出ている:

- [Relevant Search](https://www.manning.com/books/relevant-search)
- [Deep Learning for Search](https://www.manning.com/books/deep-learning-for-search)


### オンラインで読める記事など

多数ありとてもカバーしきれないので，独断によりほんの一部を紹介:

- [情報検索・検索エンジン Advent Calendar 2019](https://qiita.com/advent-calendar/2019/search)
- [ゼロから始めるランク学習](https://www.szdrblog.info/entry/2018/12/03/004600)
- [検索体験を向上する Query Understanding とは](https://recruit-tech.co.jp/blog/2019/12/25/query-understanding-overview/)
- [A/Bテストより10~100倍効率的なランキング評価手法　インターリービング（Interleaving）のまとめと実践](https://qiita.com/mpkato/items/99bd55cc17387844fd62)
- [Elasticsearchのための新しい形態素解析器 「Sudachi」](https://qiita.com/sorami/items/99604ef105f13d2d472b)
- [ニュース記事からのトレンドキーワード抽出](https://qiita.com/moco_beta/items/0b0f08ed29f39544d87f)
- [サービス特性にあった検索システムの設計戦略](https://techlife.cookpad.com/entry/2019/11/18/110000)
- [How Search Works](https://www.blog.google/products/search/how-search-works/)
