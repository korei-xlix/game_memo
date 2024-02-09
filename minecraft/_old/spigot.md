# minecraft攻略メモ ～コマンド～

# 目次 <a name="aMokuji"></a>
* [起動オプション](#aStartOption)
* [v1.18マイニング分布](#a118mining)
* [最寄りの座標表示コマンド](#aLocate)
* [エンドラRTA 公式ルール](#aEnDraRTTAOfficial)




# Multiverse-Core コマンド <a name="aMultiverse-Core"></a>
Multiverse-Core：サーバ管理プラグインでよく使うコマンドです。  

```
ワールド情報を参照する
mv info world

ワールドにテレポートする
mv tp [ワールド名]

ワールドに入った時のゲームモードを設定する
mvm set gamemode [0-3] [ワールド名]
	0: サバイバルモード
	1: クリエイティブモード
	2: アドベンチャーモード
	3: スペクテイターモード

ワールドの難易度を設定する
mvm set difficulty [0-3] [ワールド名]
	0: ピースフル
	1: イージー
	2: ノーマル
	3: ハード

魔物の沸きの有無
mvm set monsters true world
mvm set monsters false world

天気の変化の有無
mvm set weather true world
mvm set weather false world

時間の変化の有無
mvrule doDaylightCycle true world
mvrule doDaylightCycle false world


ワールドを生成する
mv create [ワールド名] [NORMAL/NETHER/THE_END]

ワールドを削除する
mv delete [ワールド名]

初期スポーンを現在地に再設定する
mv set spawn


管理者権限を与える
op [ユーザ名]
　※spigotを使う際、真っ先に自分に使うコマンド
　※荒らしに使われるので他のユーザには絶対使わないこと

```







Multiverse-Portals：ゲート開設プラグイン

/mvp wand	斧を出す

/mvp create [ポータル名]	ポータル作成

/mvp remove [ポータル名]	ポータル削除

/mvp select [ポータル名]	ポータル選択

/mvp modify dest p:[ポータル名]		選択してるポータルと繋ぐ

/mvp list					ポータル一覧



1. /mvp wandで木の斧を出す。他の木の斧でもよい

2. ポータルの枠を作成し、木の斧でポータルの枠の左上をクリック、右下を右クリック

3. /mvp listでポータル名が被って無いことを確認し
   /mvp create [ポータル名1]でポータル1を作成
.

4. 2つ目のポータルの枠を作成し、木の斧で枠を指定して
   /mvp create [ポータル名2] p:[ポータル名1]でポータル1に繋がるポータルを作成。

5. このままではポータル1からポータル2に行くことが出来ないので
   /mvp select [ポータル名1]でポータル1を選択する。

6. /mvp modify dest p:[ポータル名2]でポータル1からポータル2へ繋ぎポータルの完成


------------------------------------------------------------
コマンドブロック経済（JAVA 1.16.5）
https://tokoton0ch.com/2020/02/20/post-1268/

コマンドブロックの入手
/give @p command_block

黄色のコマンドブロック：インパルス「動力が必要（レッドストーンが必要）」
緑色のコマンドブロック：チェーン「常時実行（常にアクティブ）」
青色のコマンドブロック：リピート（反復）「動力が必要（レッドストーンが必要）」


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




ベイクドポテト			baked_potato
パンプキンパイ			pumpkin_pie
ステーキ				cooked_beef

ラピスラズリ			lapis_lazuli
糸						string
乾燥した昆布			dried_kelp
火打石					flint
粘土					clay_ball
エンダーパール			ender_pearl

鉄インゴット			iron_ingot
金インゴット			gold_ingot
ダイヤ					diamond

名前タグ				name_tag
白紙の地図				map

フグ					pufferfish
金のニンジン			golden_carrot
マグマクリーム			magma_cream

矢						arrow
弓						bow
盾						shield
剣						diamond_sword
ピッケル				diamond_pickaxe
斧						diamond_axe
シャベル				diamond_shovel
クワ					diamond_hoe

白色の染料				white_dye
橙色の染料				orange_dye
赤紫色の染料			magenda_dye
空色の染料				light_blue_dye
黄色の染料				yellow_dye
黄緑色の染料			lime_dye
桃色の染料				pink_dye
灰色の染料				gray_dye
薄灰色の染料			light_gray_dye
青緑色の染料			cyan_dye
紫色の染料				purple_dye
青色の染料				blue_dye
茶色の染料				brown_dye
緑色の染料				green_dye
赤色の染料				red_dye
黒色の染料				black_dye



エンチャント本
ダメージ増加			/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:sharpness,lvl:5}]}
アンデッド特攻			/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:smite,lvl:5}]}
火属性					/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:fire_aspect,lvl:2}]}
ドロップ増加			/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:looting,lvl:3}]}
範囲ダメージ増加		/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:sweeping,lvl:3}]}

射撃ダメージ増加		/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:power,lvl:5}]}
フレイム				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:flame,lvl:1}]}
無限					/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:infinity,lvl:1}]}

シルクタッチ			/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:silk_touch,lvl:1}]}
幸運					/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:fortune,lvl:3}]}
効率強化				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:efficiency,lvl:5}]}

耐久力					/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:unbreaking,lvl:3}]}
修繕					/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:mending,lvl:1}]}

ダメージ軽減			/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:protection,lvl:4}]}
火炎耐性				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:fire_protection,lvl:4}]}
爆発耐性				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:blast_protection,lvl:4}]}

落下耐性				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:feather_falling,lvl:4}]}
水中採掘				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:aqua_affinity,lvl:1}]}
水中歩行				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:depth_strider,lvl:3}]}
氷渡り					/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:frost_walker,lvl:2}]}
ソウルスピード			/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:soul_speed,lvl:3}]}

水中呼吸				/give @p minecraft:enchanted_book{HideFlags:1,StoredEnchantments:[{id:respiration,lvl:3}]}

釣竿（宝釣り・入れ食い・耐久力）
						/give @p minecraft:fishing_rod{HideFlags:1,Enchantments:[{id:unbreaking,lvl:3},{id:luck_of_the_sea,lvl:3},{id:lure,lvl:3}]}

クロスボウ（貫通4・高速装填3・耐久力）
						/give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:unbreaking,lvl:3},{id:quick_charge,lvl:3},{id:piercing,lvl:4}]}
クロスボウ（拡散1・高速装填3・耐久力）
						/give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:unbreaking,lvl:3},{id:quick_charge,lvl:3},{id:multishot,lvl:1}]}

水生特効5・忠誠3・召雷1	/give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:loyalty,lvl:3},{id:impaling,lvl:5},{id:channeling,lvl:1}]}
水生特効5・激流3		/give @p minecraft:crossbow{HideFlags:1,Enchantments:[{id:impaling,lvl:5},{id:riptide,lvl:3}]}



stop		サーバ停止
list		ログイン中のユーザ表示
save-all	サーバ全体をセーブ



https://minecraft-ja.gamepedia.com/%E6%9F%93%E6%96%99

0	白色のテラコッタ	*
1	橙色のテラコッタ	*
4	黄色のテラコッタ	*
8	薄灰色のテラコッタ	*
12	茶色のテラコッタ	*
14	赤色のテラコッタ	*

2	赤紫色のテラコッタ	\
3	空色のテラコッタ	\
5	黄緑色のテラコッタ	\
6	桃色のテラコッタ	\
11	青色のテラコッタ	\
13	緑色のテラコッタ	\
15	黒色のテラコッタ	\

7	灰色のテラコッタ
9	水色のテラコッタ
10	紫色のテラコッタ



https://minecraft-blog.net/?p=9605

/mv rule doDaylightCycle false world

execute unless score @p Coin matches 1.. run scoreboard players set @p Coin 0

execute if entity @e[scores={Coin=5..}] run give @p iron_ingot 1

execute if entity @e[scores={Coin=5..}] run scoreboard players remove @p Coin 5


------------------------------------------------------------
サーバの建て方
https://docs.google.com/document/d/1vJta5yIS07ofzGKkFwy6gkESrZzA0mXTJysZnW9Le_A/edit

バニラサーバ
https://www.minecraft.net/ja-jp/download/server

spigot版マイクラ：改造マイクラ
https://hub.spigotmc.org/jenkins/job/BuildTools/

1.gitを導入する

2.git bashを実行する

3.spigotをgitで見えるフォルダに入れる

4.コマンドを実行する
java -Xmx1024M -jar BuildTools.jar --rev latest
java -Xmx1024M -jar BuildTools.jar --rev 1.17
java -Xmx1024M -jar BuildTools.jar --rev 1.17.1

※1GB以上でないと起動時に警告がでる

5.spigot-1.16.5.jarをコピーして、適当にサーバディレクトリを作成する

6.一回サーバを起動する
java -Xmx1024M -Xms1024M -jar spigot-1.17.0.jar nogui

7. eula.txtのfalse → trueに書き換える

8.サーバをもう一回起動して、stopで終了する

9.plugins フォルダに、Multiverse-Core-*.jar、Multiverse-Portals-*.jar を入れる

10.サーバをもう一回起動する

11.mv list でワールドが表示されればOK

12. マイクラクライアントでIPログインする（自分のPCのローカルIPアドレスだよ）


＜server.propertyの調整＞

コマンドブロック有効
enable-command-block=true

最大接続数
max-players=32

ホワイトリスト制
white-list=true

サーバー紹介文
motd=A Minecraft Server \u00A79[version 1.14.x] By Spigot


ホワイトリストにユーザを追加するコマンド
whitelist add [username]



＜LukePerem＞
config設定  config.yml

前提：postgresqlを使用する場合、db、ユーザは予めpostgresql側で作成しておく

storage-method: postgresql
address: localhost
database: minecraft
username: root
password: ''

管理者権限設定
lp user lucida3poi permission set luckperms.*
lp creategroup admin
lp user lucida3poi parent add admin

lp creategroup member
lp group default parent add member

lp listgroups
lp group admin listmembers


初期プラグイン権限設定
lp user lucida3poi permission set villagerbank.create false
lp user lucida3poi permission set villagerbank.create true
lp user lucida3poi permission unset villagerbank.create



https://seesaawiki.jp/perominecraft/d/LuckPerms%20-%20%BB%C8%CD%D1%CA%FD%CB%A1%28%BD%E9%BF%B4%BC%D4%B8%FE%A4%B1%29



According to the command usage, you should be able to define per-world permissions like so: /lp user/group <user|group> permission set <perm> <value> world=<world [コマンドの使用法に従って、ワールドごとの権限を次のように定義できるはずです: /lp user/group <user|group> permission set <perm> <value> world=<world] >

Examples:

/lp group default permission set essentials.sethome false world=anarchy

/lp user stonewickSMP permission set essentials.god true world=anarchy

Apparently, there is an older way of doing it: /lp user/group <user|group> permission set <perm> <value> global <world>



＜GriefPrevention＞
SeaLevelOverrides
-1にする（※新ワールド生成時も確認しておくこと）

TNTやクリーパーでの建物爆破制限を解除する
ただし、土地保護されたものは破壊できない
BlockSurfaceCreeperExplosions: false
BlockSurfaceOtherExplosions: false

ピストンの動作を許可する
PistonMovement: EVERYWHERE



＜LWC＞
core.ymlのblocksのautoRegisterを全てfalseに設定する
autoRegister: false




------------------------------

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







                           









***
[[トップへ戻る]](/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= https://github.com/korei-xlix/  
::Homepage= https://website.koreis-labo.com/  
::Twitter= https://twitter.com/korei_xlix  
