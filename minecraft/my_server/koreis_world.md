# ゲームメモ：minecraft：村テンプレート ***

**★当リポジトリの利用にあたっては、必ず本readmeを確認してください★**  
  

このドキュメントはMinecrafttの **Template** の座標、村発展の進捗メモです。  
  





## 目次 / Table of Contents

* [readme.md](../../readme.md)
  * [利用にあたって (Important notices for use)](../../readme.md#利用にあたっての注意事項--important-notices-for-use)

* [ワールド情報](#ワールド情報)
  * [ゲーム初期情報](#ゲーム初期情報)
  * [旗の色](#旗の色)

* [座標情報](#座標情報)
  * [座標：村](#座標情報村)
    * [建築物の位置](#建築物の位置)

  * オーバーワールド
    * [座標：オーバワールド 建造](#座標情報オーバワールド-建造物)
    * [座標：オーバワールド 土地](#座標情報オーバワールド-土地)
    * [座標：オーバワールド 海](#座標情報オーバワールド-海)
  * [座標：ネザー](#座標情報ネザー)
  * [座標：エンド](#座標情報エンド)

* ゲーム記録
  * [作るトラップ](#作るトラップ)
  * [交易](#交易)
  * [ヤギの角](#ヤギの角)
  * [金型](#金型)
  * [友好動物](#友好動物)
  





## ワールド情報

[目次へ戻る](#目次--table-of-contents)  
  

### プレイスタイル

```text
<<<<<<< HEAD
バージョン  1.21.10
【Local Server：PaperMC】

難易度      ノーマル
モード      サバイバル
チートあり（管理用）
素材は自力で集める

```


### ゲーム初期情報

```text
SEED値
**********

初期地点座標
execute in minecraft:overworld run tp @p - - -
execute in overworld run tp @s - - -
@   * ~ *
=======
バージョン  1.21.11
【Local Server：PaperMC】

チートあり（管理用）
素材は自力で集める
　　※サーバワールドごとに異なる
>>>>>>> origin/minecraft_edit

```
  


<<<<<<< HEAD
=======

### 各ワールド情報

* [world：normal](#ワールド情報world)
* [world_nther：nether](#ワールド情報world_nether)
* [world_end：end](#ワールド情報world_end)
  

#### ワールド情報：world

```text
首都ワールド

モード：creative
難易度：easy
SEED値：-3618384834958624377

初期地点座標
mv tp e:world:16,64,-47

その他設定
　現在をスポーン位置に設定する
　　mv setspawn
　X=0,Z=0を中心にして、16000 0 の範囲に移動制限をかける
　　mv worldborder center 0 0
　　mv worldborder set 16000 0
　コマンドブロック取得
　　give @a minecraft:command_block

time set day
mv gamerule set minecraft:advance_time false world
mv gamerule set minecraft:advance_weather false world
mv gamerule list world --filter advance

```

#### ワールド情報：world_nether

```text

モード：creative
難易度：easy
SEED値：-3618384834958624377

初期地点座標
mv tp e:world:16,64,-47

```

#### ワールド情報：world_end

```text

モード：creative
難易度：easy
SEED値：-3618384834958624377

初期地点座標
mv tp e:world:16,64,-47

```
  



>>>>>>> origin/minecraft_edit
### 旗の色

```text
赤..村・エンドシティ
青..建築施設
緑..ダンジョン
黄..地点、ゲート等

```
  





## 持ち物

[目次へ戻る](#目次--table-of-contents)  
  

* 武器
  * [-] 剣
  * [-] 剣（フレイム）
  * [-] 斧
  * [-] 斧（シルクタッチ）
  * [-] 弓
  * [-] 弓（フレイム）
  * [-] クロスボウ（貫通）
  * [-] クロスボウ（拡散）
  * [-] トライデント（招来）
  * [-] トライデント（激流）
  * [-] メイス

* 道具
  * [-] ピッケル（シルクタッチ）
  * [-] ピッケル（幸運）
  * [-] シャベル（強化Ⅱ）
  * [-] シャベル（強化Ⅴ）
  * [-] クワ
  * [-] ハサミ
  * [-] 釣り竿

* 箱
  * [-] バンドル
  * [-] エンダーチェスト
  * [-] シュルカー
  





## 座標情報

[目次へ戻る](#目次--table-of-contents)  
  


### 座標情報：村

<<<<<<< HEAD
```text
初期地点座標
execute in overworld run tp @s - - -
　　@   * ~ *

初期村
locate structure #minecraft:village
　　@   * ~ *

ゲーム起点：村の入り口（赤ブロック位置）
execute in minecraft:overworld run tp @p - - -
execute in overworld run tp @s - - -

移動制限コマンド
setworldspawn
worldborder center ~ ~
worldborder set 20000 0

コマンドブロック取得
give @a minecraft:command_block

```
=======
　[初期位置](#ワールド情報world)  
  

```text
初期村
minecraft:locate structure #minecraft:village
　　@   -544,~,-752
mv tp e:world:-544,~,-752

ゲーム起点：村の入り口（赤ブロック位置）
mv tp e:world:  ,  ,  

```
  

>>>>>>> origin/minecraft_edit


### 建築物の位置

```text
初期村ゲート
execute in minecraft:overworld run tp @p - - -
execute in overworld run tp @s - - -

TTT
execute in minecraft:overworld run tp @p - - -
execute in overworld run tp @s - - -

ガーディアントラップ
execute in minecraft:overworld run tp @p - - -
execute in overworld run tp @s - - -

カエルトラップ
execute in minecraft:overworld run tp @p - - -
execute in overworld run tp @s - - -

```


### 座標情報：オーバワールド 建造物

```text
村
locate structure minecraft:village
　　@   * ~ *

森の洋館
locate structure minecraft:mansion
　　@   * ~ *

前線基地
locate structure minecraft:pillager_outpost
　　@   * ~ *

古代都市
locate structure minecraft:ancient_city
　　@   * ~ *

要塞（エンドポータル）
locate structure minecraft:stronghold
　　@   * ~ *

鍾乳洞
locate biome minecraft:dripstone_caves
　　@   * ~ *

トライアルチャンバー
locate structure trial_chambers
　　@   * ~ *

砂漠のピラミッド（砂漠）
locate structure minecraft:desert_pyramid
locate structure minecraft:temple
　　@   * ~ *

ジャングルの寺院（ジャングル）
locate structure minecraft:jungle_pyramid
locate structure minecraft:temple
　　@   * ~ *

イグルー（雪原）
locate structure minecraft:igloo
locate structure minecraft:temple
　　@   * ~ *

魔女の家（湿地）
locate structure minecraft:swamp_hut
locate structure minecraft:temple
　　@   * ~ *

廃坑
locate structure minecraft:mineshaft
　　@   * ~ *

旅路の遺跡
locate structure minecraft:trail_ruins
　　@   * ~ *

```


### 座標情報：オーバワールド 土地

```text
石の山岳
locate biome minecraft:stony_peaks
　　@   * ~ *

タイガ
locate biome minecraft:taiga
　　@   * ~ *

サバンナ
locate biome minecraft:savanna
　　@   * ~ *

荒野（メサ）
locate biome minecraft:mesa
　　@   * ~ *

ジャングル
locate biome minecraft:jungle
　　@   * ~ *

竹林
locate biome minecraft:bamboo_jungle
　　@   * ~ *

砂漠
locate biome minecraft:desert
　　@   * ~ *

花の森
locate biome minecraft:flower_forest
　　@   * ~ *

ヒマワリ平原
locate biome minecraft:sunflower_plains
　　@   * ~ *

沼地
locate biome minecraft:swampland
　　@   * ~ *

マングローブの沼
locate biome minecraft:mangrove_swamp
　　@   * ~ *

雪原
locate biome minecraft:ice_plains
　　@   * ~ *

樹氷
locate biome minecraft:ice_plains_spikes
　　@   * ~ *

マッシュルームの島
locate biome minecraft:mushroom_island
　　@   * ~ *

サクラ
locate biome minecraft:cherry_grove
　　@   * ~ *

ペールガーデン
locate biome minecraft:pale_garden
　　@   * ~ *

```


### 座標情報：オーバワールド 海

```text
神殿
locate structure minecraft:monument
　　@   * ~ *

暖かい海
locate biome minecraft:warm_ocean
　　@   * ~ *

海底遺跡（暖かい海）
locate structure minecraft:ocean_ruin_warm
locate structure minecraft:ruins
　　@   * ~ *

深い海
locate biome minecraft:deep_ocean
　　@   * ~ *

凍った深海
locate biome minecraft:deep_frozen_ocean
　　@   * ~ *

冷たい海
locate biome minecraft:cold_ocean
　　@   * ~ *

海底遺跡（冷たい海）
locate structure minecraft:ocean_ruin_cold
locate structure minecraft:ruins
　　@   * ~ *

```


### 座標情報：ネザー

```text
拠点村ゲート
execute in minecraft:the_nether run tp @p - - -
execute in nether run tp @s - - -
@   * ~ *


ネザー要塞
locate structure minecraft:fortress
　　@   * ~ *

砦の遺跡（ネザー）
locate structure minecraft:bastion_remnant
　　@   * ~ *

真紅の森（赤い森）
locate biome minecraft:crimson_forest
　　@   * ~ *

歪んだ森（青森）
locate biome minecraft:warped_forest
　　@   * ~ *

三角地帯
locate biome minecraft:basalt_deltas
　　@   * ~ *

ソウルサンドの谷
locate biome minecraft:soulsand_valley
　　@   * ~ *

```


### 座標情報：エンド

```text
観測位置（エンド側ゲート）
execute in minecraft:the_end run tp @p 0 100 0
execute in the_end run tp @s 0 100 0

エンドシティ（＊船あり）
locate structure minecraft:end_city
　　@   * ~ *

エンドシティ（＊船なし）
locate structure minecraft:end_city
　　@   * ~ *

```
  





## 作るトラップ

[目次へ戻る](#目次--table-of-contents)  
  

* [-] ゴミ箱（サボテン式）
* [-] 鉄トラップ（最優先）
* [-] スライムトラップ
* [-] 天空トラップ
* [-] 無限溶岩工場
* [-] 羊毛工場
* [-] ポーション販売機
* [-] 鶏増殖機
* [-] 自動牛焼き機
* [-] 自動粘土製造機
* [-] ダイヤ交換所
* [-] カエルトラップ

* [-] 植林場
  * [-] オークの木
  * [-] シラカバの木
  * [-] アカシアの木（砂漠）
  * [-] トウヒの木（タイガ）
  * [-] ジャングルの木（ジャングル）
  * [-] ダークオークの木
  * [-] マングローブの木（マングローブ）
  * [-] 赤い森の木（ネザー）
  * [-] 青い森の木（ネザー）

* [-] 自動畑（全種）
  * [-] にんじん
  * [-] じゃがいも
  * [-] ビートルート
  * [-] 小麦
  * [-] かぼちゃ
  * [-] すいか
  * [-] さとうきび
  * [-] カカオ
  * [-] 竹
  * [-] ネザーキノコ

* [-] ビリジャートラップ
* [-] ガーディアントラップ
* [-] ブレイズトラップ
* [-] ドラウンドトラップ
* [-] エンダーマントラップ
* [-] シュルカートラップ
  





## 交易

[目次へ戻る](#目次--table-of-contents)  
  

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

* [-] 防具鍛冶(1)【溶鉱炉】
  * 盾
  * ダイヤ靴
  * ダイヤアーマー
  * ダイヤヘルメット
  * ダイヤレギンス

* [-] 防具鍛冶(2)【溶鉱炉】
  * チェーン靴
  * チェーンアーマー
  * チェーンヘルメット
  * チェーンレギンス

* [-] 革職人【みずがめ】
  * 革の馬鎧
  * サドル
  * 皮靴
  * 皮アーマー
  * 皮ヘルメット
  * 皮レギンス

* [-] 武器鍛冶【エンチャ剥がし】
  * ダイヤ斧（道具でも可）
  * ダイヤ剣

* [-] 道具鍛冶【道具台】
  * ダイヤくわ
  * ダイヤ斧（武器でも可）
  * ダイヤシャベル
  * ダイヤつるはし

* [-] 石工【石切台】
  * レンガ
  * 磨かれたシリーズ
  * テラコッタ（各色）

* [-] 肉屋【燻製器】
  * とりの生肉→エメラルド
  * うさぎの生肉→エメラルド
  * 豚の生肉→エメラルド
  * 調理した豚肉
  * うしの生肉→エメラルド
  * 羊の生肉→エメラルド

* [-] 司書【書見台】 エンチャント本  
  * **打撃系**  
    * [-] ダメージ増加５（剣・斧・特攻と競合）
    * [-] 火属性２（剣専用）
    * [-] ドロップ増加３（剣専用）
    * [-] (X)ノックバック２（剣専用）
    * [-] 範囲ダメージ３（剣専用）
    * [-] アンデッド特攻５（剣、斧、ダメージ増加・特攻と競合）
    * [-] (X)虫特攻５（剣、斧、ダメージ増加・特攻と競合）

  * **ツール用**  
    * [-] 効率強化５
    * [-] シルクタッチ（幸運と競合）
    * [-] 幸運３（シルクタッチと競合）

  * **弓用**  
    * [-] 射撃ダメージ増加５
    * [-] 無限（修繕と競合）
    * [-] フレイム
    * [-] (X)パンチ２

  * **クロスボウ用**  
    * [-] 高速装填３
    * [-] 貫通４（拡散と競合）
    * [-] 拡散（貫通と競合）

  * **トライデント用**  
    * [-] 忠誠３
    * [-] 水生特攻５
    * [-] 召雷（激流と競合）
    * [-] (X)激流３（召雷と競合）

  * **メイス用**  
    * [-] 重撃５
    * [-] 防具貫通４

  * **防具用**  
    * [-] ダメージ軽減４（～耐性と競合）
    * [-] 火炎耐性４（～耐性と競合）
    * [-] 爆発耐性４（～耐性と競合）
    * [-] (X)飛び道具耐性４（～耐性と競合）
    * [-] (X)棘の鎧３
    * [-] 落下耐性４（靴専用）
    * [-] 水中歩行３（靴専用・氷渡りと競合）
    * [-] (X)氷渡り２（靴専用・水中歩行と競合）
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

* 司書にはないエンチャント本  
  * [-] スニーク速度上昇３（レギンス用）  
        古代都市  
  * [-] ソウルスピード３（レギンス用）  
        古代都市  
  * [-] ウィンドバースト３（メイス用）  
        不吉な宝物庫  
  





## ヤギの角

[目次へ戻る](#目次--table-of-contents)  
  

* **通常のヤギ（沈思、歌声、探求、感覚）**  
  * [-] 沈思
  * [-] 歌声
  * [-] 感覚
  * [-] 探求

* **叫ぶヤギ（称賛、号令、憧憬、夢想）**  
  * [-] 称賛
  * [-] 号令
  * [-] 憧憬
  * [-] 夢想
  





## 金型

<<<<<<< HEAD
|場所                  |テンプレート          |素材  |
|:--|:--|:--|
|[-] ピグリン要塞      |ネザライト強化        |  |
=======
|場所 |テンプレート |素材 |
|:--|:--|:--|
|[-] ピグリン要塞      |ネザライト強化        |                  |
>>>>>>> origin/minecraft_edit
|[-]                   |ブタの鼻風の装飾      |ブラックストーン  |
|[-] ネザー要塞        |あばら模様の装飾      |ネザーラック      |
|[-] エンド要塞        |要塞風の装飾          |エンドストーン    |
|[-] 難破船            |海洋風の装飾          |丸石          |
|[-] ピラミッド        |砂丘風の装飾          |砂岩          |
|[-] ジャングルの寺院  |密林風の装飾          |苔むした丸石  |
|[-] 前哨基地          |略奪者風の装飾        |丸石          |
|[-] 海底神殿(ガーディアン)  |潮流風の装飾    |プリズマリン      |
|[-] 森の羊羹          |ヴェックス風の装飾    |丸石              |
|[-] エンドシティ      |尖塔風の装飾          |プルプァブロック  |
|[-] 古代都市          |監獄風の装飾          |深層岩の丸石      |
|[-]                   |静寂の装飾            |深層岩の丸石      |
|[-] トレイル遺跡      |先駆者風の装飾        |テラコッタ  |
|[-]                   |牧者風の装飾          |テラコッタ  |
|[-]                   |職人風の装飾          |テラコッタ  |
|[-]                   |主人風の装飾          |テラコッタ  |
|[-] 宝物庫            |ねじ止め風の装飾      |銅ブロック  |
|[-] 不吉な宝物庫      |ブリーズロッド        |テラコッタ  |
  





## 友好動物

<<<<<<< HEAD
|動物              |居場所          |繁殖  |特技  |
=======
|動物|居場所|繁殖|特技|
>>>>>>> origin/minecraft_edit
|:--|:--|:--|:--|
|[-] ニワトリ   |明るさ9以上、上に空き2以上ある草ブロック   |種系の作物   |      |
|  [-] 通常種   |草原など          |  |  |
|  [-] 熱帯種   |荒野（メサ）など  |  |  |
|  [-] 寒帯種   |タイガなど        |  |  |
|[-] ウシ         |明るさ9以上、上に空き2以上ある草ブロック   |小麦         |バケツを使うと牛乳がとれる  |
|  [-] 通常種   |草原など          |  |  |
|  [-] 熱帯種   |荒野（メサ）など  |  |  |
|  [-] 寒帯種   |タイガなど        |  |  |
|[-] ブタ         |明るさ7以上、上に空き2以上ある草ブロック   |ニンジン、ジャガイモ、ビートルート  |鞍で騎乗 要:ニンジン+釣り竿  |
|  [-] 通常種   |草原など          |  |  |
|  [-] 熱帯種   |荒野（メサ）など  |  |  |
|  [-] 寒帯種   |タイガなど        |  |  |
|[-] カエル       |沼地及びマングローブの沼地でスポーンする   |スライムボール  |マグマキューブを倒すとフロッグライトを落とす  |
|  [-] 通常種（橙色）   |草原など          |  |  |
|  [-] 亜熱帯種（白色） |マングローブなど  |  |  |
|  [-] 寒冷地種（緑色） |氷原など          |  |  |
|[-] ヒツジ       |明るさ7以上、上に空き2以上ある草ブロック   |小麦        |ハサミを使うと羊毛がとれる  |
|[-] オオカミ     |タイガの草ブロックなど                     |骨          |狼鎧を装備可 ペットは共闘可能  |
|[-] ネコ         |                |      |      |
|[-] ウサギ       |                |      |      |
|[-] ウマ         |草原                                       |餌:砂糖、小麦、リンゴ、干草(ペット) 繁殖:金のリンゴ、金のニンジン    |鞍で騎乗 馬鎧装備可 何度か乗るとペット可  |
|[-] ラバ         |草原？ or 馬＆ロバで繁殖                   |馬と同じ 繁殖はできない              |鞍で騎乗 何度か乗るとペット可  |
|[-] ロバ         |草原                                       |馬と同じ ウマとのみ繫殖できる→ラバ  |鞍で騎乗 何度か乗るとペット可 チェスト付けられる  |
|[-] スケルトンホース   |落雷時にスポーンする場合あり         |なし                                 |鞍で騎乗（ゲーム最速）         |
|[-] ゾンビホース       |自然発生なし？コマンドでスポーン     |なし                                 |鞍で騎乗                       |
|[-] ハチ         |                |      |      |
|[-] カメ         |砂浜                                       |海藻        |大人に成長時に亀の甲羅をドロップ 海藻を与えるとタマゴを生む  |
|[-] オウム       |                |      |      |
|[-] パンダ       |                |      |      |
|[-] ヤギ         |                |      |      |
|[-] アレイ       |                |      |      |
|[-] ラクダ             |砂漠の村１つにつき１頭               |サボテン    |鞍で騎乗 インベントリあり  |
|[-] アルマジロ         |荒野、サバンナ                       |蜘蛛の目    |ブラシを使うとアルマジロの革がとれる  |
|[-] ストライダー       |ネザー                               |なし        |鞍で騎乗 要:青キノコ+釣り竿）  |
  

### 特技詳細








***
***
[[トップへ戻る]](../../readme.md)　/
[[minecraft]](/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= [https://github.com/korei-xlix/](https://github.com/korei-xlix/)  
::Web= [https://website.koreis-labo.com/](https://website.koreis-labo.com/)  
::X= [https://x.com/korei_xlix](https://x.com/korei_xlix)  
***
