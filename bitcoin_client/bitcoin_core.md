## Bitcoin Core: リファレンス実装

リファレンス実装クライアント（リファレンス・クライアント）  *Bitcoin Core* （Satoshi clientとも呼ばれます） は bitcoin.orgサイトからダウンロード可能です。このクライアントはビットコイン・システムのあらゆる機能（ウォレット機能、全トランザクション元帳（ブロックチェーン）を用いたトランザクション正当性評価エンジン機能、P2Pビットコイン・ネットワークでのフル・ノード機能）が実装されています。

[最初のウォレットの選択ページ](http://bitcoin.org/en/choose-your-wallet)でBitcoin Coreを選択することでリファレンス・クライアントがダウンロードできます。利用しているOSに合ったインストーラーをダウロードします。 Windowsの場合はZIPファイル、または実行ファイル（.exe）。Mac OSの場合はディスクイメージ（.dmg）Linuxの場合はUbuntu用にPPAパッケージ、またはtar.gzファイルが用意されています。下図に、bitcoin.org が推奨するビットコインクライアントのリストを示します。

!["bitcoin.orgのクライアント選択画面"](00_images/msbt_0301.png "bitcoin.orgのクライアント選択画面")

 ### Bitcoin Core を起動する
 
 インストーラ・パッケージ（exe、dmg、PPA）をダウンロードした場合、他の一般的なアプリケーションと同様にインストールが可能です。Windowsの場合はインストーラーの指示に従いインストールを進めます。Mac OSの場合は、dmgファイルを起動し、Bitcoin-QTアイコンを_アプリケーション_フォルダにドラッグします。また、Ubuntuの場合は、PPAファイルをダブルクリックするとパッケージ・マネージャが起動します。インストールが終了すればBitcoin-Qtと呼ばれるアプリケーションのアイコンがアプリケーションリストの中に表示されるはずです。そのアイコンをダブルクリックすることでビットコイン・クライアントが起動されます。
 
最初の起動時にBitcoin Coreはブロックチェーンのダウンロードを開始します。このプロセスは数日間かかる場合もあります（下図参照）。"Balance"の近くの"out of sync"の表示が消え"Syncronized"と表示されるまで、バックグラウンドでプロセス起動させたまま待つ必要があります。

!["ブロックチェーンをダウンロード中のBitcoin Core の画面"](00_images/msbt_0302.png "ブロックチェーンをダウンロード中のBitcoin Core の画面")

---
**【TIP】**

Bitcoin Core は2009年にビットコインが生まれた時点からの全てのトランザクション情報である、トランザクション元帳（ブロックチェーン）を保持します。2013年末時点でブロックチェーンのサイズは数十ギガバイトの大きさになっており、Bitocoin Core は数日かけてこれをダウンロードします。クライアントがブロックチェーンのダウンロードを完了するまで、トランザクション処理やアカウントの残高の更新はできません。最初の起動時には、ディスク空き容量やネットワーク帯域、そして時間の余裕等に気をつけるようにしてください。

---

#### Bitcoin Core をソースコードからコンパイルする

もしあなたが開発者であれば、GitHub上の[公式アカウントページ](https://github.com/bitcoin/bitcoin)のサイドバーからZIPファイルのソース・コードをダウンロード、またはgitコマンドでcloneし、それをコンパイルすることも可能です。以下の例ではUnixライクなシステム（LinuやMac OS）上でgitコマンドによりソースコードをローカルにcloneを実行した例を示します。

```
$ git clone https://github.com/bitcoin/bitcoin.git
Cloning into 'bitcoin'...
remote: Counting objects: 31864, done.
remote: Compressing objects: 100% (12007/12007), done.
remote: Total 31864 (delta 24480), reused 26530 (delta 19621)
Receiving objects: 100% (31864/31864), 18.47 MiB | 119 KiB/s, done.
Resolving deltas: 100% (24480/24480), done.
$
```


 [GitHub bitcoin page], select Download ZIP from the sidebar. Alternatively, use the git command line to create a local copy of the source code on your system. In the following example, we are cloning the source code from a Unix-like command line, in Linux or Mac OS:
し、