# Minecraft知識
**Minecraft**  


# このドキュメントについて <a name="aHowto"></a>
このドキュメントはMinecrafttの知識メモです。  


# 目次 <a name="aMokuji"></a>
* [起動オプション](#aStartOption)
* [v1.18マイニング分布](#a118mining)
* [最寄りの座標表示コマンド](#aLocate)
* [エンドラRTA 公式ルール](#aEnDraRTTAOfficial)




# 起動オプション <a name="aStartOption"></a>

```
-Xmx2G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
```




# v1.18マイニング分布 <a name="a118mining"></a>

参考: [効率的なブランチマイニングの新常識‼全鉱石対応・ダイヤモンドがとれる高さなど鉱石分布について詳しく解説](https://www.youtube.com/watch?v=4d7_nVLU6WM)  

```
石炭
	136～320
	0～192		Y=96がピーク
	※Y=0以下には生成されない

	山あり=Y-136付近
	山なし=Y=96付近

鉄
	80～320		Y=232がピーク
	-24～56		Y=16がピーク
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
	16～112		Y=48がピーク
	鍾乳洞に多く生成
	Y=0以上に銅鉱脈あり

金
	Y=-16がベスト
	-64～32		Y=-16がピーク
	-48未満
	32～256	※メサ限定

ラピス
	Y=8がベスト※深層岩除け
	洞窟はY=0付近
	32～32		Y=0がピーク
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




# 最寄りの座標表示コマンド <a name="aLocate"></a>

最寄りのバイオームや建物の座標を出すチートコマンドです。  

```
locate #minecraft:village			村
locate minecraft:mansion			森の洋館
locate minecraft:monument			神殿
locate minecraft:pillager_outpost	前線基地
locate minecraft:stronghold			要塞（エンドポータル）
locatebiome badlands						荒野（メサ）
locatebiome jungle							ジャングル
locatebiome minecraft:desert				砂漠
locatebiome minecraft:warm_ocean			暖かい海
locatebiome minecraft:deep_ocean			深い海
locatebiome minecraft:deep_frozen_ocean		凍った深海
locatebiome minecraft:flower_forest			花の森
locatebiome minecraft:sunflower_plains		ヒマワリ平原
locatebiome minecraft:ice_spikes			樹氷
locatebiome minecraft:swamp					沼地
locatebiome minecraft:dripstone_caves		鍾乳洞
locate structure minecraft:ancient_city

locate fortress				ネザー要塞
locate bastion_remnant		砦の遺跡（ネザー)
locatebiome crimson_forest		真紅の森（赤い森）
locatebiome warped_forest		歪んだ森（青森）
locatebiome basalt_deltas		三角地帯

locate endcity				エンドシティ



-X/-Z     -Z          +X/-Z
          [NORTH]
-X                      +X
[WEST]       ●      [EAST]

          [SOUTH]
-X/+Z     +Z          +X/+Z
```




# 管理者コマンド <a name="aAdminCommand"></a>

よく使う、管理者が扱えるMinecraftバニラのコマンドです。  

```
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
worldborder set 12000 0

初期スポーンを現在地に設定する
setworldspawn

強制セーブする
save-all

ワールドのシード値を表示する
seed

スポナーを取得する
give @s spawner
　※取得できるのはスポナーの外装だけ。これにスポーンエッグを使うと機能する。

```




# エンドラRTA 公式ルール <a name="aEnDraRTTAOfficial"></a>

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
  
**流れ**  
1. ワールドを生成　＜ＲＴＡ開始＞  
2. 必要なものを集める  
   必須：鉄、バケツ、弓（蜘蛛の糸）、矢（羽根、火打石）、打ち金（鉄、火打石）  
   かまど、食べ物、エンダーパール（エンダーマン）  
   あれば：鉄装備  
3. 溶岩からできる黒曜石でネザーポータルを作成  
   ※バケツがあればダイヤピッケルなしでも、水と溶岩で地形にポータルが作れる  
4. ネザーにてブレイズを倒して入手できるブレイズロッドを集める  
   ※2～4は平行作業可能  
5. エンダーパールとブレイズパウダー（ブレイズロッドから作成）を組み合わせてできる  
   エンダーアイを使いエンドポータルを探す  
   ※エンダーパールがたくさんなくても先に探せる  
6. エンドポータルに必要数エンダーアイをセットしポータルを起動後  
   エンドポータルからジ・エンドへ  
7. ジ・エンドにてエンダードラゴンの回復基となるエンダークリスタルを破壊後  
   エンダードラゴンを討伐  
8. エンダードラゴン討伐後に生成される祭壇（帰還用ポータル）に入る  
   ＜ＲＴＡ終了＞  




***
[トップへ戻る](/readme.md)  
  
::Project= Game Memo  
::Admin= Korei (@korei-xlix)  
::github= https://github.com/korei-xlix/  
::Homepage= https://koreixlix.wixsite.com/profile  
