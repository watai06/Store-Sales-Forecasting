# Kaggle Weekly Sales Forecast

このリポジトリは、Kaggleコンペティションで使用した「週次売上予測モデル」に関するノートブックとデータ前処理コードをまとめたものです。

## ファイル構成

| ファイル名 | 内容 |
|-----------|------|
| `dataprocessing.ipynb` | データの前処理、特徴量エンジニアリング |
| `model.ipynb` | LightGBMによる学習・予測・提出ファイル作成 |

## 使用モデル

- LightGBM（回帰）
- 評価指標：RMSE（Root Mean Squared Error）

## 工夫した点

- 月・週ごとの売上トレンドを特徴量に取り入れ
- date列を月・期などに分解し、モデルに与えやすい形に変換
- マイナスの売上予測値は0でクリッピング

## 結果

| スコア | 数値 |
|--------|------|
| Public Score | 3519.97015 |
| Private Score | 3633.47416 |

## 使用環境

- Python 3.x
- Pandas / NumPy / LightGBM / Scikit-learn
