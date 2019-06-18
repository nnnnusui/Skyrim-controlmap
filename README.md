# 概要
ゲームパッドで操作して、キーボードはホットキー等のサブ入力限定にしたい！
と思って作成した、Skyrimの操作設定ファイルです。

## 内容

+ 本体  
└ Data/Interface/Controls/PC/controlmap.txt

+ Interface Hard Coded Key Tweaks の設定ファイル  
└ hardcode_data.txt


## 導入・使用方法
Skyrim直下の[Date]フォルダと、このzip内の[Date]フォルダを統合してください。

### ゲーム内でキーボードに”MODホットキー設定”を入れたい場合、

1. 設定→ゲームプレイ→Xbox360コントローラ をOFFに (コントローラが一時的に使用不能になります)
2. MCM等を開き、設定したいキー設定をする
3. 設定→ゲームプレイ→Xbox360コントローラ をONに戻す

### ！キーボードでできる操作
|||
|---|---|
|矢印キー|メニュー選択|
|Enter|決定|
|Delete|キャンセル 戻る|
|Esc|ジャーナル(メニュー)を開く|



## 対応MOD
### @同梱
- [Use both xbox 360 controller AND Keyboard SIMULTANEOUSLY]()
- [Xbox360 Controller KeyRemap (for Japanese keyboard)]()
### @共存可能
- [SkyUI]() (- FavoriteHotKey)
- その他MCMからキーボードにキー設定できるMOD全て(多分)

---


## 設定変更
### 使用ツール
- [Interface Hard Coded Key Tweaks]() (以下IHCKT
- [Skyrim Pad Config]() (以下SPC

**※注意**  
IHCKTを使用すると、SPCの設定はリセットされ、一時的にゲームパッドが使えなくなります。  
IHCKT → SPC の順番に利用してください。

### 手順
1. このファイルのバックアップを取っておいてください。”controlmap.txt”さえなくさなければやり直しが効きます。作業中も、変更を加えたら逐一バックアップを取り、どの段階かわかるようにリネームしておくと後悔が減ります。
2. IHCKT・SPC をDL、それぞれ解凍します(同じフォルダでも構いません)。  
(このzipの[hardcode_data.txt]も入れるとキーボードの設定を流用できます)

**！キーボードの操作設定**

3. このファイルをSkyrimに導入(上書き)します。
4. 導入した後、IHCKTを起動 キーボードでやりたい操作を設定し、「Save&Write Changeｓ」をおして設定を上書きします。

**！コントローラの操作設定**

5. SPCを開き、変更を加えたい”controlmap.txt”を指定します。お好みのキー設定に変えてください。

**最後に、**  

6. 変更を加えた”controlmap.txt”を、[Skyrim\Data\Interface\Controls\PC]に導入します。

これで変更は完了です。が、

**もしもキーボードが反応しなかった場合**  

7. controlmap.txtを開いて反応しなかったキーを探します。  
[Cancel	0xd3	0xff	0x2000	0	0	0	0x8]  
このような文があると思います。この8カラム目の文、この場合だと[0x8]を 削除 してみてください。


### controlmap.txt について

||キー名|Keybord|Mouse|xboxコン|不明|不明|不明|不明(グループ分け?)|
|---|---|---|---|---|---|---|---|---|
|例:|Cancel|0xd3|0xff|0x2000|0|0|0|0x8|


## このファイルの作成過程

- [Use both xbox 360 controller AND Keyboard SIMULTANEOUSLY]()

をベースに

- [Interface Hard Coded Key Tweaks]() でキーボードのキー登録を粗方削除  
  + メニュー画面関連のみキーボードでも操作できるように残す

- [Skyrim Pad Config]() で [Xbox360 Controller KeyRemap (for Japanese keyboard)]()の設定を再現  
  + お気に入りメニュー操作の[SkyUI]()対応化
  + LB+操作の追加

したものです。

[Use both xbox 360 controller AND Keyboard SIMULTANEOUSLY]: https://skyrim.2game.info/detail.php?id=30913
[Interface Hard Coded Key Tweaks]: https://skyrim.2game.info/detail.php?id=88
[Skyrim Pad Config]: https://skyrim.2game.info/detail.php?id=655
[Xbox360 Controller KeyRemap (for Japanese keyboard)]: https://skyrim.2game.info/detail.php?id=1177
[SkyUI]: https://skyrim.2game.info/detail.php?id=3863
