# minecraft攻略メモ
  
<h1>～マイクラ知識・コマンド集～</h1>  
  

**★このリポジトリの改造、流用、配布、クローンは禁止です★**  
    **Modification, diversion, distribution, and cloning of this repository are prohibited**  
  

<h1 id="aHowto">このドキュメントについて / About this document</h1>  
このドキュメントはMinecrafttの知識とコマンド集です。  
  




<h1 id="aMokuji">目次 / Table of contents</h1>  

* [readme.md](/readme.md)

* [起動オプション](#aStartOption)
* [操作方法](#aControl)

* [マイニング分布](#a118mining)
* [最寄りの座標表示コマンド](#aLocate)
* [管理者コマンド](#aAdminCommand)
* [コマンド研究](#aCommandResearch)
* [エンドラRTA 公式ルール](#aEnDraRTTAOfficial)
* [カエル仕様](#aFlog)
  





<h1 id="aStartOption">起動オプション</h1>  
  
  [目次へ戻る](#aMokuji)  
  

```text
-Xmx2G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
```
  





<h1 id="aControl">操作方法</h1>  
  
  [目次へ戻る](#aMokuji)  
  

```text
A   N  海藻きりかえ　　　ロックオン
B   M
X   G    パレット切り替え
Y   ESC

バック
Z    C
スタートJ

左ジョイスティック
P
モードシフト　　I
```
  





<h1 id="a118mining">マイニング分布</h1>  
  
  [目次へ戻る](#aMokuji)  
  

参考: [効率的なブランチマイニングの新常識‼全鉱石対応・ダイヤモンドがとれる高さなど鉱石分布について詳しく解説](https://www.youtube.com/watch?v=4d7_nVLU6WM)  
  

```text
石炭
    136～320
    0～192        Y=96がピーク
    ※Y=0以下には生成されない

    山あり=Y-136付近
    山なし=Y=96付近

鉄
    80～320        Y=232がピーク
    -24～56        Y=16がピーク
    Y=72未満は小さい塊が分布
    Y=0未満に鉄の鉱脈がある

    山あり=Y=232
    山なし=Y=16

ダイヤ
    Y=-53がベスト
    ※Y=-54が溶岩層

    仕様：
        Y=16未満
        下にいくほど生成率があがる

銅
    Y=48がベスト
    16～112        Y=48がピーク
    鍾乳洞に多く生成
    Y=0以上に銅鉱脈あり

金
    Y=-16がベスト
    -64～32        Y=-16がピーク
    -48未満
    32～256    ※メサ限定

ラピス
    Y=8がベスト※深層岩除け
    洞窟はY=0付近
    32～32        Y=0がピーク
    64未満

レッドストーン
    -64～15
    -64～-32
    下ほど生成率が高い

エメラルド
    -16～320
    高くなるほど生成率があがる
    ※山岳バイオームのみ
```
  





<h1 id="aLocate">最寄りの座標表示コマンド</h1>  
  
  [目次へ戻る](#aMokuji)  
  

最寄りのバイオームや建物の座標を出すチートコマンドです。  

```text
locate structure #minecraft:village              村
locate structure minecraft:mansion               森の洋館
locate structure minecraft:monument              神殿
locate structure minecraft:pillager_outpost      前線基地
locate structure minecraft:ancient_city          古代都市
locate structure minecraft:stronghold            要塞（エンドポータル）
locate biome minecraft:dripstone_caves           鍾乳洞

locate biome minecraft:badlands                  荒野（メサ）
locate biome minecraft:jungle                    ジャングル
locate biome minecraft:desert                    砂漠
locate biome minecraft:flower_forest             花の森
locate biome minecraft:sunflower_plains          ヒマワリ平原
locate biome minecraft:swamp                     沼地
locate biome minecraft:mangrove_swamp            マングローブの沼
locate biome minecraft:ice_spikes                 樹氷
locate biome minecraft:mushroom_fields            マッシュルームの島
locate biome cherry_grove                         サクラ

locate biome minecraft:warm_ocean                 暖かい海
locate biome minecraft:deep_ocean                 深い海
locate biome minecraft:deep_frozen_ocean          凍った深海

locate structure fortress                         ネザー要塞
locate structure bastion_remnant                  砦の遺跡（ネザー)

locate biome minecraft:crimson_forest             真紅の森（赤い森）
locate biome minecraft:warped_forest              歪んだ森（青森）
locate biome minecraft:basalt_deltas              三角地帯
locate biome minecraft:soul_sand_valley           ソウルサンドの谷

locate structure endcity                          エンドシティ
                                                  

-X/-Z     -Z          +X/-Z
          [NORTH]
-X                      +X
[WEST]       ●      [EAST]

          [SOUTH]
-X/+Z     +Z          +X/+Z
```
  





<h1 id="aAdminCommand">管理者コマンド</h1>  
  
  [目次へ戻る](#aMokuji)  
  

よく使う、管理者が扱えるMinecraftバニラのコマンドです。  

```text
ゲームモードを変更する
gamemode survival
    survival: サバイバルモード
    creative: クリエイティブモード
    spectator: スペクテイターモード
    adventure: アドベンチャーモード

ゲームの難易度を変更する
difficulty normal
    peaceful: ピースフル
    easy: イージー
    normal: ノーマル
    hard: ハード

時間を変更する
time set day
    sunrise‌: 日の出。数値は23000。
    day: 日中午前。数値は1000。
    noon: 日中午後。数値は6000。
    sunset‌: 日の入り。数値は12000。
    midnight: 深夜。数値は18000。
    [数値]: 数値に応じた時間に変更する

天気を変更する
weather clear
    clear: 晴れ
    rain : 雨
    thunder : 雷雨

現在地から周囲5000ブロックまでを境界にする
worldborder center ~ ~
worldborder set 16000 0

初期スポーンを現在地に設定する
setworldspawn

強制セーブする
save-all

ワールドのシード値を表示する
seed

スポナーを取得する
give @s spawner
　※取得できるのはスポナーの外装だけ。これにスポーンエッグを使うと機能する。

execute in minecraft:the_nether run tp @p 100 100 100

コマンドブロックを取得する
give @a minecraft:command_block
```
  





<h1 id="aCommandResearch">コマンド研究</h1>  
  
  [目次へ戻る](#aMokuji)  
  

* [Minecraft公式wiki コマンド](https://minecraft.fandom.com/ja/wiki/%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89)

* [ターゲットセレクター](https://minecraft.fandom.com/ja/wiki/%E3%82%BF%E3%83%BC%E3%82%B2%E3%83%83%E3%83%88%E3%82%BB%E3%83%AC%E3%82%AF%E3%82%BF%E3%83%BC)

* [nbtデータ プレイヤー](https://minecraft.fandom.com/ja/wiki/Player.dat%E3%83%95%E3%82%A9%E3%83%BC%E3%83%9E%E3%83%83%E3%83%88)

* 座標（pos）：F3の **Blick** の項目を見ること。
  

```text
scoreboard: スコアボード操作

スコアボードを消す（表示）
scoreboard objectives setdisplay sidebar

スコアボードを消す（points）
scoreboard objectives remove points

衝撃：無条件：動力必要
clear @p[nbt={Inventory:[{Slot:8b,id:"minecraft:diamond_sword"}]}] minecraft:diamond_sword 0

チェーン：条件あり：動力必要
item replace entity @p hotbar.8 with minecraft:diamond 1

give: アイテムを渡す

clear: アイテム消去

ダイヤヘルムを装備してたら、ダイヤを1個消す
clear @p[nbt={Inventory:[{Slot:103b,id:"minecraft:diamond_helmet"}]}] minecraft:diamond 1

スロット右にダイヤヘルムがあｔったら、ダイヤを1個消す
clear @p[nbt={Inventory:[{Slot:8b,id:"minecraft:diamond_helmet"}]}] minecraft:diamond 1

clear @p[nbt={Inventory:[{Slot:8b,id:"minecraft:enchanted_book"}]}] minecraft:enchanted_book 1

clear @p[nbt={Inventory:[{Slot:8b,id:"minecraft:enchanted_book",tag:{StoredEnchantments:[{lvl:1}]}}]}] minecraft:enchanted_book 0

item: ブロックのインベントリ操作

チェストの左上にダイヤを1個セットする
item replace block 0 -60 0 container.0 with minecraft:diamond 1

execute : 他のコマンドを実行する汎用コマンド

インベントリにあるアイテム数を計算
/execute as @a store result score @s points run clear @s minecraft:iron_ingot 0

1.18.20のアップデートでhasitemというのが追加されます。このhasitemが特定のアイテムを持つと検知するコマンドです。
例えばダイヤモンドの剣を持つと攻撃力上昇レベル5が付与したい場合コマンドブロックでこのコマンドを入力します
/execute @e[hasitem={item=diamond_sword, location=slot.weapon.mainhand}] ~~~ effect @s strength 1 4 true
そして反復にすればできます。このhasitemは装備を検知したり、アイテムの数を指定したり、スロットの位置を指定することだってできます。

/setblock ~ ~2 ~ minecraft:chest
/data merge block ~ ~2 ~ {Items:[{id:"minecraft:arrow",Count:1,Slot:0},{id:"minecraft:arrow",Count:1,Slot:1},{id:"minecraft:arrow",Count:2,Slot:2},・・・{id:"minecraft:arrow",Count:4,Slot:26}]}

```
  





<h1 id="aEnDraRTTAOfficial">エンドラRTA 公式ルール</h1>  
  
  [目次へ戻る](#aMokuji)  
  

参考: [ニコ生エンダードラゴン討伐TA・RTA記録室](https://wikiwiki.jp/enderdragon/)  
  

* ワールドの生成開始と同時にタイマースタート  
　エンドラ討伐後に生成されるポータル突入と同時にタイマーストップ  
* 難易度はHARDモード
* F3使用禁止
* MODは原則禁止  
　日本語MODは禁止（言語の壁が競技の障害とならないように）  
　軽量化MODはOK（個人のPCスペックで技量に差がでないように）  
* サーバコマンドは原則禁止
* 人数は何人でも問題はないが、ある程度の基準統一のために記録は人数で分別
  

<h2>流れ</h2>  

* 1. ワールドを生成　＜ＲＴＡ開始＞  

* 2. 必要なものを集める  
  必須：鉄、バケツ、弓（蜘蛛の糸）、矢（羽根、火打石）、打ち金（鉄、火打石）  
  かまど、食べ物、エンダーパール（エンダーマン）  
  あれば：鉄装備  

* 3. 溶岩からできる黒曜石でネザーポータルを作成  
  ※バケツがあればダイヤピッケルなしでも、水と溶岩で地形にポータルが作れる  

* 4. ネザーにてブレイズを倒して入手できるブレイズロッドを集める  
   ※2～4は平行作業可能  

* 5. エンダーパールとブレイズパウダー（ブレイズロッドから作成）を組み合わせてできる  
  エンダーアイを使いエンドポータルを探す  
  ※エンダーパールがたくさんなくても先に探せる  

* 6. エンドポータルに必要数エンダーアイをセットしポータルを起動後  
  エンドポータルからジ・エンドへ  

* 7. ジ・エンドにてエンダードラゴンの回復基となるエンダークリスタルを破壊後  
  エンダードラゴンを討伐  

* 8. エンダードラゴン討伐後に生成される祭壇（帰還用ポータル）に入る  
  ＜ＲＴＡ終了＞  
  





<h1 id="aFlog">カエル仕様</h1>  
  
  [目次へ戻る](#aMokuji)  
  

* スライムボールで孵化できる。（つがいに食わせる）
* リードでひっぱれはする

* タマゴは水に生むので、水中でスライムボールを食われて。
* タマゴは運べない。
* タマゴが孵化すると、オタマジャクシになる。  
  この状態で水バケツで運べる。  
* 成長するとカエルになる。

* なお成長したバイオームによって色が変わる。  
  * 白：マングローブ、砂漠  
  * 橙：平原、湿地  
  * 緑：氷原、タイガ  

* カエルがスライム、マグマスライムを攻撃すると、フロッグライトを生成する。  
  生成するフロッグライトのカラーはカエルの色によって異なる。  
  * 白：真珠色  
  * 橙：黄土色  
  * 緑：新緑色  

* [参考](https://minecraft.fandom.com/ja/wiki/%E3%82%AB%E3%82%A8%E3%83%AB)  
  





***
[[トップへ戻る]](/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= [https://github.com/korei-xlix/](https://github.com/korei-xlix/)  
::Web= [https://website.koreis-labo.com/](https://website.koreis-labo.com/)  
::X= [https://twitter.com/korei_xlix](https://twitter.com/korei_xlix)  
