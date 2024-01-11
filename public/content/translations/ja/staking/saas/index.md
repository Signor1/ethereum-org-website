---
title: ステーキングサービス
description: ETHステーキングプールの始め方の概要
lang: ja
template: staking
emoji: ":money_with_wings:"
image: /staking/leslie-saas.png
alt: 雲に浮かぶサイのレスリー
sidebarDepth: 2
summaryPoints:
  - サードパーティーのノードオペレータが、バリデータクライアントの運用を実施
  - 32 ETHを保有し、ノードを実行することの技術的な複雑さを回避したい方向けの選択肢
  - 信頼せず、必ず引き出し鍵を必ず保持すること
---

## ステーキングサービスとは {#what-is-staking-as-a-service}

ステーキング・アズ・ア・サービス(SaaS)は、バリデータになるための 32 ETH を預け入れ、ノードの運用については、サードパーティに委任できるステーキングサービスのことです。 このプロセスでは通常、鍵の生成と預け入れを伴う初期セットアップを案内され、署名鍵をオペレータにアップロードします。 これは、通常は月額手数料で、バリデータの運用を代行するサービスです。

## サービスを使ってステークする利点 {#why-stake-with-a-service}

イーサリアムのプロトコルは、ステーキングの委任をネイティブにはサポートしないため、これらのサービスは需要を満たすために作られたものです。 ステーキングする 32 ETH はあるものの、ハードウェアを扱うのが苦手な場合、ステーキング・アズ・ア・サービス(SaaS)を利用すると、難しい部分を委任しながらネイティブブロックの報酬を得ることができます。

<CardGrid>
  <Card title="自分自身のバリデータ" emoji=":desktop_computer:">
    イーサリアムコンセンサスに参加する自身の署名鍵セットを有効化するためのに、32 ETHを預け入れます。 ダッシュボードで進捗状況を監視し、ETH報酬が貯まっていくのを見ます。
  </Card>
  <Card title="簡単に開始" emoji="🏁">
    ハードウェア仕様、セットアップ、ノードメンテナンス、アップグレードに煩わされる必要はありません。
    自身の署名情報をアップロードすることで、SaaSプロバイダーに難しい部分をアウトソースすることができ、わずかな手数料でバリデータを代行してもらうことができます。
  </Card>
  <Card title="リスクを制限" emoji=":shield:">
    多くの場合、ステークした資金の引き出しや送金を可能にする鍵へのアクセス権を手放す必要はありません。 これらは署名鍵とは異なり、別々に保管することで、ステーカーのリスクを制限することができます(ただし、完全に排除することはできません)。
  </Card>
</CardGrid>

<StakingComparison page="saas" />

## 考慮すべき事項 {#what-to-consider}

ETH のステーキングを支援するステーキング・アズ・ア・サービス(SaaS)プロバイダーは増えていますが、それぞれ異なるリスクと利点があります。

各 SaaS プロバイダーの顕著な長所や短所を示すため、下記の属性指標が使用されています。 ステーキングに役立つサービスを選ぶ際に、これらの属性をどのように定義しているかの参考として、このセクションをご利用ください。

<StakingConsiderations page="saas" />

## ステーキングサービスプロバイダーを探す {#saas-providers}

下記は、利用可能なステーキング・アズ・ア・サービス(SaaS)プロバイダーです。 上記の指標を参考に、これらのサービスをご利用ください。

<InfoBanner emoji="⚠️" isWarning>
<a href="/developers/docs/nodes-and-clients/client-diversity/">クライアントの多様性</a>をサポートすることが、ネットワークのセキュリティを向上させ、ご自身のリスクを制限する上で、重要であることにご留意ください。 マジョリティを占めるクライアントを制限している証拠があるサービスは、<em style={{ textTransform: "uppercase" }}>「クライアントの多様性」</em>として表示されます。
</InfoBanner>

### ステーキングサービスプロバイダー

<StakingProductsCardGrid category="saas" />

### キージェネレーター

<StakingProductsCardGrid category="keyGen" />

ここに記載すべきステーキング・アズ・ア・サービス(SaaS)プロバイダーをご存知の場合は [製品掲載ポリシー](/contributing/adding-staking-products/)を確認し、記載すべきかどうかをご確認の上、レビューに提出してください。

## よくある質問 {#faq}

<ExpandableCard title="鍵の保有者" eventCategory="SaasStaking" eventName="clicked who holds my keys">
  流れはプロバイダーによって異なりますが、一般的には、必要な署名鍵(32 ETHにつき1つの鍵)を設定し、プロバイダーにアップロードし、プロバイダーが代理で検証を行います。 署名鍵だけでは、あなたの資金を引き出したり、送金したり、使用することはできません。 ただし、コンセンサスのための投票はできるため、適切に行われない場合はオフラインでのペナルティやスラッシングにつながる可能性があります。
</ExpandableCard>

<ExpandableCard title="鍵は2種類" eventCategory="SaasStaking" eventName="clicked so there are two sets of keys">
  すべてのアカウントは、<em>署名鍵</em>と<em>引き出し鍵</em>の両方で構成されています。 バリデータがチェーンの状態を証明し、同期し、ブロックを提案するには、バリデータクライアントが署名鍵に容易にアクセスできる必要があります。 これらは何らかの形でインターネットに接続されていなければならないため、本質的に「ホットキー」とみなされます。 署名鍵は、バリデータが証明できるようにするための必須の鍵であり、送金や引き出しに使用する鍵とは、セキュリティ上の理由から別のものになっています。

これらの鍵はすべて、24 語のニーモニックシードフレーズを使って、いつでも再現可能です。 <em>必ずこのシードフレーズを安全にバックアップしておいてください。忘れてしまうと、引き出せる時が来たときに、引き出し鍵を生成することができません</em>。
</ExpandableCard>

<ExpandableCard title="引き出しが可能になる時期" eventCategory="SaasStaking" eventName="clicked when can I withdraw">
  SaaSプロバイダーで32 ETHをステークした場合も、そのETHは正式なステーキングデポジットコントラクトに預け入れられます。 そのため、SaaSステーカーもソロスステーカーと同じく、現在のところ資金を引き出すことはできません。 つまり、ETHのステーキングは、現状では、一方通行の入金だけとなります。 ただし、これは上海アップグレードが行われるまでです。
</ExpandableCard>

<ExpandableCard title="スラッシングされた場合" eventCategory="SaasStaking" eventName="clicked what happens if I get slashed">
SaaSプロバイダーを利用することは、ノードの運用を誰かに委ねるということです。 このため、ノードのパフォーマンスが低下するリスクが伴い、このリスクはご自身で制御することはできません。 バリデータがスラッシングされた場合は、自分のバリデータ残高にペナルティが課せられ、バリデータプールから強制的に取り上げられます。 また、これらの資金は、プロトコルレベルで引き出しが可能になるまでロックされます。

保証や保険のオプションの詳細については、各 SaaS プロバイダーにお問い合わせください。 バリデータのセットアップをご自身で完全に制御したい場合は、<a href="/staking/solo/">ETH のソロステークの方法</a>についてさらに学びましょう。
</ExpandableCard>

## 参考文献 {#further-reading}

- [ステーキングサービスの評価](https://www.attestant.io/posts/evaluating-staking-services/) - _Jim McDonald 2020_