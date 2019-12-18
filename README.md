# SENKIN_PostScript_calculateROP
SENKINの結果から生成速度(Rate of Production: ROP)を計算するポスト処理スクリプト
## ファイル構成
### 入力ファイル
1. 計算結果ファイル (`input/datasheet`，t(sec), P, T, Xのスペース区切りテキスト)
2. 化学反応に関するバイナリファイル (`input/cklink`，CKinterpで作成されるもの，SENKINの計算で使用したものを引っ張ってくる)
### 計算コード
1. `cklib.f` (CHEMKINの便利なサブルーチン集，`cklink`を読み込み)
2. `calc_rop.f` (メインのPROGRAM，`datasheet`読み込み，エンタルピーを計算)
### 出力ファイル
1. `rop` (計算結果，モルベースと質量ベース)
2. `terminalout` (標準出力，特に使用していない)
## 使用方法
```
$ make
$ ./calc_rope
```
