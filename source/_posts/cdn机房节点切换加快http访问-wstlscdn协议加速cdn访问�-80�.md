---
title: CDN ルーム ノードの切り替えにより、http アクセスが高速化されます-- ws+TLS+CDN プロトコルは CDN アクセスを高速化します。
tags: []
id: '1159'
categories:
  - - uncategorized
date: 2019-10-31 03:43:09
---

最近の10月は記事があまり書かれなかった。 今日、水が出てくると、私はギアを補充します。  
多くの人々は10月頃、外国メーカーの小型機が壁に取り上げられました。 ほとんどの人はYouTube、v2Rayグループを見ます。 ws+TLS+CDN というプロトコルが生き返った。 もちろん、多くの人々は、CDNがなぜネットワークのように速くないのか不思議に思います。  
みんなでケーキを食べます。 N分に分けて サンノゼへ? (あなたは、無料のcf、外国の加速、国内減速の紛れもない事実を、高速に行くと思いますか)  
国内3大キャリアと言えば、輸出地域の場所は異なっています。 地球の周りを大きな円。 遅延は速くなります。 これには CDN シャントが必要です。 ほとんどの人は、cloud flare の CDN 製品を使用しています。 しかし、無料の自然ウォークは、アメリカのサンノゼです。 部屋を変更する方法。 cloud flare公式サイトには、マシンルームがあります。 金だ はい、金はあなたに強くなります。 cloud flareは、以前は香港のいくつかの良いマシンルームにサインアップしました。 しかし、今、基本的にアメリカのサンノゼです。  
お金を使いたくないので、多くの経験が欲しいです。 栗を上げろ 小型機 10Mだ しかし、あなたのネットワークは明らかに10Mを走ることができないのは難しいことではありません。 優待機室。 明らかに、単純な金。 自分でボタンをクリックするだけで完了です。  
しかし、白い話をしたいので、より良く、安定した加速を望む。 結局のところ、CFの無料トラフィック。 ws+tls というプロトコルは http です。 ので、Webページです。 だからCDNは解析を高速化できる. (CDN で紹介) ここでは説明しません。 国内無料白鳥と撮影雲、小さな水道管はテンセント、アリを歩きます。 効果はかなり悪いです。 (CDNを自分で作るように頼んだのですか? 後で話しましょう)  
では、良い cloud flare の CDN ルームを見つける方法について説明します。 [リンク](https://www.hostloc.com/thread-469169-1-1.html)があります。 良い使用のためのマシンルームで、どのように変更しますか? 見続ける。  
他のマシンルームをどのように使用するか。 白い言葉。 **cloud flare 登録プログラム**  
に登録していない人は、登録プログラムを提供する人をオンラインで見つける必要があります。 今、cloud flareは、この承認は厳しいです。 まさか、以前は合格しなかった。  
他の人のcloud flare登録プランでcloud flareアカウントにログインし、他の登録プログラムに参加します。 まず、cloud flare でドメイン名を削除し、他のユーザーの登録プログラムに入力します。 ドメイン名追加レコードを解決します。 ドメイン名の 1 つが、他のユーザーが計画した CHAME レコード解決を行います。

http サイトのドメイン名解決は、ネットワークの状況に応じて異なるホストを移動する必要があります。 ネットワーク配布 (CDN) サービスを最適化して、エクスペリエンスを向上させます。 (CDN ホストで動的ルーティング テーブルを作成して、解決最適化回線を改善することはできません)、別の方法を選択します。  
この時点で、ドメイン DNS パーサーは cloud flare を歩く必要はありません。 他の家に変更しました。 (テンセントのdnspodを非常にお勧めします)それは、ドメイン名にアクセスする人々のためのリンクを持っています。 この機能により,CDNルーム解析を割り当てる問題を解決できる.  
まずdnspod解析に移動します。 解決値を追加します。 ここで一言言ってください。  
tips;ドメイン名解析は、通常、独自の ipv4 ホスト アドレスまたは ipv6 ホスト アドレスです。 歩くcloud flareの解析セットにCDNシェルをセットした。 他のユーザーは、ドメイン名攻撃をサーバー アドレスに解決しません。 彼はCDN配布のアドレスにpingを実行したので。 chame というソースをドメイン名解決に選ぶときです。 これは、chame 解析を高速化するために、1 つ、複数の A レコード解決を指定できます。

したがって、元のドメイン名アドレス、A 解決値を削除します。 ドメイン名の既定値として chme を使用します。 DNS キャッシュをクリアします。 ping で得られる解決値が相手の cloud flare 登録プラン内の chame 解決値である場合は、次の手順に進みます。  
@,Aノードを追加する. ネットワークが選択されている場所で、通信事業者の解決を選択します。 cloud flareCDNルームのIPアドレスを入力します。  
tips: モバイル輸出は香港にあり、アジア太平洋地域ではより良い遅延があります。 例えば、香港、シンガポール、東京などです。 ユニコムはサンノゼを初めて押した。 他の人を歩くのは理想的ではありません。 通信は当然CN2です。 ヨーロッパを考えることができます。 しかし、遅延が高く、安定したパケットをドロップしません。 具体的には、cloud flare CDN マシンルームテーブルを参照してください。  
より良いマシンルームを選択するために自分自身をテストします。 ウェブマスターツールを使用してpingを実行できます。 テスト ノードの状況を地域別に確認します。  
私の個人的な使用は、約60msに移動の遅延を減らすことです。 安定したYouTube 1080pは、(結局10M)カードトンではない小さなマシンです。

**テンセントクラウドプロモーション広告を挿入**します。 (Google 広告はクリックしません)。 それは一度にわずか3セントでした。 それは、あなたがテンセントクラウド製品を購入するために私のリンクにサインアップする国内広告プロモーションの下では良いではありません。 私も取るために手数料を持っている。 死んだピリの顔の波。 ウェブサイトは収入がなく、広告によって支えられております。 小遣いを稼ぐ。

産業の知恵のアップグレードを支援し、クラウドサーバーは、最初の88元から、さらに千元バウチャーギフトパック無料ピックアップ! [このアクセスをポイントします](https://cloud.tencent.com/act/cps/redirect?redirect=1048&cps_key=8d80a5274f7ac63bba5112dbb40c5037&from=console)