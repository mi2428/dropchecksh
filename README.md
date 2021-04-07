# dropchecksh

## 使い方
macOS Big Sur 向けに改修済み．

### シンプルに

```
% ./dropchesksh --fullcheck
```

### 特定テストだけ実施・特定テストだけスキップする

```
% ./dropchecksh --ping-gw --ping-internet
% ./dropchecksh --fullcheck --skip-traceroute --skip-www
```

### コマ番号を指定してアドレスをチェックする

事前にTTDBからドロップチェックCSVをダウンロードしておく．
タグドロップの場合はインターフェイス名・ネットワークサービス名を変更する必要あり．
静的アドレス設定にも対応．

```
% ./dropchecksh --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28
% ./dropchecksh --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28 --skip-www --interface en9 --network-service uni
% ./dropchecksh --fullcheck --interface en9 --network-service uni --cidr 10.1.130.200/24 10.1.130.1
```

タグインターフェイスの警告とアドレス自動設定をスキップする．

```
% ./dropchecksh --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28 --skip-precheck
```

### ビラを袋詰する

ドロップケーブルに貼り付ける出展社向けの取扱説明書の袋詰作業．  
Podごとに束を作るので，紙に書いてあるコマ番号からPodを割り出せると便利．

```
% ./dropchecksh --csv ~/Downloads/dropcheck.csv --show-drop-info --koma 4a28
```
