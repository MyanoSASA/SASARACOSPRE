# **SASARACOS**
SASARACOS(SASA RAilway COntrol System)はStormworks鉄道のCamodo~Terminal Spycakes間の移動閉塞運転の実現を目指して開発されたシステムです。</br>
今までのシステムが区間ごとに車両を整理していたのに対し、このシステムでは各車と通信を行って車両ごとに管理を行います。
## 具体的には...?
![Stormworks 2022-02-20 22-52-56_Moment](https://user-images.githubusercontent.com/99597447/156719001-9582915d-edb4-4450-8bab-8b898c511da2.jpg)
こういうかんじにつめれる（協力:yasuさん）
## すごいとこ
* ATACSなみにつめつめ運転できる。
* 司令室のマイコンで一通りの計算をやってるので車上装置がとってもかるい上に前方互換性がある。
* アドオン自体が軽い(62fps普通に出る)
## だめなとこ(言い訳付き)
* 最大4編成までしか同時管理できない。(だってそもそも4編成以上も同時走行とかあんまないでしょ......)
* たまに同期ずれする(これに関しては私は悪くない)
## 動かすのに必要なもの
* 鉄道車両
* 車上マイコン(https://steamcommunity.com/sharedfiles/filedetails/?id=2774126318)
* サーバーアドオン(https://steamcommunity.com/sharedfiles/filedetails/?id=2780627989)
## セットアップ
### 車上マイコン
* マイコンキットの各コンポーネントをいい感じに配置してください。
* 1運転台につき一つづつ設置してください。
* 電力は必ず通してください。
* keyインプットには運転台のキーあるいはR-BUSのI have control 信号を接続してください。
* キーパッド2つは運転席から触れる位置に設置してください。
#### 車上マイコンの設定
![SASARACOSUSAGE](https://user-images.githubusercontent.com/99597447/156719818-b43ddad8-eddb-4bdb-a3c6-f9ddad5a957e.png)
* TrainIDには司令側キーパッドと同じ値を入力してください
* DestinationIDはCamodoに向かう側の運転台には2を、Terminal Spycakesに向かう側の運転台には1を入力してください。
### 司令室
* 制御盤左側にあるキーパッドの上段「1」「2」「3」「4」のいずれかに車上マイコンと同じIDを入力してください。
## 実際に動かしてみよう
### 車上用マイコンの表示
![モニタ表示](https://user-images.githubusercontent.com/99597447/156725246-7362468d-dfcd-4cae-8bc7-26f25eb96552.png)
### 司令室の各部の説明
![制御盤](https://user-images.githubusercontent.com/99597447/156725806-5d1bd395-a632-488a-a1c1-bc250f761252.png)
![列車アイコンの説明](https://user-images.githubusercontent.com/99597447/156726830-ee4126af-7274-4702-a33a-3aa2dcf9af13.png)
これであとは到着次第運転席を切り替える操作をしていけば勝手に移動閉塞の制御が行われます。
## 運転順序の変更方法
駅とかで自動的に先発列車が決定されたけど変更したい！！ってときは自動的に先発指定を受けた列車側の行き先ID(DestinationID)を3に設定して先発させたい列車を発車させてください。
## プラグイン(保安装置)開発者向け無線アウトプット内容
### 車上装置の受信用アンテナのコンポジット受信内容:
#### Bool
1.接続ステータス
#### Number
1.前を走行中の列車のSID(0の場合は前に列車なし)</br>
2.前を走行中の列車までの距離もしくは終端駅の進入可能位置までの距離</br>
このあともあったりするけどほぼ使用されてないです
## 運用上の注意
* 列車IDは１０００未満に設定してください。
* 行き先IDは正しく設定してください。事故ります。
## お問い合わせ
ついったかDiscordのDMに連絡ください
## 更新ログ(2022/05/25更新)
* バージョン2.5.7(2022/04/15リリース):三角含めたSpycakes〜Camodo間の全分岐点の制御が可能に。
* バージョン3.0(2022/05/22リリース):司令室のデザインを一新し、駅分岐点の制御を自動化(開通進路を選択すると自動的に進路を構成してくれるように)
