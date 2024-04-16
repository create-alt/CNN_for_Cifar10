# CNN_for_Cifar10<br>
10クラスの画像データである*Cifar-10*( https://www.cs.toronto.edu/~kriz/cifar.html )の分類用モデルの作成を行った。<br>
評価指標はaccuracy。NN構築にはKerasのSeaquentialを使用。事前学習モデルは不使用。<br>
元データに4種類の前処理を施すことでそれぞれについてモデルを作成し、**アンサンブル**を行った。<br>
さらに、学習用データについては水平反転や小回転による**データ拡張**を行い、学習精度の向上を目指した。<br>
これからも定期的にコードの改善を行っていく予定。<br>

暫定精度：84.21%<br>

課題：dropoutとBatchNormalizationの挿入位置。<br>
&emsp;&emsp;&emsp;&emsp;dropoutは全結合の前のみ かつ　BatchNormalizationの後　といった調整が必要とみられる。<br>
&emsp;&emsp;&emsp;&emsp;（ 参考： https://qiita.com/fkxyz1224/items/c38a18741ebb88ea5fa2 ）
