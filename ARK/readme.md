# Game Memo
  
<h1>～ARK～</h1>  
  

**★このドキュメントの改造、流用、配布、クローンは禁止です★**  
    **Modification, diversion, distribution, and cloning of this document are prohibited**  
  

<h1 id="aHowto">このドキュメントについて / About this document</h1>  
このドキュメントはARKのメモを示すものです。  
  





<h1 id="aMokuji">目次 / Table of contents</h1>  

* [readme.md](/readme.md)

* 資料編
  * [マップ概要](#aMap)
  * [恐竜図鑑](dinosaur.md)
  * [料理レシピ](cook.md)
  * [イースターエッグ一覧](easter.md)
  * [野生恐竜生成コマンド](cheet.md)
  * [ARK豆知識](#aSeed)
  * [ホロ鯖設定](holo_kaicho.md)

* ARK設定編
  * [ゲーム設定](#aGameSetting)
  * [導入mod](#aMod)
  * [コマンド一覧](#aCommands)

* [ARK2の情報](#aARK2info)
* [参考資料](#aMaterial)

* [テイム恐竜一覧](__theme.md)

  





<h1 id="aMap">マップ概要</h1>  
ARKのマップ概要を示します。  
  
  [目次へ戻る](#aMokuji)  
  

* **ストーリーARK**  
  * The Island
  * Scorched Earth
  * Aberration
  * Extinction
  

* **ストーリーARK::チャレンジ**  
  * Genesis part 1
  * Genesis part 2
  

* **カスタムARK（拡張マップ）**  
  * The Center
  * Valguero
  * Ragnarok
  * Crystal Isles
  * Lost Island
  * Fjordur
  






<h1 id="aGameSetting">ゲーム設定</h1>  
わたしが調整したゲーム設定を示します。  
  
  [目次へ戻る](#aMokuji)  
  

<h2>一般</h2>  

```text
難易度=1.0（0.2） 
経験値倍率=1.0（1.0） 
テイム速度=8.0（1.0） 

採取量=2.0（1.0） 
マップ内の恐竜数=2.0（1.0） 
PvEモード=True（False） 
マップにプレイヤーの位置を表示=True 
最高難易度に設定=True（False） 
シングルプレイの設定を使用する=False（True） 
複数のプラットフォームフロアを許可=True（False） 
リスペックを無制限化=True（False） 
飛行スピードレベリングを許可=True 
```
  

<h2>詳細設定</h2>  

```text
PVE飛行運搬を許可=True（False） 
PVE建造物の所有権失効時間の無効化=True（False） 
PVE恐竜の所有権失効時間の無効化=True（False） 
プラットフォームへの建築禁止を無効化=True（False） 
産卵可能になるまでの期間=0.005（1.0）　0.03 
交配可能になるまでの期間=0.005（1.0）　0.03 
卵の孵化速度=100.0（1.0）　24.0 
赤ちゃんの成熟速度= 100.0（1.0）　24.0 
赤ちゃんの食糧消費速度=0.01（1.0） 
採取可能物のリスポーン速度=0.25（1.0） 
赤ちゃんの世話間隔=0.015（1.0）　0.08 
赤ちゃんの世話の猶予期間=15.0（1.0）　15.0 
赤ちゃんの世話の刷り込み時のバフ効果減少速度=1.0（1.0） 

資源のリスポーンに必要なプレイヤーからの距離=1.0（1.0） 
資源のリスポーンに必要な建物からの距離=0.1（1.0） 
作物の成長速度=0.8（1.0） 
テイム済み恐竜データ（※レベルアップ時のステ上昇率） 
　体力=0.45（0.2） 
　攻撃=0.415（0.17） 

テイム時恐竜ボーナス（※テイム済み恐竜に割り振られたポイント毎のステータス） 
　体力=0.55（0.14） 
　攻撃=0.55（0.14） 

テイム済恐竜データ傾向（※テイムされたときに得られるステータス） 
　体力=1.0（0.44） 
　攻撃=1.0（0.44） 

搭乗者のいない恐竜への防護柵のダメージ有効化=False（False） 
ダメージ値のテキスト表示=True（False） 
レイド恐竜の餌やりを有効化=True（False） 
カスタムレシピの効果=2.0（1.0） 
制作速度によるカスタムレシピの性能=2.0（1.0） 
物質クレート戦利品品質=10.0（5.0） 
釣りあげた戦利品の品質=10.0（5.0） 
土台の建造物設置上限=10.0（1.0） 
```
  





<h1 id="aMod">導入mod</h1>  
  
  [目次へ戻る](#aMokuji)  
  

* Structures Plus（Open Source）
* Awesome SpyGlass!
* DinoTracker
* Dino Mindwipe
* Dino Colourizer
* Kibble Station
* Upgrade Station v1.81
* Beacon Enhancer
* Tribute and Element Transfers
* Polymer Converter
* Ragnarok Plus　※Map:Ragnarokのみ
* Better Weypoint
  





<h1 id="aCommands">コマンド一覧</h1>  
  
  [目次へ戻る](#aMokuji)  
  

```text

SaveWorld
　現段階でデータセーブをマニュアル実施する。
　※通常30分ごとにオートセーブされている。

DestroyWildDinos
　マップ上のすべての野生の恐竜を破壊する。

Fly
　無敵状態になって、地形を抜けたり、空中を移動できる。スタックしたときなどに使える。

Walk
　Flyから解除、地上を歩ける。


stat fps
　画面右上にFPSを表示する。再実行すると表示を消す。

t.maxfps 60
　FPS制限をかける。数値はFPS値。
　ARKは無設定だとFPSを無制限に上げてくるので、制限をかけることをおすすめする。」

SetTimeOfDay 10:00:00
SetTimeOfDay 20:00:00
　時間の変更

※永久にFPS制限をかけるにはconfigを編集する。
\\ARK\ShooterGame\Saved\Config\WindowsNoEditor
Engine.ini
に以下を記載
[/script/engine.renderersettings]
t.maxfps=60


＜Steamの起動オプション設定＞
-USEALLAVAILABLECORES -d3d10
※ それでも重たい場合
-USEALLAVAILABLECORES -d3d10 -sm4

イースターイベント起動
-USEALLAVAILABLECORES -d3d10 -sm4 -ActiveEvent=Easter

夏イベント起動
-USEALLAVAILABLECORES -d3d10 -sm4 -ActiveEvent=Summer

ハロウィン起動
-USEALLAVAILABLECORES -d3d10 -sm4 -ActiveEvent=FearEvolved

```
  





<h1 id="aSeed">ARK豆知識</h1>  
ARKの豆知識を示します。  
  
  [目次へ戻る](#aMokuji)  
  

<h2>DinoTrackerのUIが開かなくなる</h2>
シングル→マルチに切り替えると起こる問題です。  
あるいは後追加の他のmodとバインドが競合しても起こるかもしれません。  
またこのmodにより装備を変更するとARKがクラッシュする場合があります。  
  
**一度modを入れ直すと解消できるようです。**  
  
手順は以下です。  

* 1.ARKからログオフする  

* 2.modのサブスクライブを解除する  

* 3.DinoTrackerのファイルを削除する  

```text
\Steam\steamapps\common\ARK\ShooterGame\Saved\SaveGames\ModDinoTracker.sav
```

* 4.マルチでログインする  

* 5.ログオフする  

* 6.modをサブスクライブする  

* 7.ログインする（マルチ）  

* 8.DinoTrackerを作り、装備する。そして Shift+C を押す。  

* 9.キーをバインドしなおしてセーブする  
  





<h1 id="aMaterial">参考資料 / Reference material</h1>  
**※敬称略**  

* [野生恐竜生成コマンド](https://knut.hatenablog.jp/entry/2017/09/04/215617)

* [アイテムIDs](https://ark.gamepedia.com/Item_IDs/ja)

* [イースターエッグ一覧](https://ark.gamepedia.com/ARK:_Winter_Wonderland_4/ja)
  





<h1 id="aARK2info">ARK2の情報</h1>  
ARK2の情報はこちらです？  
  
  [目次へ戻る](#aMokuji)  
  









***
[[トップへ戻る]](/readme.md)　/
[[readme:ARK]](/game_memo/ARK/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= [https://github.com/korei-xlix/](https://github.com/korei-xlix/)  
::Web= [https://website.koreis-labo.com/](https://website.koreis-labo.com/)  
::Twitter= [https://twitter.com/korei_xlix](https://twitter.com/korei_xlix)  
