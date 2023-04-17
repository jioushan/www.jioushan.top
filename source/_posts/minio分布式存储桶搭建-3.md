---
title: ミシオ分散バケット構築
tags: []
id: '1233'
categories:
  - - 未分类
date: 2022-03-04 13:50:44
---

長い間、水1つを書いていない!

MINIOとは? (紹介しない、自力で)

このソフトウェアは オープンソースがあまりにも速く維持されているからです

おそらく、過去にそれを構築した小さなパートナーは、それがそうであると考えています

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9sZWVoYW8ub3NzLWNuLXNoZW56aGVuLmFsaXl1bmNzLmNvbS8yMDIwLTAxLTIxLTE0MTc0OS5wbmc?x-oss-process=image/format,png)

しかし、今ではこのようになる

![](https://blog.min.io/content/images/size/w2000/2021/04/console_header--2-.png)

**分散ストレージの**展開 公式[ドキュメント](https://docs.min.io/)に従って展開します。 しかし、一度OKであれば、我々はまた、公式に考えるのはあまりにも単純です。

ピットを踏んで2日間頭痛がしました 過去に踏んだピットに比べて 頭痛がします ソリティ私はこの記事を水。

なぜなら、私たちはセルバー(サーバー)側を配備しているからです

MC ユーザー側は、基本的にコマンド ラインまたはサード パーティのツールにアクセスします。 あまり話しません。 (バケットを使用していない限り)。 △ 自らおばあさんをする

ここでは、公式の [Docker Compose 展開を](https://docs.min.io/docs/deploy-minio-on-docker-compose.html) 使用します

**ステップ1**

だから、composeとdockerの下にあなたのLinuxインストールを困らせる

**ステップ2**

wget の下の 2 つのファイル (wget の自己インストールなし wget)

[https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/docker-compose.yaml](https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/docker-compose.yaml?raw=true)

[https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/nginx.conf](https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/nginx.conf?raw=true)

**ステップ3**

その後、公式の命令に従います

```
$ docker-compose pull

$ docker-compose up
```

その後、彼はあなたのサーバープロセス上で実行され、butは、ドメイン名を介してそれにアクセスしたい、nginxアンチジェネレーション(リバースプロキシ)を自分で研究することをお勧めします

プロセスはポート 9000,9001,9002 を占有します。

Yaml には、展開前に自分で変更できると書いてある

MINIO\_ROOT\_USER: minio

MINIO\_ROOT\_PASSWORD: minio123