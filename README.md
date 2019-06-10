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
% ./dropcheck --fullcheck --csv ~/Downloads/dropcheck.csv --koma 4a28
```
