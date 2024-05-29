# minecraft攻略メモ
  
<h1>～これーWorld 座標メモ～</h1>  
  

**★このリポジトリの改造、流用、配布、クローンは禁止です★**  
    **Modification, diversion, distribution, and cloning of this repository are prohibited**  
  

<h1 id="aHowto">このドキュメントについて / About this document</h1>  
このドキュメントはMinecrafttのこれーWorldの座標メモです。  
  




<h1 id="aMokuji">目次 / Table of contents</h1>  

* [readme.md](/readme.md)

* [ワールド情報](#aWorldInfo)

* [座標情報](#aCoordinateInfo)
  * [座標：村](#aCoordinateInfoVillage)
  * [座標：オーバワールド 建造](#aCoordinateInfoOWBuills)
  * [座標：オーバワールド 土地](#aCoordinateInfoOWLocal)
  * [座標：オーバワールド 海](#aCoordinateInfoOWSea)
  * [座標：ネザー](#aCoordinateInfoNether)
  * [座標：エンド](#aCoordinateInfoEnd)

* [作るトラップ](#aCreateTrap)
* [交易](#aTrade)
* [ヤギの角](#aGoatHone)
  





<h1 id="aWorldInfo">ワールド情報</h1>  
  
  [目次へ戻る](#aMokuji)  
  


<h2>プレイスタイル</h2>

```text
バージョン：1.20.0
難易度：ノーマル
モード：サバイバル
チートあり（管理用）
素材は自力で集める
```


<h2>SEED値</h2>

```text
-6542443134725437512  
```


<h2>初期スポーン</h2>

```text
execute in minecraft:overworld run tp @p -2327 69 528
    -2327 69 528

設定コマンド
setworldspawn
worldborder center ~ ~
worldborder set 20000 0
```
  





<h1 id="aCoordinateInfo">座標情報</h1>  
  
  [目次へ戻る](#aMokuji)  
  


<h2 id="aCoordinateInfoVillage">座標情報：村</h2>  

```text
execute in minecraft:overworld run tp @p -2327 69 528  

locate structure #minecraft:village
    -2327 - 528                                   平地村
    -992 - 944                                    砂漠村
    2492 - 388                                    樹氷村
    -1259 - -332                                  砂漠村・前線基地あり
                                                  
/tp @p -2327 69 528

/tp @p 904 192 163                                TTT
```


<h2 id="aCoordinateInfoOWBuills">座標情報：オーバワールド 建造物</h2>  

```text
/tp @p -2321 68 607                               コマンドワープ帰還
                                                  

execute in minecraft:overworld run tp @p -2321 68 607

locate structure minecraft:mansion                森の洋館
@    -544 - -5040

locate structure minecraft:pillager_outpost       前線基地
    -672 - 1344

locate structure minecraft:ancient_city           古代都市
    -2072 -50 1563

locate structure minecraft:stronghold             要塞（エンドポータル）
    - - -

locate biome minecraft:dripstone_caves            鍾乳洞
    -1019 2 911
```


<h2 id="aCoordinateInfoOWLocal">座標情報：オーバワールド 土地</h2>  

```text
locate biome minecraft:savanna                    サバンナ
    216 118 -370

locate biome minecraft:badlands                   荒野（メサ）
    -263 - 170

locate biome minecraft:jungle                     ジャングル
    -296 - -169

locate biome minecraft:desert                     砂漠
    -329 - -130

※砂漠・メサ・ジャングルが重なる
locate biome minecraft:flower_forest              花の森
      363 72 -1108    小さい

locate biome minecraft:sunflower_plains           ヒマワリ平原
      269 - -1346    小さい

locate biome minecraft:swamp                      沼地
    -3075 84 -919  小さい
    4348 64 1974

locate biome minecraft:mangrove_swamp             マングローブの沼
      -1960 67 153

locate biome minecraft:ice_spikes                 樹氷
      2492 - 388

※村あり
locate biome minecraft:mushroom_fields            マッシュルームの島
      5115 70 1678

locate biome minecraft:cherry_grove               サクラ
      77 109 -1185
                                                  
```


<h2 id="aCoordinateInfoOWSea">座標情報：オーバワールド 海</h2>  

```text
locate structure minecraft:monument               神殿
      723 - 80

locate biome minecraft:warm_ocean                 暖かい海
      -415 72 270

locate biome minecraft:deep_ocean                 深い海
      718 - 80

※神殿あり
locate biome minecraft:deep_frozen_ocean          凍った深海
      1504 71 -507
                                                  
```


<h2 id="aCoordinateInfoNether">座標情報：ネザー</h2>  

```text
execute in minecraft:the_nether run tp @p 87 37 135

初期
      87 37 135                                   初期観測地点

ゲート
      -293 67 87                                  拠点村ゲート

locate structure fortress                         ネザー要塞
      -453 80 -74
      -80 - 160  村ゲート近く

locate structure bastion_remnant                  砦の遺跡（ネザー)
      -1134 33 -746  チートあり
      228 81 157
      -720 - 80  村ゲート近く

locate biome minecraft:crimson_forest             真紅の森（赤い森）
      87 37 135

locate biome minecraft:warped_forest              歪んだ森（青森）
      192 82 315
      58 - 409  村ゲート近く

locate biome minecraft:basalt_deltas              三角地帯
      229 51 -38
      -582 - 377 村ゲート近く

locate biome minecraft:soul_sand_valley           ソウルサンドの谷
      -173 89 385
                                                  
```


<h2 id="aCoordinateInfoEnd">座標情報：エンド</h2>  

```text
execute in minecraft:the_end run tp 0 100 0

locate structure minecraft:end_city               エンドシティ
      -912 - -896    シップあり
                                                  
```
  





<h1 id="aCreateTrap">作るトラップ</h1>  
  
  [目次へ戻る](#aMokuji)  
  

* [-] 鉄トラップ（最優先）
* [-] 天空トラップ
* [-] 無限溶岩工場
* [-] 羊毛工場
* [*] ポーション販売機
* [*] 鶏増殖機
* [-] 自動粘土製造機  

* [-] 自動畑（全種）
  * にんじん
  * じゃがいも
  * ビートルート
  * 小麦
  * パン
  * かぼちゃ
  * すいか
  * さとうきび
  * カカオ

* [*] ガーディアントラップ
* [*] ブレイズトラップ
* [*] ドラウンドトラップ
* [*] エンダーマントラップ
  





<h1 id="aTrade">交易</h1>  
  
  [目次へ戻る](#aMokuji)  
  

* [-] 農民【コンポスター】
  * にんじん
  * じゃがいも
  * 小麦
  * ビートルート
  * かぼちゃ
  * スイカ

* [-] 漁師【たる】
  * バケツ一杯のタラ
  * 焼いたタラ
  * 調理したシャケ
  * 釣り竿

* [-] 羊飼い【機織り機】
  * ハサミ
  * 羊毛（各色）
  * ベッド（各色）
  * 絵画

* [-] 矢師【矢台】
  * 木の棒→エメラルド
  * 矢
  * 弓
  * クロスボウ

* [-] 司祭【醸造台】
  * 腐肉→エメラルド
  * レッドストーンの粉
  * ラピスラズリ
  * グロウストーン
  * エンダーパール

* [-] 製図家【製図台】
  * エメラルド→空の地図
  * エメラルド→海洋探検家の地図
  * エメラルド→森林探検家の地図
  * 額縁

* [-] 防具鍛冶【錬金かまど】
  * 盾
  * ダイヤ靴
  * ダイヤアーマー
  * ダイヤヘルメット
  * ダイヤレギンス

* [-] 武器鍛冶【エンチャ剥がし】
  * ダイヤ斧
  * ダイヤ剣

* [-] 道具鍛冶【道具台】
  * ダイヤくわ
  * ダイヤ斧
  * ダイヤシャベル
  * ダイヤつるはし

* [*] 石工【石切台】
  * レンガ
  * 磨かれたシリーズ
  * テラコッタ（各色）

* [*] 肉屋【燻製器】
  * とりの生肉→エメラルド
  * うさぎの生肉→エメラルド
  * 豚の生肉→エメラルド
  * 調理した豚肉
  * うしの生肉→エメラルド
  * 羊の生肉→エメラルド

* [-] 革職人【みずがめ】
  * 革の馬鎧
  * サドル

* [*] 司書【書見台】 エンチャント本  

  * **打撃系**  
    * [-] ダメージ増加５
    * [-] 火属性２（剣専用）
    * [-] ドロップ増加３（剣専用）
    * [-] (X)ノックバック２（剣専用）
    * [-] 範囲ダメージ３（剣専用）
    * [-] アンデッド特攻５
    * [-] (X)虫特攻５

  * **ツール用**  
    * [-] 効率強化５
    * [-] シルクタッチ
    * [-] 幸運３

  * **弓用**  
    * [-] 射撃ダメージ増加５
    * [-] 無限
    * [-] フレイム
    * [-] (X)パンチ２

  * **クロスボウ用**  
    * [-] 高速装填３
    * [-] 貫通４
    * [-] 拡散

  * **トライデント用**  
    * [*] 忠誠３
    * [-] 水生特攻５
    * [-] 召雷
    * [-] (X)激流３

  * **防具用**  
    * [-] ダメージ軽減４
    * [-] 火炎耐性４
    * [-] 爆発耐性４
    * [*] (X)飛び道具軽減４
    * [-] (X)棘の鎧３
    * [-] 落下耐性４（靴専用）
    * [-] 水中歩行３（靴専用）
    * [-] (X)氷渡り２（靴専用）
    * [-] 水中採掘（メット用）
    * [-] 水中呼吸３（メット用）

  * **釣り竿用**  
    * [-] 宝釣り３
    * [-] 入れ食い３

  * **その他**  
    * [-] 耐久３
    * [-] 修繕
    * [-] 消滅の呪い
    * [-] 束縛の呪い

> スニーク速度上昇３、ソウルスピード３は司書にはない
  





<h1 id="aGoatHone">ヤギの角</h1>  
  
  [目次へ戻る](#aMokuji)  
  

* **通常のヤギ（沈思、歌声、探求、感覚）**  
  * [*] 沈思
  * [*] 歌声
  * [*] 感覚
  * [*] 探求

* **叫ぶヤギ（称賛、号令、憧憬、夢想）**  
  * [*] 称賛
  * [*] 号令
  * [*] 憧憬
  * [*] 夢想
  





***
[[トップへ戻る]](/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= [https://github.com/korei-xlix/](https://github.com/korei-xlix/)  
::Web= [https://website.koreis-labo.com/](https://website.koreis-labo.com/)  
::X= [https://twitter.com/korei_xlix](https://twitter.com/korei_xlix)  
