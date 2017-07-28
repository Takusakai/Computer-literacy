# MATLABによる画像処理
## サンプリングする
サンプリングとは一定の間隔でデータを測定することで、音や映像をデジタルデータに変換する際に用いられる処理方法の一つである。このレポートではサンプリングの精度を落としていった結果を報告する。
画像「neko」を原画像とする。これは縦960画素、横1706画素による長方形のディジタルカラー画像である。

ORG=imread('neko.jpg');

imagesc(ORG); axis image;

の部分で原画像を読み込み、表示する。結果を図1に示す。

![原画像](https://github.com/Takusakai/Computer-literacy/blob/master/neko1.jpg)
:-図1　原画像

原画像1/2サンプリングするには、画像を1/2倍に縮小して解像度を凝縮した後に、2倍に拡大すればよい。その部分のコードが以下である。

IMG = imresize(ORG,0.5);

IMG2 = imresize(IMG,2,'box');

1/2サンプリングした結果が図2である。

![neko2](https://github.com/Takusakai/Computer-literacy/blob/master/neko2..jpg)  図２　1/2サンプリング

同様にしていくと1/4、1/8、1/16、1/32とサンプリングされていく。
図３～図6にその結果を示す。

![neko3](https://github.com/Takusakai/Computer-literacy/blob/master/neko3.jpg)
図3　1/4サンプリング

![neko4](https://github.com/Takusakai/Computer-literacy/blob/master/neko4.jpg)
図4　1/8サンプリング

![neko5](https://github.com/Takusakai/Computer-literacy/blob/master/neko5.jpg)
図5　1/16サンプリング

![neko6](https://github.com/Takusakai/Computer-literacy/blob/master/neko6.jpg)
図6　1/32サンプリング

このように間隔が大きくなればなるほど画像がモザイク状になっていく。

