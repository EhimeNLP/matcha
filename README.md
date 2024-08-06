# MATCHA

訪日観光客向けメディア[MATCHA](https://matcha-jp.com/)の記事から、日本語のテキスト平易化のためのデータセットを構築しました。
これらは、専門家によって平易に書き換えられた記事と元の記事から構築された、文単位のパラレルコーパスです。
16,000件を公開します。<br>

## 更新履歴
2024年4月23日&emsp;Ver.1.0&ensp;論文誌の投稿に合わせて公開 <br>
2023年8月25日&emsp;Ver.0.2&ensp;[YANS](https://moguranosenshi.sakura.ne.jp/files/yans2023-miyata.pdf)の発表に合わせて拡張 <br>
2023年5月&ensp;&nbsp;1日&emsp;Ver.0.1&ensp;[JSAI](https://doi.org/10.11517/pjsai.JSAI2023.0_3Xin414)の発表に合わせて一部公開 <br>

## ファイルについて
- `matcha.comp`と`matcha.simp`にそれぞれ難解な文と平易な文が行ごとにペアになって含まれています。
- `matcha.tag`には各行の文対のそれぞれに対して以下の3つの情報がタブ区切りで書き込まれています。
  1. 難解な文と平易な文の意味的な対応が 完全一致（Align）または 部分一致（Partial）のどちらであるか
  2. 難解な文と平易な文が 何文 対 何文 で対応しているか
  3. 抽出されたテキストがタイトル（title, subtitle, subsubtitle）または本文（body）のどちらであるか
  <br>
  
  | matcha.comp | matha.simp | matcha.tag |
  | :--- | :--- | :--- | 
  | そこでネズミを退治するため、島で育てられたのが猫だったのです。 | そのとき、島の人は猫にネズミをとってもらいました。それで、猫をたくさん育てました。 | Align\t1-2\t[body] |
  | ネズミを退治するほかにも、島の猫は漁師が捨てた魚の頭や骨などを食べて生活していました。 | 猫はネズミをとったり、漁師(魚をとって生活する人)が捨てた魚の頭や骨(Bone)などを食べたりしました。 | Partial\t1-1\t[body] |
  |︙ | ︙ | ︙ |
  
<br>
  
## 文献情報

\[1\] 宮田莉奈, 惟高日向, 山内洋輝, 柳本大輝, 梶原智之, 二宮崇, 西脇靖紘. <br>
&emsp;&nbsp;&nbsp;MATCHA：専門家が平易化した記事を用いたやさしい日本語パラレルコーパス. <br>
&emsp;&nbsp;&nbsp;自然言語処理, Vol.31, No.2, pp.590-609, June 2024. <br>

\[2\] 宮田莉奈, 惟高日向, 山内洋輝, 柳本大輝, 梶原智之, 二宮崇, ⻄脇靖紘. <br>
&emsp;&nbsp;&nbsp;[専門家が平易化した記事を用いたやさしい日本語パラレルコーパスの構築](https://moguranosenshi.sakura.ne.jp/files/yans2023-miyata.pdf). <br>
&emsp;&nbsp;&nbsp;NLP若手の会第18回シンポジウム (YANS), August 2023.

\[3\] 惟高日向, 山内洋輝, 柳本大輝, 宮田莉奈, 梶原智之, 二宮崇, 西脇靖紘. <br>
&emsp;&nbsp;&nbsp;[専門家が平易化した記事を用いたやさしい日本語パラレルコーパスの試作](https://doi.org/10.11517/pjsai.JSAI2023.0_3Xin414). <br>
&emsp;&nbsp;&nbsp;人工知能学会第37回全国大会 (JSAI), June 2023.
