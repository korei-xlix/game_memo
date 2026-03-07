# ゲームメモ：minecraft：modの取り扱い・サーバの立て方 ***

**★当リポジトリの利用にあたっては、必ず本readmeを確認してください★**  
  

このドキュメントはMinecrafttの サーバの立て方、modの取り扱いをまとめたメモです。  
説明の前提として、この資料は、mineceaftをマルチサーバかつ、Multiverse-Coreを使ったマルチワールドで遊ぶ方法で記載してます。Multiverse-Coreを導入しても、普通にマルチサーバかつシングルワールドで遊ぶことも可能です。たぶん。  
  
管理者スキルの前提として、サーバやmodは、パソコンのこと、minecraft管理ができる方向けです。特にパソコン初心者の方はminecraftや、最悪パソコンのシステムを壊すリスクがあるため、おすすめしません。  
  
また、**本メモにより不具合やシステムを損傷するなどする可能性がありますが、**  
**すべて自己責任** でお願いします。  
  





## 目次 / Table of Contents

* [readme.md](../../readme.md)
  * [利用にあたって (Important notices for use)](../../readme.md#利用にあたっての注意事項--important-notices-for-use)

* [Minecraft Fablic+VulkanModの導入](#minecraft-fablicvulkanmodの導入)
  * [大前提](#大前提)
  * [Fablic+VulkanModの導入手順](#fablicvulkanmodの導入手順)

* [サーバの建て方(PaperMC)](#サーバの建て方minecraft-papermcの導入)
  * [PaperMC・Multiverse-Coreとは](#papermcmultiverse-coreとは)
  * [サーバを建てる](#サーバを建てる)
  * [サーバの調整](#サーバの調整serverproperty)
  * [プラグインの導入](#プラグインの導入)

* [サーバコマンド](../manual/command.md#コマンド)

* [過去の資料](#過去の資料)
  * [Minecraft Forge+Optifineの導入](#minecraft-forgeoptifineの導入非推奨)
  





## Minecraft Fablic+VulkanModの導入

[目次へ戻る](#目次--table-of-contents)  
  

参考：[サーバの立て方(X Server Game's)](https://games.xserver.ne.jp/minecraft-media/minecraft-forge/)  
  

### 大前提

大前提として、mineceaftをマルチサーバかつ、Multiverse-Coreを使ったマルチワールドで遊ぶには、Java版のminecraftが必要です。  
bedrock版や、realmsでは遊べません。  
  



### Fablicとは

Fablicは多くのmodを動かすためのベースとなるminecraftクライアント用のmodです。  
また、今回はグラフィックAPIをOpenGLからVulkanに入れ替える、VulkanModも導入します。これにより、Minecraftの描画処理が向上するようですが、Optifineが使えなくなるため（OptifineはOpenGLを使用しているため）シェーダーが使えません。というより、記事を書いている時はVulkanModで動くシェーダーはなかったです。  
しかし、Minecraft自体がOpenGLをやめる動きがあるので、早めにVulkanに乗り換えしておいたほうがいいと考えます。  
  



### Fablic+VulkanModの導入手順

FablicとVulkanModを導入する方法は以下の通りです。  
  

1. JDK(Java SE Development Kit)を導入する  
  Forge Installerを実行するために、JDKを導入します。  
  **JDKのインストーラはOracleからダウンロードできます。**  
  　　[[Java SE Development Kit Installer(Oracle)](https://www.oracle.com/jp/java/technologies/downloads/)]  

1. JDKをインストールする  
  **JSKインストーラを実行し、インストールを実行します。**  
  インストールの完了後、閉じるをクリックすればOKです。  

1. minecraftのバージョンを確認する  
  Fablicを動かすminecraftのバージョンを確認します。  
  minecraftと導入するFablicのバージョンはそろえる必要があります。  
  **一度minecraftを起動し、バージョンを確認します。**  

1. Fablicを入手する  
  Fablicのインストーラを入手します。  
  **Fablicインストーラは以下のサイトから入手できます。（URLは当方で確認済）**  
  　　[[Fablic Installer](https://fabricmc.net/use/installer/)]  

1. Fablicをインストールする  
  インストーラから、動かすMinecraftのバージョンを指定します。  
  **Fablicインストーラを実行し、インストールを実行します。**  

1. minecraftでFablic用の起動構成を作成する  

    1. minecraftランチャーを起動し、「起動構成」-「新規作成」を選びます。  

    1. 起動構成を設定します。  
      名前：起動構成の名称を付けます。  
      バージョン：導入したFablicと同じバージョンを選択します。  
      ゲームディレクトリ：Fablicを動かすminecraftのゲームデータの保存先を指定します。  
      分かりやすく、最新Release配下に適当なフォルダを作成して、そこを指定します。  
      　　C:\Users\[ユーザ名]\AppData\Roaming\.minecraft\Fablic_1.21.11　とか  

    1. 「保存」を押して、起動構成を保存します。  

1. VulkanModのバージョンを確認する  
  VulkanModのインストーラを入手します。  
  動かすminecraftと同じバージョンのインストーラを入手します。  
  **VulkanModインストーラは以下のサイトから入手できます。（URLは当方で確認済）**  
  　　[[VulkanMod Installer](https://modrinth.com/mod/vulkanmod)]  

1. ダウンロードしたVulkanModをそのままクライアントのmodsフォルダに入れます。  
      　　C:\Users\[ユーザ名]\AppData\Roaming\.minecraft\fablic_1.21.11\mods 以下  

1. minecraftランチャーから、作成した起動構成を指定して、ゲームを始めます。  
  タイトル左下のバージョン表示で、導入したFablicのバージョンが表示されていれば、Fablicの導入完了です。  
  また、「設定」→「ビデオ設定」画面で、VulkanModの設定画面が表示されていれば、VulkanModの導入も完了です！  
  





## サーバの建て方・Minecraft PaperMCの導入

[目次へ戻る](#目次--table-of-contents)  
  

参考：[マイクラのPaperMCとは？(Lolipouゲームブログ)](https://gamers.lolipop.jp/blog/minecraft/paper-guide/)  
  



### PaperMC・Multiverse-Coreとは

今のところ、minecraftをマルチサーバかつマルチワールドで遊ぶには、Multiverse-Coreというプラグイン頼みのようですが、これはサーバ用プラグインなので、使うにあたってはサーバを建てるしかありません。  
Multiverse-Coreを使うのに一番安定してそうな、PaperMCでサーバを建てて、そのあとMultiverse-Coreを導入します。  
これらを導入することで、通常１つのサーバでは、「オーバーワールド」「ネザーワールド」「エンドワールド」の３つのワールドでしか遊べないところを、「オーバーワールド２」「オーバーワールド３」など複数のワールドに増やして遊ぶことができます。  
サーバが１個しかいらないので、大幅なコストダウンになると思います。（パフォーマンスを除いては..）  
  



### サーバを建てる

サーバを建てる方法は以下の通りです。  
  

1. JDK(Java SE Development Kit)を導入する  
  サーバに、JDKを導入します。  
  **ローカルサーバで既にForgeを導入していればスキップできます。**  
  **JDKのインストーラはOracleからダウンロードできます。**  
  　　[[Java SE Development Kit Installer(Oracle)](https://www.oracle.com/jp/java/technologies/downloads/)]  

1. JDKをインストールする  
  **ローカルサーバで既にForgeを導入していればスキップできます。**  
  **JSKインストーラを実行し、インストールを実行します。**  
  インストールの完了後、閉じるをクリックすればOKです。  

1. minecraftのバージョンを確認する  
  Forgeを動かすminecraftのバージョンを確認します。  
  minecraftと導入するForgeのバージョンはそろえる必要があります。  
  **一度minecraftを起動し、バージョンを確認します。**  

1. PaperMCのバージョンを確認する  
  PaperMCを入手します。  
  動かすminecraftと同じバージョンのPaperMCを入手します。  
  **PaperMCは以下のサイトから入手できます。（URLは当方で確認済）**  
  　　[[PaperMC](https://papermc.io/downloads/paper)]  

1. PaperMCの起動準備をする  

    1. サーバ上に適当なフォルダを作成し、そこにダウンロードしたPaperMCを設置します。  

    1. PaperMCを設置したフォルダに、メモ帳などでバッチファイルを作成します。  
       ファイル名は、windowsの場合はrun.bat、linuxの場合はrun.shなど、シェルが起動する名称にします。  

    1. バッチファイルを開き、以下を記載します。  
       **@echo off**  
       **java -Xmx3G -Xms3G -jar [PaperMC ファイル名]**  
       **pause**  

    1. 一度バッチファイルを実行し、  
       「続行するには何かキーを押してください」が出るまで待って、  
       プロンプトを閉じます。  

    1. PaperMCを設置したフォルダにある「eula.txt」をメモ帳で開き、  
       「eula=false」を「eula=true」に書き換え、保存します。  

1. サーバを起動する  
   バッチファイルを実行し、minecraft serverのコンソールが起動すればOKです。  
   サーバを停止するには、コンソールで「stop」コマンドを入力すると安全に停止できます。  
  

<<<<<<< HEAD
=======
1. 自分をオペレータに追加、ホワイトリストに追加しておく  
   コンソールから、以下を実行します。これをやっておかないと、サーバへの接続や編集ができません。  
   　　op [自分のマイクラname]
   　　whitelist add [自分のマイクラname]
  

>>>>>>> origin/minecraft_edit


### サーバの調整：server.property

PaperMCのcommands.yml、server.propertiesを編集します。  
  

```text
【commands.yml】
＜コマンドブロック有効＞
command-block-overrides: []
　↓↓↓
command-block-overrides:
  - "*"


【server.properties】
＜最大接続数＞
max-players=20
　↓↓↓
max-players=＜任意の人数＞

＜サーバー紹介文＞
motd=A Minecraft Server
　↓↓↓
motd=A Minecraft Server \u00A79[version 1.21.10] By PaperMC

＜ホワイトリスト制＞
white-list=false
　↓↓↓
white-list=true

以後、ゲーム内で以下のコマンドでホワイトリストにユーザを追加できます。
/whitelist add [username]

<<<<<<< HEAD
=======
サーバへの接続
　　IPアドレス：[サーバのIPアドレス]:25565
　　　　※ローカルサーバの場合、パソコンのIPアドレス（localhostはダメっぽい？）

>>>>>>> origin/minecraft_edit
```
  



### プラグインの導入

Multiverse-Coreを含めたプラグインを導入するには、  
PaperMCを設置したフォルダ配下の「plugins」以下に、プラグインファイルを配置するだけです。  
ベースとなるプラグインとして以下を導入します。  
  


<<<<<<< HEAD
#### **Multiverse-Core**
=======
#### **Multiverse-Core（※必須）**
>>>>>>> origin/minecraft_edit

ワールドを生成したり、調整したりするサーバプラグインです。  
  
　　[[ダウンロード](https://dev.bukkit.org/projects/multiverse-core/files)]  
  
　　[[コマンド](../manual/command.md#コマンドmultiverse-core)]  
  


<<<<<<< HEAD
#### **Multiverse-Portalsm**
=======
#### **Multiverse-Portalsm（※必須）**
>>>>>>> origin/minecraft_edit

ワールドのポータルを設置するサーバプラグインです。  
  
　　[[ダウンロード](https://dev.bukkit.org/projects/multiverse-portals/files)]  
  
　　[[コマンド](../manual/command.md#コマンドmultiverse-portalsm)]  
  


<<<<<<< HEAD
#### **WorldEdit**
=======
#### **WorldEdit（※必須）**
>>>>>>> origin/minecraft_edit

マイクラの建築作業を補助するサーバプラグインです。  
  
　　[[参考記事](https://games.xserver.ne.jp/minecraft-media/worldedit/)]  
  
　　[[ダウンロード](https://dev.bukkit.org/projects/worldedit)]  
  


<<<<<<< HEAD
#### **WorldGuard**
=======
#### **WorldGuard（※必須）**
>>>>>>> origin/minecraft_edit

サーバー上のワールドを保護してくれるサーバプラグインです。  
  
　　[[参考記事](https://games.xserver.ne.jp/minecraft-media/worldguard/)]  
  
　　[[ダウンロード](https://dev.bukkit.org/projects/worldguard)]  
  


<<<<<<< HEAD
#### **LuckPerms**

プレイヤーの権限（コマンド利用や機能制限）を管理するサーバプラグインです。  
WEBブラウザを使って簡単に権限の管理や設定ができます。  
  
　　[[参考記事](https://yaaaa.net/luckperms/)]  
  
　　[[ダウンロード](https://www.spigotmc.org/resources/luckperms.28140/)]  
  
　　[[コマンド](../manual/command.md#コマンドluckperms)]  
  


```text
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

```
  


#### **GriefPrevention**
=======
#### **GriefPrevention（※必須）**
>>>>>>> origin/minecraft_edit

TNTやクリーパーでの建物爆破制限を設定したり、保護された土地を破壊から守ったりするサーバプラグインです。  
WorldGuardよりできることは限定されますが、一般ユーザが単独で自由に設定できます。  
  
　　[[参考記事](https://seesaawiki.jp/kotaserver/d/Grief%20Prevention)]  
  
　　[[ダウンロード](https://dev.bukkit.org/projects/grief-prevention)]  
  

```text
config.ymlの確認

SeaLevelOverrides
  全て-1にする（※新ワールド生成時も確認しておくこと）

# BlockSurfaceCreeperExplosions: true
# BlockSurfaceOtherExplosions: true
BlockSurfaceCreeperExplosions: false
BlockSurfaceOtherExplosions: false
  TNTやクリーパーでの建物爆破制限を解除する
  ただし、土地保護されたものは破壊できない

# PistonMovement: CLAIMS_ONLY
PistonMovement: EVERYWHERE
  ピストンの動作を許可する

```
  


<<<<<<< HEAD
#### **LWC Extended**
=======

#### **LWC Extended（※必須）**
>>>>>>> origin/minecraft_edit

チェストやかまど、ドアなど自分のものを守るためのサーバプラグインです。  
一般ユーザが単独で自由に設定できます。  
  
　　[[参考記事](https://yaaaa.net/lwc/)]  
  
　　[[ダウンロード](https://www.spigotmc.org/resources/lwc-extended.69551/)]  
  

```text
core.ymlの確認

autoRegister: false
  blocksのautoRegisterをfalseに設定することで、保護しなくなる。
  保護をしない：false
  保護する：private
  過度な保護をしないのであれば、全てfalseでいい。

```
  



<<<<<<< HEAD
=======
#### **LuckPerms**

プレイヤーの権限（コマンド利用や機能制限）を管理する便利なサーバプラグインです。  
WEBブラウザを使って簡単に権限の管理や設定ができます。  
条件が進むと権限を自動的に昇格するなどもできるようです。  
  
　　[[参考記事](https://yaaaa.net/luckperms/)]  
  
　　[[ダウンロード](https://www.spigotmc.org/resources/luckperms.28140/)]  
  
　　[[コマンド](../manual/command.md#コマンドluckperms)]  
  



>>>>>>> origin/minecraft_edit


## 過去の資料

### Minecraft Forge+Optifineの導入（非推奨）

[目次へ戻る](#目次--table-of-contents)  
  

参考：[サーバの立て方(X Server Game's)](https://games.xserver.ne.jp/minecraft-media/minecraft-forge/)  
  

### Forgeとは

ForgeはFablic同様、多くのmodを動かすためのベースとなるminecraftクライアント用のmodです。  
また副効果として、クライアントの動作が軽くなるようです。なので、とくにmodを使わなくても導入しておいたほうがいいかもしれません。  
このドキュメントでは、クライアントにForgeを入れた状態で説明していきます。  
また、Forgeと合わせて、シェーダを使うmod「Optifine」も導入します。  
  



### Forge+Optifinrの導入手順

ForgeとOptifineを導入する方法は以下の通りです。  
  

1. JDK(Java SE Development Kit)を導入する  
  Forge Installerを実行するために、JDKを導入します。  
  **JDKのインストーラはOracleからダウンロードできます。**  
  　　[[Java SE Development Kit Installer(Oracle)](https://www.oracle.com/jp/java/technologies/downloads/)]  

1. JDKをインストールする  
  **JSKインストーラを実行し、インストールを実行します。**  
  インストールの完了後、閉じるをクリックすればOKです。  

1. minecraftのバージョンを確認する  
  Forgeを動かすminecraftのバージョンを確認します。  
  minecraftと導入するForgeのバージョンはそろえる必要があります。  
  **一度minecraftを起動し、バージョンを確認します。**  

1. Forgeのバージョンを確認する  
  Forgeのインストーラを入手します。  
  動かすminecraftと同じバージョンのインストーラを入手します。  
  Latest（最新版）」と「Recommended（安定版）」がありますが、
  最新版は不具合のリスクがあるので、  
  「安定版」を選んだほうがよいです。  
  **Forgeインストーラは以下のサイトから入手できます。（URLは当方で確認済）**  
  　　[[Forge Installer](https://files.minecraftforge.net/net/minecraftforge/forge/)]  

1. Forgeをインストールする  
  **Forgeインストーラを実行し、インストールを実行します。**  
  クライアント（ローカルで遊ぶ場合）は、「Client」を選択します。  
  インストールが完了したら、OKをクリックしてください。  

1. minecraftでForge用の起動構成を作成する  

    1. minecraftランチャーを起動し、「起動構成」-「新規作成」を選びます。  

    1. 起動構成を設定します。  
      名前：起動構成の名称を付けます。  
      バージョン：導入したForgeと同じバージョンを選択します。  
        1.21.11の場合　release 1.21.11-forge61.0.6  
      ゲームディレクトリ：Forgeを動かすminecraftのゲームデータの保存先を指定します。  
      分かりやすく、最新Release配下に適当なフォルダを作成して、そこを指定します。  
      　　C:\Users\[ユーザ名]\AppData\Roaming\.minecraft\forge_1.21.11　とか  

    1. 「保存」を押して、起動構成を保存します。  

1. Optifineのバージョンを確認する  
  Optifineのインストーラを入手します。  
  動かすminecraftと同じバージョンのインストーラを入手します。  
  minecraftのバージョンアップ直後は、最新のOptifineが出てくるのに時間がかかるので、
  対応バージョンがなければ適用は待ちましょう。  
  **Optifineインストーラは以下のサイトから入手できます。（URLは当方で確認済）**  
  　　[[Optifine Installer](https://optifine.net/downloads)]  

1. ダウンロードしたOptifineをそのままクライアントのmodsフォルダに入れます。  
      　　C:\Users\[ユーザ名]\AppData\Roaming\.minecraft\forge_1.21.11\mods 以下  

1. minecraftランチャーから、作成した起動構成を指定して、ゲームを始めます。  
  タイトル左下のバージョン表示で、導入したForgeのバージョンが表示されていれば、Forgeの導入完了です。  
  また、「設定」→「ビデオ設定」画面で、左下にOptifineのバージョンが表示されていれば、Optifineの導入も完了です！  



### Optifineシェーダの適用

任意のシェーダを適用するには、シェーダパックをシェーダーフォルダに入れます。  
      　　C:\Users\[ユーザ名]\AppData\Roaming\.minecraft\forge_1.21.11\shaderpacks 以下  
  
シェーダパックを適用するには、「設定」→「ビデオ設定」→「シェーダの詳細」から、
任意のシェーダパックを選択します。  
クライアントは自動的に再起動されます。  
  

#### **おすすめシェーダパック**

* **初心者・万能型：Complementary Reimagined**  
  　　[File URL](https://www.curseforge.com/minecraft/shaders/complementary-reimagined)  

* **幻想的：BSL Shaders**  
  　　[File URL](https://www.curseforge.com/minecraft/shaders/bsl-shaders)  

* **低スペック向け：MakeUp - Ultra Fast**  
  　　[File URL](https://www.curseforge.com/minecraft/shaders/makeup-ultra-fast-shader)  
  





***
***
[[トップへ戻る]](../../readme.md)　/
[[minecraft]](/readme.md)  
  
::Admin= Korei (@korei-xlix)  
::github= [https://github.com/korei-xlix/](https://github.com/korei-xlix/)  
::Web= [https://website.koreis-labo.com/](https://website.koreis-labo.com/)  
::X= [https://x.com/korei_xlix](https://x.com/korei_xlix)  
***
