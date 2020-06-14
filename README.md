# CDDA-newamazon
Cataclysm: Dark Days AheadのMOD「NewAmazon」について

## 概要
崩壊後の世界で活躍する謎の団体「NewAmazon」を媒介とした取引という設定で、E-inkタブレットPCを使用してキャッシュと物資を取引するレシピを追加します。

動作確認に使用した本体バージョンは以下の通りです。
* 0.E安定版

本MODの製作にあたっては陽輝満月(ヨウキノミツツキ)様の「CashDEoKaimono」を参考にさせて頂きました。  
この場をお借りしてお礼申し上げます。ありがとうございました。


## 詳細
プレイヤーにとって需要の高いもの、手に入れにくいもの、製作できないものをキャッシュで購入できるようにしました。  
プレイヤーにとって需要の低いもの、手に入れにくいが2つ以上は必要ないもの（スキル本など）をキャッシュに交換できるようにしました。  
性質上ゲームバランスがどうしてもヌルくなりますので、シビアなプレイがしたい方やCDDA初心者の方には推奨しません。

まずは「スターターキット」を購入（製作）するところから始めて下さい。

### 物資をキャッシュで購入
E-inkタブレットPCがあれば、キャッシュで物資を購入（レシピで製作）できます。  

本MODでの物資の購入には以下の特徴があります。  
* 購入から使えるまでに時間がかかります（宅配という設定のため）
* 軍用、高級な物資の購入には、プライム会員になる必要があります
* 購入した物資はもれなく段ボール箱に梱包されています

主に制約となる形ですが、
世界観のフレーバー＆参考にさせて頂いた「CashDEoKaimono」との差別化を目的としています。

### 物資をキャッシュに売却
E-inkタブレットPCがあれば、物資をキャッシュに売却（レシピで製作）できます。

ただしCDDAの仕様で、任意の額がチャージされたキャッシュカードは生成することができません。  
そのため本MODでは専用のキャッシュカードを使用します。  

物資の購入時は、専用のキャッシュカードと通常のキャッシュカード両方を使用することができます。  

### プライム会員
「スターターキット」から得られる一般会員証でもある程度の取引が可能ですが、プライム会員証を購入すると以下の特典が発生します。
* 購入から使えるまでの時間が短縮されます
* 軍用、高級な物資が購入できるようになります

プライム会員には3段階のレベルがあり、上位の会員ほど特典が強化されます。※1

※1  
上位の会員証は下位の会員証（一般会員証含む）の機能を包含しています。  
上位の証を手に入れたら、下位の証は破棄してください。  
上位の証を使用する（特典のある）レシピと、下位の証を使用する（特典のない）レシピが、"製作可能"として混在してしまいます。


## 免責事項
* 本MODに登場する存在、名称等は架空のものであり、現実のいかなる存在、名称等とは関係ありません。
* 本MODを使用した、または後述の導入手順に従ったことで損害が発生した場合、当方は責任を負いません。


## 導入方法
### 通常の導入手順
1. NewAmazonのフォルダをdata/mods/のディレクトリに配置してください
2. 世界作成時に「追加 - NewAmazon」を選択してください

### 既存の世界に後付けで導入したい場合の導入手順
1. NewAmazonのフォルダをdata/mods/のディレクトリに配置してください
2. save/世界名/のディレクトリの「mods.json」ファイルを開いてください
3. "newamazon"をJSONの配列に追加してください

以下のような形で編集します。（編集前に世界のセーブデータのバックアップ取得を推奨いたします）  
***
「mods.json」編集前（「コア - Dark Days Ahead」「削除 - NPCの欲求」だけ入った状態）  
```
[
  "dda",
  "no_npc_food"
]
```
***
「mods.json」編集後（「追加 - NewAmazon」を追加した状態）  
```
[
  "dda",
  "no_npc_food",
  "newamazon"
]
```
***
編集を正しく行えば本MODに関しては問題は発生しないと思われますが、一度導入したMODを逆の手順で削除することはしないでください。  
MODによって追加されたアイテムなどが既にワールド上に存在する場合、異常な状態となりクラッシュの原因となります。


## サポート
バグの報告やご要望は、GithubのリポジトリにIssueとして上げて頂けるとありがたいです。  
<https://github.com/artstar234/CDDA-newamazon>

したらばやDiscordに上げて頂いても良いですが、たまに見ている程度なので見逃す可能性が高いです。  
また見ても基本的に返信しません。  

感想などはしたらばやDiscordなどにご自由にご記入ください。

ご要望のある方は、以下のQ&Aのご確認をお願いいたします。

## Q&A
Q:交換ラインナップを増やしてほしいです。  

A:可能です。増やしたい内容を教えてください。  
ただし以下の条件に当てはまるご要望は基本的には対応しません。  
* キャッシュで購入
  - カテゴリ全部、またはそれに近いもの（「銃器全部」や「弾倉全部」など。作業量が多いため）
* キャッシュに売却
  - 手に入れやすいもの
  - 簡単に製作できるもの
* 両方
  - MOD追加アイテム
  - 重量や容量が大きいアイテム  （ドローンによる宅配という設定のため）
  - 重量や容量が大きくなる交換量  （木材100個など。同上の理由）
***
Q:購入金額・売却金額を変更してほしいです。  

A:基本的には対応しません。  
万人に受け入れられる設定は難しく、ご要望頂いた方の希望に合わせると他の方が不満と感じる可能性があるため。  
金額の変更だけなら簡単なので、各自でjsonファイルを修正頂ければと思います。  
***
Q:開発版に対応してほしいです。  

A:私が開発版を追いかけておらず、仕様変更への追随が困難であるため、対応できません。
***
Q:レシピの表示順がバラバラなのが気になります。何らかの基準でソートしてほしいです。  

A:CDDAのシステム制約※2なので、対応できません。

※2  
必要スキルが同じレシピの表示順は、JSONファイル内での記述順序に関わらずゲームをロードする度にバラバラになります。  
対応方法があれば、教えていただけると大変助かります。
***
Q:邪魔な段ボール箱や届くまでの時間を無くしてほしいです。  

A:詳細の項目に記載したとおり、独自性のために入れている特徴のため、対応しません。  
世界設定のフレーバーとして楽しんでいただければと思います。  
プライム会員になることで、届くまでの時間は短縮可能です。  
***
Q:物資をキャッシュに交換した際に、通常のキャッシュカードにチャージできないのは何故ですか。  
またはチャージした通常のキャッシュカードを生成しないのは何故ですか。  
独自のキャッシュカードでは「CashDEoKaimono」や自動販売機で使えないため、やめてほしいです。  

A:CDDAの仕様※3で、任意の額がチャージされたキャッシュカードなどは生成できません。  
本MODでは両方のキャッシュカードを使用できるようにしたので問題ないと思います。  
「CashDEoKaimono」を併用した場合などで使いづらいことは理解していますが、ご了承ください。  

※3  
キャッシュカードは任意の量を装填した状態で製作することができません。  
セント（キャッシュカードの中身）は任意の量を製作することができますが、
キャッシュカードには装填できないフラグが付いており、セントを手に入れてもチャージできないようになっています。  

従って本MODでは以下の対処としました。
* 装填できないフラグを消したキャッシュカードを別アイテムとして用意
* 通常のセントは自然生成されないことから、グラフィックや説明文がデバッグ用になっているため、セントも別アイテムとして用意

キャッシュカードが別アイテムになっていることの影響で、以下の用途に使用することができません。  
* ATM（預入や全振替の対象になりません。そのためATMを使用した通常のキャッシュへの変換はできません）
* 自動販売機
* キャッシュカードを利用したクラフト（プラスチック片など）
* 「CashDEoKaimono」などの別MOD
***


## ライセンス等
本MODの権利者および管理者は「artstar234」です。

本MODはクリエイティブ・コモンズの 表示 - 継承 3.0 非移植 ライセンスで提供します。  
ライセンスの条件に従う限り、改変および再配布は自由に行ってかまいません。  
ライセンスに従って再配布等される場合は、クレジットへの記載と以下のリンクを記載してください。  
<https://github.com/artstar234/CDDA-newamazon>  


## 更新履歴
2020/05/27  
公開
