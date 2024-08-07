# 研究「サッカーにおけるキックモーションの３次元姿勢推定に基づく解析」

## 1. 概要
スポーツバイオメカニクス観点からの評価方法に基づいて、三次元姿勢推定(Strided Transformer)を行い関節角度推移を解析する <br>
※詳細はpdfファイルに記載

![image](https://github.com/Sumisumisumith/Kickmotion-Evaluation-System/assets/130366050/17876b14-527a-45cf-8314-0230e6b34fcc)

![image](https://github.com/Sumisumisumith/Kickmotion-Evaluation-System/assets/130366050/3c6bc79c-0a1a-4cc2-80eb-a5c33390479e)

## 2. 環境
- 使用言語：Python3.10.12,Pytorch
- 開発環境：google colablatory(T4 GPU使用)

## 3. システム構成
1. キックモーション映像を入力として、Strided Transformerを実行
2. 実行結果で得た三次元関節座標から三次元角度推移を計算
3. 被験者10人x2本ずつのキックモーション動画に対して①と②を繰り返す
4. step③で得たデータセット20サンプルに対して最尤推定によるガウス分布フィッティングを行う
5. グラフに可視化して出力

## 4. 内容
1. サッカーにおけるスポーツバイオメカニクス
2. Strided Transformer
3. 関節データ解析：最尤推定

## 5．今後の計画
1. ３次元姿勢推定
   - データセットを作成する際、撮影した動画のキック時前後1秒を手動でトリミングしていたが、物体検知を用いてトリミングを行うことでデータセットを作成しやすくする
3. 関節データ解析
   - 逆強化学習を用いて、サッカー経験者のキックの軌跡を学習することで関節データを解析する
   - ガウス過程力学モデル（GPDM）を用いて、全関節を考慮する
   
## 6．参考文献
- [StridedTransformer-Pose3D] 機械学習で動画の人物の姿勢推定 [Python] - TeDokology <br>
https://www.12-technology.com/2022/07/stridedtransformer-pose3d-python.html

## 6．その他
