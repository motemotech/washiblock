# Washiblock - ブロックチェーンシミュレーター

このプロジェクトは、ブロックチェーンネットワークのシミュレーションを行うC++プログラムです。複数のノード間でのブロック生成と伝播をシミュレートします。

## 必要な環境

- C++コンパイラ（g++推奨）
- C++11以上のサポート

## コンパイルと実行手順

### 1. コンパイル

```bash
g++ -o washiblock washiblock.cpp -std=c++11
```

### 2. 実行

```bash
./washiblock
```

## プログラムの概要

このシミュレーターは以下の機能を提供します：

- **ノード数**: 10ノード（デフォルト）
- **ハッシュレート**: ノード0が9、その他のノードが1
- **ブロック伝播遅延**: 6000ミリ秒（デフォルト）
- **ブロック生成時間**: 600000ミリ秒（平均）
- **終了ラウンド**: 100000ブロック

## 出力内容

実行すると以下のような出力が表示されます：

- `blockgeneration`: ブロック生成イベント
- `block propagation`: ブロック伝播イベント
- 各イベントには時刻、ノード番号、ブロック高さが表示されます

## 実行の停止

プログラムは長時間実行されるため、停止したい場合は `Ctrl+C` を押してください。

## パラメータの変更

プログラム内の以下の変数を変更することで、シミュレーション条件を調整できます：

- `delay`: ブロック伝播遅延時間
- `generationTime`: ブロック生成時間
- `endRound`: シミュレーション終了ラウンド
- `N`: ノード数
- `hashrate[]`: 各ノードのハッシュレート

## 注意事項

- シミュレーションは計算集約的なため、実行には時間がかかります
- メモリ使用量にご注意ください
- 大きなendRound値を設定する場合は、十分な実行時間を確保してください 