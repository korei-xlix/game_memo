# ゲームメモ：minecraft：コマンドメモ

**★当リポジトリの利用にあたっては、必ず本readmeを確認してください★**  
  

このドキュメントはMinecrafttの知識とコマンド集です。  
  





## 目次 / Table of Contents

* [readme.md](../../readme.md)
  * [利用にあたって (Important notices for use)](../../readme.md#利用にあたっての注意事項--important-notices-for-use)

* 操作系メモ
  * [起動オプション](#起動オプション)
  * [操作方法](#操作方法)

* コマンドメモ
  * [バニラのコマンド](#バニラのコマンド)
  * [サーバコマンド](#サーバコマンドバニラmultiverse-core共通)
  * [コマンド：Multiverse-Core](#コマンドmultiverse-core)
  * [コマンド：Multiverse-Portalsm](#コマンドmultiverse-portalsm)
  * [コマンド：LuckPerms](#コマンドluckperms)

  * [最寄りの座標表示コマンド](#最寄りの座標表示コマンド)
  * [コマンド研究](#コマンド研究)

* 各仕様メモ
  * [マイニング分布](#マイニング分布)
  * [エンドラRTA 公式ルール](#エンドラrta-公式ルール)
  * [カエル仕様](#カエル仕様)
  * [村判定仕様](#村判定仕様)

* minecraftサーバメモ
  * [Korei's World（Realms鯖）](../my_server/koreis_world_realms.md)
  





## 起動オプション

[目次へ戻る](#目次--table-of-contents)  
  

```text
-Xmx2G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M

```
  





## 操作方法

[目次へ戻る](#目次--table-of-contents)  
  

```text
A   N     海藻きりかえ　　　ロックオン
B   M
X   G     パレット切り替え
Y   ESC

バック
Z    C
スタートJ

左ジョイスティック
P
モードシフト　　I

F3+F4       ゲームモード切替

```
  





## コマンド

### バニラのコマンド

[目次へ戻る](#目次--table-of-contents)  
  

よく使う、管理者が扱えるMinecraftバニラのコマンドです。  
マルチの場合はMultiverse-Coreのほうを参照ください。  
  

```text
ゲームモードを変更する
gamemode [モード]
　survival ：サバイバルモード
　creative ：クリエイティブモード
　spectator：スペクターモード
　adventure：サバイバルモード

ゲームの難易度を変更する
difficulty [難易度]
　easy    ：イージー
　normal  ：ノーマル
　hard    ：ハード
　peaceful：ピースフル

時間を変更する
time set [時間]
　sunrise‌ ：日の出。数値は23000。
　day     ：日中午前。数値は1000。
　noon    ：日中午後。数値は6000。
　sunset‌  ：日の入り。数値は12000。
　midnight：深夜。数値は18000。
　[数値]  ：数値に応じた時間に変更する

天気を変更する
weather [天気]
　clear  ：晴れ
　rain   ：雨
　thunder：雷雨

現在地から周囲16000ブロックまでを境界にする
worldborder center ~ ~
worldborder set 16000 0

初期スポーンを現在地に設定する
setworldspawn

テレポートする
　ワールド内テレポート
　　tp @p [X] [Y] [Z]

　ワールド間テレポート
　　execute in minecraft:[ワールドの種類] run tp @p [X] [Y] [Z]
　　　normal ：オーバーワールド
　　　nether ：ネザーワールド
　　　the_end：エンドワールド


スポナーを取得する
give @s spawner
　※取得できるのはスポナーの外装だけ。これにスポーンエッグを使うと機能する。

コマンドブロックを取得する
give @a minecraft:command_block
　黄色のコマンドブロック：インパルス「動力が必要（レッドストーンが必要）」
　緑色のコマンドブロック：チェーン「常時実行（常にアクティブ）」
　青色のコマンドブロック：リピート（反復）「動力が必要（レッドストーンが必要）」

```
  



### サーバコマンド（バニラ・Multiverse-Core共通）

[目次へ戻る](#目次--table-of-contents)  
  

サーバ制御用のコマンドです。  
  

```text
サーバ停止
stop

ログイン中のユーザ表示
list

強制セーブする
save-all

ワールドのシード値を表示する
seed


ホワイトリストにユーザを追加する
whitelist add [username]

管理者権限を与える
op [ユーザ名]
　※荒らしに使われるので他のユーザには絶対使わないこと

管理者権限をはく奪する
deop [ユーザ名]

```
  



### コマンド：Multiverse-Core

```text
ワールド情報を参照する
mv info [ワールド名]

ゲームモードを変更する（ログオフすると元に戻る）
gamemode [モード]
　survival ：サバイバルモード
　creative ：クリエイティブモード
　spectator：スペクターモード
　adventure：サバイバルモード

ワールドに入った時のゲームモードを設定する
mv modify [ワールド名] set gamemode [モード]
　survival ：サバイバルモード
　creative ：クリエイティブモード
　spectator：スペクターモード
　adventure：サバイバルモード

ワールドに入った時のゲーム難易度を設定する
mv modify [ワールド名] set difficulty [難易度]
　easy    ：イージー
　normal  ：ノーマル
　hard    ：ハード
　peaceful：ピースフル

ゲームルール情報を参照する
mv gamerule list [ワールド名]
mv gamerule list [ワールド名] --filter advance

時間の変化有無設定
mv gamerule set minecraft:advance_time [true/false] [ワールド名]

天気の変化有無設定
mv gamerule set minecraft:advance_weather [true/false] [ワールド名]

エンティティスポーン情報を参照する
mv entity-spawn-config info [ワールド名]

魔物の沸き有無設定
mv entity-spawn-config modify [ワールド名] monster set spawn [true/false]

X:0,Z:0から周囲16000ブロック（直径）までを境界にする
mv worldborder center 0 0
mv worldborder set 16000

初期スポーンを現在地に設定する
mv setspawn

テレポートする
　ワールドの初期スポーン地にテレポート
　　mv tp [ワールド名]

　ワールドの指定位置にテレポート
　　mv tp e:[ワールド名]:[X],[Y],[Z]



ワールドの一覧を表示する
mv list

ワールドを生成する
mv create [ワールド名] [ワールドの種類]
　normal ：オーバーワールド
　nether ：ネザーワールド
　the_end：エンドワールド

ワールドを削除する
mv delete [ワールド名]

```
  


### コマンド：Multiverse-Portalsm

```text
ポータル一覧
mvp list

斧を出す
mvp wand

ポータルを作成
mvp create [ポータル名]

ポータル削除
mvp remove [ポータル名]

ポータル選択
mvp select [ポータル名]

選択してるポータルと繋ぐ
mvp modify dest p:[ポータル名]


ポータルの作成と接続方法

1. /mvp wandで木の斧を出す。他の木の斧でもよい

2. ポータルの枠を作成し、木の斧でポータルの枠の左上をクリック、右下を右クリック

3. /mvp listでポータル名が被って無いことを確認し
   /mvp create [ポータル名1]でポータル1を作成

4. 2つ目のポータルの枠を作成し、木の斧で枠を指定して
   /mvp create [ポータル名2] p:[ポータル名1]でポータル1に繋がるポータルを作成。

5. このままではポータル1からポータル2に行くことが出来ないので
   /mvp select [ポータル名1]でポータル1を選択する。

6. /mvp modify dest p:[ポータル名2]でポータル1からポータル2へ繋ぎポータルの完成

```
  


### コマンド：LuckPerms

基本的にWebエディタから操作をするほうが、間違いはないと思われます。  
  

```text
WEBエディタを開く
lp editor

LP情報を表示する
lp info

グループを表示する
lp listgroups

グループのメンバー一覧を表示する
lp group [グループ名] listmembers


管理者権限設定
lp user lucida3poi permission set luckperms.*
lp creategroup admin
lp user lucida3poi parent add admin

lp creategroup member
lp group default parent add member


初期プラグイン権限設定
lp user lucida3poi permission set villagerbank.create false
lp user lucida3poi permission set villagerbank.create true
lp user lucida3poi permission unset villagerbank.create

```
  



### コマンド：WorldEdit

[参考資料](https://games.xserver.ne.jp/minecraft-media/worldedit/)  
  

```text
領域指定用の斧を召喚
左クリック=開始位置、右クリック=終了位置
　　//wand

指定領域をブロックに入れ替える
　　//set [id]

指定領域を空気ブロックに入れ替える
　　//set air

指定領域を土ブロックに入れ替える
　　//set minecraft:grass_block



```
  



### 最寄りの座標表示コマンド

[目次へ戻る](#目次--table-of-contents)  
  

最寄りのバイオームや建物の座標を出すチートコマンドです。  

```text
locate structure [オブジェクト名]
locate biome [バイオーム名]
　　詳細は、korei_world.mdとかに書いてある

-X/-Z     -Z          +X/-Z
          [NORTH]
-X                      +X
[WEST]       ●      [EAST]

          [SOUTH]
-X/+Z     +Z          +X/+Z
```
  



### コマンド研究

[目次へ戻る](#目次--table-of-contents)  
  

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
  



### コマンドブロック経済

```text
https://tokoton0ch.com/2020/02/20/post-1268/

コマンドブロックの入手
/give @p command_block

/gamerule commandBlockOutput false

/scoreboard objectives remove Coin

①スコアボードにの「Coin」を追加します。
scoreboard objectives add Coin dummy

②「Coin」を0にセットします。
※「Coin」を持っている時も0になります。設置場所やCoin追加方法には工夫が必要です。
scoreboard players set @p Coin 0

③サイドバーに「Coin」を表示します。
scoreboard objectives setdisplay sidebar Coin




execute if entity @e[scores={Coin=5..}] run scoreboard players remove @p Coin 5

give @p iron_ingot 1




ベイクドポテト   baked_potato
パンプキンパイ   pumpkin_pie
ステーキ    cooked_beef

ラピスラズリ   lapis_lazuli
糸      string
乾燥した昆布   dried_kelp
火打石     flint
粘土     clay_ball
エンダーパール   ender_pearl

鉄インゴット   iron_ingot
金インゴット   gold_ingot
ダイヤ     diamond

名前タグ    name_tag
白紙の地図    map

フグ     pufferfish
金のニンジン   golden_carrot
マグマクリーム   magma_cream

矢      arrow
弓      bow
盾      shield
剣      diamond_sword
ピッケル    diamond_pickaxe
斧      diamond_axe
シャベル    diamond_shovel
クワ     diamond_hoe

白色の染料    white_dye
橙色の染料    orange_dye
赤紫色の染料   magenda_dye
空色の染料    light_blue_dye
黄色の染料    yellow_dye
黄緑色の染料   lime_dye
桃色の染料    pink_dye
灰色の染料    gray_dye
薄灰色の染料   light_gray_dye
青緑色の染料   cyan_dye
紫色の染料    purple_dye
青色の染料    blue_dye
茶色の染料    brown_dye
緑色の染料    green_dye
赤色の染料    red_dye
黒色の染料    black_dye



エンチャント本
ダメージ増加   /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:sharpness,lvl:5}]}
アンデッド特攻   /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:smite,lvl:5}]}
火属性     /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:fire_aspect,lvl:2}]}
ドロップ増加   /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:looting,lvl:3}]}
範囲ダメージ増加  /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:sweeping,lvl:3}]}

射撃ダメージ増加  /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:power,lvl:5}]}
フレイム    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:flame,lvl:1}]}
無限     /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:infinity,lvl:1}]}

シルクタッチ   /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:silk_touch,lvl:1}]}
幸運     /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:fortune,lvl:3}]}
効率強化    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:efficiency,lvl:5}]}

耐久力     /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:unbreaking,lvl:3}]}
修繕     /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:mending,lvl:1}]}

ダメージ軽減   /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:protection,lvl:4}]}
火炎耐性    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:fire_protection,lvl:4}]}
爆発耐性    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:blast_protection,lvl:4}]}

落下耐性    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:feather_falling,lvl:4}]}
水中採掘    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:aqua_affinity,lvl:1}]}
水中歩行    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:depth_strider,lvl:3}]}
氷渡り     /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:frost_walker,lvl:2}]}
ソウルスピード   /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:soul_speed,lvl:3}]}

水中呼吸    /give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:respiration,lvl:3}]}

釣竿（宝釣り・入れ食い・耐久力）
      /give @p minecraft:fishing_rod{HideFlags:1,Enchantments:[{id:unbreaking,lvl:3},{id:luck_of_the_sea,lvl:3},{id:lure,lvl:3}]}

クロスボウ（貫通4・高速装填3・耐久力）
      /give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:unbreaking,lvl:3},{id:quick_charge,lvl:3},{id:piercing,lvl:4}]}
クロスボウ（拡散1・高速装填3・耐久力）
      /give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:unbreaking,lvl:3},{id:quick_charge,lvl:3},{id:multishot,lvl:1}]}

水生特効5・忠誠3・召雷1 /give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:loyalty,lvl:3},{id:impaling,lvl:5},{id:channeling,lvl:1}]}
水生特効5・激流3  /give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:impaling,lvl:5},{id:riptide,lvl:3}]}



https://minecraft-ja.gamepedia.com/%E6%9F%93%E6%96%99

0 白色のテラコッタ *
1 橙色のテラコッタ *
4 黄色のテラコッタ *
8 薄灰色のテラコッタ *
12 茶色のテラコッタ *
14 赤色のテラコッタ *

2 赤紫色のテラコッタ \
3 空色のテラコッタ \
5 黄緑色のテラコッタ \
6 桃色のテラコッタ \
11 青色のテラコッタ \
13 緑色のテラコッタ \
15 黒色のテラコッタ \

7 灰色のテラコッタ
9 水色のテラコッタ
10 紫色のテラコッタ



https://minecraft-blog.net/?p=9605

/mv rule doDaylightCycle false world

execute unless score @p Coin matches 1.. run scoreboard players set @p Coin 0

execute if entity @e[scores={Coin=5..}] run give @p iron_ingot 1

execute if entity @e[scores={Coin=5..}] run scoreboard players remove @p Coin 5




https://ch.nicovideo.jp/kirisamealice/blomaga/ar1744541

1.アイテム数検知用スコアの作成
[チャット/コマンドブロック]
/scoreboard objectives add [スコアの名前(英文字のみ)] dummy ["表示名(日本語可)"]

2.アイテム数を検知し、スコアに代入
『コマンドブロック[インパルス/無条件/動力が必要]』
/execute positioned [コマンド発動座標] as @p[distance=..1] store result score @s [スコアの名前(英文字のみ)] run clear @s [検知するアイテム] 0

3.指定したアイテムを指定数以上所持している場合、アイテム消去
『コマンドブロック[チェーン/条件(どちらでも可)/常時実行]』
/execute if score @p [スコアの名前(英文字のみ)] matches [検知するアイテム数の必要数] run clear @p [消去するアイテム] [個数]

4(任意).テキスト表示
『コマンドブロック[チェーン/条件(どちらでも可)/常時実行]』
/tell @p[scores={[スコアの名前(英文字のみ)]=[検知するアイテム数の必要数]}] [表示テキスト]





動画内で使用したコマンド:
1.アイテム数検知スコアの作成
/scoreboard objectives add DiamondCount dummy "ダイヤ所持数"
・『DiamondCount』でアイテム数を検知するスコアを作成

2.アイテム数を検知し、スコアに代入
/execute positioned ~1 ~ ~ as @p[distance=..1] store result score @s DiamondCount run clear @s minecraft:diamond 0
・指定座標にいたプレイヤーのダイヤモンドの所持数を『DiamondCount』に代入

3.指定したアイテムを指定数以上所持している場合、アイテム消去
/execute if score @p DiamondCount matches 10.. run clear @p minecraft:diamond 10
・『DiamondCount』が10以上の時、ダイヤモンドを10個消去する
　∟座標を指定すると誤作動を防止できる

4(任意).テキスト表示
/tell @p[scores={DiamondCount=10..}] ダイヤを10個消費しました
・消去したプレイヤーにテキストを表示する

```
  





## マイニング分布

[目次へ戻る](#目次--table-of-contents)  
  

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
  





## エンドラRTA 公式ルール

[目次へ戻る](#目次--table-of-contents)  
  

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
  


### 流れ

* 1. ワールドを生成　＜ＲＴＡ開始＞  

* 2.必要なものを集める  
  必須：鉄、バケツ、弓（蜘蛛の糸）、矢（羽根、火打石）、打ち金（鉄、火打石）  
  かまど、食べ物、エンダーパール（エンダーマン）  
  あれば：鉄装備  

* 3.溶岩からできる黒曜石でネザーポータルを作成  
  ※バケツがあればダイヤピッケルなしでも、水と溶岩で地形にポータルが作れる  

* 4.ネザーにてブレイズを倒して入手できるブレイズロッドを集める  
   ※2～4は平行作業可能  

* 5.エンダーパールとブレイズパウダー（ブレイズロッドから作成）を組み合わせてできる  
  エンダーアイを使いエンドポータルを探す  
  ※エンダーパールがたくさんなくても先に探せる  

* 6.エンドポータルに必要数エンダーアイをセットしポータルを起動後  
  エンドポータルからジ・エンドへ  

* 7.ジ・エンドにてエンダードラゴンの回復基となるエンダークリスタルを破壊後  
  エンダードラゴンを討伐  

* 8.エンダードラゴン討伐後に生成される祭壇（帰還用ポータル）に入る  
  ＜ＲＴＡ終了＞  
  





## カエル仕様

[目次へ戻る](#目次--table-of-contents)  
  

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
  





## 村判定仕様

[目次へ戻る](#目次--table-of-contents)  
  

村判定の範囲仕様を示す。なお、ここでは統合版の話でまとめる。  
  
参考: [村判定の実際の範囲と高さをクリエで検証【統合版】](https://timekyousyou.com/minecraftbe-village-range)  
  

結論から。  
正確な広さは村のベッドから95マス内、高さ76マス内。  
村のベッドは、村長と紐づけされたベッドのことだが、村長は固定できず、人口増加で勝手に代わってしまう。  
なので、村を作るときは、ベッド群を一か所作っておいて、そこ以外の95マス以内にはベッドを置かないようにする。  
  
村人を使うトラップや交易所を作る場合は、ベッド群になりえる位置から200マス以上離したところに置くこと。  
交易所を作る場合は、交易所となりえる位置から200マス以内にはベッドを置かないこと。  
  


### 村のベッド＝村の中心

**村のベッドは、村長と紐づけされたベッドのことを言う。**  
ただ、この"村長"は固定できず、人口増加とともに勝手に代わってしまう。  
なお、村長を特定するのは、ベルを壊したときに怒った村人＝村長ということ。  
  


### 村の実際の範囲

　　　　　　　　　　　　村のベッド  
◆----------◆----------□----------◆----------◆  
　95マス以上　　95マス　　　95マス　　　95マス以上  
  
紐づけは100マス離れていればできるということ。  
村A、Bで判定を重ねたくなければ、200マス以上離せばいい。  
  

### 村の実際の高さ

　　◆  
　　｜　76マス以上  
　　◆  
　　｜　76マス  
　　□　　村のベッド
　　｜　76マス  
　　◆  
　　｜　76マス以上  
　　◆  
  
紐づけは76マス離れていればできるということ。  
76マスを超えると、紐づけされない。  
  





***
***
[[トップへ戻る]](../../readme.md)　/
[[minecraft]](/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= [https://github.com/korei-xlix/](https://github.com/korei-xlix/)  
::Web= [https://website.koreis-labo.com/](https://website.koreis-labo.com/)  
::X= [https://x.com/korei_xlix](https://x.com/korei_xlix)  
***
