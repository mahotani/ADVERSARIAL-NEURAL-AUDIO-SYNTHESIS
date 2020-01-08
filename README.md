# ADVERSARIAL NEURAL AUDIO SYNTHESIS

## ABSTRACT
**link :** https://arxiv.org/abs/1902.08710  
効率的な音声生成は機械学習のタスクの中で難しい部類である。  
WaveNetのような自己回帰モデルで音声生成はできるが、1回1回のサンプル生成に時間がかかり、その都度評価もしなければならないので生成が遅い。  
対照的に、Generative Adversarial Network(GAN)は効率的に音声を生成できるが、綺麗な音にするのが難しい。  
十分な条件下で行えばGANでもうまくいきます。  
この研究では、NSynthデータセットに対して実証実験をしてみてGANを使ってWaveNetのような自己回帰モデルでの生成よりもめっちゃ早く効率的に音声を生成できることを実証する。  

## 1 INTRODUCTION
生成のクオリティと汎用性の両方を効率的に達成するにはオーディオを生成するための生成モデルをトレーニングすることは難しい課題です。  
WaveNetなどの自己回帰モデルで汎化問題は解決されたが、1度に1オーディオしか生成できず、新規のオーディオは過去に生成されたオーディオに依存するため、生成速度が遅いのが問題でした。  
なので、たくさんの人が高速化に取り組んできましたが、これらの方法はかなりの確率でオーバーフィットをもたらしていました。  
また、敵対的学習であるGANが画像生成において高いクオリティを出しています。  
実際に、スペクトログラムとGANによる音声認識などの他のタスクではいくつか成功例があります。  
しかし、オーディオをスペクトルなどに画像化して、画像生成用のGANを用いて生成しようとすると、画像ほどのクオリティはなかなか出せません。  

### 1.1 GENERATING INSTRUMENT TIMBRES

