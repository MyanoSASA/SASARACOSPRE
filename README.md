# SASARACOS_PRE
SASARACOS(SASA RAilway COntrol System)はStormworks鉄道のCamodo~Terminal Spycakes間の移動閉塞運転の実現を目指して開発されたシステムです。</br>
今までのシステムが区間ごとに車両を整理していたのに対し、このシステムでは各車と通信を行って車両ごとに管理を行います。
# すごいとこ
* ATACSなみにつめつめ運転できる。
* 司令室のマイコンで一通りの計算をやってるので車上装置がとってもかるい上に前方互換性がある。
* アドオン自体が軽い(62fps普通に出る)
# だめなとこ(言い訳付き)
* 最大4編成までしか同時管理できない。(だってそもそも4編成以上も同時走行とかあんまないでしょ......)
* たまに同期ずれする(これに関しては私は悪くない)
* 運用に癖がある(これに関しても駅管理だからユルシテ....)