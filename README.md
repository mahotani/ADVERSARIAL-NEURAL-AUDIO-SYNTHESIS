# ADVERSARIAL NEURAL AUDIO SYNTHESIS

## ABSTRACT
**link :** https://arxiv.org/abs/1902.08710  
効率的な音声生成は機械学習のタスクの中で難しい部類である。  
WaveNetのような自己回帰モデルで音声生成はできるが、1回1回のサンプル生成に時間がかかり、その都度評価もしなければならないので生成が遅い。  
対照的に、Generative Adversarial Network(GAN)は効率的に音声を生成できるが、綺麗な音にするのが難しい。  
十分な条件下で行えばGANでもうまくいきます。  
この研究では、NSynthデータセットに対して実証実験をしてみてGANを使ってWaveNetのような自己回帰モデルでの生成よりもめっちゃ早く効率的に音声を生成できることを実証する。  
