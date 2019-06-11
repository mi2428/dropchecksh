# dropchecksh
## 使い方
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
```
% ./dropchecksh --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28
% ./dropchecksh --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28 --skip-www --interface vlan1
```

タグインターフェイスの警告とアドレス自動設定をスキップする．
```
% ./dropchecksh --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28 --skip-precheck
```

### ビラを袋詰する
ドロップケーブルに貼り付ける出展社向けの取扱説明書の袋詰作業．  
Podごとに束を作るので，紙に書いてあるコマ番号からPodを割り出せると便利．
```
fukurozume $1
# main $@
```
