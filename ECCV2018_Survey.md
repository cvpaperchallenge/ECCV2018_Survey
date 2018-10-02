* [Viewpoint Estimation - Insights & Model](http://openaccess.thecvf.com/content_ECCV_2018/html/Gilad_Divon_Viewpoint_Estimation_-_ECCV_2018_paper.html)
    * 対象物体がどの角度から撮影されたものかを推定する研究．Engineering的に，何をするのが精度向上に寄与するのかを検討してまとめている感じの論文．書き方がシンプルでわかりやすいし，後続の研究には役立ちそう．

* [Video Re-localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Feng_Video_Re-localization_via_ECCV_2018_paper.html)
    * Queryの動画と意味的に同じシーンをReferenceから抜き出してくるタスクの提案．タスク自体を新規性としているけど，従来の動画検索タスクとそこまで変わらない．でも新しくデータセットを用意（Temporal Boundaryカッチリつけなきゃいけなくてかなり大変）して最近やられていなかった問題に焦点を当てようとしているのが強い．あと図1のタスクのサンプルがDBZのフュージョンのシーンでずるい．

* [A Deeply-initialized Coarse-to-fine Ensemble of Regression Trees for Face Alignment](http://openaccess.thecvf.com/content_ECCV_2018/html/Roberto_Valle_A_Deeply-initialized_Coarse-to-fine_ECCV_2018_paper.html)
    * 顔の器官点検出手法の新規提案．CNNで各器官点の尤度マップを出した後に3DモデルとのフィッティングとかEnsemble Regression Tree (ERT) ベースの手法とかを適用させている．DeepベースとERTベースの良いとこ取り? 32FPSとかなり高速でありながら非常に高い精度を達成．

* [Deep Kalman Filtering Network for Video Compression Artifact Reduction](http://openaccess.thecvf.com/content_ECCV_2018/html/Guo_Lu_Deep_Kalman_Filtering_ECCV_2018_paper.html)
    * 動画の圧縮（H.264など）によって生じるアーティファクトを除去して，圧縮した動画をキレイに復元するための手法を提案．従来はアーティファクトの乗っている汚いフレームの系列だけから復元をしようとしていたのに対して，提案手法では復元したキレイなフレームの系列も利用してより良い復元を実現するための手法を提案している．活発に研究されているタスクではなさそうなので結果の比較手法はやや少なめ．

* [Exploring Visual Relationship for Image Captioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Ting_Yao_Exploring_Visual_Relationship_ECCV_2018_paper.html)
    * 画像キャプショニングをする際にObjectなどのRelationshipを取り入れる手法を提案．画像にObject DetectionやRelationship Detectionをかけて，それらをグラフ構造で表現してGraph Convolutionする．その出力をMean Pooling/Attentionで処理した後にLSTMに入力してキャプションを生成．各物体の空間的・意味的な関係性を記述することでキャプション生成をしているところがポイントという主張．

* [Sequential Clique Optimization for Video Object Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yeong_Jun_Koh_Sequential_Clique_Optimization_ECCV_2018_paper.html)
    * Video Object Segmentationの新規手法提案．各フレームのsalient objectを検出した後，各フレーム，各objectのインスタンスを要素とした完全K部グラフを考えて，それに対する最大クリーク問題として定式化．この問題はNP困難なのでそれを効率的に解くための手法を提案．従来の手法より大きく精度が向上している．

* [Spatial Pyramid Calibration for Image Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Yan_Wang_Spatial_Pyramid_Calibration_ECCV_2018_paper.html)
    * 空間的な非対称性を畳み込みに導入するだけでなく、複数スケールの領域からの視覚的手がかりを抽出してより豊かな情報を組み込むことができるマルチスケールの空間非対称再校正（MS-SAR）を提案する。

* [Visual Text Correction](http://openaccess.thecvf.com/content_ECCV_2018/html/Amir_Mazaheri_Visual_Text_Correction_ECCV_2018_paper.html)
    * 動画とテキスト（間違った単語を含む）を入力として，間違っている単語の検出と正しい単語の推定をする新しい問題設定 (Visual Text Correction) の提案．面白いとは思うけどいまいちアプリケーションがわかりにくいし，後続の研究が出るかどうか微妙なところ．

* [X-ray Computed Tomography Through Scatter](http://openaccess.thecvf.com/content_ECCV_2018/html/Adam_Geva_X-ray_Computational_Tomography_ECCV_2018_paper.html)
    * X線CTの撮影に関する研究．従来のX線CTだと体に当たって散乱する光子はノイズとして扱われてたけど，そういうのもうまく使ってよりX線の照射を少なく効率的に撮影しようとする研究．CV系でこんなに医用系に寄った研究見るの初めてかもしれない．

* [Graph Distillation for Action Detection with Privileged Information in RGB-D Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Zelun_Luo_Graph_Distillation_for_ECCV_2018_paper.html)
    * 限定された訓練データと部分的に守られているモダリティが利用可能で現実的かつ挑戦的な条件下で、マルチモーダルな動画における行動検出に取り組む技術を提案する。

* [Modular Generative Adversarial Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Bo_Zhao_Modular_Generative_Adversarial_ECCV_2018_paper.html)
    * モジュールネットワークに触発され，様々な機能を再利用可能で互換性のあるいくつかのマルチドメインimage-to-image変換用のModularGANを提案．これらのモジュールは同時に学習され，互いに組み合わされて，画像翻訳タスクの領域に応じて特定のネットワークを構築することができる．実験の結果，提案モデルが魅力的な知覚結果を提示するだけでなく，マルチドメインフェイシャル特性を伝達するタスクに関する最先端の手法よりも優れていることを示唆した．

* [R2P2: A ReparameteRized Pushforward Policy for Diverse, Precise Generative Path Forecasting](http://openaccess.thecvf.com/content_ECCV_2018/html/Nicholas_Rhinehart_R2P2_A_ReparameteRized_ECCV_2018_paper.html)
    * 車の未来の軌跡を予測する手法を提案する研究．予測のDiversityとPrecisionのトレードオフを考慮するような目的関数?の設計が主なContribution? ReparametaRizedでR2はちょっと苦しいのでは感．R2D2っぽく言いたいだけ...

* [DFT-based Transformation Invariant Pooling Layer for Visual Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Jongbin_Ryu_DFT-based_Transformation_Invariant_ECCV_2018_paper.html)
    * CNNで使われる従来のMax/Average Poolingの代わりとしてDFTベースのPooling手法を提案．Global Average Poolingすると位置不変性が得られるけど，shapeとかの情報が落ちたりするという問題を解決したいというMotivation．こういう割と汎用的なモジュールで定着させるのはかなりインパクトのある結果がないと難しそう．

* [X2Face: A network for controlling face generation by using images, audio, and pose codes](http://openaccess.thecvf.com/content_ECCV_2018/html/Olivia_Wiles_X2Face_A_network_ECCV_2018_paper.html)
    * 顔を映した動画が入力で，その顔の姿勢とか表情を別の入力でcontrolする研究．別の入力は同じような顔の動画だったり，音声だったりPose Code Vectorだったり，いろんな入力でcontrolできる．学習はself-supervisedでできるようになっていて，色々応用が聞きそうな気がする．

* [Compositional Learning of Human Object Interactions](http://openaccess.thecvf.com/content_ECCV_2018/html/Keizo_Kato_Compositional_Learning_of_ECCV_2018_paper.html)
    * Human-object interactionの認識で，未知のペアに対しても動くようなzero-shot learning系の手法を提案．人って普通椅子とかソファに座るけど，テレビに座ったり棚の上に座ったりすることもあるよね，そういう意外な未知のペアに対してもうまく動くのが必要だよね，というMotivation．ベンチマーク手法を結構用意して結果を載せていて今後も続けさせようという感じがある．

* [Learning to Navigate for Fine-grained Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Ze_Yang_Learning_to_Navigate_ECCV_2018_paper.html)
    * Fine-grained RecognitionでDiscriminativeな領域をself-supervisedで見つけながらうまく学習・認識するための手法を提案．Navigator, Teacher, Scruntinizerの3つで構成．ちょっと面白そうな気がするんだけど，うまく名前を付けているだけかも?

* [Cross-Modal Ranking with Soft Consistency and Noisy Labels for Robust RGB-T Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Chenglong_Li_Cross-Modal_Ranking_with_ECCV_2018_paper.html)
    * ビジュアルトラッキングのためのロバストなRGB-Tオブジェクトの特徴を学習するグラフベースのクロスモーダルランキングアルゴリズムを提案した。

* [Light-weight CNN Architecture Design for Fast Inference](http://openaccess.thecvf.com/content_ECCV_2018/html/Ningning_Light-weight_CNN_Architecture_ECCV_2018_paper.html)
    * 効率的なネットワーク設計のための実践的ガイドラインの提案および新規のアーキテクチャであるShuffleNet V2の提示．さらにそのネットワークの速度と計算において最先端であることを検証した．

* [Fully Motion-Aware Network for Video Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Shiyao_Wang_Fully_Motion-Aware_Network_ECCV_2018_paper.html)
    * 統合フレームワークで、ピクセルレベルとインスタンスレベルの両方のオブジェクトの特徴を共同で較正する完全に動きを認識するネットワーク（MANET）と呼ばれるend-to-endモデルを提案した。

* [Shift-Net: Image Inpainting via Deep Feature Rearrangement](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhaoyi_Yan_Shift-Net_Image_Inpainting_ECCV_2018_paper.html)
    * ディープな特徴の再配置により細部までの再現，高速なスピードを実現し、画像補完のための新しいShift-Netを提案した。

* [Choose Your Neuron: Incorporating Domain Knowledge through Neuron Importance](http://openaccess.thecvf.com/content_ECCV_2018/html/Ramprasaath_Ramasamy_Selvaraju_Choose_Your_Neuron_ECCV_2018_paper.html)
    * 新規クラスの領域知識をネットワークニューロンの重要性に基づいて分類器の重みに直接マッピングすることを学習するニューロン重視の体重移動（NIWT）と呼ばれる方法を提案した。

* [Joint 3D tracking of a deformable object in interaction with a hand](http://openaccess.thecvf.com/content_ECCV_2018/html/Aggeliki_Tsoli_Joint_3D_tracking_ECCV_2018_paper.html)
    * 複雑で変形可能な物体を手との相互作用において追跡することができる新規の方法を提案する。

* [Interpolating Convolutional Neural Networks Using Batch Normalization](http://openaccess.thecvf.com/content_ECCV_2018/html/Gratianus_Wesley_Putra_Data_Interpolating_Convolutional_Neural_ECCV_2018_paper.html)
    * ビジュアルクラスを区別するためのバッチ正規化レイヤーを作成しそれらを結合して新しいタスクを解決する方法を定式化することによってこのメカニズムの簡単なエミュレーションを提案した。

* [Learning Warped Guidance for Blind Face Restoration](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaoming_Li_Learning_Warped_Guidance_ECCV_2018_paper.html)
    * ぼんやりしたぼやけた、ノイズの多い、低解像度の、または圧縮された画像（すなわち、劣化した観察）からの盲目の顔の復元問題に取り組み，劣化した観測と高品質の誘導画像の両方を入力と同じアイデンティティからとることによって、誘導ブラインドフェイス復元モデル、GFRNetを提案した。

* [NAM: Non-Adversarial Unsupervised Domain Mapping](http://openaccess.thecvf.com/content_ECCV_2018/html/Yedid_Hoshen_Separable_Cross-Domain_Translation_ECCV_2018_paper.html)
    * 画像のDomain変換手法の提案．CycleGANがPopularだけど，学習が安定しなかったりするし，ドメイン間で1対1の対応を仮定しているので1対多，多対1とかは扱いにくかったりと問題があると指摘．提案手法は，Adversarialな学習をするんじゃなくて，ドメインXの画像を生成するGeneratorと，ドメインXからドメインYに変換するTranslatorを同時に学習（GeneratorとTranslatorは敵対してないからNon-adversarial）．CycleGANが定番になりつつあるけどそれに全力で立ち向かっていて面白い．学習の安定とかがあまり実験的に示していなさそうに見える（ちゃんと確認してない）ので少し残念．

* [Task-driven Webpage Saliency](http://openaccess.thecvf.com/content_ECCV_2018/html/Quanlong_Zheng_Task-driven_Webpage_Saliency_ECCV_2018_paper.html)
    * Webページ上でタスク駆動の視覚的顕著性を予測するためのend to end学習フレームワークを提示する。

* [Appearance-Based Gaze Estimation via Evaluation-Guided Asymmetric Regression](http://openaccess.thecvf.com/content_ECCV_2018/html/Yihua_Cheng_Appearance-Based_Gaze_Estimation_ECCV_2018_paper.html)
    * 顔（というか目）画像を入力として視線方向を推定する手法の研究．左右の目を入力としたときのAsymmetric（左右の目の方向は物理的に一貫するはずだけど，同じ回帰手法を左右の目に適用しても性能は結構違う）を考慮してどうこうするらしい．Asymmetricを扱うことの重要性はAbstract, Introductionからは読み取れず．

* [Pivot Correlational Neural Network for Multimodal Video Categorization](http://openaccess.thecvf.com/content_ECCV_2018/html/Sunghun_Kang_Pivot_Correlational_Neural_ECCV_2018_paper.html)
    * 隠れ状態、ならびにネットワークにおけるモーダルに依存しない旋回流とモーダル固有ストリームの予測との間の相関を最大にすることによって、マルチモーダルビデオカテゴリのピボット相関ニューラルネットワーク（ピボットCorrNN）を構築した。

* [Interactive Boundary Prediction for Object Selection](http://openaccess.thecvf.com/content_ECCV_2018/html/Hoang_Le_Interactive_Boundary_Prediction_ECCV_2018_paper.html)
    * 本稿では、対話型を意識した境界予測に基づく境界ベースのセグメンテーション手法を紹介した。

* [Scenes-Objects-Actions: A Multi-Task, Multi-Label Video Dataset](http://openaccess.thecvf.com/content_ECCV_2018/html/Heng_Wang_Scenes-Objects-Actions_A_Multi-Task_ECCV_2018_paper.html)
    * シーン、物体、行動の分類を含む多面的な問題として動画の理解を目的とした、新しい大規模でマルチタスクのマルチラベル動画データセットを導入しました。

* [Transferable Adversarial Perturbations](http://openaccess.thecvf.com/content_ECCV_2018/html/Bruce_Hou_Transferable_Adversarial_Perturbations_ECCV_2018_paper.html)
    * 画像に少しだけノイズを混ぜてモデルの認識性能を落とさせるAdversarial Perturbtationsの研究．従来White-box attack（モデルのパラメータが既知）ではかなり強い手法が出てきているけど，Black-box attack（モデルのパラメータが未知）ではイマイチ．この研究ではBlack-box attackを強くするために，あるモデル用に学習したPerturbutationsが他のモデルにも転移可能にするような手法を提案．

* [Incremental Non-Rigid Structure-from-Motion with Unknown Focal Length](http://openaccess.thecvf.com/content_ECCV_2018/html/Thomas_Probst_Incremental_Non-Rigid_Structure-from-Motion_ECCV_2018_paper.html)
    * 焦点距離が未知である以前の斜視カメラモデルおよび等角投影面を用いて、増分非剛体構造 - 運動（NRSfM）のための方法を提示する。テンプレートベースの場合、カメラ組み込み関数の4つのパラメータを推定する方法を提案した。

* [Semantically Aware Urban 3D Reconstruction with Plane-Based Regularization](http://openaccess.thecvf.com/content_ECCV_2018/html/Thomas_Holzmann_Semantically_Aware_Urban_ECCV_2018_paper.html)
    * 建物の周囲が滑らかな表面で表されている間に、平面シーンと建物の直線アウトラインを得ることができる都市背景の3D再構成方法を提案した。

* [Learning to Dodge A Bullet](http://openaccess.thecvf.com/content_ECCV_2018/html/shi_jin_Learning_to_Dodge_ECCV_2018_paper.html)
    * バレットタイム映像を生成するための手法を提案．提案手法は最低3枚の画像を入力として，視点のモーフィングをすることで間の映像を生成することでバレットタイム映像を作る．従来だと線形なカメラの動きに対するモーフィングなどしかやられていなかったところを，円形の動きにも対応できるようにしたところがポイントっぽい．

* [Training Binary Weight Networks via Semi-Binary Decomposition](http://openaccess.thecvf.com/content_ECCV_2018/html/Qinghao_Hu_Training_Binary_Weight_ECCV_2018_paper.html)
    * バイナリウェイトネットワークを学習するための新規なセミバイナリ量子化手法と、バイナリ制約下でセミバイナリ分解因子を解く交互最適化手法を提案した。

* [Learnable PINs: Cross-Modal Embeddings for Person Identity](http://openaccess.thecvf.com/content_ECCV_2018/html/Samuel_Albanie_Learnable_PINs_Cross-Modal_ECCV_2018_paper.html)
    * 顔→音声　音声→顔のクロスモーダルな検索を可能とした．これを評価することで新しいタスクのベンチマークを確立した．また，テレビドラマの字幕を自動的に検索しラベリングするアプリケーションを示している．

* [Toward Characteristic-Preserving Image-based Virtual Try-On Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Bochao_Wang_Toward_Characteristic-Preserving_Image-based_ECCV_2018_paper.html)
    * 新しい幾何学的マッチングモジュールおよび新しいマージング戦略を用いた試行モジュールを含む、CP-VTONと名付けられた特徴を保持する画像生成に向けて、完全に学習可能な画像ベースの仮想試着パイプラインを提案した。

* [Deep Feature Factorization For Unsupervised Concept Discovery](http://openaccess.thecvf.com/content_ECCV_2018/html/Edo_Collins_Deep_Feature_Factorization_ECCV_2018_paper.html)
    * 画像内または画像のセット内で類似の意味概念を定位することができる方法であるディープ・フィーチャ・ファクタライゼーション（DFF）を提案した。

* [SOD-MTGAN: Small Object Detection via Multi-Task Generative Adversarial Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Yongqiang_Zhang_SOD-MTGAN_Small_Object_ECCV_2018_paper.html)
    *   
    小型物体の検出問題に対処するために、エンドツーエンドのマルチタスクGAN（MTGAN）を提案   
    ぼやけた小さな画像から鮮明な超解像度画像の復元の有用性を示す 

* [Human Motion Analysis with Deep Metric Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/HUSEYIN_COSKUN_Human_Motion_Analysis_ECCV_2018_paper.html)
    * 2つのモーションシーケンスの類似度を測定するための新しいロス関数とネットワークアーキテクチャを提案する。2つのデータセットで実験を行い従来の動作測定基準より大幅な改善

* [Dist-GAN: An Improved GAN using Distance Constraints](http://openaccess.thecvf.com/content_ECCV_2018/html/Ngoc-Trung_Tran_Generative_Adversarial_Autoencoder_ECCV_2018_paper.html)
    * Mode collapseと勾配消失を緩和するGANの訓練アルゴリズムの提案． ""discriminator-score distance""を用いて新しいジェネレータ目標を提案する。また，再構成されたサンプルを実サンプルとみなして，識別機の収束とオートエンコーダの収束を結合．generatorがMode collapseとなるのを防ぐためにオートエンコーダをlatent-data distance constraintで正規化．

* [Cross-Modal and Hierarchical Modeling of Video and Text](http://openaccess.thecvf.com/content_ECCV_2018/html/Bowen_Zhang_Cross-Modal_and_Hierarchical_ECCV_2018_paper.html)
    * 動画とテキストのクロスモーダル変換の学習手法の提案．複数のモダリティに対応した階層的なシーケンシャルデータのモデリング手法の検討．大規模動画と文章のデータセットで実証的な研究を行い，有効性を実証．zero-shot 行動認識とビデオキャプションにおいて有用

* [Deep Image Demosaicking using a Cascade of Convolutional Residual Denoising Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Filippos_Kokkinos_Deep_Image_Demosaicking_ECCV_2018_paper.html)
    * 本研究では、統合的なノイズ除去とデモザイク問題に対して高品質の画像を生成する新規な深い学習システムを提案した。

* [Deep Clustering for Unsupervised Learning of Visual Features](http://openaccess.thecvf.com/content_ECCV_2018/html/Mathilde_Caron_Deep_Clustering_for_ECCV_2018_paper.html)
    * 教師なし学習の新たな手法として畳み込みネットワークの出力をk-meansでクラスタ分類し，その結果を教師ラベルとして学習を行うDeepClusterを提案した．

* [Domain Adaptation through Synthesis for Unsupervised Person Re-identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Slawomir_Bak_Domain_Adaptation_through_ECCV_2018_paper.html)
    * 学習済みモデルの目に見えない照明条件下で有効化にするための微調整を必要とする問題を軽減するために数百の照明条件を含む新しい合成データセットを提案した。

* [Facial Expression Recognition with Inconsistently Annotated Datasets](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiabei_Zeng_Facial_Expression_Recognition_ECCV_2018_paper.html)
    * 一貫性のないラベルを持つ複数のデータセットから分類子を学習する方法IPA2LTフレームワークを提案した。

* [Single Shot Scene Text Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Lluis_Gomez_Single_Shot_Scene_ECCV_2018_paper.html)
    * シーン中のテキスト検索問題に取り組む研究．新規性はsingle-shot CNNアーキテクチャを使用したこと．このアーキテクチャでテキストベースの画像検索タスクが，CNNの出力のテキストの質問の簡単な最近傍検索としてキャスト．実験により，提案手法が処理速度を大幅に向上させ，優れていることを示している．

* [DeepVS: A Deep Learning Based Video Saliency Prediction Approach](http://openaccess.thecvf.com/content_ECCV_2018/html/Lai_Jiang_DeepVS_A_Deep_ECCV_2018_paper.html)
    * DeepVSと呼ばれる新しい深層学習に基づく映像顕著性予測法を提案   
    saliency-structured ConvLSTMを提案 

* [Generalizing A Person Retrieval Model Hetero- and Homogeneously](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhun_Zhong_Generalizing_A_Person_ECCV_2018_paper.html)
    * 人の再識別（re-ID）のための新しい教師なしドメイン適応方法，Het-Homogeneous Learning（HHL）を提案した。

* [A New Large Scale Dynamic Texture Dataset with Application to ConvNet Understanding](http://openaccess.thecvf.com/content_ECCV_2018/html/Isma_Hadji_A_New_Large_ECCV_2018_paper.html)
    * 大規模な動的テクスチャデータセットの提案．外観と動的なテクスチャが分かれているカテゴリと外観が動的なテクスチャになっているカテゴリの2種類のカテゴリがある1万以上の動画を含んだDynamic Texture DataBase(DTDB)を提案．

* [Deep Cross-modality Adaptation via Semantics Preserving Adversarial Learning for Sketch-based 3D Shape Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiaxin_Chen_Deep_Cross-modality_Adaptation_ECCV_2018_paper.html)
    * スケッチベースの3次元形状形成のための新しいモダリティ適応モデルを提案した。バッチ単位で最も難しいサンプルを取得することによって重要性を認識するメタ学習を採用し、モダリティ固有の差別的な特徴を学習した。クロスモダリティの不一致を解消するために、スケッチの特徴を3Dシェイプの特徴空間に転送することで、変換ネットワークを提案した。SHREC 2013，SHREC2014での実験結果は，state-of-the-artと比較し，優れた検索性能を示す．

* [BiSeNet: Bilateral Segmentation Network for Real-time Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Changqian_Yu_BiSeNet_Bilateral_Segmentation_ECCV_2018_paper.html)
    * リアルタイム性のあるセマンティックセグメンテーションの速度と精度を同時に向上させるためのバイラテラルセグメンテーションネットワーク（BiSeNet）を提案する。提案するBiSeNetには、Spatial Path（SP）とContext Path（CP）という2つのパスが含まれていて、SPは元の画像から空間情報を保持し、CPは、軽量モデルとグローバル平均プールを利用して精度と速度を向上させた。

* [Face De-spoofing](http://openaccess.thecvf.com/content_ECCV_2018/html/Yaojie_Liu_Face_De-spoofing_ECCV_2018_paper.html)
    * 偽装顔を現実の顔に逆分解させ、偽装ノイズパターンを生成することにより、顔の偽装を解決する新たな方法の提案。

* [Towards End-to-End License Plate Detection and Recognition: A Large Dataset and Baseline](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhenbo_Xu_Towards_End-to-End_License_ECCV_2018_paper.html)
    * ナンバープレートデータセットCCPDの紹介   
    CCPDを用いてバウンディングボックスを予測，高速かつ正確にLP番号を同時認識できる新規ネットワークモデルを提案(RPnet)   
    精度・速度ともに現在の物体検出よりも優れている 

* [Self-supervised Tracking by Colorization](http://openaccess.thecvf.com/content_ECCV_2018/html/Carl_Vondrick_Self-supervised_Tracking_by_ECCV_2018_paper.html)
    * グレースケール動画のカラー化する学習モデル作成  
    グランドトゥルースラベルなしの学習だが，最新のオプティカルフローによる手法よりも優れた性能発揮

* [Pose Proposal Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Sekii_Pose_Proposal_Networks_ECCV_2018_paper.html)
    * 自然かつ時間的な一貫性を用いて、参照フレームから色をコピーすることによってグレースケールの動画をカラーにする学習モデルを作成した．

* [Incremental Multi-graph Matching via Diversity and Randomness based Graph Clustering](http://openaccess.thecvf.com/content_ECCV_2018/html/Tianshu_Yu_Incremental_Multi-graph_Matching_ECCV_2018_paper.html)
    * インクリメンタルな複数グラフマッチングの手法を考案。順次グラフを入力して最適化していく方法を考案した。

* [Single Image Intrinsic Decomposition Without a Single Intrinsic Image](http://openaccess.thecvf.com/content_ECCV_2018/html/Wei-Chiu_Single_Image_Intrinsic_ECCV_2018_paper.html)
    * 画像における変動要因を解消する手法の提案した．固有の画像に対し効果的に分解された画像を学習し弱教師あり学習で拡張した2ストリームCNNフレームワークを提示した。合成画像と実画像の両方のデータセットによる実験研究に有効性を実証。

* [Triplet Loss with Theoretical Analysis in Siamese Network for Real-Time Object Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Xingping_Dong_Triplet_Loss_with_ECCV_2018_paper.html)
    * Pairwise LossにSiameseネットワークフレームワークを追加することで、オブジェクトトラッキングのための様々な特徴を抽出するための新しいTriplet Lossを提案する。入力を追加せずに，元のサンプルの組み合わせでより強力な機能を実現するため，より多くの要素を学習に利用できる．また，手法の有用性を証明するたえ，勾配とback-propagationの比較を組み合わせた理論的解析を提案．ベースラインのトラッキングとほぼ同等のフレームレートで動作し，優れたパフォーマンス達成．最近のリアルタイムのトラッキングと同等の精度を達成．

* [Learning to Learn Parameterized Image Operators](http://openaccess.thecvf.com/content_ECCV_2018/html/Qingnan_Fan_Learning_to_Learn_ECCV_2018_paper.html)
    * 画像オペレータの近似・加速・改善のために，ディープネットワークが使用されていて，このオペレータはよい結果にするために微調整が必要なパラメータを多数持つ．   
    これを改善するための，ネットワークの重みを自動的に調整する新しいデカップル学習アルゴリズムの提案． 

* [HBE: Hand Branch Ensemble network for real time 3D hand pose estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yidan_Zhou_HBE_Hand_Branch_ECCV_2018_paper.html)
    * 単一の深度画像から手関節の3D座標を推定するときに，精度とリアルタイム性の両方を考慮した，ハンドブランチアンサンブルネットワーク(HBE)という3ブランチの畳み込みニューラルネットワークの設計．   
    3つのブランチはそれぞれ，親指，人差し指，その他の指の3つの部分に対応している． 

* [Generative Semantic Manipulation with Mask-Contrasting GAN](http://openaccess.thecvf.com/content_ECCV_2018/html/Liang_Generative_Semantic_Manipulation_ECCV_2018_paper.html)
    * 猫→犬のような，独自の形状を維持しながら，オブジェクトの意味的意味を変更するための，コントラスト-GANの提案．  
    合成されたサンプルをターゲットデータの近くに直接作成せず、ターゲットとの距離比較を最適化．  
    他の条件付きGANに比較してパフォーマンス向上を示した．

* [Learning to Fuse Proposals from Multiple Scanline Optimizations in Semi-Global Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Johannes_Schoenberger_Learning_to_Fuse_ECCV_2018_paper.html)
    * Semi-Global Matching(SGM)の集約方式を，スキャンラインで最適化して推定された視差を融合する学習ベースの方法に着かえることを提案．ここで，提案されるSGM-Forestアルゴリズムはピクセル毎の分類を用いて問題を解決．SGM-ForestはETH3D stereo benchmarkで1位にランクされている．

* [Less is More: Picking Informative Frames for Video Captioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Yangyu_Chen_Less_is_More_ECCV_2018_paper.html)
    * ビデオキャプションにおいて有益なフレームをピッキングするplug-and-playのPickNetを提案．標準的なエンコーダ/デコーダのフレームワークに基づき，視覚的多様性を最大にすることと生成キャプションとGrandTruthの不一致を最小限に抑えることを報酬としてを逐次的に訓練する強化学習ベースの手順を開発．結果的に，コンパクトなフレームのセットを選択して，性能が低下せずにキャプションを生成する．実験により，6~8フレームで一般的なベンチマークでの競合性能を達成．

* [Deep Pictorial Gaze Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Seonwook_Park_Deep_Pictorial_Gaze_ECCV_2018_paper.html)
    * 片眼画像の入力からの視線方向の推定のために特別に設計された新規な深層ニューラルネットワークアーキテクチャを提案した。

* [SkipNet: Learning Dynamic Execution in Residual Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Xin_Wang_SkipNet_Learning_Dynamic_ECCV_2018_paper.html)
    * 最大精度を出すには，より畳み込み層の多いネットワークが必要であるが，多くの入力では浅いネットワークで十分．   
    本論文では，入力毎にネットワークの畳み込みレイヤーをスキップすることを学習することで，計算量の削減を行うSkipNetsの提案   
    精度を維持しながら計算量を30～90%削減成功 

* [Mask TextSpotter: An End-to-End Trainable Neural Network for Spotting Text with Arbitrary Shapes](http://openaccess.thecvf.com/content_ECCV_2018/html/Pengyuan_Lyu_Mask_TextSpotter_An_ECCV_2018_paper.html)
    * 自然画像におけるテキストの検出と認識をend-to-endで学習できるNural NetworkモデルであるMask TextSpotterを提案．セマンティックセグメンテーションにより，正確なテキスト検出と認識を可能に．ICDAR2013，ICDAR2015，Total-Textでの実験によりstate-of-the-art．

* [Deep Adaptive Attention for Joint Facial Action Unit Detection and Face Alignment](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhiwen_Shao_Deep_Adaptive_Attention_ECCV_2018_paper.html)
    * 顔面アクションユニット（AU）の検出と顔面アライメントは2つの相関の高いタスク  
    関節AU検出と顔面アライメントのためのエンドツーエンドの深い学習フレームワークを開発

* [Semantic Scene Understanding under Dense Fog with Synthetic and Real Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Christos_Sakaridis_Semantic_Scene_Understanding_ECCV_2018_paper.html)
    * 合成霧データと実霧データを用いて、軽合成霧から濃霧実霧へのセマンティックセグメンテーションモデルを多段階に徐々に適応させるカリキュラムモデル適応（CMAda）という新しい手法を提案した。

* [RIDI: Robust IMU Double Integration](http://openaccess.thecvf.com/content_ECCV_2018/html/Hang_Yan_RIDI_Robust_IMU_ECCV_2018_paper.html)
    * スマホIMUだけで自然な人間の動きの軌跡を推定する慣性航法の新しいデータ駆動型アプローチを提案  
    線形加速度と角速度の履歴から速度ベクトルを回帰し、線形加速度の低周波バイアスを補正し、位置を推定するために2回積分

* [Weakly-supervised Video Summarization using Variational Encoder-Decoder and Web Prior](http://openaccess.thecvf.com/content_ECCV_2018/html/Sijia_Cai_Weakly-supervised_Video_Summarization_ECCV_2018_paper.html)
    * 潜在的セマンティック・モデリングのためにウェブ・ビデオを活用し、原則的な方法でビデオ要約のあいまい性を減らすために、VESDと呼ばれる生成的要約フレームワークを導入

* [Transferring Common-Sense Knowledge for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Krishna_Kumar_Singh_Transferring_Common-Sense_Knowledge_ECCV_2018_paper.html)
    * ソースからターゲットカテゴリへのコモンセンス知識（DOCK）を転送することにより、オブジェクトを検出するためのスケーラブルなアプローチを提示．要はスプーンがメタリックのような常識を教えると検出結果が良くなるみたいな研究

* [Person Search in Videos with One Portrait Through Visual and Temporal Links](http://openaccess.thecvf.com/content_ECCV_2018/html/Qingqiu_Huang_Person_Search_in_ECCV_2018_paper.html)
    * 異なる環境で撮影されたポートレート画像を元に動画中から人物を検索するタスクを提案し，このタスクにおいてアイデンティティ伝播のための視覚的、時間的リンクを組み込んだ新たなフレームワークとデータベースを構築した論文．

* [Eliminating the Dreaded Blind Spot: Adapting 3D Object Detection and Monocular Depth Estimation to 360° Panoramic Imagery](http://openaccess.thecvf.com/content_ECCV_2018/html/Gregoire_Payen_de_La_Garanderie_Eliminating_the_Dreaded_ECCV_2018_paper.html)
    * 自動車のための長方形の360°のパノラマ画像を，従来の直線的画像用に開発された最新のDeep Networkアーキテクチャに適応させるアプローチを提案．アノテーション付きの車載データセットの可用性の欠如に対応し，現在の自動車のデータセットをスタイルや投影変換によって適応．単眼パノラマ画像から車両の深さや3D姿勢を復元するため．既存のアーキテクチャを再学習し，適応．

* [Folded Recurrent Neural Networks for Future Video Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Marc_Oliu_Folded_Recurrent_Neural_ECCV_2018_paper.html)
    * 同等の再帰AEモデルと比較して，計算コスト，メモリコストが低いビデオ予測アーキテクチャであるFolded Recurrent Neural Networksを提案．エンコーダとデコーダ間で情報を水平に渡すdouble-mappingGRU(dGRU)により達成．dGRUにより任意の段階でAE全体で使用する必要がなくなり，必要なエンコーダ/デコーダのみが実行される．学習中にノイズの多い識別機能を提供することで収束を促進．MMNISTとUCF101で3つのstate-of-the-artのアプローチを補油化し，2，3倍すくないメモリ使用量と計算コストを達成．

* [Deep Regression Tracking with Shrinkage Loss](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiankai_Lu_Deep_Regression_Tracking_ECCV_2018_paper.html)
    * 回帰ネットワークの主要なボトルネックが前景-背景の極端なデータの不均衡であると特定．訓練データのバランスをとるため，簡単な訓練データの重みを不利にする新しいロスを提案．残差を適用することで，複数の畳み込みレイヤと出力のレスポンスマップを融合．

* [Stroke Controllable Fast Style Transfer with Adaptive Receptive Fields](http://openaccess.thecvf.com/content_ECCV_2018/html/Yongcheng_Jing_Stroke_Controllable_Fast_ECCV_2018_paper.html)
    * 連続的かつ空間的なストロークサイズ制御を実現するスタイル転送ネットワークを提案した。

* [Part-Aligned Bilinear Representations for Person Re-Identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Yumin_Suh_Part-Aligned_Bilinear_Representations_ECCV_2018_paper.html)
    * 人物の再識別のための部分一致表現を学習するネットワークの提案．外観と身体部分の特徴マップを生成する2ストリームネットワークと2つの特徴マップを画像に結合する双線プール層で成る．Market-1501，CUHK03，CUHK01，DukeMTMC，MARSでstate-of-the-artを実証し，アプローチの有用性を検証

* [Joint 3D Face Reconstruction and Dense Alignment with Position Map Regression Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Yao_Feng_Joint_3D_Face_ECCV_2018_paper.html)
    * 3D顔面構造の再構築と密なアライメントの提供を同時に行う簡単な方法を提案する。これを達成するために、UV空間内の完全な顔の3D形状を記録するUV位置マップと呼ばれる2次元表現を設計し、単一の2D画像から回帰する単純なCNNを学習させた。

* [Learning Efficient Single-stage Pedestrian Detection by Asymptotic Localization Fitting](http://openaccess.thecvf.com/content_ECCV_2018/html/Wei_Liu_Learning_Efficient_Single-stage_ECCV_2018_paper.html)
    * R-CNNの精度を維持しながら，SDDの速度を実現する歩行者検出器の研究．Asymoptotic Localization Fitting(ALF)という単純であり効果的なモジュールの提案．さらに歩行者検出のベンチマークのCityPerosnsとCaltechの最新鋭の性能を達成するため効率的な歩行者検出アーキテクチャのALFNetを設計することで精度とスピードの両方を実現

* [Unsupervised Hard-Negative Mining from Videos for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/SouYoung_Jin_Unsupervised_Hard-Negative_Mining_ECCV_2018_paper.html)
    * ハードネガティブ、すなわち、検出器によって現在正または曖昧であると評価されているネガティブ例と，ハードポジティブ例をラベルのないビデオデータからマイニングする手法を提案

* [Focus, Segment and Erase: An Efficient Network for Multi-Label Brain Tumor Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xuan_Chen_Focus_Segment_and_ECCV_2018_paper.html)
    * 多ラベル脳腫瘍のセグメンテーションでは、クラスの不均衡およびクラス間干渉が一般的であり、挑戦的な問題．本稿では、これに対処するための新しいエンドツーエンドの訓練可能なネットワークFSENetを提案．

* [Maximum Margin Metric Learning Over Discriminative Nullspace for Person Re-identification](http://openaccess.thecvf.com/content_ECCV_2018/html/T_M_Feroz_Ali_Maximum_Margin_Metric_ECCV_2018_paper.html)
    * 人の再識別に対して標本数が少ない問題に効率的に対処し，既存の最先端技術に比べて大幅なパフォーマンス向上をもたらす，Nullspace Kernel Maximum Margin Metric Learning(NK3ML)という新しいメタ学習のフレームワークの提案．人の再同定の4つのベンチマークのデータセットによる実験により，提案アルゴリズムが既存のアルゴリズムより優れている結果．

* [Efficient Relative Attribute Learning using Graph Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Zihang_Meng_Efficient_Relative_Attribute_ECCV_2018_paper.html)
    * 顔が若い⇔老けのような相対属性学習と属性予測の両方を実行できる単純なフレームワークを提示

* [Object Level Visual Reasoning in Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Fabien_Baradel_Object_Level_Visual_ECCV_2018_paper.html)
    * 動画内の意味的な時空間的相互作用について推論し，学習売るモデルを提案．最先端の物体検出ネットワークの統合により．物体レベルでこの推論ができる．これにより，このモデルはセマンティックな物体のインタラクションの詳細な空間的相互作用を学習できる．3つの標準なデータセット(Twenty-BN Something-Something,VLOG,EPIC Kitchens)で評価し，すべてでstate-of-the-art

* [Learning-based Video Motion Magnification](http://openaccess.thecvf.com/content_ECCV_2018/html/Tae-Hyun_Oh_Learning-based_Video_Motion_ECCV_2018_paper.html)
    * 今までのVideo Motion Magnificationでは，ガウシアンフィルタであったが，DeepLearningを導入してデータから直接学習できるようにした.学習では2フレームを入力として学習しており，時間フィルタで学習していないのに周波数ベースの動きが確認でき，以前までの微分フィルタ同様の動きをすることを確かめた.

* [Video Object Segmentation with Joint Re-identification and Attention-Aware Mask Propagation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaoxiao_Li_Video_Object_Segmentation_ECCV_2018_paper.html)
    * template matchingとtemporal propagationを１つのネットワークにしたDyeNetを提案．end-to-endで学習し，見失ったターゲットが異なるポーズや大きさになって再び現れた時でもセグメンテーションができる．

* [Multimodal Unsupervised Image-to-image Translation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xun_Huang_Multimodal_Unsupervised_Image-to-image_ECCV_2018_paper.html)
    * 異なるドメインの画像は共通のContent空間があるが, Style空間は共有しないと仮定から, 画像のStyleとContentを別々にEncodeして後からconcatしてupsampleをして変換を行う.

* [Learning to Detect and Track Visible and Occluded Body Joints in a Virtual World](http://openaccess.thecvf.com/content_ECCV_2018/html/Matteo_Fabbri_Learning_to_Detect_ECCV_2018_paper.html)
    * CGデータを使って、オクルージョンに強い複数人のポーズ推定と追跡を行う研究。４つのブランチを持つネットワークで、見えている部分のヒートマップ、オクルージョンが発生している一のヒートマップ、パートアフィニティフィールド、時間的アフィニティフィールドである。

* [Local Spectral Graph Convolution for Point Set Feature Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Chu_Wang_Local_Spectral_Graph_ECCV_2018_paper.html)
    * point cloudの新しい認識手法のSoTA. 今までの３次元点群は独立した方法で抽象化されており，隣接する点の相対的なレイアウトや特徴は無視されていた.この問題をspectrag strategy greaph convolution on local graph と novel graph pooling strategyで解決する(提案手法). グラフの畳み込みでは特徴が共同で学習され点の近傍から最も近い近傍グラフ上で実行する.

* [Meta-Tracker: Fast and Robust Online Adaptation for Visual Object Trackers](http://openaccess.thecvf.com/content_ECCV_2018/html/Eunbyung_Park_Meta-Tracker_Fast_and_ECCV_2018_paper.html) [[GitHub](https://github.com/silverbottlep/meta_trackers)]
    * online adaptation-based trackで使われる初期ネットワークを調整するofflineなmeta-learning-basedな方法を提案して、それを既存SoTA手法に組み込むことでonline adaptationを用いたvisual object trackersタスクでSoTA達成

* [VSO: Visual Semantic Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Konstantinos-Nektarios_Lianos_VSO_Visual_Semantic_ECCV_2018_paper.html)
    * visual odometryのタスクで、セマンティックスを利用して、中期で対応点同士をトラッキングするフレームワークを提案する。

* [Progressive Lifelong Learning by Distillation and Retrospection](http://openaccess.thecvf.com/content_ECCV_2018/html/Saihui_Hou_Progressive_Lifelong_Learning_ECCV_2018_paper.html)
    * Lifelong learningにおいて、「蒸留」と「回顧」を用いたテクニックで古いタスクへの適応維持と新しいタスクへの適応をバランスよく行う。このテクニックで、古いタスクと新しいタスクの両方で精度の向上ができた。

* [Spatio-Temporal Channel Correlation Networks for Action Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Ali_Diba_Spatio-Temporal_Channel_Correlation_ECCV_2018_paper.html)
    * 3D CNNにとって時空間相関は十分なのかという問いからスタート。時空間特徴ではなく、時間特徴と空間特徴それぞれで3D CNNのチャンネル間の相関をモデル化する新しいブロックを導入する。Spatio-Temporal Channel Correlationと呼ぶ。

* [Long-term Tracking in the Wild: a Benchmark](http://openaccess.thecvf.com/content_ECCV_2018/html/Efstratios_Gavves_Long-term_Tracking_in_ECCV_2018_paper.html) [[GitHub](https://oxuva.github.io/long-term-tracking-benchmark/)]
    * 単一オブジェクトトラッキングのデータセットとベンチマークを提案。データセットはtrainは平均2.4分、頻繁にオブジェクトは消えるものであり、testはpascalみたいにサーバーを通じて行う。

* [Online Detection of Action Start in Untrimmed, Streaming Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Zheng_Shou_Online_Detection_of_ECCV_2018_paper.html)
    * Online Detection of Action Startのタスクで,hard negativeをGANを用いてtraining中生成して.負のサンプルからの変わり目をアシストする機構を加え,データ不足を解消.

* [Two Stream Pose Transfer Guided by Dense Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Natalia_Neverova_Two_Stream__ECCV_2018_paper.html)
    * ポーズを変更した人物画像を生成する際にDensePoseの出力結果を利用した。変更前の画像中に写っている服のテクスチャーをポーズ変更後の対応する部位に移動させることができる。しかし、定性的には従来手法の方が服の模様などをうまくワープさせることができている。

* [Simultaneous 3D Reconstruction for Water Surface and Underwater Scene](http://openaccess.thecvf.com/content_ECCV_2018/html/Yiming_Qian_Simultaneous_3D_Reconstruction_ECCV_2018_paper.html)
    * 水面と水中を同時に3D復元する手法の提案.複数視点の関係を導いた後, 水面上から複数視点で観測されたシーンを用いてオプティカルフローを用いて推定する.

* [Multiple-gaze geometry: Inferring novel 3D locations from gazes observed in monocular video](http://openaccess.thecvf.com/content_ECCV_2018/html/Ernesto_Brau_Stereo_gaze_Inferring_ECCV_2018_paper.html)
    * 人の視線方向を用いて何を見ているのかを理解するのを発展させるためのデータセットの提案。データセットは単眼カメラで撮られており、複数の人が約0.58m以内の物を59%の時間見ているものである。

* [Multi-Scale Context Intertwining for Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Di_Lin_Multi-Scale_Context_Intertwining_ECCV_2018_paper.html)
    * セマンティックセグメンテーションのための、異なるスケールから特徴を集約する構造を提案する。LSTMを使って、特徴マップの大小双方向に特徴を伝えるようになっていて、スーパピクセルで領域を定めている。

* [Object-centered image stitching](http://openaccess.thecvf.com/content_ECCV_2018/html/Charles_Herrmann_Object-centered_image_stitching_ECCV_2018_paper.html)
    * ２枚の画像をつなげる際に、中心にオブジェクトがあっても高品質に繋げられるように、そのような状況を想定したMRFの項を新しく導入するなどしたシステムを提案している。

* [Grassmann Pooling for Fine-Grained Visual Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Xing_Wei_Grassmann_Pooling_for_ECCV_2018_paper.html)
    * CNNの双線形特徴行列が特異値によって測定され得る局所CNN特徴要素の大きさおよび相関に敏感であり,特異ベクトルは不変であり特徴表現として適しているので,CNN特徴行列を特異ベクトルからなる正規直交行列に変換する代替のプーリング法を提案した.

* [Diagnosing Error in Temporal Action Detectors](http://openaccess.thecvf.com/content_ECCV_2018/html/Humam_Alwassel_Diagnosing_Error_in_ECCV_2018_paper.html)
    * 時間的アクション検出の性能を分析するための診断ツールを導入する。これは、単一のスカラーメトリックとは異なるもの。

* [CGIntrinsics: Better Intrinsic Image Decomposition through Physically-Based Rendering](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhengqi_Li_CGIntrinsics_Better_Intrinsic_ECCV_2018_paper.html)
    * CGデータを使って、Intrinsic decompositionのCNNを学習する。CGは物理演算ベースのレンダリングが行われた画像。

* [A Closed-form Solution to Photorealistic Image Stylization](http://openaccess.thecvf.com/content_ECCV_2018/html/Yijun_Li_A_Closed-form_Solution_ECCV_2018_paper.html) [[GitHub](https://github.com/NVIDIA/FastPhotoStyle)]
    * StyleTransfer.2段階の変形によって変換する。1段階目でContentにStyleを入れて中間的な画像に変換し, 2段階目で目立つアーティファクトを除去して写真的な出力を行う。

* [Two at Once: Enhancing Learning and Generalization Capacities via IBN-Net](http://openaccess.thecvf.com/content_ECCV_2018/html/Xingang_Pan_Two_at_Once_ECCV_2018_paper.html)
    * 3D CNN間のチャネル間の相関をモデル化するSpatio-Temporal Channel Correlation’ (STC) blockを提案.既存の3D-ResNetに適用すると2~3%ほどの精度が上昇した.また，2D CNNから3D CNNへの安定した初期値を提案するtranfer learningの利点を示した.

* [Collaborative Deep Reinforcement Learning for Multi-Object Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Liangliang_Ren_Collaborative_Deep_Reinforcement_ECCV_2018_paper.html)
    * 複数人追跡のタスクで、深層強化学習で同一のネットワークのもので、物体検出と予測を同時に行う。

* [Single Image Highlight Removal with a Sparse and Low-Rank Reflection Model](http://openaccess.thecvf.com/content_ECCV_2018/html/Jie_Guo_Single_Image_Highlight_ECCV_2018_paper.html)
    * 単一画像を入力として反射成分を分離する手法を提案.画像内のハイライト領域が疎であると仮定し、拡散色を限られた数の異なる色で良好に表現できると仮定し，除去タスクはALM法で解けるnuclear normとL1-norm最小化問題で定式化して解いた.

* [Hierarchical Relational Networks for Group Activity Recognition and Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Mostafa_Ibrahim_Hierarchical_Relational_Networks_ECCV_2018_paper.html)
    * シーン内の潜在的な相互作用を持つグラフ構造のある人々の関係表現を計算する教師付き学習パラダイムと教師なし学習パラダイムの両方で使用できるネットワークを提案した.

* [Towards Human-Level License Plate Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiafan_Zhuang_Towards_Human-Level_License_ECCV_2018_paper.html)
    * セマンティックセグメンテーションと文字認識の組み合わせで、車のナンバーの読み取りが人間よりもできるという結果を得ている。

* [Stacked Cross Attention for Image-Text Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Kuang-Huei_Lee_Stacked_Cross_Attention_ECCV_2018_paper.html)
    * 画像と説明文が与えられた時に、説明文中の単語が画像のどこに対応しているのかを検出するタスク。

* [Deep Discriminative Model for Video Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Mohammad_Tavakolian_Deep_Discriminative_Model_ECCV_2018_paper.html)
    * 適切なパラメータを初期化する学習の後, クラス識別のためにfinetuningしてAutoencoderを作成し, video-based scene classificationを作成した.

* [The Mutex Watershed: Efficient, Parameter-Free Image Partitioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Steffen_Wolf_The_Mutex_Watershed_ECCV_2018_paper.html)
    * （セマンティクではない）セグメンテーションの手法を提案。細胞壁での分割の結果を示している。

* [Monocular Depth Estimation with Affinity, Vertical Pooling, and Label Enhancement](http://openaccess.thecvf.com/content_ECCV_2018/html/YuKang_Gan_Monocular_Depth_Estimation_ECCV_2018_paper.html)
    * 単眼画像からデプス推定を行うタスクで、隣接するピクセル間の関係をモデル化するためのAffinity layerを提案するなどして最新手法を上回った。

* [Improved Structure from Motion Using Fiducial Marker Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Joseph_DeGol_Improved_Structure_from_ECCV_2018_paper.html)
    * 環境に基準マーカーが配置されている状況でのSfMの手法を提案。同時にマーカーが配置されている３Dのデータセットも公開している。

* [Temporal Modular Networks for Retrieving Complex Compositional Activities in Video](http://openaccess.thecvf.com/content_ECCV_2018/html/Bingbin_Liu_Temporal_Modular_Networks_ECCV_2018_paper.html)
    * 自然言語でクエリが与えられた時、compositional neural network layoutと対になるネットワークモジュールを組み立てるためのセマンティックな構造を抽出するモジュラーネットワークのアプローチを、ビデオ検索のタスクで行った。

* [Quantized Densely Connected U-Nets for Efficient Landmark Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhiqiang_Tang_Quantized_Densely_Connected_ECCV_2018_paper.html)
    * スタックされた複数のU-netのスキップをU-net間で密に行うことで、パラメータを効率的に利用できることを示した。姿勢推定問題などで効果を確認した。

* [Real-to-Virtual Domain Uni_x000c_cation for End-to-End Autonomous Driving](http://openaccess.thecvf.com/content_ECCV_2018/html/Luona_Yang_Real-to-Virtual_Domain_Uni_ECCV_2018_paper.html)
    * 教師なしで、end-to-endの自動運転のためのrealからvirtual絵のドメイン変換のフレームワークを提案する。

* [Beyond Part Models: Person Retrieval with Refined Part Pooling (and A Strong Convolutional Baseline)](http://openaccess.thecvf.com/content_ECCV_2018/html/Yifan_Sun_Beyond_Part_Models_ECCV_2018_paper.html)
    * 画像内の人物を検索するタスクで、複数のパーツごとに畳み込みの記述子を出力するネットワークの提案と、よく似た輪郭を出すために、パーツをリファインするプーリングを提案する。

* [Fully-Convolutional Point Networks for Large-Scale Point Clouds](http://openaccess.thecvf.com/content_ECCV_2018/html/Dario_Rethage_Fully-Convolutional_Point_Networks_ECCV_2018_paper.html)
    * 今まで問題であったPointNetなどのメモリ不足などを、入力を生の3次元点群データを入れて、内部で順序付いた構造に変換して3DConvを行うことで解消した。これによって、未処理センサデータを処理したりする必要がなくなった。点群データを最大200kポイントで処理できるE2Eな手法。

* [Real-Time Hair Rendering using Sequential Adversarial Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Lingyu_Wei_Real-Time_Hair_Rendering_ECCV_2018_paper.html)
    * 参照画像が与えられた時に、リアルタイムで、髪の毛のcolorとlightningを3Dモデルに反映する。

* [Visual Tracking via Spatially Aligned Correlation Filters Network](http://openaccess.thecvf.com/content_ECCV_2018/html/mengdan_zhang_Visual_Tracking_via_ECCV_2018_paper.html)
    * Visual trackingのタスクで、相関フィルタにおいて境界の影響とアスペクト比のバリエーションの問題に対処するためのネットワーク構造を提案した。

* [Spatio-temporal Transformer Network for Video Restoration](http://openaccess.thecvf.com/content_ECCV_2018/html/Tae_Hyun_Kim_Spatio-temporal_Transformer_Network_ECCV_2018_paper.html)
    * Spatial Transformer Networkを時間的な方向にも拡張したSpatio-temporal Transformer Networkの提案。時間的に見えていない瞬間があっても、flowを計算することができる。ビデオのデブラーや超解像に応用できる

* [Value-aware Quantization for Training and Inference of Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Eunhyeok_Park_Value-aware_Quantization_for_ECCV_2018_paper.html)
    * トレーニング時にメモリや計算量削減のために,誤差逆伝播の間に値を量子化して計算を行い，後に復元する手法を提案

* [Lambda Twist: An Accurate Fast Robust Perspective Three Point (P3P) Solver](http://openaccess.thecvf.com/content_ECCV_2018/html/Mikael_Persson_Lambda_Twist_An_ECCV_2018_paper.html)
    * ポーズ推定の3点計測で今までは全ての根を四分円をにして幾何学的に無効なものは破棄していたが,提案手法により,対角化を用いてcubicにして楕円方程式を用いて解いた.

* [Monocular Depth Estimation Using Whole Strip Masking and Reliability-Based Refinement](http://openaccess.thecvf.com/content_ECCV_2018/html/Minhyeok_Heo_Monocular_Depth_Estimation_ECCV_2018_paper.html)
    * WSMのup samplingと信頼性に基づく精密化に基づく単眼奥行き推定アルゴリズムを提案.奥行き推定CNN(WSM)を提案した後CRFを適用して推定された深度を改良した.

* [Task-Aware Image Downscaling](http://openaccess.thecvf.com/content_ECCV_2018/html/Heewon_Kim_Task-Aware_Image_Downscaling_ECCV_2018_paper.html)
    * Autoencoderを用いた画像縮小法を提案した.ダウンスケーリングとアップスケーリングを共同で学習することで,今までよりも綺麗な画像圧縮が達成できた.

* [Single Image Scene Refocusing using Conditional Adversarial Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Parikshit_Sakurikar_Single_Image_Scene_ECCV_2018_paper.html)
    * 写真を撮るとき、焦点を当てている物体以外はぼやける（写真撮るときそうなりますよね）ので、そのぼやけたところを綺麗に復元するGAN。２段階で学習しており、１段階目で入力画像をぼかすことによってシーンポイントの輝度を計算する。２段階目で、計算された放射輝度と共にinput画像を使用して、リフォーカス制御パラメータδに基づいてリフォーカス画像を生成する。

* [Model-free Consensus Maximization for Non-Rigid Shapes](http://openaccess.thecvf.com/content_ECCV_2018/html/Thomas_Probst_Model-free_Consensus_Maximization_ECCV_2018_paper.html)
    * 整数計画法を用いたモデルフリーなconsensus 最大化とBranch and Bound(BnB)を用いた最適解法の提案．Newsapper datasetやSfm Hand datasetにてshape matchingの評価をした．

* [BSN: Boundary Sensitive Network for Temporal Action Proposal Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Tianwei_Lin_BSN_Boundary_Sensitive_ECCV_2018_paper.html)
    * 動画内のアクションの始まりと終わりを検出するタスクで、局所的な時間領域でアクションがあるかを提案し、大域的にそれの確信度を評価する方法をとり、大幅にSotaを更新した。

* [Attentive Semantic Alignment with Offset-Aware Correlation Kernels](http://openaccess.thecvf.com/content_ECCV_2018/html/Paul_Hongsuck_Seo_Attentive_Semantic_Alignment_ECCV_2018_paper.html)
    * Sematic Correspondeceのタスクで、アテンションを使って、セマンティックに対応する物体同士のオフセットを算出する手法を提案した。

* [Deeply Learned Compositional Models for Human Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Wei_Tang_Deeply_Learned_Compositional_ECCV_2018_paper.html)
    * 姿勢推定のための人体の複雑な構成パターンを学習するディープニューラルネットを開発する。さらに、新たに骨格ベースのパーツ表現を提案する。

* [Real-Time MDNet](http://openaccess.thecvf.com/content_ECCV_2018/html/Ilchae_Jung_Real-Time_MDNet_ECCV_2018_paper.html)
    * トラッキングタスクのために、新しいロスを導入した。RCNNのような物体検出をベースとした発想になっている。

* [Women also Snowboard: Overcoming Bias in Captioning Models](http://openaccess.thecvf.com/content_ECCV_2018/html/Lisa_Anne_Hendricks_Women_also_Snowboard_ECCV_2018_paper.html)
    * キャプションのデータセットにはバイアスが多いという前提のもと、ジェンダーの単語が与える影響を調査した。さらに、ジェンダーに関するキャプションが含まれている時に、画像にかかるアテンションをジェンダーに関わらず正確に当てるための手法をロスを工夫することによって提案。

* [Progressive Structure from Motion](http://openaccess.thecvf.com/content_ECCV_2018/html/Alex_Locher_Progressive_Structure_from_ECCV_2018_paper.html)
    * SfMのタスクで、入力される画像の順番に依存せず、また、事前に画像のつながりについての大域的な知識を必要しない手法を提案する。

* [Occlusion-aware R-CNN: Detecting Pedestrians in a Crowd](http://openaccess.thecvf.com/content_ECCV_2018/html/Shifeng_Zhang_Occlusion-aware_R-CNN_Detecting_ECCV_2018_paper.html)
    * 歩行者検出ではオクルージョンが発生するとして、体のパーツごとにオクルージョンが発生しているかを算出するプーリングを提案している。

* [Affinity Derivation and Graph Merge for Instance Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yiding_Liu_Affinity_Derivation_and_ECCV_2018_paper.html)
    * セマンティックセグメンテーションのブランチとピクセル間の親和性をマップで出力するブランチの二つからグラフマージして、インスタンスセグメンテーションを行う手法の提案。

* [Second-order Democratic Aggregation](http://openaccess.thecvf.com/content_ECCV_2018/html/Tsung-Yu_Lin_Second-order_Democratic_Aggregation_ECCV_2018_paper.html)
    * CNNから二次集合の特徴を抽出する研究。

* [Improving Sequential Determinantal Point Processes for Supervised Video Summarization](http://openaccess.thecvf.com/content_ECCV_2018/html/Aidean_Sharghi_Improving_Sequential_Determinantal_ECCV_2018_paper.html)
    * 結果として得られるsequential modelが予想される要約の長さについて事前知識を受け入れられるようにする確率的モジュールGDPPを提案.今までのSeqDPPに比べ,ロスやexposure biasを改善し効率的に学習できるように設計し,精度はかなり伸びた.

* [Seeing Deeply and Bidirectionally: A Deep Learning Approach for Single Image Reflection Removal](http://openaccess.thecvf.com/content_ECCV_2018/html/Jie_Yang_Seeing_Deeply_and_ECCV_2018_paper.html)
    * 写真に写り込んでいる、ガラスの反射を取り除くためのGANベースの手法を提案。背景画像の生成、反射画像の生成、さらに背景画像の生成とそれまでに得られた画像を使いながら生成するカスケード構造のネットワーク。良い結果が得られている。

* [Specular-to-Diffuse Translation for Multi-View Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Shihao_Wu_Specular-to-Diffuse_Translation_for_ECCV_2018_paper.html)
    * GANにより多視点の物体のspecular画像からdiffuse画像を生成するS2Dnet(Specular-to-Diffuse network)の提案．入力は多視点の光沢のあるシーンの画像のみで，マスクやカメラ，ライトの情報は必要ではない．

* [SEAL: A Framework Towards Simultaneous Edge Alignment and Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhiding_Yu_SEAL_A_Framework_ECCV_2018_paper.html)
    * エッジの補正と検出の学習を同時に行うフレームワークの提案。物体の境界のマップを出力することができる。境界のラベルがNoisyであっても学習できることが強み。

* [Question Type Guided Attention in Visual Question Answering](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Shi_Question_Type_Guided_ECCV_2018_paper.html)
    * Quesution Type-guided Attentiion(QTA)というVQAの手法の提案．QTAでは疑問文(テキスト)の情報を利用することで，ResNetとFaster R-CNNネットワークから得られたボトムアップ，トップダウンの視覚的特徴をバランスさせる．

* [Neural Procedural Reconstruction for Residential Buildings](http://openaccess.thecvf.com/content_ECCV_2018/html/Huayi_Zeng_Neural_Procedural_Reconstruction_ECCV_2018_paper.html)
    * Neural Procedural Reconstructionという新しい3D再構成手法を提案.既存の方法のほとんどは、低レベルのジオメトリ解析を使用して原始的な構造を抽出しているが,提案手法では,建物構造全体のグローバル分析を行い,不完全でsparceな入力データからも再構築が可能であることを示した.

* [Self-Calibration of Cameras with Euclidean Image Plane in Case of Two Views and Known Relative Rotation Angle](http://openaccess.thecvf.com/content_ECCV_2018/html/Martyushev_Self-Calibration_of_Cameras_ECCV_2018_paper.html)
    * focal lengthとprincipal point coordinatesの３つの内部パラメータが不明でしかし固定であるときに、Euclidean image planeを使ってカメラのキャリブレーションを行うアルゴリズムの提案。

* [Towards Optimal Deep Hashing via Policy Gradient](http://openaccess.thecvf.com/content_ECCV_2018/html/Xin_Yuan_Towards_Optimal_Deep_ECCV_2018_paper.html)
    * スケール可能な画像検索のために、policy gradientを経由してバイナリコードを効率よく学習するためのrelaxation-freeな方法を提案する。

* [Piggyback: Adapting a Single Network to Multiple Tasks by Learning to Mask Weights](http://openaccess.thecvf.com/content_ECCV_2018/html/Arun_Mallya_Piggyback_Adapting_a_ECCV_2018_paper.html) [[GitHub](https://github.com/arunmallya/piggyback)]
    * 既に学習されたタスクの性能に影響を与えることなく単一のDNNを複数のタスクに適応させる方法の提案．

* [Generating 3D Faces using Convolutional Mesh Autoencoders](http://openaccess.thecvf.com/content_ECCV_2018/html/Anurag_Ranjan_Generating_3D_Faces_ECCV_2018_paper.html)
    * 顔のメッシュデータを（少ないパラメータで）操作するために、spectral convolutionを使って、オートエンコーダーを学習する方法を提案した。

* [ICNet for Real-Time Semantic Segmentation on High-Resolution Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Hengshuang_Zhao_ICNet_for_Real-Time_ECCV_2018_paper.html)
    * リアルタイムでsemantic segmentationができるICNetの提案.1024x2048の高解像度の画像に対して30fpsでsemantic segmentationができる．

* [Memory Aware Synapses: Learning what (not) to forget](http://openaccess.thecvf.com/content_ECCV_2018/html/Rahaf_Aljundi_Memory_Aware_Synapses_ECCV_2018_paper.html)
    * モデルは記憶できるものは限られており学習すべきものは無制限の新しい情報なことをを考慮して、知識を選択的に保存または消去しなければならないという思考から,Memory Aware Synapsesという手法を提案した.ある説明変数が目的変数にどれくらい影響を及ぼすかのparametersの重要性を計算し,前のタスクで大事であったparameterが上書きされるのを防いだ.結果的に良いparameterだけ学習していく.

* [Deep Texture and Structure Aware Filtering Network for Image Smoothing](http://openaccess.thecvf.com/content_ECCV_2018/html/Kaiyue_Lu_Deep_Texture_and_ECCV_2018_paper.html)
    * テクスチャの特徴(模様など)を抽出するTexture Prediction Nwtwork(TPN)と物体の境界線などを抽出するStructure Prediction Network(SPN)の二つを組み合わせてTexture and Structure Aware Filtering Network(TSAFN)を作る．TPNにより得られた模様などはブラーがかかり，SPNによって得られた境界線などは保存される．

* [Linear RGB-D SLAM for Planar Environments](http://openaccess.thecvf.com/content_ECCV_2018/html/Pyojin_Kim_Linear_RGB-D_SLAM_ECCV_2018_paper.html)
    * 今までのSLAMでは高次元の非線形最適化問題であったため収束する保証はなかったので,線形カルマンフィルタを用いて新しいSLAM方法の提案.回転が主な非線形の理由だったので,マンハッタンワールドの構造規則性を用いて線形にした.

* [DeepJDOT: Deep Joint distribution optimal transport for unsupervised domain adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Bharath_Bhushan_Damodaran_DeepJDOT_Deep_Joint_ECCV_2018_paper.html)
    * optimal transportに基づいた教師なしのDAのためのDeepJDOTモデルを提案した。ソース分布とターゲット分布の共通の潜在空間を学習することを目的としており、optimal tranportによる特徴/ラベル領域分布の不一致を最小化することで達成した。結果の精度もADDAと比べてかなり上がっている。ネットワークは論文中の図を参照したが良い

* [W-TALC: Weakly-supervised Temporal Activity Localization and Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Sujoy_Paul_W-TALC_Weakly-supervised_Temporal_ECCV_2018_paper.html)
    * video levelのweak labelで動画の分類を行った。同じラベルの動画中の動作は同じ特徴量を持ち、他のものは他の特徴量をもつものとするCo-Activity Similarity Lossを提案した。そのロスでネットワークに重みをつけた後に、分類をして動画分類を行った。

* [Unsupervised Video Object Segmentation with Motion-based Bilateral Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Siyang_Li_Unsupervised_Video_Object_ECCV_2018_paper.html)
    * video object segmentationタスクで，静的で意味が類似しているオブジェクトからの誤検出を減らすために，motionとforeground, backgroundが直接紐づくようなネットワークを提案.複数のデータセットでSoTA達成.

* [Disentangling Factors of Variation with Cycle-Consistent Variational Auto-Encoders](http://openaccess.thecvf.com/content_ECCV_2018/html/Ananya_Harsh_Jha_Disentangling_Factors_of_ECCV_2018_paper.html) [[GitHub](https://github.com/ananyahjha93/cycle-consistent-vae)]
    * 潜在変数空間を２つの部分空間に分解するために、cycle-consistencyをVAEに利用したネットワークを提案。従来手法と違って、adversarial trainingではない。

* [Mancs: A Multi-task Attentional Network with Curriculum Sampling for Person Re-identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Cheng_Wang_Mancs_A_Multi-task_ECCV_2018_paper.html)
    * 人物再同定のネットワークにアテンション機構を導入し、より安定する人物特徴をランキングロスの学習で獲得するための新しいカリキュラムサンプリングの方法を提案した。

* [Multi-view to Novel view: Synthesizing Views via Self-Learned Confidence](http://openaccess.thecvf.com/content_ECCV_2018/html/Shao-Hua_Sun_Multi-view_to_Novel_ECCV_2018_paper.html)
    * 複数の視点のCG画像から新しい視点の画像を生成する。元の画像に写っている箇所を示すための、コンフィデンスマップも出力するようにした。

* [Part-Activated Deep Reinforcement Learning for Action Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Lei_Chen_Part-Activated_Deep_Reinforcement_ECCV_2018_paper.html)
    * 強化学習のフレームワークの中で、人体の構造を算出することで、行動予測を行う手法の提案。

* [Online Dictionary Learning for Approximate Archetypal Analysis](http://openaccess.thecvf.com/content_ECCV_2018/html/Jieru_Mei_Online_Dictionary_Learning_ECCV_2018_paper.html)
    * 大きなデータセットに有効なArchetype Analysisのためのオンライン辞書学習のアプローチを提案する。

* [Estimating Depth from RGB and Sparse Sensing](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhao_Chen_Estimating_Depth_from_ECCV_2018_paper.html)
    * RGB画像とsparseなdepth mapからdenseなdepth mapをdeep(conv NN)により予測する．

* [Unsupervised Domain Adaptation for Semantic Segmentation via Class-Balanced Self-Training](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Zou_Unsupervised_Domain_Adaptation_ECCV_2018_paper.html)
    * 自己学習(self-training)を組み込み、CNNでセマンティクセグメンテーションのための教師なしドメイン適用を行う。大きなクラスラベルに擬似ラベルが偏らないようにクラスのバランスをとる工夫も含まれている。

* [Zoom-Net: Mining Deep Feature Interactions for Visual Relationship Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Guojun_Yin_Zoom-Net_Mining_Deep_ECCV_2018_paper.html)
    * Visual Relationship Recognitionを解くためのネットワークを提案。特に、空間的な位置を考慮したコンテキストの特徴表現を学習するためのプーリング方法を提案

* [Joint Camera Spectral Sensitivity Selection and Hyperspectral Image Recovery](http://openaccess.thecvf.com/content_ECCV_2018/html/Ying_Fu_Joint_Camera_Spectral_ECCV_2018_paper.html)
    * 候補のデータセットから最適なCamera Spectral Sensitivityを選択することと、アウルゴリズムで選択されたカメラで捉えられた単一のRGB画像からHSIを復元するためのマッッピングを学習することを同時に行えるCNNベースの手法を提案する。

* [Compositing-aware Image Search](http://openaccess.thecvf.com/content_ECCV_2018/html/Hengshuang_Zhao_Compositing-aware_Image_Search_ECCV_2018_paper.html)
    * 背景のコンテキストに合う前景を検索する手法を提案。Conv netで前景と背景をそれぞれ特徴抽出し、Triplet lossによって特徴空間に配置をしている。

* [Zero-Shot Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Ankan_Bansal_Zero-Shot_Object_Detection_ECCV_2018_paper.html)
    * あるクラスに対して全く画像データが与えられない状況下に対する物体検出の手法としてzero-shot object detectionを提案。手法としてはクラスembeddingのconvex combinationとzero-shot image classificationの応用でラベルembeddingを拡張して、直接、クラスembeddingの空間に対するregionのマッピングを学習する。この論文では評価として、新たにデータセット（Fashion-ZSD, Pascal-ZSD）を用意している。

* [ForestHash: Semantic Hashing With Shallow Random Forests and Tiny Convolutional Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Qiang_Qiu_ForestHash_Semantic_Hashing_ECCV_2018_paper.html)
    * セマンティックハッシングの問題を行うために比較的浅いランダムフォレスト(RF)や小さな畳み込みネット(CNN)を用いる。CNNによるエンベディング特徴をRFに入力することで効果的にハッシングを行う方法を提案した。

* [ML-LocNet: Improving Object Localization with Multi-view Learning Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaopeng_Zhang_ML-LocNet_Improving_Object_ECCV_2018_paper.html)
    * 複数視点からの見えを分離・統合して学習を進めるMulti-view Co-training Algorithmを提案。最初は特徴表現を学習するために複数視点からの見えでそれぞれ学習して統合、次に視点ごとに協調して学習することで位置決めの精度を向上。同一物体を異なるビューポイントから学習することでより効果的に物体検出する方法を確立した。

* [MPLP++: Fast, Parallel Dual Block-Coordinate Ascent for Dense Graphical Models](http://openaccess.thecvf.com/content_ECCV_2018/html/Siddharth_Tourani_MPLP_Fast_Parallel_ECCV_2018_paper.html)
    * デンスな離散グラフモデルはCVやバイオ画像処理にて重要である。MAP-solverを提案する。Max Product Linear Programming (MPLP)アルゴリズムを用いることで性能のみでなく、並列化にも有利なため高速な処理ができるようになった。6D Object Recognitionに適用することが可能である。

* [A Zero-Shot Framework for Sketch based Image Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Sasikiran_Yelamarthi_A_Zero-Shot_Framework_ECCV_2018_paper.html)
    * スケッチ画像からの自然画像検索の問題にZero-shot学習を用いる。SoTAとなったモデルはAdversarial AutoEncoder（AAE）やVariational AutoEncoder（VAE）を使ったモデルであった。

* [In the Eye of Beholder: Joint Learning of Gaze and Actions in First Person Vision](http://openaccess.thecvf.com/content_ECCV_2018/html/Yin_Li_In_the_Eye_ECCV_2018_paper.html)
    * headwornカメラで撮影された動画から，人が何をしているのかとどこを見ているのかを推定するための新しいディープモデルを提案．standard EGTEA datasetでSoTAを達成．

* [SAN: Learning Relationship between Convolutional Features for Multi-Scale Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Kim_SAN_Learning_Relationship_ECCV_2018_paper.html)
    * CNNベースの物体検出法は，スケールに応じてアクティブなチャンネルが完全に異なる．これは，分類器にとって学習を難しくしている．そこで著者らは，Scale Aware Network（SAN) を提案した．これは，異なるスケールにおいても不変な部分空間の畳み込み特徴をマップする．これによりCNNベールの検出手法はスケールの変化によりロバストになると主張．空間情報を用いないでチャンネル間の関係を考慮した，ユニークな学習手法も構築した．  
    提案手法をVOC PASCAl とMS COCOデータセットを用いて評価した.

* [A Systematic DNN Weight Pruning Framework using Alternating Direction Method of Multipliers](http://openaccess.thecvf.com/content_ECCV_2018/html/Tianyun_Zhang_A_Systematic_DNN_ECCV_2018_paper.html)
    * DNNのシステマティックなweight pruningフレームワーク (ADMM) を提案．DNNのweight pruning問題を非凸最適化問題として定式化した後，ADMMを適応．MNISTでLeNet-5を学習したところ，accuracyが悪くならずに71.2x weight reductionを達成．

* [Iterative Crowd Counting](http://openaccess.thecvf.com/content_ECCV_2018/html/Viresh_Ranjan_Iterative_Crowd_Counting_ECCV_2018_paper.html)
    * CNNを用いた密度推定により、群衆のカウント問題に取り組んだ。この問題に対して２つのブランチネットワークを構築し、高解像な密度マップを生成する。最初のブランチでは低解像の密度マップを構築、次のブランチでは低解像マップから結果の出力や高解像のマップ生成を行う。両者の出力から総合的に結果を出力する。

* [A Dataset for Lane Instance Segmentation in Urban Environments](http://openaccess.thecvf.com/content_ECCV_2018/html/Brook_Roberts_A_Dataset_for_ECCV_2018_paper.html)
    * lane instanceのセマンティックセグメンテーションを半自動的に行う手法を提案．これにより一画像あたり5秒でセマンティックセグメンテーションを行うことができる．ただし動画限定．

* [Out-of-Distribution Detection Using an Ensemble of Self Supervised Leave-out Classifiers](http://openaccess.thecvf.com/content_ECCV_2018/html/Apoorv_Vyas_Out-of-Distribution_Detection_Using_ECCV_2018_paper.html)
    * メジャーな分布から外れたout-of-distribution (OOD)を検出して、self-supervised learningにより特徴表現学習を実行する。アンサンブル識別器によりOODを検出、in-distribution（ID）のサンプルとの誤差を計算する誤差関数も新規に定義。

* [Penalizing Top Performers: Conservative Loss for Semantic Segmentation Adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xinge_Zhu_Penalizing_Top_Performers_ECCV_2018_paper.html)
    * 訓練データとして実画像の代わりに人口データを用いると，ドメインシフトによるパフォーマンスの低下を招く．そこで，ドメイン適応のために有効なloss関数を新手に提案した．GTAVやSynthiaで学習し，Cityscapesでテストしたところ，mIoUが向上した．

* [Compound Memory Networks for Few-shot Video Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Linchao_Zhu_Compound_Memory_Networks_ECCV_2018_paper.html)
    * Few-shot video classificationのタスクにおいて、新たにKey-value Networkから派生したCompound Memory Networkを提案。

* [Straight to the Facts: Learning Knowledge Base Retrieval for Factual Visual Question Answering](http://openaccess.thecvf.com/content_ECCV_2018/html/Medhini_Gulganjalli_Narasimhan_Straight_to_the_ECCV_2018_paper.html)
    * Facts, question-image pairsをco-embeddingすることをベースとしたKnowledge-based VQAの新たな手法を提案した．画像からセマンティックコンセプトの検出，画像特徴抽出を行い，質問文からsupport factの検出及び特徴抽出を行う．提案手法が答えを予測する同時に，supporting factsも同時に検出する．現在の新たなデータセットKnowledge-based なVQAデータセットFVQAにおいてSOTAな精度を達成した．

* [Interpretable Basis Decomposition for Visual Explanation](http://openaccess.thecvf.com/content_ECCV_2018/html/Antonio_Torralba_Interpretable_Basis_Decomposition_ECCV_2018_paper.html)
    * Inerpretable Basis Decompositionという，分類タスク用のネットワークのためのvisual explanationフレームワークを新たに提案．入力画像のneural activationを解釈可能な成分にぶんかいするとのこと．

* [How Local is the Local Diversity? Reinforcing Sequential Determinantal Point Processes with Dynamic Ground Sets for Supervised Video Summarization](http://openaccess.thecvf.com/content_ECCV_2018/html/Yandong_Li_How_Local_is_ECCV_2018_paper.html)
    * 長い動画に対して、局所的な重要な部分を取り出しvideo summarizationを行うことの重要性を提案。その上で強化学習をdynamic seqDDPに対して適応することで、精度を上げた。

* [Dividing and Aggregating Network for Multi-view Action Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Dongang_Wang_Dividing_and_Aggregating_ECCV_2018_paper.html)
    * 多視点行動認識のため，Dividing and Aggregating Network (DA-Net) を提案．このネットワークでは，低階層では視点に依存しない特徴を学習され，高階層では各視点固有の特徴が学習される．

* [Shape Reconstruction Using Volume Sweeping and Learned Photoconsistency](http://openaccess.thecvf.com/content_ECCV_2018/html/Vincent_Leroy_Shape_Reconstruction_Using_ECCV_2018_paper.html)
    * 多視点RGB画像からの３次元形状復元に取り組んだ論文．学習ベースの手法が，形状復元の精度とロバスト性の向上に効果的かどうかを調べた．既存手法では難しい，複雑な表面の復元についてもターゲットとしている．

* [RT-GENE: Real-Time Eye Gaze Estimation in Natural Environments](http://openaccess.thecvf.com/content_ECCV_2018/html/Tobias_Fischer_RT-GENE_Real-Time_Eye_ECCV_2018_paper.html)
    * 頭の姿勢(位置)からground truth annotationを作るのではなく、頭とさらにeye tracking glassesを利用することによって自動的にアノテーションすることができる手法を提案。この手法によって集められたデータセットを提案した。

* [Pairwise Body-Part Attention for Recognizing Human-Object Interactions](http://openaccess.thecvf.com/content_ECCV_2018/html/Haoshu_Fang_Pairwise_Body-Part_Attention_ECCV_2018_paper.html)
    * human-object interactions recognitionタスクにおいて体のパーツごとにattentionを付けるべきということを主張した論文．そのために，新たにpairwiseなbody-part attention modelを提案した．

* [Motion Feature Network: Fixed Motion Filter for Action Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Myunggi_Lee_Motion_Feature_Network_ECCV_2018_paper.html)
    * 行動認識を行うための手法として新たにMFNetとmotion blockを提案．motion blockによりRGB画像のみでフレームのspatio-temporal relationshipを獲得できるとのこと．また，motion blockは既存手法にも取り付けられる．JesterとSomething-Somethingデータセットで実験を行ったところ，Top-1 acc.がベースラインから8%程度向上．

* [Reverse Attention for Salient Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Shuhan_Chen_Reverse_Attention_for_ECCV_2018_paper.html)
    * salient object detectionにおけるdeep networkのコンパクト化を提案した．side-output residual featureを学習するための残差学習に初めて着手した．また，reverse attentionの提案も行った．6つのデータセットで実験したところSoTA手法より優れていた．

* [Dynamic Sampling Convolutional Neural Networks\n](#N/A)
    * position-specificカーネルを現在のポジションだけでなく複数のサンプルされた近傍領域からも学習を行うことで受容野を拡大することに成功したという論文．PASCAL VOC 2012データセットを用いて物体検出実験を行ったところmAPが81.7%であった．

* [DDRNet: Depth Map Denoising and Refinement for Consumer Depth Cameras Using Cascaded CNNs](http://openaccess.thecvf.com/content_ECCV_2018/html/Shi_Yan_DDRNet_Depth_Map_ECCV_2018_paper.html)
    * コンシューマー向け距離センサによるデノイジングとリファインメントを実施する。Cascaded CNNによりどうタスクを実行した。Unsupervised Lossも考案して同ネットワークを最適化。

* [Stereo Computation for a Single Mixture Image](http://openaccess.thecvf.com/content_ECCV_2018/html/Yiran_Zhong_Stereo_Computation_for_ECCV_2018_paper.html)
    * 単一混合画像から左ステレオ画像と右ステレオ画像を計算する問題を新たに提案．

* [Volumetric performance capture from minimal camera viewpoints](http://openaccess.thecvf.com/content_ECCV_2018/html/Andrew_Gilbert_Volumetric_performance_capture_ECCV_2018_paper.html)
    * CNNのautoencoderを利用して人間の動作のvolumetric reconstractionを少数のカメラで可能にするモデルを提案。

* [Liquid Pouring Monitoring via Rich Sensory Inputs](http://openaccess.thecvf.com/content_ECCV_2018/html/Tz-Ying_Wu_Liquid_Pouring_Monitoring_ECCV_2018_paper.html)
    * 液体を注ぐ動作のモニタリングに関して、よりrobustなシステムのために新たにタスクを２つで提案。新たに提案したタスクとして容器の最初の状態、そして手の3Dの軌道の１ステップ先の予測。

* [Move Forward and Tell: A Progressive Generator of Video Descriptions](http://openaccess.thecvf.com/content_ECCV_2018/html/Yilei_Xiong_Move_Forward_and_ECCV_2018_paper.html)
    * LSTMを通して動画から重要な部分をクリップとして複数取り出していき、各クリップについてCaptioningを行うことで、全体的に一貫性のあるパラグラフを生成するフレームワークの提案

* [DYAN: A Dynamical Atoms-Based Network for Video Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Wenqian_Liu_DYAN_A_Dynamical_ECCV_2018_paper.html)
    * フレーム推定を行うためのネットワークとして新たにDYANを提案．このネットワークは，既存手法に比べパラメータ数が少なく，トレーニングも楽に行うことができる．

* [Deep Structure Inference Network for Facial Action Unit Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Ciprian_Corneanu_Deep_Structure_Inference_ECCV_2018_paper.html)
    * action unit recognitionはpatchとmulti-labelが重要になるという主張から、Deep Structured Inference Networkという、patchとmulti-labelに対応するAction unit recognitionのためのモデルを提案。　これにより、既存手法と比較して、BP4Dで5.4%、DISFAで8.2%精度が上昇した。

* [Physical Primitive Decomposition](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhijian_Liu_Physical_Primitive_Decomposition_ECCV_2018_paper.html)
    * 物理モデルを分解して理解するための研究である。具体的には物体のボクセル、画像特徴、軌跡をそれぞれエンコーディングして物体の操作を学習・推論する。材質やアフォーダンスを同時に理解する方法を提案し、例えば画像からハンマーは鉄と木から構成されるということを理解。

* [Boosted Attention: Leveraging Human Attention for Image Captioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Shi_Chen_Boosted_Attention_Leveraging_ECCV_2018_paper.html)
    * タスク特化のアテンションやstimulus-basedなアテンションを組み合わせるBoosted Attentionを提案して画像キャプションに適用した。

* [Is Robustness the Cost of Accuracy? -- Lessons Learned from 18 Deep Image Classifiers](http://openaccess.thecvf.com/content_ECCV_2018/html/Dong_Su_Is_Robustness_the_ECCV_2018_paper.html)
    * 様々なモデルに対して，精度のみでなくロバスト性についても評価した論文．

* [Dynamic Multimodal Instance Segmentation guided by natural language queries](http://openaccess.thecvf.com/content_ECCV_2018/html/Edgar_Margffoy-Tuay_Dynamic_Multimodal_Instance_ECCV_2018_paper.html)
    * 画像と文章の入力からセマンティックセグメンテーションを実施する。VQAの出力がセグメンテーションという理解。

* [Hierarchy of Alternating Specialists for Scene Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Hyo_Jin_Kim_Hierarchy_of_Alternating_ECCV_2018_paper.html)
    * シーン認識において，キッチンとバーのような似ているが異なるクラスの認識精度を高めるため，写っている物体の関係を考慮する手法を提案．

* [SwapNet: Garment Transfer in Single View Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Amit_Raj_SwapNet_Garment_Transfer_ECCV_2018_paper.html)
    * 画像から画像への変換のみで衣類の変換を行うためのネットワークを提案．弱教師あり学習による学習アプローチについても紹介されている．

* [What do I Annotate Next? An Empirical Study of Active Learning for Action Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Fabian_Caba_What_do_I_ECCV_2018_paper.html)
    * 一時的なactionの局在化のためのactive learning frameworkの提案。これを行うために、様々なaction selection functionを持ちいてパフォーマンスを比較した。

* [Combining 3D Model Contour Energy and Keypoints for Object Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Bogdan_Bugaev_Combining_3D_Model_ECCV_2018_paper.html)
    * Model Contour energy とkeypointsの特性を合わせた３Dトラッキングの手法の提案

* [AGIL: Learning Attention from Human for Visuomotor Tasks](http://openaccess.thecvf.com/content_ECCV_2018/html/Ruohan_Zhang_AGIL_Learning_Attention_ECCV_2018_paper.html)
    * あるタスクにおける人の視線の動きをもとに、visual attention modelを生成し、Imitation Learningと組み合わせることにより、従来のImitation Learningより精度が高いAttention Guided Imitation Learning frameworkを提案。新しいデータセットを作成。

* [PersonLab: Person Pose Estimation and Instance Segmentation with a Bottom-Up, Part-Based, Geometric Embedding Model](http://openaccess.thecvf.com/content_ECCV_2018/html/George_Papandreou_PersonLab_Person_Pose_ECCV_2018_paper.html)
    * 

* [Accelerating Dynamic Programs via Nested Benders Decomposition with Application to Multi-Person Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Shaofei_Wang_Accelerating_Dynamic_Programs_ECCV_2018_paper.html)
    * 

* [Separating Reflection and Transmission Images in the Wild](http://openaccess.thecvf.com/content_ECCV_2018/html/Patrick_Wieschollek_Separating_Reflection_and_ECCV_2018_paper.html)
    * deep learningを用いて画像と光の反射・伝搬？（transmit)成分の分離を行う．詳しく読んでませんがアブストラクトを見た感じすごそうなので1.

* [Point-to-Point Regression PointNet for 3D Hand Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Liuhao_Ge_Point-to-Point_Regression_PointNet_ECCV_2018_paper.html)
    * point cloudベースで手の三次元姿勢を推定するpoint to point regression pointnetを提案。CVPR2018で発表したHand PointNetの続編。

* [Summarizing First-Person Videos from Third Persons' Points of View](http://openaccess.thecvf.com/content_ECCV_2018/html/HSUAN-I_HO_Summarizing_First-Person_Videos_ECCV_2018_paper.html)
    * 

* [Learning Category-Specific Mesh Reconstruction from Image Collections](http://openaccess.thecvf.com/content_ECCV_2018/html/Angjoo_Kanazawa_Learning_Category-Specific_Mesh_ECCV_2018_paper.html)
    * 単一画像からオブジェクトの3D形状とカメラ位置，テクスチャを復元する手法を提案．形状は平均形状とインスタンスごとの形状の２つで表現される．提案する3D推定メカニズムは3Dのground truthを必要としないといった特徴がある．

* [StereoNet: Guided Hierarchical Refinement for Real-Time Edge-Aware Depth Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Sameh_Khamis_StereoNet_Guided_Hierarchical_ECCV_2018_paper.html)
    * 

* [Visual Question Answering as a Meta Learning Task](http://openaccess.thecvf.com/content_ECCV_2018/html/Damien_Teney_Visual_Question_Answering_ECCV_2018_paper.html)
    * meta learningをVAQに対して適応する手法の提案。テストの際にも学習を行うため、scalabilityが上がった。

* [SRFeat: Single Image Super Resolution with Feature Discrimination](http://openaccess.thecvf.com/content_ECCV_2018/html/Seong-Jin_Park_SRFeat_Single_Image_ECCV_2018_paper.html)
    * 従来のGANベースの単一画像超解像 (SISR) 手法は高周波ノイズを含んでしまう．そこで，これを解決しさらにリアルな結果を得るため，新たにGANベースのSISR手法を提案した．このGANはdiscriminatorをもう一つもつをいう特徴がある．PSNRとSSIMを用いて提案手法を評価したところ，SoTAな性能を確認することができた．

* [Deep Factorised Inverse-Sketching](http://openaccess.thecvf.com/content_ECCV_2018/html/Kaiyue_Pang_Deep_Factorised_Inverse-Sketching_ECCV_2018_paper.html)
    * 写真などから、スケッチ画像を生成するのではなく、スケッチを書くプロセスを逆を行うことによって、スケッチから、元画像の等高線を復元するフレームワークの提案。

* [Multimodal image alignment through a multiscale chain of neural networks with application to remote sensing](http://openaccess.thecvf.com/content_ECCV_2018/html/Armand_Zampieri_Multimodal_image_alignment_ECCV_2018_paper.html)
    * Non-rigidのimage registrationにおける、Scale-specific Neural Networkの提案。最終それぞれのスケールを最後の結果として一度に出力するため、効率的。

* [Improving Deep Visual Representation for Person Re-identification by Global and Local Image-language Association](http://openaccess.thecvf.com/content_ECCV_2018/html/Dapeng_Chen_Improving_Deep_Visual_ECCV_2018_paper.html)
    * 自然言語の記述（description) に視覚的な特徴量を補助として追加して学習を行う方法を提案．他の補助情報を比べ，言語がよりコンパクトに記述できたとのこと．他の補助情報を用いることなくSoTA達成．

* [Robust Optical Flow Estimation in Rainy Scenes](http://openaccess.thecvf.com/content_ECCV_2018/html/Ruoteng_Li_Robust_Optical_Flow_ECCV_2018_paper.html)
    * 雨天時におけるオプティカルフロー推定手法を提案．  
    Residue channel (single channel) とcolored-residue imageという雨に影響を受けない２つの画像を求めることによりオプティカルフローを求めるとのこと．

* [Image Generation from Sketch Constraint Using Contextual GAN](http://openaccess.thecvf.com/content_ECCV_2018/html/Yongyi_Lu_Image_Generation_from_ECCV_2018_paper.html)
    * 既存のエッジ画像からの画像生成手法は，入力されたエッジ画像の影響を受け過ぎるため，入力が悪い（途切れているなど）とリアルな画像が生成できないという問題がある．この研究では，きれいなエッジ画像と実画像の同時分布を学習することにより，入力が多少悪くても比較的リアルな画像が出力できるようにした．

* [Accurate Scene Text Detection through Border Semantics Awareness and Bootstrapping](http://openaccess.thecvf.com/content_ECCV_2018/html/Chuhui_Xue_Accurate_Scene_Text_ECCV_2018_paper.html)
    * 画像内のテキストを検出するためのデータ拡張手法を提案．トレーニングデータにおける文字領域の一部を，インペインティングにより背景に変換することでデータを拡張した．MSRA-TD500等のデータセットで実験したところF値がよくなった．

* [CNN-PS: CNN-based Photometric Stereo for General Non-Convex Surfaces](http://openaccess.thecvf.com/content_ECCV_2018/html/Ikehata_CNN-PS_CNN-based_Photometric_ECCV_2018_paper.html)
    * 

* [Making Deep Heatmaps Robust to Partial Occlusions for 3D Object Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Markus_Oberweger_Making_Deep_Heatmaps_ECCV_2018_paper.html)
    * 

* [Recognition in Terra Incognita](http://openaccess.thecvf.com/content_ECCV_2018/html/Beery_Recognition_in_Terra_ECCV_2018_paper.html)
    * 新しい（未知な）環境の認識度合いを計測するためのデータセットを提案．データセットの各画像は，動物の集団を20個のカメラにより撮影したものである．カメラは固定されているため人間バイアスはかからないとのこと．取り組む課題は少ないロケーションの認識を学習することと，新たなロケーションにおける動物の検出と分類を一般化することである．トレーニングデータに含まれるロケーションではSoTAであったが，新たなロケーションではうまくいかなかった．

* [Super-Resolution and Sparse View CT Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Guangming_Zang_Super-Resolution_and_Sparse_ECCV_2018_paper.html)
    * ロバストな3DCT再構築のためのフレームワークを提案．そのために，3Dテンソルを事前に考案した．

* [Modeling Visual Context is Key to Augmenting Object Detection Datasets](http://openaccess.thecvf.com/content_ECCV_2018/html/NIKITA_DVORNIK_Modeling_Visual_Context_ECCV_2018_paper.html)
    * 物体検出のための新しいdata augmentationの手法の提案。visual context modelを用いて、物体を新たに配置するのに適した場所を生成、それに合わせて、物体（インスタンス）のスケールを変更してオリジナル画像に対してペーストを行う。この新しくできた画像を用いて、学習を行う。このaugmentationにより、精度が向上したクラスがいくつ増える結果となった。（全てではない）

* [Occlusions, Motion and Depth Boundaries with a Generic Network for Optical Flow, Disparity, or Scene Flow Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Eddy_Ilg_Occlusions_Motion_and_ECCV_2018_paper.html)
    * 視差やオプティカルフローを併用してオクルージョン領域を推定する効率的な学習ベースの手法を提案．オクルージョンとモーション境界の推定でSoTAを達成．

* [Unsupervised Domain Adaptation for 3D Keypoint Estimation via View Consistency](http://openaccess.thecvf.com/content_ECCV_2018/html/Xingyi_Zhou_Unsupervised_Domain_Adaptation_ECCV_2018_paper.html)
    * 

* [Improving DNN Robustness to Adversarial Attacks using Jacobian Regularization](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Jakubovitz_Improving_DNN_Robustness_ECCV_2018_paper.html)
    * adversarial attackに対するロバスト性を向上させるための新しいアプローチを理論的に導出．ネットワークのヤコビアンのフロベニウスノルムを用いて正規化するとのこと．提案手法はトレーニングの後処理として適用される．経験的には精度をあまり下げることなくロバスト性が向上できたとのこと．

* [A Framework for Evaluating 6-DOF Object Trackers](http://openaccess.thecvf.com/content_ECCV_2018/html/Mathieu_Garon_A_Framework_for_ECCV_2018_paper.html)
    * リアルなデータとさらにより難易度が高いシナリオにおける6-DOFに対するデータセットの提案。

* [Self-Supervised Relative Depth Learning for Urban Scene Understanding](http://openaccess.thecvf.com/content_ECCV_2018/html/Huaizu_Jiang_Self-Supervised_Relative_Depth_ECCV_2018_paper.html)
    * 

* [Actor-centric Relation Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Chen_Sun_Actor-centric_Relation_Network_ECCV_2018_paper.html)
    * Action detectionに関するモデルの提案。ActionとSceneの時空間的な関係性を学習するモデルを提案。この手法は、クロップされたactor(画像中の人物)の特徴量と画像の特徴量のペアを抽出することで、最終的にaction classificationに利用される。複数のデータセットでSOTAを達成。

* [Self-produced Guidance for Weakly-supervised Object Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaolin_Zhang_Self-produced_Guidance_for_ECCV_2018_paper.html)
    * 

* [Attribute-Guided Face Generation Using Conditional CycleGAN](http://openaccess.thecvf.com/content_ECCV_2018/html/Yongyi_Lu_Attribute-Guided_Face_Generation_ECCV_2018_paper.html)
    * 低解像度の顔画像を入力したとき，高解像度な顔画像を与えた属性（attribute）を満たすように出力する手法を提案．CycleGANを条件づけることによりこれを達成した．

* [Neural Network Encapsulation](http://openaccess.thecvf.com/content_ECCV_2018/html/Hongyang_Li_Neural_Network_Encapsulation_ECCV_2018_paper.html)
    * 

* [Deep Regionlets for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Hongyu_Xu_Deep_Regionlets_for_ECCV_2018_paper.html)
    * 

* [Deep Adversarial Attention Alignment for Unsupervised Domain Adaptation: the Benefit of Target Expectation Maximization](http://openaccess.thecvf.com/content_ECCV_2018/html/Guoliang_Kang_Deep_Adversarial_Attention_ECCV_2018_paper.html)
    * 

* [Fighting Fake News: Image Splice Detection via Learned Self-Consistency](http://openaccess.thecvf.com/content_ECCV_2018/html/Jacob_Huh_Fighting_Fake_News_ECCV_2018_paper.html)
    * 

* [Learning Monocular Depth by Distilling Cross-domain Stereo Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaoyang_Guo_Learning_Monocular_Depth_ECCV_2018_paper.html)
    * 

* [Riemannian Walk for Incremental Learning: Understanding Forgetting and Intransigence](http://openaccess.thecvf.com/content_ECCV_2018/html/Arslan_Chaudhry__Riemannian_Walk_ECCV_2018_paper.html)
    * 

* [Weakly Supervised Region Proposal Network and Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Peng_Tang_Weakly_Supervised_Region_ECCV_2018_paper.html)
    * 弱教師あり学習物体検出は、アノテーションが少ないことから、CNNの恩恵を受けていなかったが、Region Proposal Networkを用いて弱教師あり学習物体検出を行う提案をした。sliding window boxをもとに、粗くregionを生成する。その後、proposal refinementを行い、更にボックスの数を絞る。これによって生成されたボックスをRegion of InterestとしてWSODを行う手法。

* [Beyond local reasoning for stereo confidence estimation with deep learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Fabio_Tosi_Beyond_local_reasoning_ECCV_2018_paper.html)
    * 問題が限定的。手法はunetみたい。一応そのnetと別の組み合わせ？新しい応用みたい。ただ、手法の精度は高い

* [DeepGUM: Learning Deep Robust Regression with a Gaussian-Uniform Mixture Model](http://openaccess.thecvf.com/content_ECCV_2018/html/Stephane_Lathuiliere_DeepGUM_Learning_Deep_ECCV_2018_paper.html)
    * アイディアが良い。外れ値の影響を減らすために初めに教師なし学習でデータを整理。深く読みたくなる。例えば、パラメータは増えてないのか、テストに外れ値があったらどうなるのか、結果は良いと書いているがフェアなのか。

* [Into the Twilight Zone: Depth Estimation using Joint Structure-Stereo Optimization](http://openaccess.thecvf.com/content_ECCV_2018/html/Aashish_Sharma_Into_the_Twilight_ECCV_2018_paper.html)
    * 低照度の画像の時の深度推定。構造を確認しながら最適化。最適化が高級（著者らも言及）。比較は意外と少なめ。

* [Generalized Loss-Sensitive Adversarial Learning with Manifold Margins](http://openaccess.thecvf.com/content_ECCV_2018/html/Marzieh_Edraki_Generalized_Loss-Sensitive_Adversarial_ECCV_2018_paper.html)
    * マニフォルドの距離をGANに応用。新しい方針なので良い気はするが、比較が少なく、そこまで画期的ではないと感じる。

* [Adversarial Open Set Domain Adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Kuniaki_Saito_Adversarial_Open_Set_ECCV_2018_paper.html)
    * 0.5 未知であることを認識する手法。手法が面白く、またtを変えたときの実験など解析も良い。一方で、デファクトになるデータセット・手法であるかは一概には言えない。

* [Connecting Gaze, Scene and Attention](http://openaccess.thecvf.com/content_ECCV_2018/html/Eunji_Chong_Connecting_Gaze_Scene_ECCV_2018_paper.html)
    * 視線を推定するネットワーク。ただ、ネットワークに工夫があまり見られない。データセットも公開するようだが（まだ公開されていない）、デファクトになるとは考えにくい

* [Multi-modal Cycle-consistent Generalized Zero-Shot Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/RAFAEL_FELIX_Multi-modal_Cycle-consistent_Generalized_ECCV_2018_paper.html)
    * 見たことがない事柄についても、semanticについて学習したGANがあれば生成できるという手法。とてもおもしろく、コードも公開予定。ただ、実際の生成された画像がないのが残念。

* [Understanding Degeneracies and Ambiguities in Attribute Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Attila_Szabo_Understanding_Degeneracies_and_ECCV_2018_paper.html)
    * attributeというが、typeとviewであれば、https://arxiv.org/abs/1804.04732と似ていると思うが、定量評価がないので、評価しにくい

* [Start, Follow, Read: End-to-End Full Page Handwriting Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Curtis_Wigington_Start_Follow_Read_ECCV_2018_paper.html)
    * タイトル、アブストだけで読むべきだと判断。崩れ文字の手書き文字認識。文の始まり、文中の歪みなどを検出させて整形して認識。ICDAR17のコンペよりもアノテーションデータなしで良い成果。

* [Rethinking the Form of Latent States in Image Captioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Bo_Dai_Rethinking_the_Form_ECCV_2018_paper.html)
    * Captioningにおけるlatent spaceをspatialな情報も含む2Dにしたほうが良いのではないかという提案。納得性もあるし、future workとして上げているattentionとの相性も良さそう。

* [ConvNets and ImageNet Beyond Accuracy: Understanding Mistakes and Uncovering Biases](http://openaccess.thecvf.com/content_ECCV_2018/html/Pierre_Stock_ConvNets_and_ImageNet_ECCV_2018_paper.html)
    * 0.5 解析論文。imagenetの結果は過小評価されていると指摘。例えば、間違えと判断されたラベルをAMTで人に確認したところ、4/5が結果に対して同意した。Imagenetの信頼性などについて言及しているものの、次のデータセットを提唱しているわけではない。

* [Deep Shape Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Filip_Radenovic_Deep_Shape_Matching_ECCV_2018_paper.html)
    * エッジを用いたmatching手法。手法の概要が分かりづらい。手法はstate-of-the-artといっているが、必ずしもそうではないように結果からは見える。

* [Neural Stereoscopic Image Style Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Xinyu_Gong_Neural_Stereoscopic_Image_ECCV_2018_paper.html)
    * 立体視用のstyle transfer（領域がニッチ）。右と左で一貫性を持つように補正を行う。一貫性に関する解析や、ユーザー体験調査などは行っている。

* [Semi-supervised FusedGAN for Conditional Image Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Navaneeth_Bodla_Semi-supervised_FusedGAN_for_ECCV_2018_paper.html)
    * 0.5 ConditionalGANの学習を行う時に低層に関してnon-conditionalなGANの学習と共有することで、よりdiversityを上げる。結果の図、及びinception scoreなども高いことを確認。一方で、少し手法が簡単なところもあり、定量的な評価を鳥のデータセット以外でもあるとベター。

* [Affine Correspondences between Central Cameras for Rapid Relative Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Ivan_Eichhardt_Affine_Correspondences_between_ECCV_2018_paper.html)
    * AffineCorrespondenceを用いた3Dの向きなどの推定手法。state-of-the-artと言っているが、比較手法が少ないと感じる。

* [Bi-directional Feature Pyramid Network with Recursive Attention Residual Modules For Shadow Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Lei_Zhu_Bi-directional_Feature_Pyramid_ECCV_2018_paper.html)
    * 0.5 RecurrentAttentionResidualModuleとBidirectionalFeaturePyramidNetworkを影の検出に導入。影の検出自体は、ニッチのように思えるが、比較はしっかりしている。また結果の図は顕著に良いことがわかる。失敗した例も載っている。

* [Joint Learning of Intrinsic Images and Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Anil_Baslamisli_Joint_Learning_of_ECCV_2018_paper.html)
    * ShapeNetに対してセグメンテーションを推定するネットワークを追加。結果的にはjoint learningのほうが良いというもの。ただ、それはかなり一般的な結論な気がする。

* [Visual Reasoning with a Multi-hop FiLM Generator](http://openaccess.thecvf.com/content_ECCV_2018/html/Florian_Strub_Visual_Reasoning_with_ECCV_2018_paper.html)
    * Multi hopのFiLM層の提案。VQAの問題に適応したところ、Single Hopよりも高い性能を出した。画像の言語との融合はホットトピックであり、state of the artを上回っているのでテクニックを必読。詳細な解析も載っている。

* [View-graph Selection Framework for SfM](http://openaccess.thecvf.com/content_ECCV_2018/html/Rajvi_Shah_View-graph_Selection_Framework_ECCV_2018_paper.html)
    * SfMを行う際に、View-Graphのネットワークを最適化を行うことによって、SfMの再構成誤差を削減する。コードも公開予定。ただ、比較手法が少ない。

* [Fine-grained Video Categorization with Redundancy Reduction Attention](http://openaccess.thecvf.com/content_ECCV_2018/html/Chen_Zhu_Fine-grained_Video_Categorization_ECCV_2018_paper.html)
    * 詳細動画像識別における、Redundancy Reduction Attentionの導入。RRAを導入することにより、高精度化を実現。空間的および時間的なattentionにより選択された特徴からをsummary featureを作成して、それらを用いて判別する

* [Space-time Knowledge for Unpaired Image-to-Image Translation](http://openaccess.thecvf.com/content_ECCV_2018/html/Aayush_Bansal_Recycle-GAN_Unsupervised_Video_ECCV_2018_paper.html)
    * Cycle-GANでは時系列について考慮がされていなかったが、提案ではそのlossを定義することにより動画像の生成に関して精度向上を行った。具体的にCycle-GANでは非常に細かなピクセルの違いのみで表情の違いが表され、提案ではターゲットの表情も変わっている。

* [Integral Human Pose Regression](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiao_Sun_Integral_Human_Pose_ECCV_2018_paper.html)
    * 人物のポーズ推定。従来のheat mapを用いた手法では微分不可能な表現になっていたが、インテグラルを導入することで微分可能となる。実験は様々行っているものの、どのような状況で役立つのか分かりづらい（practicalなどのようなシナリオなのか）

* [Recurrent Tubelet Proposal and Recognition Networks for Action Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Dong_Li_Recurrent_Tubelet_Proposal_ECCV_2018_paper.html)
    * Recurrent Tubelet ProposalとRecurrent Tubelet Recognitionを用いた人の動作認識。時系列を考慮した範囲推定RTP（t-1の結果をインプットに入力）、及びその範囲推定結果を用いてRTRによる識別を実施。従来手法よりも高精度で識別できている。

* [Learning to Predict Crisp Edge](http://openaccess.thecvf.com/content_ECCV_2018/html/Ruoxi_Deng_Learning_to_Predict_ECCV_2018_paper.html)
    * セグメンテーション問題。境界領域の識別を導入することにより、識別性能を上げた。また、bottom-upとtop-downなネットワークを導入した。ただ、性能向上の具合は著しくはない。

* [Open Set Learning with Counterfactual Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Lawrence_Neal_Open_Set_Learning_ECCV_2018_paper.html)
    * counterfactual image generationという画像の生成手法を用いることによって、オープンセット認識の識別率を向上させた。ただ、向上した数値がわずか

* [Estimating the Success of Unsupervised Image to Image Translation](http://openaccess.thecvf.com/content_ECCV_2018/html/Lior_Wolf_Estimating_the_Success_ECCV_2018_paper.html)
    * シンプリシティ原理による教師なしクロスドメインマッピングの成功を活用し予測する境界を提案。それにより画像生成の精度向上。

* [Joint Map and Symmetry Synchronization](http://openaccess.thecvf.com/content_ECCV_2018/html/Qixing_Huang_Joint_Map_and_ECCV_2018_paper.html)
    * シンメトリーな物体であっても頑健に特徴の地図計算が可能な手法の提案。シンメトリーな物体のグループを作成して同時に最適化を行う点などを導入。ただ、大きなアドバンテージが認められない。

* [Single Image Water Hazard Detection using FCN with Reflection Attention Units](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaofeng_Han_Single_Image_Water_ECCV_2018_paper.html)
    * 道路上の水たまり検出。反射をモデル化して、Reflection Attention Unitを提案。実用的な問題であり、データセットの公開、及び精度向上も十分。ただ、もしあれば、他のデータセットでも調査してほしかった。

* [Realtime Time Synchronized Event-based Stereo](http://openaccess.thecvf.com/content_ECCV_2018/html/Alex_Zhu_Realtime_Time_Synchronized_ECCV_2018_paper.html)
    * 双眼のイベントカメラを用いて深度推定などを行う場合において，カメラの運動に起因する被写体ブレに頑強な手法を提案．左右のカメラから得られたspatial-temporalなvolumeをmatchingさせる際の目的関数を工夫．

* [Transferring GANs: generating images from limited data](http://openaccess.thecvf.com/content_ECCV_2018/html/yaxing_wang_Transferring_GANs_generating_ECCV_2018_paper.html)
    * 0.5 GANにおける転移学習の有用性の研究．pretrainしたモデルを用いることにより，収束が早まることを確認．conditional GANにおいても，conditionalでないGANの学習済み重みを用いても収束が早まることを確認．また，ソース・ターゲットのデータセット間の関係も調査し，データセットがdenseであること（Celebデータセットのように，データ同士の際が小さいものが集まっている）がdivesityが大きいこと（ImageNetやPlacesのような）よりも重要だと確認．

* [To learn image super-resolution, use a GAN to learn how to do image degradation first](http://openaccess.thecvf.com/content_ECCV_2018/html/Adrian_Bulat_To_learn_image_ECCV_2018_paper.html)
    * 超解像において，劣化過程をもデータ駆動で学習させるために，高解像と低解像２つのネットワークを持つGANを提案．既存研究に比べ実際の劣化した画像をよく超解像することを可能に。敵対的損失は高解像度の画像が生成されたものかを識別するタスクと，低解像度の画像が生成されたものかを識別するタスクの２つの和で与える

* [Unsupervised CNN-based co-saliency detection with graphical optimization](http://openaccess.thecvf.com/content_ECCV_2018/html/Kuang-Jui_Hsu_Unsupervised_CNN-based_co-saliency_ECCV_2018_paper.html)
    * co-sailiencyを推定する教師なしで学習するネットワークを提案．工夫は損失関数で，単一画像のsilencyのロスと，co-silencyのロスをグラフィカルモデルを用いて定式化することで，２つのロスを同時に最適化することを可能に．教師あり学習に匹敵する性能を実現．

* [Fast Light Field Reconstruction With Deep Coarse-To-Fine Modeling of Spatial-Angular Clues](http://openaccess.thecvf.com/content_ECCV_2018/html/Henry_W._F._Yeung_Fast_Light_Field_ECCV_2018_paper.html)
    * 光線がどの方向から飛んできたかを記録できるLight Field(LF)カメラの画像において，粗いLF画像から密なLF画像を再構成するend-to-endなネットワークの提案

* [Unified Perceptual Parsing for Scene Understanding](http://openaccess.thecvf.com/content_ECCV_2018/html/Tete_Xiao_Unified_Perceptual_Parsing_ECCV_2018_paper.html)
    * より深い画像理解のため、複数の観点（場所，物体，部分，材料，テクスチャ）から画像をセグメンテーションする

* [PARN: Pyramidal Affine Regression Networks for Dense Semantic Correspondence Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Sangryul_Jeon_PARN_Pyramidal_Affine_ECCV_2018_paper.html)
    * semanticsを考慮したdenseな対応点マッチング(Dense Semantic Correspondence)のタスクを解くため，スケールのことなる局所的なアフィン変換を階層的に組み合わせたものを推定するe2eなネットワークの提案．dense samntic correspondenceの複数のbench markでSOTA．

* [Structural Consistency and Controllability for Diverse Colorization](http://openaccess.thecvf.com/content_ECCV_2018/html/Safa_Messaoud_Structural_Consistency_and_ECCV_2018_paper.html)
    * 白黒画像の着色のタスクにおいて，画像における着色に一貫性を持たせるように工夫したネットワークの提案．VAEをベースにして，画素同士の条件付き確率場によるロスを組み込む．

* [Online Multi-Object Tracking with Dual Matching Attention Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Ji_Zhu_Online_Multi-Object_Tracking_ECCV_2018_paper.html)
    * Multi-Object Trackingのタスクを，Single Object Trackingの結果を注意機構を持つネットワークで統合することにより解く手法の提案．

* [MaskConnect: Connectivity Learning by Gradient Descent](http://openaccess.thecvf.com/content_ECCV_2018/html/Karim_Ahmed_MaskConnect_Connectivity_Learning_ECCV_2018_paper.html)
    * ニューラルネットの構造を学習によって取得させる．ブロック単位の連結を学習する．面白い点は，ブロック単位の連結を表現する重みを用意し，あるタスクに最適な構造を，タスクそのものの学習に伴って最適化するところ．

* [FloorNet: A Unified Framework for Floorplan Reconstruction from 3D Scans](http://openaccess.thecvf.com/content_ECCV_2018/html/Chen_Liu_FloorNet_A_Unified_ECCV_2018_paper.html)
    * 0.5 point cloud，上からの画像，部屋の画像から部屋の間取りを再構成．様々な情報を複雑なネットワークで統合し，間取りを出力．基本手法に比べて大きな精度向上

* [Image Manipulation with Perceptual Discriminators](http://openaccess.thecvf.com/content_ECCV_2018/html/Diana_Sungatullina_Image_Manipulation_with_ECCV_2018_paper.html)
    * 0.5 新しいDiscriminatorとして，VGGなど学習済みのモデルの中間層からも真偽を判断するperceptual discriminatorの提案．

* [Transductive Centroid Projection for Semi-supervised Large-scale Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Yu_Liu_Transductive_Centroid_Projection_ECCV_2018_paper.html)
    * クラスタリングを用いるNNの半教師あり学習において問題になっていた計算量を削減するため，クラスタリングに相当するNNのモジュールの提案

* [Eigendecomposition-free Training of Deep Networks with Zero Eigenvalue-based Losses](http://openaccess.thecvf.com/content_ECCV_2018/html/Zheng_Dang_Eigendecomposition-free_Training_of_ECCV_2018_paper.html)
    * 固有値分解をNN上で行えるようにすることで，古典的な画像処理のアルゴリズムにNNを導入することを可能に。

* [Self-supervised Knowledge Distillation Using Singular Value Decomposition](http://openaccess.thecvf.com/content_ECCV_2018/html/SEUNG_HYUN_LEE_Self-supervised_Knowledge_Distillation_ECCV_2018_paper.html)
    * 0.5 蒸留の際，教師モデルと生徒モデルの近さを，各モデルの重みの特異値で測る。

* [Snap Angle Prediction for 360$^{\circ}$ Panoramas](http://openaccess.thecvf.com/content_ECCV_2018/html/Bo_Xiong_Snap_Angle_Prediction_ECCV_2018_paper.html)
    * 360度カメラの画像から、任意の画角の画像を予測するモデルの提案．360度画像と特定の画学との関係を得るために，強化学習を用いる．ベースラインよりも5倍早い計算時間を実現．

* [Saliency Preservation in Low-Resolution Grayscale Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Shivanthan_Yohanandan_Saliency_Preservation_in_ECCV_2018_paper.html)
    * 顕著性がカラー高解像度画像とグレースケール低解像度とでどの程度違うか調査。知覚の生理学的側面への貢献も強調。

* [PPF-FoldNet: Unsupervised Learning of Rotation Invariant 3D Local Descriptors](http://openaccess.thecvf.com/content_ECCV_2018/html/Tolga_Birdal_PPF-FoldNet_Unsupervised_Learning_ECCV_2018_paper.html)
    * point cloudの局所特徴量を教師なしで学習したネットワークで抽出する手法を提案．point cloud同士の対応点のマッチングで良いスコア

* [BusterNet: Detecting Copy-Move Image Forgery with Source/Target Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Rex_Yue_Wu_BusterNet_Detecting_Copy-Move_ECCV_2018_paper.html)
    * 画像編集を検出するend-to-endなネットワークBusterNetを提案．同時に，画像編集検出のタスクのためのデータセットを作成する枠組みも提案． BusterNetは画像編集を検知するブランチと類似領域を検知する２つのブランチを持ち，その統合結果を出力．既存手法の性能を超え，また既知の画像編集検出に対する攻撃にロバストであることも確認．

* [Double JPEG Detection in Mixed JPEG Quality Factors using Deep Convolutional Neural Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Jin-Seok_Park_Double_JPEG_Detection_ECCV_2018_paper.html)
    * jpgの画像編集された部位を検出するため、編集された部分とそれ以外で、jpgの圧縮がかけられた回数が異なる性質を利用

* [Unsupervised holistic image generation from key local patches](http://openaccess.thecvf.com/content_ECCV_2018/html/Donghoon_Lee_Unsupervised_holistic_image_ECCV_2018_paper.html)
    * 画像の一部分のパッチの少数の集合から，構造についての事前知識を与えず，教師なしで画像全体を復元する手法の提案．パッチの部分を推定するブランチと，バッチを含む画像全体を復元するネットワークをU-Net+GANを用いて実現．

* [CrossNet: An End-to-end Reference-based Super Resolution Network using Cross-scale Warping](http://openaccess.thecvf.com/content_ECCV_2018/html/Haitian_Zheng_CrossNet_An_End-to-end_ECCV_2018_paper.html)
    * reference-basedな超解像のタスクを，end-to-endで実現する手法の提案．工夫は，referenceの情報を，解像度ごとに，超解像を行うブランチに与えているネットワークの構造を提案した部分．

* [DCAN: Dual Channel-wise Alignment Networks for Unsupervised Scene Adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Zuxuan_Wu_DCAN_Dual_Channel-wise_ECCV_2018_paper.html)
    * ドメインアダプテーションにより、教師の無いターゲットドメインでのセグメンテーションを学習．中間層のフィーチャーでアライメントを取る。

* [YouTube-VOS: Sequence-to-Sequence Video Object Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Ning_Xu_YouTube-VOS_Sequence-to-Sequence_Video_ECCV_2018_paper.html)
    * 動画解析のタスクにおいては，長時間の時間-空間的依存を扱うことが重要だが，良いデータセットがなかったため，あまり研究されてこなかった．本研究では，YouTubeのデータから約3,000ビデオクリップを含むvideo object segmentation用のデータセットを提案．このデータセットを用い，長時間の時間-空間的依存を扱えるvideo segmentationの手法を提案

* [Selfie Video Stabilization](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiyang_Yu_Selfie_Video_Stabilization_ECCV_2018_paper.html)
    * 自撮り動画の手ブレ補正を，顔の形状を陽に取得し，それを目印に使うことで行う手法の提案．

* [Videos as Space-Time Region Graphs](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaolong_Wang_Videos_as_Space-Time_ECCV_2018_paper.html)
    * オブジェクト同士の関係を時空間中のグラフとして陽に抽出し，行動認識を行う。

* [Parallel Feature Pyramid Network for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Seung-Wook_Kim_Parallel_Feature_Pyramid_ECCV_2018_paper.html)
    * 物体検出のタスクにおいて，陽に複数の解像度で特徴をとるようなネットワークを提案．複数の解像度を使うことで，今までアーキテクチャでは難しかった小さい物体も検出できることを期待．MS-COCOを用いた実験でSSDに対しての性能向上を確認．

* [Goal-Oriented Visual Question Generation via Intermediate Rewards](http://openaccess.thecvf.com/content_ECCV_2018/html/Junjie_Zhang_Goal-Oriented_Visual_Question_ECCV_2018_paper.html)
    * VQAの研究は数多くなされているが，実応用を考えた場合，システムからトンチンカンな質問ばかりされてはユーザは使う意欲を失ってしまう．そこで，VQAにおける”効率的な質問”の生成を，質問回数の少なさなどを報酬とした強化学習を用いて学習．

* [WildDash - Creating Hazard-Aware Benchmarks](http://openaccess.thecvf.com/content_ECCV_2018/html/Oliver_Zendel_WildDash_-_Creating_ECCV_2018_paper.html)
    * 自動車のためのsemantic及びインスタンスセグメンテーションのための新しいデータセットを提案する。提案手法では、テストデータセットに高度に表現されたメタ情報を含めることで、エラー分析の際に経験的評価に基づいた推論を可能にする。（特定の事故に対してロバストではない等と評価できる。)さらに既存のデータセットは西欧諸国の状況に偏り過ぎている点も解消した。

* [Reinforced Temporal Attention and Split-Rate Transfer for Depth-Based Person Re-identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Nikolaos_Karianakis_Reinforced_Temporal_Attention_ECCV_2018_paper.html)
    * 奥行き(depth)に基づいた人物再識別のための新しい手法を提示する。この手法では、データ不足の問題に対処するために、大きなRGBデータから事前に訓練されたモデルを活用する。さらにvideo sequencesのための Reinforced Temporal Attention unitを提案する。これらの手法を用いることで、depth-based person　re-identification タスクにおいて良い結果、さらに服を交換した場合のタスクにおいては、RGB-basedよりも良い結果をもたらす。

* [DF-Net: Unsupervised Joint Learning of Depth and Flow using Cross-Network Consistency](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuliang_Zou_DF-Net_Unsupervised_Joint_ECCV_2018_paper.html)
    * ラベルなしビデオシーケンスを使用したsingle depth predection(単焦点深度予測)とオプティカルフロー推定についての教師なし学習フレームワークを提案している。このフレームワークのキモは、rigid regionsに対して、induced 3D scene flowを逆投影することによって、予測されたシーン深度とカメラモーションを使用して2Dオプティカルフローを合成することができるということである。

* [Generating Multimodal Human Dynamics with a Transformation based Representation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xinchen_Yan_Generating_Multimodal_Human_ECCV_2018_paper.html)
    * motion sequence generationを学習するためのMotion Transformation Variational Auto-Encoders (MT-VAE)を提案する。提案手法は、モーションモードの特徴埋め込み（モーションシーケンスの再構成が可能）と、あるモーションモードから次のモーションモードへの遷移を表す特徴変換を合わせて学習する。

* [Learning Rigidity in Dynamic Scenes with a Moving Camera for 3D Motion Field Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhaoyang_Lv_Learning_Rigidity_in_ECCV_2018_paper.html)
    * この論文で主に提案するもの。  
    - 動くカメラを用いた動的シーンに対する学習ベースの剛性および姿勢推定アルゴリズムの提案  
    - 剛性、ポーズ、および既存の2Dオプティカルフローからの推論に基づいて構築された、RGBD 3Dモーション領域推定フレームワーク。

* [Learning Visual Question Answering by Bootstrapping Hard Attention](http://openaccess.thecvf.com/content_ECCV_2018/html/Mateusz_Malinowski_Learning_Visual_Question_ECCV_2018_paper.html)
    * 特徴ベクトルの大きさに基づいてそのサブセットを選択するという、HardAttentionのための新しいアプローチを提案する。提案手法は、VQAデータ・セットで、SoftAttentionの結果を上回る。さらにこの手法は、ソフトアテンションに比べて、計算効率上の利点がある。

* [Image Reassembly Combining Deep Learning and Shortest Path Problem](http://openaccess.thecvf.com/content_ECCV_2018/html/Marie-Morgane_Paumard_Image_Reassembly_Combining_ECCV_2018_paper.html)
    * - 正方形切り取り断片の相対位置を予測するためのいくつかの深い畳み込みニューラルネットワークアーキテクチャを提案  
    - パズルの異なるケースに対応する再アセンブリ問題を実装するいくつかのグラフ構築アルゴリズムを提案

* [RESOUND: Towards Action Recognition without Representation Bias](http://openaccess.thecvf.com/content_ECCV_2018/html/Yingwei_Li_RESOUND_Towards_Action_ECCV_2018_paper.html)
    * 較正されたデータセットと表現バイアスの概念、およびデータセットのrepresentation biasを客観的に定量化するRESOUNDアルゴリズムを提案している。提案手法を用いて、既存のデータセットをサンプリングすることによって新しいデータセット(the proposed Diving48 dataset)を構築する。特に行動認識タスクにおいてのデータセットバイアスを軽減することを目的としている。

* [Key-Word-Aware Network for Referring Expression Image Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Hengcan_Shi_Key-Word-Aware_Network_for_ECCV_2018_paper.html)
    * Referring expression image segmentationのためのキーワード認識ネットワークとキーワード認識型ビジュアルコンテキストモデルを含むネットワークを提案する。各画像領域ごとにキーワードを抽出し、自然言語クエリに基づいて複数の画像領域の中からキーワード認識型視覚コンテキストをモデル化するkey-word-aware network (KWAN)を提案する。  
      
    - 内部でCNNとRNNを用いて、画像領域とキーワードの特徴をエンコードする。  
    - それらに基づいて、アテンションモデルが各画像領域のキーワードを見つける  
    - 抽出したvisual features, key-word-aware visual context features、key word featuresを元に各画像領域を分類する。  
    

* [Mutual Learning to Adapt for Joint Human Parsing and Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xuecheng_Nie_Mutual_Learning_to_ECCV_2018_paper.html)
    * 本論文では、human parsingと姿勢推定のための Mutual Learning to Adapt model (MuLA)を提案する。MuLAは、既存の事後処理またはマルチタスク学習ベースの方法とは異なり、パラレルタスクのguidance informationを再利用してモデルパラメータを予測する。さらに、畳み込みニューラルネットワークとエンドツーエンドで訓練可能なものだけで構成されているのが特徴。そしてPASCAL-Person-Partデータセットで既存手法を上回る結果。

* [Simple Baselines for Human Pose Estimation and Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Bin_Xiao_Simple_Baselines_for_ECCV_2018_paper.html)
    * Human Pose EstimationとTrackingのためのシンプルなベースラインを提案。姿勢推定はResNetに基づいて作成され、低解像度および低解像度のフィーチャマップからヒートマップを推定する最も簡単な方法を使用する。Trackingは、ICCV’17 PoseTrack Challengeの勝者と同じ、greedy matching methodを使用している。

* [Pose Partition Networks for Multi-Person Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xuecheng_Nie_Pose_Partition_Networks_ECCV_2018_paper.html)
    * 多人数のPose推定のためのPose Partition Network (PPN)を提案。提案手法は、人物検出と関節分割の候補を回帰手法で得ることを提案している。WAF・extendedPASCAL-Person-Part・MPII Human Pose Multi-Person datasetにおいて、既存手法を上回る結果に。

* [Wasserstein Divergence For GANs](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiqing_Wu_Wasserstein_Divergence_For_ECCV_2018_paper.html)
    * W-metの緩和版であり、k-Lipschitz制約を必要としない、Wasserstein divergence (W-div)を提案している。

* [A Segmentation-aware Deep Fusion Network for Compressed Sensing MRI](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhiwen_Fan_A_Segmentation-aware_Deep_ECCV_2018_paper.html)
    * 圧縮センシングMRIのためのSADFNと呼ばれるセグメンテーションネットワークを提案する。セグメンテーションネットワークのさまざまな層からのすべてのフィーチャを融合するmultilayer feature aggregation (MLFA) メソッドを用いる。 SADFNモデルはCS-MRIにおいて最先端の性能を達成した。

* [Deep Metric Learning with Hierarchical Triplet Loss](http://openaccess.thecvf.com/content_ECCV_2018/html/Ge_Deep_Metric_Learning_ECCV_2018_paper.html)
    * 適応的に更新された階層ツリーを通して、トレーニングサンプルを選択するhierarchical triplet loss (HTL)を提案する。画像検索や顔認識の標準トリプレットロスを大幅に上回り、多くのベンチマークで新しい最先端の結果を得ている。

* [Generative Adversarial Network with Spatial Attention for Face Attribute Editing](http://openaccess.thecvf.com/content_ECCV_2018/html/Gang_Zhang_Generative_Adversarial_Network_ECCV_2018_paper.html)
    *   
    

* [Proxy Clouds for Live RGB-D Stream Processing and Consolidation](http://openaccess.thecvf.com/content_ECCV_2018/html/Adrien_Kaiser_Proxy_Clouds_for_ECCV_2018_paper.html)
    * RGB-Dデータを平面の組み合わせで表現するProxy Cloudという中間表現の提案．RGB-Dセンサから得られるデータは解像度の低さやノイズの多さが問題になるが，Proxy Coludに変換したデータも用いることで様々な実問題で精度向上を目的とする．Proxy Cloudは軽量に計算可能．

* [Synthetically Supervised Feature Learning for Scene Text Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Liu_Synthetically_Supervised_Feature_ECCV_2018_paper.html)
    * 1 シーンテキスト認識のための新しいアルゴリズムを提案する。このアルゴリズムは、合成データ生成プロセスと生成されたデータを使用して、特徴抽出を行うencoder-generator-discriminator-decoderアーキテクチャを備えている。さらに、提案方法は、明示的な取り扱いなしに、入力画像に曲面上にあるテキストなど、厳しい幾何学的歪みが含まれている場合でも対処できることを示している。結果提案手法が、テキスト認識におけるベンチマークを著しく上回ることを示している。

* [Scale Aggregation Network for Accurate and Efficient Crowd Counting](http://openaccess.thecvf.com/content_ECCV_2018/html/Xinkun_Cao_Scale_Aggregation_Network_ECCV_2018_paper.html)
    * 集団計測のためのencoder-decoder network(Scale Aggregation Network :SANet)を提案する。Encoderは、scale aggregation modulesを用いて、マルチフィーチャー抽出し、Decoderは、転置されたコンボリューションのセットを使用して高解像度密度マップを生成する。ユークリッド損失関数と局所パターン一貫性損失関数を組み合わせた新しい損失関数を提案する。

* [PM-GANs: Discriminative Representation Learning for Action Recognition Using Partial-modalities](http://openaccess.thecvf.com/content_ECCV_2018/html/Lan_Wang_PM-GANs_Discriminative_Representation_ECCV_2018_paper.html)
    * 1

* [OmniDepth: Dense Depth Estimation for Indoors Spherical Panoramas.](http://openaccess.thecvf.com/content_ECCV_2018/html/NIKOLAOS_ZIOULIS_OmniDepth_Dense_Depth_ECCV_2018_paper.html)
    * 単一の360o画像からシーンの深度を推定する学習フレームワークを提案。ground truth depthを元に学習することが新規性である。そのために、3Dデータセットを再利用し、レンダリングによって360oデータセットを合成する。ただし、現状では室内ケース、一定の照明、no stitching artifactsである場合に限られる。

* [Hashing with Binary Matrix Pursuit](http://openaccess.thecvf.com/content_ECCV_2018/html/Fatih_Cakir_Hashing_with_Binary_ECCV_2018_paper.html)
    * 二段階ハッシュ法（two stage hashing methods）の理論的、実験的改善を提案する。

* [Probabilistic Video Generation using Holistic Attribute Control](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiawei_He_Probabilistic_Video_Generation_ECCV_2018_paper.html)
    * ビデオ生成および将来の予測のための確率的生成フレームワークを提案している。提案手法は、潜在空間分布から完全なビデオフレームに順次引き出されたサンプルをデコードすることによってビデオ（ショートクリップ）を生成する

* [Transductive Semi-Supervised Deep Learning using Min-Max Features](http://openaccess.thecvf.com/content_ECCV_2018/html/Weiwei_Shi_Transductive_Semi-Supervised_Deep_ECCV_2018_paper.html)
    * 1: Feature pyramindsのためのglobal attentionとlocal reconfigulationを提案。標準的なSSDに組み込み実験を行った。その結果、マルチスケールにおける表現性を高めること

* [Deep Feature Pyramid Reconfiguration for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Tao_Kong_Deep_Feature_Pyramid_ECCV_2018_paper.html)
    * DCNNモデルの学習に有効なTSSDL（Transductive Semi-Supervised Deep Learning）法を提案する。この手法では、学習に従来のトランスダクティブ学習を適用する。さらに、外れ値などのサンプルからの影響を防ぐため、ラベルなしサンプルに対して信頼度を導入する。特徴記述子間の距離を最小にするためにMin-Max Feature (MMF) regularizationも提案する。最先端のSSLメソッドと同等画像分類精度を達成している。

* [Quadtree Convolutional Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Pradeep_Kumar_Jayaraman_Quadtree_Convolutional_Neural_ECCV_2018_paper.html)
    * 手書き文字などの疎な画像データを効率よく学習するための、Quadtree Convolutional Neural Network（QCNN）を提案する。この手法では、疎なデータを密なテンソルに格納する代わりに、空でないものを線形四分木として表現する。結果、従来の手法に比べてメモリコストと計算コストを削減し、且つ同等の精度を得ることができた。

* [Correcting the Triplet Selection Bias for Triplet Loss](http://openaccess.thecvf.com/content_ECCV_2018/html/Baosheng_Yu_Correcting_the_Triplet_ECCV_2018_paper.html)
    * Triplet loss(画像分類、画像検索、顔認識などで使用)は現在多く使用されているが、Tripletのサンプリングに影響されるという問題を抱えている。この論文では、Tripletのサンプリングの分布を適応的に補正することにより、Tripletサンプリングのバイアスを低減しようとするadapted triplet lossを提案している。この手法によりMNISTなどを用いた画像分類で良い結果となった。

* [ECO: Efficient Convolutional Network for Online Video Understanding](http://openaccess.thecvf.com/content_ECCV_2018/html/Mohammadreza_Zolfaghari_ECO_Efficient_Convolutional_ECCV_2018_paper.html)
    * long-termかつ高速に動画を処理可能なネットワークを提案した論文。隣接するフレームは冗長な情報が多いため、2DCNNでsingle frameから特徴量を十分離れた時間で複数取得し、それらの特徴量を合わせたものを3DCNNへ入力する。3DCNNはflow情報ではなく、離れた時間の関係性を見出すために使用している。

* [Learning to Anonymize Faces for Privacy Preserving Action Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhongzheng_Ren_Learning_to_Anonymize_ECCV_2018_paper.html)
    * ビデオから個人情報をピクセルレベルで取り出しながら、行動認識の精度を保とうとしているもの。様々な修正が可能（Blur,mask,noise,super-pixel,Edgeに変換）。修正するときの手法によって行動認識の精度が変化している・行動認識と個人情報の認証に関してはbaselineより高い精度を出している。

* [Adversarial Open-World Person Re-Identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiang_Li_Adversarial_Open-World_Person_ECCV_2018_paper.html)
    * 大量の人たちから追跡対象となる人物を追跡するOpen-World Person Re-Identificationに取り組んだ論文。追跡対象に非常に類似した人物が発生しやすい状況下であるため、追跡対象に類似した人物を生成することで識別器を強化していく。

* [Graph R-CNN for Scene Graph Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Jianwei_Yang_Graph_R-CNN_for_ECCV_2018_paper.html)
    * 画像に写っている物体と物体間の関係性を表現するグラフ構造の学習法Graph R-CNNを提案．入力が鳥の画像であったときに出力例として，(bird->stand on ->branch->on->tree, bird->has->wings, leaf->on->tree, ...)のような関係性を表現するグラフが出力となる．手順は1)各物体の検出 2)物体間の関係性がないエッジを切り捨て，3)ノードに隣接エッジの関係を表現する文脈の付与. 新たにシーンのグラフ説明に対する評価としてよりrealisticな適切な指標を提案し，既存手法を大きく上回る精度を出した．

* [Contemplating Visual Emotions: Understanding and Overcoming Dataset Bias](http://openaccess.thecvf.com/content_ECCV_2018/html/Rameswar_Panda_Contemplating_Visual_Emotions_ECCV_2018_paper.html)
    * 画像の感情を正しく推定しようとした論文。現在の手法では、amusement part with negative motionのような画像を入力すると、""amusement / joy""として認識されてしまう。これは学習データ内のamusement parkのほとんどに""joy""というラベルが与えられているというラベルのバイアスによって発生している。本論文はこのようなデータのバイアスをなくすことを目的としている。

* [Graph Adaptive Knowledge Transfer for Unsupervised Domain Adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhengming_Ding_Graph_Adaptive_Knowledge_ECCV_2018_paper.html)
    * グラフで教師なしdomain adaptationを適用したという論文。複数ラベルベースのグラフから確率分布を考えて、ラベル伝播を行うことによってtargetに対してラベルを正確に降ることが出来たという論文

* [Deep Recursive HDRI: Inverse Tone Mapping using Generative Adversarial Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Siyeong_Lee_Deep_Recursive_HDRI_ECCV_2018_paper.html)
    * 一枚のLDRI(Low Dynamic Range Images)から，複数の輝度の段階のHDRI(High Dynamic Range Image)を生成する手法を提案．LDRI->HDRIへの変換はinverse tone mapping problemに分類されるタスク．従来手法はCNNを用いて画像を生成していたが，この論文ではconditional GANを用いることでそれを実現することでより精度の高いHDRIを得た．新規性としては, conditional GANのGeneratorは輝度のあげる，さげるに対応したG_plus, G_minusを用い，generatorの出力を入力に入れる再起構造にすることで輝度の段階が異なる画像の生成にもそれに応じて変換ネットワークを追加する必要がなくなったこと，学習の順番として，l1 lossの最小化をしてからGANのadversarial lossを小さくするように学習していく．

* [Deep Cross-Modal Projection Learning for Image-Text Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Ying_Zhang_Deep_Cross-Modal_Projection_ECCV_2018_paper.html)
    * 画像とテキストのマッチングをとるタスクに取り組んだ論文。近年では、bi-directional ranking lossを用いた手法が大きな隆盛を見せているが、提案手法では分離可能な特徴量を学習する損失関数として、cross-modal projection matching loss（CMPC）とcross-modal projection matching loss（CMPM）という新しい損失関数を提案した。

* [Composition Loss for Counting, Density Map Estimation and Localization in Dense Crowds](http://openaccess.thecvf.com/content_ECCV_2018/html/Haroon_Idrees_Composition_Loss_for_ECCV_2018_paper.html)
    * 大衆が写っている(数十人-1000人規模)の画像から写っている人数を導出することを目的とした論文．localizeの問題だと,情報がスパースであるなどの問題がある．この論文ではcounting, dense estimation, localizerの３種類の問題を一度に解くことで解決を図る．これはこれら３種類の情報は相互的な情報を持っているため同時に学習することが有益であると述べている．手法の新規性は，1)DenseNetをベースとした一つのネットワークでcounting, dense extimation, localizerを推論し，各出力の結果を統合させることで最終的な推測人数としていること 2)Composition lossを提案したこと 3)また大衆画像からの推測のためのUCF-QNRFデータセットを作成し，counting, dense estimation, localizerのすべての観点で既存手法よりも精度が向上．

* [Person Search by Multi-Scale Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Xu_Lan_Person_Search_by_ECCV_2018_paper.html)
    * 画像中に写っている人物の抽出，人物認識において，どのようなバウンディングボックスのサイズでも対応できることが重要である．この論文では，Faster-RCNNで抽出された人物のバウンディングボックスを入力賭して，人物のre-identificationを行うためのCross-Level Semantic Alignment(CLSA) approachを提案した．ResNet-50ベースのperson identificationで，後ろの畳み込み層数層(論文中では3層)に交差エントロピー誤差に加えて，後ろの層から徐々に伝搬させる誤差を加えることで，マルチスケールな画像に対応できるネットワークの学習を行った．CUHK-SYU,PRSAの二つのperson search taskに適用し，既存手法と比較して両方のデータセットで精度が向上した．

* [Efficient 6-DoF Tracking of Handheld Objects from an Egocentric Viewpoint](http://openaccess.thecvf.com/content_ECCV_2018/html/Rohit_Pandey_Efficient_6-DoF_Tracking_ECCV_2018_paper.html)
    * VRで使用する，手で握っているコントローラの6DoFをヘッドセットで検出した画像のみからCPU処理で検出するためのアルゴリズムの提案，およびHMDコントローラデータセットの作成．アルゴリズムはSSDがベースで，SSDの出力offset, class possibilitiesに加えてadditional fieldと呼んでいる出力を検出したい次元数に応じて増やす.どちらかというとデータセット作成がメイン．精度評価としては，入力・出力数を変化させたときの提案手法(SSD-AF)の比較のみ．VR技術の応用として今後使われそうではある

* [Deep Video Generation, Prediction and Completion of Human Action Sequences](http://openaccess.thecvf.com/content_ECCV_2018/html/Chunyan_Bai_Deep_Video_Generation_ECCV_2018_paper.html)
    * Video Generation, Video Prediction, Video Completionに取り組んだ論文。特にVideo Generationでは潜在変数ベクトルのみから、動画を生成することに成功した。従来手法よりはよい精度を出しているが、そこまで大きな手法の新規性が感じられなかった。ただし、3つのタスクを解いて評価しているという点では、かなり評価が高い。

* [Efficient Uncertainty Estimation for Semantic Segmentation in Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Po-Yu_Huang_Efficient_Uncertainty_Estimation_ECCV_2018_paper.html)
    * 不明確さ推定は現実世界のアプリケーションとしては重要であるという主張から、特にドライビングのコンテキストにおいて、sematic segmentationの不明確さを出力する手法（RTA：Region-based Temporal Aggregation）を提案した。提案手法は従来のMonte Carlo Dropoutより10倍程度高速であり、より現実世界のアプリケーションに適した手法である。

* [DeepKSPD: Learning Kernel-matrix-based SPD Representation for Fine-grained Image Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Melih_Engin_DeepKSPD_Learning_Kernel-matrix-based_ECCV_2018_paper.html)
    * Local descriptors と kernel-matrix-based SPD representationをつなげて学習を行わさせることで、非線形データからlocal descriptorsを探すのに良さを持つkernel法の良さを活かすNNを構築して、既存手法（共分散をベースとしたNN)より良い結果を出した

* [From Face Recognition to Models of Identity: A Bayesian Approach to Learning about Unknown Identities from Unsupervised Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Castro_From_Face_Recognition_ECCV_2018_paper.html)
    * 0.5 顔を識別する情報は，顔情報だけでなく，その人にあった場所や名前の部分的な記憶などを使って人間は推測している．それをcontext model, face model, identify model, label modelと分割してそれぞれをベイズモデルに落とし込み，人物認識を行う手法を提案した．珍しく，CNNを使っていない論文．比較手法としてはNNとOne class SVM. アイデアは面白いと思ったが設定がかなり限定的だと思う．

* [ShapeStacks: Learning Vision-Based Physical Intuition for Generalised Object Stacking](http://openaccess.thecvf.com/content_ECCV_2018/html/Oliver_Groth_ShapeStacks_Learning_Vision-Based_ECCV_2018_paper.html)
    * データセットの論文．球や立方体などの形をしたブロックが縦につまれた状態を画像として入力したときに，その状態が安定しているかどうかを物理的な情報を用いずに画像のみから学習する．これは人間がぱっと見てその物体が今にも崩れそうかなどを直感的に認識することになぞったもので，ロボットのピッキング作業などにも応用が可能である．実験としてAlexNetとInception-v4を用いた入力画像が安定しているかしていないかの二値分類や積み上げタスク（次にあるブロックをどこに置けばくずれないか）をあげている．

* [Fast and Precise Camera Covariance Computation for Large 3D Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Michal_Polic_Fast_and_Precise_ECCV_2018_paper.html)
    * ３次元復元においてカメラパラメータの不明確さを推定した論文。既存手法はいくつかのパラメータに制約を加えたり、計算量が大きいムーアペンローズの逆行列を用いていたが、提案手法では零空間を利用することで、高速かつ正確にカメラ共分散行列が計算できるようになった。

* [Inner Space Preserving Generative Pose Machine](http://openaccess.thecvf.com/content_ECCV_2018/html/Shuangjun_Liu_Inner_Space_Preserving_ECCV_2018_paper.html)
    * 画像全体の特徴""inner space""を保存しつつ，物体の様々なポーズに変更した画像を生成するconditional GANベースのinner space preserving generative pose machine (ISP-GPM)を提案．自然な形で画像中の人間のポーズだけ変わった画像を生成することができている．ISP-GPMはポーズの指定を行うLow-Dimensioanl Pose DiscriptorをCNNへ入力するためのCNN Interface Converterと，ポーズやテクスチャなどを段階的に学習する，Stacked Fully Convolutional Hourglass Conditional GANで構成される．またこの手法は生成画像のbackgroundを高精度に保存した画像を生成できていることが特徴である．

* [CTAP: Complementary Temporal Action Proposal Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiyang_Gao_CTAP_Complementary_Temporal_ECCV_2018_paper.html)
    * Temporal Action Proposalの検出として一般的に用いられる二つの手法，sliding windowsranking と actionness score groupingの互いの欠点を補完し，精度を上げるとして，入力としてsliding windowと actioness score groupingで得られるaction scoreとTAGを入力としてそれぞれを補完するようなフィルタをかける．それをtemporal CNNにかけて最終的な出力actionessを算出．両特徴量を用いた学習をすることによって精度が向上.

* [Learning to Reenact Faces via Boundary Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Wayne_Wu_Learning_to_Reenact_ECCV_2018_paper.html)
    * face reenactmentのためのGAN, Reenact GANの提案．顔の方向と，表情を同時に変換する．入力画像から直接，目的画像に変換するのではなく，一度boundary latent spaceに変換してから，目的画像への変換を行う. bounadary latent spaceとしてまず画像中から顔の輪郭を抽出するEncoder, 抽出した輪郭(input)から変換画像方向の輪郭へ変更するTransformer, Transformerで変更された輪郭をもとに目的画像を生成するDecoderの３つで構成される．boundary latent spaceをかませることで，Cycle GANと比較して，未知に対しても有効性が高い．

* [Fast and Accurate Intrinsic Symmetry Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Rajendra_Nagar_Fast_and_Accurate_ECCV_2018_paper.html)
    * メッシュ構造から固有の対象性を抽出するアルゴリズムを提案。具体的には固有値計算をLaplace-Beltramiの最適化問題を解くことで固有値問題に帰着させて導出した。従来より高い精度を導出している

* [Fictitious GAN: Training GANs with Historical Models](http://openaccess.thecvf.com/content_ECCV_2018/html/Yin_Xia_Fictitious_GAN_Training_ECCV_2018_paper.html)
    * GANのMin max最適化の箇所をzero-sum問題として解くことでゲーム理論のfictitious playによるナッシュ均衡を利用した勾配収束の式を定式化して、勾配変動問題と勾配収束問題について解決した。その上で既存の手法で精度の高いDCGANに組み合わせることでoriginalのDCGANよりも高いInception Scoreを算出した。

* [Audio-Visual Event Localization in Unconstrained Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Yapeng_Tian_Audio-Visual_Event_Localization_ECCV_2018_paper.html)
    * audio-visual event という問題の提案このタスクのために新たにAudio-Visual Event Datasetを作成，異なるモダリティを統合させるためのDual Multimodal Residual Network(DMRN)を提案．Audio Visual event task として，Fully and Weakly-Supervised Event LocalizationとCross-Modality Localizationを提案．前者は．音声と動画像の入力を与えたときに，その時のイベントの位置を推測する問題．例としてチェーンソーの音と人間がチェーンソーで木材を切っている動画があたえられたとき，チェーンソー付近にlocalizeする．後者は音声あるいは動画からそれと類似した動画，音声を選択するタスク．Audio単体，Visual単体より，Audio+Visualの方が各タスクにおいて精度がよかった．

* [Tackling 3D ToF Artifacts Through Learning and the FLAT Dataset](http://openaccess.thecvf.com/content_ECCV_2018/html/Qi_Guo_Tackling_3D_ToF_ECCV_2018_paper.html)
    * ToFカメラの撮影で発生するノイズをDNNを用いて事前に除去してからdepth推定を行うことが有効であることを示した．（元々ノイズを取り除くためにDNNを使用した研究がなかったらしい）またこのためのFLATデータセットを作成した．アプリケーション寄りの研究．

* [Self-Calibrating Isometric Non-Rigid Structure-from-Motion](http://openaccess.thecvf.com/content_ECCV_2018/html/shaifali_parashar_Self-Calibrating_Isometric__ECCV_2018_paper.html)
    * ３つの単眼カメラの動画から剛体でない物体(tシャツなど)の構造のキャリブレーション手法を初めて提案．単変量多項式を用いた焦点距離の算出からlocal shapeを算出．

* [Semi-Supervised Deep Learning with Memory](http://openaccess.thecvf.com/content_ECCV_2018/html/Yanbei_Chen_Semi-Supervised_Deep_Learning_ECCV_2018_paper.html)
    * 半教師あり学習の学習時に学習の中で得た情報を記憶し学習に用いる，メモリーを導入するモデル，Memory-Assisted Deep Neural Netowrok(MADNN)を提案.(記述途中)

* [Question-Guided Hybrid Convolution for Visual Question Answering](http://openaccess.thecvf.com/content_ECCV_2018/html/gao_peng_Question-Guided_Hybrid_Convolution_ECCV_2018_paper.html)
    * VQAに用いられるQuestion-Guided Hybrid Convolution(QGHC)ネットワークを提案した．従来の手法は画像と質問文の構想の特徴のヒュージョンを行い，より低層的で空間情報が含まれる特徴を重視されない．そこで，question-guided kernelsを提案し，それにより質問タイプごとに視覚特徴と質問文特徴をearly stageでヒュージョンする．また，提案手法のパラメータ数が従来のネットワークより多いので，group convolutionによりパラメータサイズの軽減を行う．提案のQGHCを様々従来のVQAネットワークに導入できる．

* [Rolling Shutter Pose and Ego-motion Estimation using Shape-from-Template](http://openaccess.thecvf.com/content_ECCV_2018/html/Yizhen_Lao_Rolling_Shutter_Pose_ECCV_2018_paper.html)
    * カメラのローリングシャッター現象（速い被写体を撮影したときにゆがんだ画像になる）に対して，力学的な情報を用いず，補正画像を生成する，RS Pose and Ego-motion Estimation (RS-PEnP)を提案．この推定は，3D-3D registration problem.と置き換えることができる．RS画像と，既知の3D情報(=どこまでのテンプレートを求めているのかは不明)を用いてSftで3次元の仮想的なdeformed shapeを取得．deformed shapと既知の3D情報から，RSカメラの位置と姿勢がわかる．提案手法は既存手法と比較して補正精度が大幅に上昇．

* [Semi-Dense 3D Reconstruction with a Stereo Event Camera](http://openaccess.thecvf.com/content_ECCV_2018/html/Yi_Zhou_Semi-Dense_3D_Reconstruction_ECCV_2018_paper.html)
    * ステレオイベントカメラ画像から検出した物体の3D構造を推定するための手法の提案．各カメラ画像から生成されるイベントマップの誤差が小さくなるような損失関数を定義して学習．

* [Local Orthogonal-Group Testing](http://openaccess.thecvf.com/content_ECCV_2018/html/Ahmet_Iscen_Local_Orthogonal-Group_Testing_ECCV_2018_paper.html)
    * 画像検索タスクにおいて，nearest-negibor searchの近似を行った手法を提案．off lineで制約をつけたベクトル定義によって検索対象の変換ベクトルを生成．類似したクエリは近傍に位置するような制約を設ける．クエリ検索時はそのベクトルをもとに検索を行うことで検索効率が向上．

* [Temporal Relational Reasoning in Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Bolei_Zhou_Temporal_Relational_Reasoning_ECCV_2018_paper.html)
    * 時間的に離れたフレームを入力として、それらの間に起きた行動を推定するネットワーク（TRN: Temporal Relation Networks）を提案した論文。サンプリングしてくるフレームを2, 3, 4フレームと変えて、multi-scaleに推定を行い、それを最後に統合する。Two-Stream CNNと3DCNNに勝っているとのことなので、新しいブランチとして派生するかも？

* [Deep High Dynamic Range Imaging with Large Foreground Motions](http://openaccess.thecvf.com/content_ECCV_2018/html/Shangzhe_Wu_Deep_High_Dynamic_ECCV_2018_paper.html)
    * 被写体の動きが大きいLDR画像数枚を用いてHDR画像を作成するにあたって，オプティカルフローを用いない，DNNを使用した手法を提案．従来の手法と比較して，不自然なghostがない画像を生成した．ネットワークは3枚の入力それぞれに対するEncoder, それらをまとめるMerger, HDRを生成するDecoderで構成される．それぞれU-NetまたはRes-Netを用いている．

* [Geometric Constrained Joint Lane Segmentation and Lane Boundary Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Jie_Zhang_Geometric_Constrained_Joint_ECCV_2018_paper.html)
    * 車線のセグメンテーションと境界の検出を同時に解くマルチタスクなフレームワークを艇あ飲した。共通のEncoderを通った後、セグメンテーションと境界検出ごとのDecoderがあり、これらのDecoderはお互いに相補し合うようにLink Encoderが導入されている。

* [Attributes as Operators](http://openaccess.thecvf.com/content_ECCV_2018/html/Tushar_Nagarajan_Attributes_as_Operators_ECCV_2018_paper.html)
    * 画像の属性値(Attributuin)をOperatorと考え，学習を行う方法を提案．sliceの場合，リンゴがスライスされた画像でなく，スライスによってどのようにobjectが変更するかというoperatorとして学習をさせる．

* [Textual Explanations for Self-Driving Vehicles](http://openaccess.thecvf.com/content_ECCV_2018/html/Jinkyu_Kim_Textual_Explanations_for_ECCV_2018_paper.html)
    * 自動運転においてDNNは欠かせない技術であるが、ブラックボックスである。本論文は「現在どのような運転がされていて、なぜそのような運転をしているか」というような道理の通ったテキストによる説明を生成するネットワークを提案した。

* [Generative Domain-Migration Hashing for Sketch-to-Image Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Jingyi_Zhang_Generative_Domain-Migration_Hashing_ECCV_2018_paper.html)
    * 運転中に運転者から見えている映像（車載カメラから見える映像）からヒートマップを作成するモデルから自動運転のモデルについて考えたもの。attentionのかかり方やdetectionのされ方によって、ドライバーの運転を模倣しているというもの

* [Recurrent Fusion Network for Image captioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Wenhao_Jiang_Recurrent_Fusion_Network_ECCV_2018_paper.html)
    * image captioning のencoderを複数個で学習，各出力結果として得たsemanticsを統合して全体としてより良いcaptionを生成するための，fusion procedureを提案．各encoderからの出力結果の相関をRNNを用いてthought vectorとして導出，相関の高いものからMulti-attentionにかけて最終的なthought vectorを生成，RNNでcaptionを生成．CNNのアンサンブル学習でimage captionの精度をあげた．といえる

* [Attention-based Ensemble for Deep Metric Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Wonsik_Kim_Attention-based_Ensemble_for_ECCV_2018_paper.html)
    * DNNを用いたMetric Learningはアンサンブル学習が非常に良い精度を出している。アンサンブル学習では、各々が異なる埋め込み関数を学習することが重要である。そこで本論文では、アテンションを用いて、それぞれ異なる物体の領域に着目するようなアンサンブル学習手法を提案した。これを実現するためにdivergence lossを提案した。

* [Egocentric Activity Prediction via Event Modulated Attention](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Shen_Egocentric_Activity_Prediction_ECCV_2018_paper.html)
    * 一人称視点動画において行動予測を行った論文。視線に基づく注視に値するイベントの予測を行うことがでい、特にlong-termなイベントの依存性を考慮することを可能にした。今後、一人称視点動画では認識だけでなく、予測も行われていくことを示唆している。

* [A+D Net: Training a Shadow Detector with Adversarial Shadow Attenuation](http://openaccess.thecvf.com/content_ECCV_2018/html/Hieu_Le_AD_Net_Training_ECCV_2018_paper.html)
    * 画像中の影の部分を抽出する，GANベースのモデルの提案．影部分を減衰させるA-Net(画像中の影部分を減衰させることで，影の抽出を困難に故意にさせて，D-Netの精度をあげることが目的)と影部分を抽出するD-Netの二つのネットワークで構成される．未知への適用時は，D-Netのみを用いて影領域を推定する．SBU shadow datasetとUCFdatasetに適用，state-of-the-artと比較しても，Balanced Error Rate (BER)が最も小さかった．影の濃さを減衰させた画像もD-Netで学習させることで，提案手法は様々な影の濃さに対応することが出来ている。

* [Stereo Vision-based Semantic 3D Object and Ego-motion Tracking for Autonomous Driving](http://openaccess.thecvf.com/content_ECCV_2018/html/Peiliang_LI_Stereo_Vision-based_Semantic_ECCV_2018_paper.html)
    * 3DのBounding Boxを獲得するためのsemanticな推定と、camera特有の動きについて獲得するために動的な物体に対してbundle adjustmentを提案して、3D objectのポーズや加速度について獲得した。semantic priorとsparseな特徴量とキネティックスの動作モデルを最適化問題として式にまとめて最適化を行った。IOUが高い場合において高い精度を算出している。将来的にはdenseな視覚情報からtemporalな特徴量を考慮される。

* [End-to-end View Synthesis for Light Field Imaging with Pseudo 4DCNN](http://openaccess.thecvf.com/content_ECCV_2018/html/Yunlong_Wang_End-to-end_View_Synthesis_ECCV_2018_paper.html)
    * 4Dライトフィールドを構築するための，end-to-endの疑似4DCNNをstacked EPI(Epipolar Plane Images)に対する2D stride convolution, 3DCNNによる画像の再構築を角度変更を介して行うことで実現.既存のstate-of-the-artより高い精度を得た．スパースな入力画像から密な4D light fieldを合成できることが特徴

* [Robust image stitching using multiple registrations](http://openaccess.thecvf.com/content_ECCV_2018/html/Charles_Herrmann_Robust_image_stitching_ECCV_2018_paper.html)
    * image stitchingやパノラマ画像作成の際に、一つの画像に対して一つのアラインメントを取るsingle registrationは、画像中に動く物体があった場合に、どちらかに焦点が当たったり、間を取ってどちらからもずれたりする。本論文では、異なるデプスごとに別々にアラインメントを取るmultiple registrationを提案した。その結果、画像中を移動する物体があった場合でも頑健にパノラマ画像生成が可能になった。

* [Fast Multi-fiber Network for Video Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Yunpeng_Chen_Fast_Multi-fiber_Network_ECCV_2018_paper.html)
    * 3DCNNの計算コストを削減する，学習パラメータが減少するが，精度は維持されるMulti-Fiber-Netoworkを提案．このfiberをN本入れた場合，学習速度がN倍速くなりかつ，精度は同程度．入力Min,中間層Mmid,出力Mout（それぞれチャネル数）とおくと，通常Connection=Min*Mmid+Mmid*Mout. 対して並列に分割すること(提案するMulti-Fiber)でConnection=(Min*Mmid+Mmid*Mout)/Nに削減することができる．また，Fiber間の接続として、multiplexerを導入することを提案．UCF-101, HMDB-51,Kinetics

* [TBN: Convolutional Neural Network with Ternary Inputs and Binary Weights](http://openaccess.thecvf.com/content_ECCV_2018/html/Diwen_Wan_TBN_Convolutional_Neural_ECCV_2018_paper.html)
    * CNNを，bianry, Ternaryを用いて既存のCNNのパラメータを近似することで学習の高速化を図る．XOR,And, Bitcount操作を導入することで，最大32倍のメモリ量の削減，40倍の学習速度を実現．VOC datasetを用いて検証．既存のbinary netと比較してmAPが5%程上昇．

* [Contextual Based Image Inpainting: Infer, Match and Translate](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuhang_Song_Contextual_Based_Image_ECCV_2018_paper.html)
    * InpaintingをInferenceステップとTranslationステップの２ステップで行った。InferenceステップはImage2Feature networkを用いて、欠けた領域を初期化する。この結果は非常にブラーがかかっているため、TranslationステップはFeature2Image networkを用いて、よりリアルでシャープな結果を得る。これはTexture Refinementをモデル化している。

* [Deep Fundamental Matrix Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Rene_Ranftl_Deep_Fundamental_Matrix_ECCV_2018_paper.html)
    * 外れ値を含んでいる行列から頑丈な推定を行う手法で、計算時間を考慮した上で最新の手法より高い精度を算出した。いろんなデータセットに対して精度を算出していて、汎用性が将来期待される理論となっている

* [Joint Person Segmentation and Identification in Synchronized First- and Third-person Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Mingze_Xu_Joint_Person_Segmentation_ECCV_2018_paper.html)
    * 複数カメラから映る同じ人の特定を異なるカメラから取り出したRGB情報とoptical flowの情報から出力されたものに対してSiamese Networkをかけたものによって特定、異なるカメラを入力として発生したcontrasive lossに対して、それを最小化するように学習を行い、良い精度を算出した

* [Linear Span Network for Object Skeleton Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Chang_Liu_Linear_Span_Network_ECCV_2018_paper.html)
    * 画像から物体の骨格を推測するための，Linear-Span Units を導入したLinear Span Networkを提案．従来提案されたHolistically-nested Edge Detectionをベースとし，各層ごとの特徴量を線形に足し合わせたlossを計算できるようなユニットを導入することで，skelton detectionのstate-of-the-artより高い検出精度を獲得．

* [Category-Agnostic Semantic Keypoint Representations in Canonical Object Views](#N/A)
    * ※参照リンクなし，google scholarなどの検索にもかからないため評価できない

* [Where are the blobs: Counting by Localization with Point Supervision](http://openaccess.thecvf.com/content_ECCV_2018/html/Issam_Hadj_Laradji_Where_are_the_ECCV_2018_paper.html)
    * detection-baseのobject-countを使用した提案手法。regression-baseだとcountよりも難しいサイズの推定などで高い精度を算出したがloss function(Image-lebel loss,key-point loss, split-level loss,false positive lossを同時に考えたloss関数)と複数のmethod(Line split method, watershed split method)を採用することで様々なdatasetに対して高い精度を算出した。

* [A Hybrid Model for Identity Obfuscation by Face Replacement](http://openaccess.thecvf.com/content_ECCV_2018/html/Qianru_Sun_A_Hybrid_Model_ECCV_2018_paper.html)
    * 指定した画像中の顔を別の人の顔に自然な形で変換するためのGANベースのモデルの提案．Stage-Iですり替えたい領域にあてはまる顔画像を生成，Stage-IIで生成した顔画像と元画像とが自然につながるように変換を行う．Stage-I, Stage-IIそれぞれに，対応するGANでネットワークを学習．より現実的な画像を生成した．

* [Exploring the Limits of Supervised Pretraining](http://openaccess.thecvf.com/content_ECCV_2018/html/Dhruv_Mahajan_Exploring_the_Limits_ECCV_2018_paper.html)
    * CNNの事前学習に関する検討を実施した論文。Instagramから画像とともにラベルも自動抽出したBillion-orderのデータセットを学習すると、ImageNetにてTop-1が85%（Top-5では98%弱）出ると結果となった。

* [TrackingNet: A Large-Scale Dataset and Benchmark for Object Tracking in the Wild](http://openaccess.thecvf.com/content_ECCV_2018/html/Matthias_Muller_TrackingNet_A_Large-Scale_ECCV_2018_paper.html)
    * 30Kの数のvideo+14millionの狭い領域でのBounding Boxがついたデータセットで従来のデータセットと比べ、大幅に数の多さを示しているデータセットの提案。VATIC toolのoptical flowでつけたannotation結果に対してすべてのフレームで間違っているかどうかを確認して、データの質を担保する。特にOfflineでのTrackingで精度の改善を示していて、いくつかのネットワーク（CFNetなど）では効果を示していないことも示している

* [Unpaired Image Captioning by Language Pivoting](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiuxiang_Gu_Unpaired_Image_Captioning_ECCV_2018_paper.html)
    * 画像の説明タスクにおいて，キャプションとして与えられていない言語に変換するときに一度中間言語pivot languageを用いてから言語を変換する手法を提案．流れとしては画像->pivot languageでの説明->目的言語での説明.画像->pivot language間は画像認識，pivot language->目的言語は機械翻訳．学習にはAIC Image Chinese Captioning (AIC-ICC)，AIC Chinese-English Machine Translation (AIC-MT)を用い，テストにMSCOCO とFlickr30K English captioning datasetsを使用．画像から直接説明言語を出力するよりも一度中間言語を介してからのほうがSelf-BLEUscoreが高く，精度が良い．同じタスクの比較はそもそも取り扱っている研究がないため難しかったようだ

* [Pairwise Relational Networks for Face Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Kang_Pairwise_Relational_Networks_ECCV_2018_paper.html)
    * 既存の顔認識技術は非常良い精度を出しているが、どこに着目しているかわからなかった。本論文では、顔の特徴点周辺の局所領域ごとの関係性を獲得するネットワーク（PRN：Pairwise Relational Network）を提案した。

* [DeepPhys: Video-Based Physiological Measurement Using Convolutional Attention Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Weixuan_Chen_DeepPhys_Video-Based_Physiological_ECCV_2018_paper.html)
    * Attention機構を導入したDNNでRGB動画または赤外線動画から被写体の心拍数，呼吸速度を推定．

* [Semantic Match Consistency for Long-Term Visual Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Carl_Toft_Semantic_Match_Consistency_ECCV_2018_paper.html)
    * 日や季節の変化を考慮したLong-TermなVisual-Localizationタスクに対する頑丈性のあるモデルの提案.入力する自然画像に対して3D Scene Modelを作成して、2D-3DマッチングしたものとSemantic SegmentationしたもののSemantic Consistency Scoringを算出してlocalizationをしたもの

* [Grounding Visual Explanations](http://openaccess.thecvf.com/content_ECCV_2018/html/Lisa_Anne_Hendricks_Grounding_Visual_Explanations_ECCV_2018_paper.html)
    * 画像の説明タスクの手法として，負例をあえて学習させることで…という特徴があり，…という特徴がないので…である，というようになぜ負例が違うのかも評価することで精度があがるという仮定のもと，phrase-criticモデルを導入，説明タスクの精度が向上．まず画像から説明文章を生成するCNNで説明文章を生成．その文章から抽出するキーワードと元の画像を入力として次にキーワードと画像が合致しているかを評価．またこのキーワードの一部を間違えさせた負例を用意し，そのキーワードと画像の合致率が低くなるように学習を行う．

* [Cross-Modal Hamming Hashing](http://openaccess.thecvf.com/content_ECCV_2018/html/Yue_Cao_Cross-Modal_Hamming_Hashing_ECCV_2018_paper.html)
    * Hamming Space Retrievalに適したHashing手法（CMHH：Cross-Modal Hamming Hashing）を提案した。CMHHは画像の特徴量抽出器、テキストの特徴量抽出器のあとにhashing layerがついており、それらの出力に対してexponential focal lossをisomorphic Hamming空間上で取る。

* [A Modulation Module for Multi-task Learning with Applications in Image Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiangyun_Zhao_A_Modulation_Module_ECCV_2018_paper.html)
    * Image RetrivalのタスクにおいてのMulti task学習で２つのtaskの相関や関係性が薄い際に発生する不機能性に対してのmodulation modelを提案したもの。それぞれのtaskから獲得できるembeddingをCNNの出力層と足し合わせて最終的な答えを出しているモデル。画像から簡単な質問に答えるタスクに対してわずかに既存手法よりも高い精度を算出した。

* [Open-World Stereo Video Matching with Deep RNN](http://openaccess.thecvf.com/content_ECCV_2018/html/Yiran_Zhong_Open-World_Stereo_Video_ECCV_2018_paper.html)
    * ステレオ動画を入力として，教師なし学習でdepth画像を出力するネットワークOpen Stereo Netの提案．特徴量抽出のFeature net, depth推定のMatch Net, フレーム間の差違を考慮するためのLSTMで構成される．損失関数は，warping errorと正則化項の足し合わせ．warping error は入力の片方の画像(e.g. Input_left)と出力された反対側の視差画像(e.g. disparity_right)の構造の類似度を表す．disparity_rightを平行移動させることで，画像中の構造が類似していればよい．これをSSIMを用いて表現している．MInput_leftとKITTI, Middlebury,Synthia,Frieburg SceneFlowに対して適用．unsupervisedで学習をおこなえるようにしたため，未知に対しても既存手法より精度の高いdepthマップを出力することができている．

* [Deblurring Natural Image Using Super-Gaussian Fields](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuhang_Liu_Deblurring_Natural_Image_ECCV_2018_paper.html)
    * マルコフ確率場が直面しているブラーkernel(BID)をうまく扱えない問題に対して超ガウシアン空間モデルを定義して、BIDをうまくとりあえ使うようにしたもの

* [Diverse and Coherent Paragraph Generation from Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Moitreya_Chatterjee_Diverse_and_Coherent_ECCV_2018_paper.html)
    * VAEを用いた画像からのキャプション生成のタスクで、画像からdetectionを行ったものに対してSentence RNNをかけて抽出したglobal vectorをconcatして出来たvectorとその前に出来たvector表現から文章を生成するというもの。KL-lossを優先させた上でreconstruction lossも定めて最小化を行った

* [Learning Compression from limited unlabeled Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiangyu_He_Learning_Compression_from_ECCV_2018_paper.html)
    * 圧縮したCNNモデルに対して精度を出すための正規化手法を提案。具体的にはガウス分布のような特徴量分布をKL divergenceを小さくするように正規化をすることで十分に訓練がされたモデルを作成するという手法、quantizationとpruningにおいて精度の改善を見せている

* [Deep Video Quality Assessor: From Spatio-temporal Visual Sensitivity to A Convolutional Neural Aggregation Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Woojae_Kim_Deep_Video_Quality_ECCV_2018_paper.html)
    * 時間・空間的な人間の視覚の感覚を、動画の質の査定に組み込むネットワーク（DeepVQA：Deep Video Quality Assessor）を提案した。今回提案した手法はfull-referenceな手法だったため、今後non-referenceな手法を行う予定である。

* [Product Quantization Network for Fast Image Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Tan_Yu_Product_Quantization_Network_ECCV_2018_paper.html)
    * 高次元の特徴量を画像から取り出す時に使用される直積量子化を使用してhard assignmentをsoft assignmentに採用する際に直積量子化を組み込むことで、層をCNNとして使用することができるという論文でそのNetworkについて提案を行っている(PQN)。ビット数に対する比較において高いmAPの精度を出している

* [Factorizable Net: An Efficient Subgraph-based Framework for Scene Graph Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yikang_LI_Factorizable_Net_An_ECCV_2018_paper.html)
    * シーングラフの効率化のためにサブグラフの隣接グラフを提案。空間情報がサブグラフの特徴量で維持されて、計算コストも削減された。画像からRPNで抽出した領域に対してグラフを形成、出来たサブグラフからROI-poolingを行ってObject間の関係性についての認識を行う

* [C-WSL: Count-guided Weakly Supervised Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Mingfei_Gao_C-WSL_Count-guided_Weakly_ECCV_2018_paper.html)
    * an asymmetric triplet lossとCNNに対してquantizationを行うことによって、識別可能でcompactな画像取得のモデルについて考えた。ここで提案されたOQNによって既存のデータセットにおいて高い精度のものを記録することが出来た。

* [The Sound of Pixels](http://openaccess.thecvf.com/content_ECCV_2018/html/Hang_Zhao_The_Sound_of_ECCV_2018_paper.html)
    * ラベルの付いていないビデオのデータに対して、別々の場所から得た音源を利用して物体のlocalizationタスクについて解いている。具体的にはvideoのsequenceデータに対してResNetから特徴量を得た後に、それに対してmaxpoolingを、対して音源からはspectgramを入手して、２つの特徴量を混ぜ合わせて最終的な出力を出している。音源分離のタスクについて精度を向上させたものとなった

* [Unsupervised Video Object Segmentation using Motion Saliency-Guided Spatio-Temporal Propagation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuan-Ting_Hu_Unsupervised_Video_Object_ECCV_2018_paper.html)
    * 教師なしsegmentationの際に問題となっているmotion, blur, occlusionなどに対してoptical flowやedge cueを使用して、前景-背景予測を可能にした・具体的にはmotion saliencyをboundary dissimilarity mapと距離mapを使用してscoringしたもの。多くのデータセットに対して精度の改善が見られた。

* [Good Line Cutting: towards Accurate Pose Tracking of Line-assisted VO/VSLAM](http://openaccess.thecvf.com/content_ECCV_2018/html/Yipu_Zhao_Good_Line_Cutting_ECCV_2018_paper.html)
    * 信頼性の小さい3D上のラインを使用して、ポーズ推定を考えたもの。VO/VSLAMという特徴点を取り出す方法に加えて、Blurやlow-textureなものに対しても考慮できるような最適化について考えて既存手法より良い結果を算出した

* [Bi-box Regression for Pedestrian Detection and Occlusion Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/CHUNLUAN_ZHOU_Bi-box_Regression_for_ECCV_2018_paper.html)
    * detectionしたデータに対して、visibleな情報からfull bodyの情報を予測するというネットワークを作成。ROI Poolingから全身を予測するNetworkと見える場所のみを予測するNetworkをマルチタスク化しているPDOEが、FRCNNをベースラインとしてそれを上回る結果を残している

* [Unveiling the Power of Deep Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Goutam_Bhat_Unveiling_the_Power_ECCV_2018_paper.html)
    * 各特徴量とその精度及びrobustnessについて分析・adaptive fusionを提案。Blurなimageをdata argumentationで増やすことで精度が改善することを示す。またdeepのfeatureとshallow featureで出したdetection scoreそれぞれに対して重み付けしたパラメーターを最小化する最適化問題を2次計画化問題として解くことでSingle Object trackingの改善を試みて、精度が改善したことを示した

* [Multi-Scale Structure-Aware Network for Human Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Lipeng_Ke_Multi-Scale_Structure-Aware_Network_ECCV_2018_paper.html)
    * Human Pose EstimationのためのMulti-scale Structure-aware Nerual Networkを提案した。Multi-scale Structure-aware NetworkはMulti-scale Supervision Network（MSS-net）とMutli-scale Regression Network（MSR-net）からなる。これらのネットワークはマルチスケールな特徴量が抽出でき、人体の構造に基づいた損失を用いることで、頑健なHuman Pose Estimationが可能になった。

* [Neural Graph Matching Networks for Fewshot 3D Action Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Michelle_Guo_Neural_Graph_Matching_ECCV_2018_paper.html)
    * Few-Shot 3D Action Recognitionのためのネットワーク（NGM：Neural Graph Matching Network）を提案した論文。NGMはGraph GenerationとGraph Matching Metricからなり、End-to-Endに学習できる。

* [Objects that Sound](http://openaccess.thecvf.com/content_ECCV_2018/html/Relja_Arandjelovic_Objects_that_Sound_ECCV_2018_paper.html)
    * 教師なしaudio-visual corresponding taskの提案(AVE-Net・AVOL-Net)。imageと音声を入力したものを2 streamにしてL2正規化したものをsoftmaxで返すNetworkで2値分類とLocalizationを行っている。imageと音声を入力する際のNetworkは別々に学習させて、それをConcatしていて、上で述べたNetworkを作成している。VGGを使ったものよりも高い精度を算出している

* [Discriminative Region Proposal Adversarial Networks for High-Quality Image-to-Image Translation](http://openaccess.thecvf.com/content_ECCV_2018/html/Chao_Wang_Discriminative_Region_Proposal_ECCV_2018_paper.html)
    * Image-to-Imageの変換をする際に、1.少量の人工的に作成した箇所を作成2.その画像に対して人工的に作られたであろう領域をDRPAN(提案手法）で推定して、3.その領域に対してInpatingをすることで変換を行うもの。様々なタスク(人の評価、Segmentation、Inpatingなど）において高い精度を示した。

* [SaaS: Speed as a Supervisor for Semi-supervised Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Safa_Cicek_SaaS_Speed_as_ECCV_2018_paper.html)
    * ラベルの正誤をモデルのパラメーターを推定しないでTrainin Speedで正しいラベルの数を推定したというもの。未知のラベルの確率分布を学習しながら更新しつつ、それが収束した後に確率分布から尤度を計算することでラベルを正しさを判定して、次の段階でそれを利用した教師あり学習を行っている。Virtual adversarial trainingには負ける点はあるもののシンプルなアルゴリズムで高い精度を示した。

* [Adaptive Affinity Field for Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Jyh-Jing_Hwang_Adaptive_Affinity_Field_ECCV_2018_paper.html)
    * 従来のSementic Segmentationはラベル付けをしていくタスクであったが、提案手法は周辺のピクセルとのsemantic relationをラベル空間上で取得するAdaptive Affinity Fieldsという概念を提案した。学習もGANより行いやすく、高い精度を出すことに成功した。

* [Semi-convolutional Operators for Instance Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Samuel_Albanie_Semi-convolutional_Operators_for_ECCV_2018_paper.html)
    * Mask-RCNNのようなタスクをCNNを用いたinvariant pixel embeddingによる転換と半教師ありのposition sensitive embeddingにより、行ったというもの。Average Precisionによる評価でMRCNNにくらべ良い結果、segmentationのタスクにおいて一番良い結果を残したことを示した

* [Effective Use of Synthetic Data for Urban Scene Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Fatemeh_Sadat_Saleh_Effective_Use_of_ECCV_2018_paper.html)
    * 通常合成画像で学習したNetworkの精度は低いが合成画像のみで学習させたモデルで精度をあげたもの。前景と後景のsemantic segmentationをrealな画像を見ることなく学習しながら予測を行い、ラベルなし画像に対してdomain適用を行うことでpsudo-labelingを行い学習をさせて安定した精度を示すことが出来た

* [Shape correspondences from learnt template-based parametrization](http://openaccess.thecvf.com/content_ECCV_2018/html/Thibault_Groueix_Shape_correspondences_from_ECCV_2018_paper.html)
    * 入力のポーズとテンプレートのポーズの対応を取る論文。encoder-decoder型のネットワークで、encoderは入力のポーズを潜在変数に落とし、decoderはその潜在変数とテンプレートのポーズを入力として入力のポーズを復元するように学習する（入力・出力ともにPoint Cloud）。

* [TextSnake: A Flexible Representation for Detecting Text of Arbitrary Shapes](http://openaccess.thecvf.com/content_ECCV_2018/html/Shangbang_Long_TextSnake_A_Flexible_ECCV_2018_paper.html)
    * これまで文字を検出する場合、軸に並行な矩形や回転ありの矩形や四角形等で検出を行ってきたが、現実には円上に並んでいたりぐにゃぐにゃになっていることが多々ある。そこで任意の配置のテキストに対応できる柔軟な表現としてText Snakeを提案した。

* [How good is my GAN?](http://openaccess.thecvf.com/content_ECCV_2018/html/Konstantin_Shmelkov_How_good_is_ECCV_2018_paper.html) [[GitHub](http://thoth.inrialpes.fr/research/ganeval/)]
    * GANの評価方法の提案を行なった論文。従来のInception ScoreやFrechet Inception Distanceに代わる評価としてGANで生成した画像を学習画像（GAN-train）やテスト画像（GAN-test）として使用することを提案。従来のGANの性能と相関して良好なスコアを出した（SoTAと言われるSNGANが最もよかった）ことから良い評価指標と位置付けた。

* [Deep Generative Models for Weakly-Supervised Multi-Label Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Hong-Min_Chu_Deep_Generative_Models_ECCV_2018_paper.html)
    * WS?MLCの問題を解く際にmulti-labelについて解くだけでなくa sequential network architectureで事後分布の推定も可能なWS-MLCを提案した。semi-supervisedな従来手法、ラベルなしデータを含むデータセットでのMLCの手法の比較でいい結果を示した

* [Attention-GAN for Object Transfiguration in Wild Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Xinyuan_Chen_Attention-GAN_for_Object_ECCV_2018_paper.html)
    * object transfiguration問題のためのattention-GANを提案．従来，object-transfigurationでは，背景も含めた，画像を一括で変換し，objectを変換していた．（e.g.Cycle-GAN）提案手法はGANのネットワークをattention-network, transfiguration network, discriminator-networkの3つを使用して学習を行う．attention networkで変換対象領域を推測し，transfiguration networkで変換された画像をattentionの結果でマスクを行う．attentionの高い箇所はtransfigurationの結果が反映され，attentionの小さい箇所は元画像の背景の影響が大きくするように合成し，最終出力とする．Cycle GANと比較してattentionを用いることで変換画像の質が向上した．

* [Skeleton-Based Action Recognition with Spatial Reasoning and Temporal Stack Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Chenyang_Si_Skeleton-Based_Action_Recognition_ECCV_2018_paper.html)
    * 従来のスケルトンベースの行動認識は、空間的な構造情報や動的（時間的）な特徴を考慮できていなかった。そこで空間的構造を理解するSpatial Reasoning Networkと動的特徴を抽出するTemporal Stack Learning Networkを用いたネットワークを提案した。Spatial Reasoning NetworkにはResidual Graph Neural Networkが使用されており、Temporal Stack Learning NetworkはVelocity NetworkとPosition NetworkのTwo-Stream構造になっている。従来手法を圧倒する精度を出している。

* [Efficient Sliding Window Computation for NN-Based Template Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Lior_Talker_Efficient_Sliding_Window_ECCV_2018_paper.html)
    * nearest neighbor(NN)に基づく検出アルゴリズムは視点変化やオクルージョンに頑強であったが、計算効率が悪く時間がかかっていた。今回提案した効率的なNNに基づくアルゴリズムは既存手法と比べ同程度の精度を示す一方で、43～200倍計算速度が向上した。

* [Learning to Reconstruct High-quality 3D Shapes with Cascaded Fully Convolutional Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Yan-Pei_Cao_Learning_to_Reconstruct_ECCV_2018_paper.html)
    * ノイズが存在したりや一部分が欠けているdepth情報から生成される3次元入力を効率的で高精度に再構築する３D convolutional networkを提案した。architectureでは2つの３D-FCNがあり、1つ目は低解像度入力からrefineすべき部分を特定し、2つ目では特定された部分について入力してrefineする。最後に再構築を行い全体を構成する。

* [Deep Reinforcement Learning with Iterative Shift for Visual Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Liangliang_Ren_Deep_Reinforcement_Learning_ECCV_2018_paper.html)
    * 強化学習(actor-critic)を用いて、single object trackingを行った研究。強化学習で訓練されたAgentが物体の「B.B.の位置をアップデートする」や「画像特徴量を再計算」などの行動を決定することで、従来手法よりも高速な計算が可能となった。OTBベンチマークでは従来のSoTAより1.7%よい精度を4倍高速に計算可能。

* [CPlaNet: Enhancing Image Geolocalization by Combinatorial Partitioning of Maps](http://openaccess.thecvf.com/content_ECCV_2018/html/Paul_Hongsuck_Seo_Enhancing_Image_Geolocalization_ECCV_2018_paper.html)
    * Image geolocalization の研究。従来の手法の多くは地図を複数の領域に分割し、どの領域で撮影された画像かをクラス分類する問題として考えられているが、分割の粒度には trade-off の問題があった。（分割サイズが大きすぎると場所の精度が下がってしまうが、小さすぎるとモデルが大きくなり、学習データが足りず overfittingしてしまう。）そこで、提案手法では粒度は荒いが、分割の仕方が異なる複数のMapを同時に用いることで、上述の問題を解決した。最終的にClassifierによって投票された領域の共通部分を取ることで、粒度の細かい結果を得られる。Im2GPS3kやYFCC4k datasetでSotAを達成。

* [Bayesian Instance Segmentation in Open Set World](http://openaccess.thecvf.com/content_ECCV_2018/html/Trung_Pham_Bayesian_Instance_Segmentation_ECCV_2018_paper.html)
    * open-set semantic instance segmentation の研究。学習時にはデータが無かった未知の物体を含む画像中の全ての物体に対してinstance segmentationを行う手法（このような手法は初めてと主張）を提案。 NYU と COCO dataset で完全な教師ありの手法と同等の結果を達成。

* [Characterizing Adversarial Examples Based on Spatial Consistency Information for Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/CHAOWEI_XIAO_Characterize_Adversarial_Examples_ECCV_2018_paper.html)
    * adversarial exampleの研究。adversarial exampleは画像のクラス分類の問題においてはよく研究されているが、それ以外の問題ではあまり議論されてこなかった。semantic segmentationのタスクにおいて空間的なコンテクスト情報を用いて、adversarial exampleを見分ける実験を行った。空間的な一貫性の情報がadversarial exampleのロバストな判別に有効であることを発見した。

* [CubeNet: Equivariance to 3D Rotation and Translation](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Worrall_CubeNet_Equivariance_to_ECCV_2018_paper.html)
    * voxelized data を入力とするCNNに付いての研究。入力の３次元回転に対して不変なCNNのアーキテクチャを初めて提案。 ModelNet10 classification challenge でSotA を達成。

* [3D Face Reconstruction from Light Field Images: A Model-free Approach](http://openaccess.thecvf.com/content_ECCV_2018/html/Mingtao_Feng_3D_Face_Reconstruction_ECCV_2018_paper.html)
    * model-free 3D face reconstruction の研究。1枚の light field image から 3D face reconstruction network を用いて depth map を推定し、point clooud、mesh の順で復元を行う。model-freeな手法で model fitting や landmark の検出は用いていないため、 facial expressionsやpose 、illuminationのバリエーションに頑強で大量の学習データも必要としない。提案手法は BU3DFE、BU-4DFE dataset の SotA を達成。（先行研究より reconstruction error を 20%以上減 ）

* [stagNet: An Attentive Semantic RNN for Group Activity Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Mengshi_Qi_stagNet_An_Attentive_ECCV_2018_paper.html)
    * 3人称視点動画を用いたgroup activity recognitionの研究。空間的コンテクスト情報を表すsemantic graphをRNNに入力することで、時空間情報を取り扱っている。key person/frameを強調するため、spatial-temporal attention を導入。

* [Supervising the new with the old: learning SFM from SFM](http://openaccess.thecvf.com/content_ECCV_2018/html/Maria_Klodt_Supervising_the_new_ECCV_2018_paper.html)
    * ラベル付けされていない動画からego-motionやdepth推定を行うネットワークを頑強にする手法を提案。structural similarity lossの導入、explainability mapを確率モデル化、伝統的handcraftなSfMを教師信号として使う方法を提案。

* [PSANet: Point-wise Spatial Attention Network for Scene Parsing](http://openaccess.thecvf.com/content_ECCV_2018/html/Hengshuang_Zhao_PSANet_Point-wise_Spatial_ECCV_2018_paper.html)
    * CNNはその構造上、情報の伝搬が局所的になってしまうという性質を緩和するためのアーキテクチャ、point-wise spatial attention network (PSANet) を提案。全ての場所の feature map が 自己適用的に学習される attention mask によって繋がっており、双方向に情報が伝搬される。

* [FishEyeRecNet: A Multi-Context Collaborative Deep Network for Fisheye Image Recti_x000c_cation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaoqing_Yin_FishEyeRecNet_A_Multi-Context_ECCV_2018_paper.html)
    * 魚眼レンズカメラで撮影された画像に生じる歪みを修正する研究（Fisheye image rectification）。1枚の Fisheye image から歪みを除去する end-to-end な networkを提案。hand-craft な特徴量を使用する従来手法とは異なり、提案手法では high-level の semantics と low-level の特徴量を同時に学習し、歪みパラメータの推定を行う。synthesized data と 実画像の両方でSotAの精度を達成。

* [ELEGANT: Exchanging Latent Encodings with GAN for Transferring Multiple Face Attributes](http://openaccess.thecvf.com/content_ECCV_2018/html/Taihong_Xiao_ELEGANT_Exchanging_Latent_ECCV_2018_paper.html)
    * 複数の face attribute を同時に transfer 出来るモデルである、ELEGANT を提案。反対の attribute を持つ2枚の画像を入力として、お互いに対応する attribute を入れ替えるように latent encoding を学習することで、disentangled な latent space を学習。これによって、複数の attribute を同時に転移出来るようにした。

* [Deep Bilevel Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Simon_Jenni_Deep_Bilevel_Learning_ECCV_2018_paper.html)
    * ネットワークのトレーニングの際の regularization に関する研究。cross-validation の考え方に着想を得ており、training用のmini-batchとvaludation用のmini-batchそれぞれから計算される勾配の方向の類似度によって、学習率の調整をbatchごとに行うことで、overfittingを防ぐ方法を提案。

* [ADVIO: An Authentic Dataset for Visual-Inertial Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Santiago_Cortes_ADVIO_An_Authentic_ECCV_2018_paper.html)
    * 歩行者視点でのVisual-Inertial Odmetryのデータセットを提案。データは iPhone、Google Pixel、Android phone、Google Tangoなどの複数のハードで同時に撮影されておりいずれのデータにもアクセス可能。また、 Google Tango、 ARCore、Apple ARKit の性能を提案したデータセットを用いて評価したところ、ARKitが最も優秀だった。

* [D2S: Densely Segmented Supermarket Dataset](http://openaccess.thecvf.com/content_ECCV_2018/html/Patrick_Follmann_D2S_Densely_Segmented_ECCV_2018_paper.html)
    * instance-aware semantic segmentation のための新しいベンチマーク Densely Segmented Supermarket (D2S) dataset を公開した。食料雑貨や日用品を中心に60カテゴリーのpixelレベルのアノテーションが付いている。21000枚の高解像度画像から構成されている。（主にレジの自動決済など産業面での応用を考えているため、構図は鉛直上部から撮影されたものとなっている。）Mask R-CNNやFCISなど複数の既存手法に付いて精度の比較を行っている。

* [PyramidBox: A Context-assisted Single Shot Face Detector](http://openaccess.thecvf.com/content_ECCV_2018/html/Xu_Tang_PyramidBox_A_Context-assisted_ECCV_2018_paper.html)
    * 顔検出の研究。コンテキスト情報を用いて、小さいサイズ、ボケ、遮蔽などの影響があっても検出が出来る、 PyramidAnchors を提案。また、コンテキスト情報と顔の特徴量を効果的に統合するためのネットワークである Low-level Feature Pyramid Networks (LFPN) を提案。 提案手法は FDDB や WIDER FACE benchmark で SotA を達成。

* [Structured Siamese Network for Real-Time Visual Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Yunhua_Zhang_Structured_Siamese_Network_ECCV_2018_paper.html)
    * 提案したトラッキング手法はリアルタイムで既存手法よりもexpected average overlap(EAO)で良い性能を出した。提案手法は2つの流れから構成されており、1つは検出領域を入力として、もうひとつは現在のフレームを入力とする。これらからターゲット領域のスコアマップを作成してトラッキングを行う。

* [Probabilistic Signed Distance Function for On-the-fly Scene Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Wei_Dong_Probabilistic_Signed_Distance_ECCV_2018_paper.html)
    * ３次元空間の復元における、３次元空間情報の representation の研究。3D空間の不確定性を表現するために Probabilistic Signed Distance Function という関数を提案。確率的に信頼性の高い部分に基づいて復元を行うことで、real-time 3D reconstruction におけるノイズの削減に成功。

* [3D Vehicle Trajectory Reconstruction in Monocular Video Data Using Environment Structure Constraints](http://openaccess.thecvf.com/content_ECCV_2018/html/Sebastian_Bullinger_3D_Vehicle_Trajectory_ECCV_2018_paper.html)
    * 単眼の動画データから3次元の車両軌道を最新のsemantic segmentationとSfMを利用して構築する手法を提案した。SfMを車両と背景にそれぞれ適応してカメラ姿勢を求め、その後全体のスケールを推定して車両軌道を構築した。またground truthを伴った3次元物体の移動軌跡データがないためデータセットを提示した。

* [Unsupervised Image-to-Image Translation with Stacked Cycle-Consistent Adversarial Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Minjun_Li_Unsupervised_Image-to-Image_Translation_ECCV_2018_paper.html)
    * 教師なしのpix2pixを提案した。提案手法はstage1ではCycleGANと同様に低解像度画像で変換精度を上げ、stage2ではstage1の重みを固定しつつ解像度を上昇させた。Cycle GANに比べてPSNR等において精度に改善が見られた。

* [Pose-Normalized Image Generation for Person Re-identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Xuelin_Qian_Pose-Normalized_Image_Generation_ECCV_2018_paper.html)
    * Person Re-identification (re-id) の研究。従来手法には scalability と generalizability の点で問題があった。GAN による pose normalization を行う手法（PN-GAN）を提案。入力画像とPN-GANによって生成された画像の両方から抽出された特徴を fusion することで SotA の精度を達成。

* [Action Anticipation with RBF Kernelized Feature Mapping RNN](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuge_Shi_Action_Anticipation_with_ECCV_2018_paper.html)
    * CNNとパラメータ共有を行いパラメータの数を減らしたRNNを用いることでリアルタイムの行動予測を可能にし、時系列モデル内部でRBFカーネルを用いることで精度を上昇させた。

* [Rendering Portraitures from Monocular Camera and Beyond](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiangyu_Xu_Rendering_Portraitures_from_ECCV_2018_paper.html)
    * 1枚の入力画像から ポートレート効果を再現する研究。CNNを用いて相対深度と portrait segmentation maps を1枚の画像から推定する。生成された粗い map を affinity に元づいて refine する方法（SPN）を提案。 それを元に bular の追加と image matting を行う。また、RNNを用いてrenderingのプロセスの高速化に成功。

* [Recovering 3D Planes from a Single Image via Convolutional Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Fengting_Yang_Recovering_3D_Planes_ECCV_2018_paper.html)
    * 1枚の画像から人工環境中に存在する平面の３次元的位置を推定する研究。 DNNを用いて画像中の平面の segmentation map と ３次元空間での平面のパラメータを同時に推定する手法を提案（plane structure-induced lossというlossを提案）。 また、DNN を既存の large-scale RGB-D dataset を用いて新しく手動でアノテーションをつけることなく学習される方法も提案。Plane segmentation の結果ではCityscapesなどのdatabaseでSotA。推定された３D平面をDepthとして評価したものも既存のSotA手法にわずかに劣るぐらいの精度。（実行時の計算速度はGTX 1080で60FPS）

* [The Devil of Face Recognition is in the Noise](http://openaccess.thecvf.com/content_ECCV_2018/html/Liren_Chen_The_Devil_of_ECCV_2018_paper.html)
    * 大規模トレーニングデータの様々なノイズが顔認識の精度に与える影響を調べるために、ノイズのとても少ないクリーンなデータベース、IMDb-Face datasetを作成、公開した。アノテーションの方法についてもどのような手法がいいか、ユーザースタディーを行なっている。

* [3DMV: Joint 3D-Multi-View Prediction for 3D Semantic Scene Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Angela_Dai_3DMV_Joint_3D-Multi-View_ECCV_2018_paper.html)
    * 室内シーンのsemantic segmentationの研究。3DのGeometryの情報と2DのRBGの情報を両方用いて、End-to-endでの学習を可能としている。ScanNet DatasetでSoTAの手法（ScanNet, ScanComplete, PointNet++）と比較して約15%の精度向上を達成。（新しいベースラインになる手法と考えられるのでGood判定）

* [Joint optimization for compressive video sensing and reconstruction under hardware constraints](http://openaccess.thecvf.com/content_ECCV_2018/html/Michitaka_Yoshida_Joint_optimization_for_ECCV_2018_paper.html)
    * compressive video sensing の研究。信号処理の理論的には時間・空間的に完全にランダムに露光するのが最も復元効率が良いが、実際にはハードウエアによって制約を受けるため、完全にランダムというのは難しい。そこで、exposure pattern と reconstruction decoder の両方をDNNを用いてハード的制約の上で両方最適化する end-to-end のフレームワークを提案。提案手法は handcraft や random pattern を用いた手法よりも高精度を達成。

* [Consensus-Driven Propagation in Massive Unlabeled Data for Face Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaohang_Zhan_Consensus-Driven_Propagation_in_ECCV_2018_paper.html)
    * annotation が与えられていない膨大な量の顔画像（6M枚以上）に対して positive face pairs を探索して label を自動で与える手法を提案。画像から得られる特徴量のk-NNごとにグループを作成し、どのグループ同士が同じlabelとなり得るかをMLPのclassifierで判断。MegaFace identification challenge において、9%のlabelのみを用いて61.78%使用している先行研究とほぼ同等の精度を達成。

* [Recovering Accurate 3D Human Pose in The Wild Using IMUs and a Moving Camera](http://openaccess.thecvf.com/content_ECCV_2018/html/Timo_von_Marcard_Recovering_Accurate_3D_ECCV_2018_paper.html)
    * 手で把持された単眼のカメラと、四肢に固定されたIMUから人間の３次元姿勢を wild な環境で推定する手法を提案。DNNで推定された2D pose に SMPL body model をfittingした後、camera poses、heading angles、3D posesの３つを同時に最適化する。TotalCapture datasetで行った評価実験では誤差が 26mm（本気で言ってる？）であった。提案手法の結果を dataset として公開。

* [Predicting Future Instance Segmentations by Forecasting Convolutional Features](http://openaccess.thecvf.com/content_ECCV_2018/html/Pauline_Luc_Predicting_Future_Instance_ECCV_2018_paper.html)
    * Video forecasting の研究。次のフレームのinstanceレベルでのsegmentationを推定する。(future instance segmentstionという新しいタスクを導入) cityscape datasetを用いた実験では、optical flowを用いたベースラインよりも良い結果となった。

* [PS-FCN: A Flexible Learning Framework for Photometric Stereo](http://openaccess.thecvf.com/content_ECCV_2018/html/Guanying_Chen_PS-FCN_A_Flexible_ECCV_2018_paper.html)
    * non-Lambertian な表面に対する photometric stereo の研究。 任意枚数の光源状況の異なる画像から法線マップを推定するCNN（PS-FCN）を提案。提案手法では、先行研究で主に用いられているような事前定義された光源方向は必要ない（学習時とテスト時で同じである必要もない）。

* [Unsupervised Class-Specific Deblurring](http://openaccess.thecvf.com/content_ECCV_2018/html/Nimisha_T_M_Unsupervised_Class-Specific_Deblurring_ECCV_2018_paper.html)
    * Unsupervised Deblurring の研究。GANを用いてdeblurringとrebulurringを行うことで、教師なしで deblurring を学習する。Face dataset、Text dataset、Checkerboard dataset を用いて行った評価実験では既存の教師ありの手法と比較して同等の精度を達成。

* [Face Super-resolution Guided by Facial Component Heatmaps](http://openaccess.thecvf.com/content_ECCV_2018/html/Xin_Yu_Face_Super-resolution_Guided_ECCV_2018_paper.html)
    * 小さな低解像度の顔画像から超解像を行うネットワークを提案した。ネットワークの特徴としては正解画像と生成した高解像度画像のlossを考えるだけでなく、低解像度画像からの情報を基にして構成された顔の構造を考慮するネットワークが存在する点である。

* [A Contrario Horizon-First Vanishing Point Detection Using Second-Order Grouping Laws](http://openaccess.thecvf.com/content_ECCV_2018/html/Gilles_Simon_A_Contrario_Horizon-First_ECCV_2018_paper.html)
    * 消失点 (vanishing points) 検出の研究。キャリビュレーションされていない単眼カメラの画像群から消失点検出を行う手法を提案。水平方向の線を先に推定する手法（horizon-first strategies）を提案。従来手法より高速かつ高精度を達成した。

* [Fast, Accurate, and, Lightweight Super-Resolution with Cascading Residual Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Namhyuk_Ahn_Fast_Accurate_and_ECCV_2018_paper.html)
    * Deep learningを用いたSuper-resolutionの精度は向上しているが、計算が重いため実用化は難しかった。この問題を解決するためにresidual networkを応用したcascading mecanismを利用し、計算量を削減しつつ既存手法と同程度の精度を示した。本論文で提案されているCascading Residual Networkはパラメータの数を減らす(計算量を減らす)のに重要な役割を果たしていくと考えられる。

* [Face Recognition with Contrastive Convolution](http://openaccess.thecvf.com/content_ECCV_2018/html/Chunrui_Han_Face_Recognition_with_ECCV_2018_paper.html)
    * Face Recognition の研究。人間は２つの異なる顔を比較する際に対照的な特徴をもつ部位に注目するという仮定から、２つの顔のうち対照的な特徴量 (contrastive features) を考慮した kernel を用いて畳み込みを行う手法（contrastive convolution）を提案。IJB-A dataset で行った評価実験でSotA。

* [Deforming Autoencoders: Unsupervised Disentangling of Shape and Appearance](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhixin_Shu_Deforming_Autoencoders_Unsupervised_ECCV_2018_paper.html)
    * 潜在変数空間においてshapeとappearanceを教師なしでdisentangleすることができるアーキテクチャ（Deforming Autoencoder）を提案。appearanceはcanonical coordinateにおけるテクスチャ、shapeはcanonical coordinateの変形としてモデル化。既存のself-supervised correspondence estimationの手法よりも良い結果となった。

* [NetAdapt: Platform-Aware Neural Network Adaptation for Mobile Applications](http://openaccess.thecvf.com/content_ECCV_2018/html/Tien-Ju_Yang_NetAdapt_Platform-Aware_Neural_ECCV_2018_paper.html)
    * pretrain された network を計算資源の限られたモバイルデバイス用に最適化する手法を提案。提案手法の NetAdapt は最適化先のデバイスの低レイヤーの詳細を知ることなく最適化を行うことが出来る。従来手法と同じレベルの最適化を1.7倍以上高速に実現。

* [ExFuse: Enhancing Feature Fusion for Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhenli_Zhang_ExFuse_Enhancing_Feature_ECCV_2018_paper.html)
    * semantic segmentation の研究。モダンな semantic segmentation の手法は学習済みのCNNの low-level と high-level の特徴量を組み合わせて行うもの（U-Netを用いる）が多い。しかし、この論文では単純なこれら２つの fusion は semantic level と spacial resolution のギャップのため、効率的では無いと主張。low-level の特徴に semantic な情報を導入、high-level の特徴に high-resolution の詳細情報を導入する新しい fusion の方法を提案。PASCAL VOC 2012 segmentation benchmark で SotA を達成。

* [AugGAN: Cross Domain Adaptation with GAN-based Data Augmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Sheng-Wei_Huang_AugGAN_Cross_Domain_ECCV_2018_paper.html)
    * 車両検出アルゴリズムを開発するための大規模なトレーニングデータを生成するpix2pix2ネットワークを提案した。生成したデータセットを用いてYOLO等で訓練を行うと検出精度において著しい改善が見られた。

* [LAPCSR:A Deep Laplacian Pyramid Generative Adversarial Network for Scalable Compressive Sensing Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Kai_Xu_LAPCSRA_Deep_Laplacian_ECCV_2018_paper.html)
    * 単一画像の compressive sensing (CS) と reconstruction の研究。階層的に画像の再構成を行う Laplacian pyramid reconstructive adversarial network (LAPRAN) を提案。提案手法は従来手法と比較して復元の忠実性が高く、柔軟かつ高速。

* [U-PC: Unsupervised Planogram Compliance](http://openaccess.thecvf.com/content_ECCV_2018/html/Archan_Ray_U-PC_Unsupervised_Planogram_ECCV_2018_paper.html)
    * 事前情報を用いずに棚に並んだ商品を認識する手法を提案した。棚画像から抽出した画像と商品画像の相関程度とこの問題に特化させ検出速度を上昇させたNeo SURFの値から有向グラフを作成し、商品の検出を行った。商品の数が増えても従来手法に比べて短時間で正確に検出できている。

* [Seeing Tree Structure from Vibration](http://openaccess.thecvf.com/content_ECCV_2018/html/Tianfan_Xue_Seeing_Tree_Structure_ECCV_2018_paper.html)
    * 

* [A Dataset of Flash and Ambient Illumination Pairs from the Crowd](http://openaccess.thecvf.com/content_ECCV_2018/html/Yagiz_Aksoy_A_Dataset_of_ECCV_2018_paper.html)
    * 

* [Compressing the Input for CNNs with the First-Order Scattering Transform](http://openaccess.thecvf.com/content_ECCV_2018/html/Edouard_Oyallon_Compressing_the_Input_ECCV_2018_paper.html)
    * 

* [Distractor-aware Siamese Networks for Visual Object Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Zheng_Zhu_Distractor-aware_Siamese_Networks_ECCV_2018_paper.html)
    * 

* [""Factual"" or ""Emotional"": Stylized Image Captioning with Adaptive Learning and Attention](http://openaccess.thecvf.com/content_ECCV_2018/html/Tianlang_Chen_Factual_or_Emotional_ECCV_2018_paper.html)
    * 

* [Constrained Optimization Based Low-Rank Approximation of Deep Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Chong_Li_Constrained_Optimization_Based_ECCV_2018_paper.html)
    * 

* [Extending Layered Models to 3D Motion](http://openaccess.thecvf.com/content_ECCV_2018/html/Dong_Lao_Extending_Layered_Models_ECCV_2018_paper.html)
    * 

* [ExplainGAN: Model Explanation via Decision Boundary Crossing Transformations](http://openaccess.thecvf.com/content_ECCV_2018/html/Nathan_Silberman_ExplainGAN_Model_Explanation_ECCV_2018_paper.html)
    * 

* [Adding Attentiveness to the Neurons in Recurrent Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Pengfei_Zhang_Adding_Attentiveness_to_ECCV_2018_paper.html)
    * 従来のRNNは時系列情報の関係性のみを学習するものだった。Element-wise-Attention Gate (EleAttG) を追加することで RNN に attentiveness の機構を導入、入力のそれぞれの要素の重要度を考慮できるようにした。action recognition のタスクにおいて精度を 5~10 %程度向上できることが確認された。

* [ESPNet: Efficient Spatial Pyramid of Dilated Convolutions for Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Sachin_Mehta_ESPNet_Efficient_Spatial_ECCV_2018_paper.html)
    * 限られた計算資源での高解像度画像の Semantic Segmentation のための高速かつ効率的な CNN の提案。新しい畳み込みモジュールである efficient spatial pyramid (ESP) によって従来のSotAの PSPNet の22倍高速で180倍メモリー効率が良い。精度は 8% の低下で実現。従来の効率的なCNNである MobileNet, ShuffleNet, ENet よりも正確。新しいパフォーマンスの尺度を提案。

* [Learning Human-Object Interactions by Graph Parsing Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Siyuan_Qi_Learning_Human-Object_Interactions_ECCV_2018_paper.html)
    * 動画・画像中の Human Object Interaction (HOI) を検出・認識する研究。与えられたシーンについて parse graph を推定する Graph Parsing Neural Network（end to end）を提案。

* [PESTO: 6D Object Pose Estimation Benchmark](http://openaccess.thecvf.com/content_ECCV_2018/html/Tomas_Hodan_PESTO_6D_Object_ECCV_2018_paper.html)
    * single RGBD 画像を用いた rigid object を対象とした 6DoF 姿勢推定のための新しいベンチマークを提案。既存の手法について総合的な評価をすると共に、Webを用いたOnlineでの評価システムも公開。公開されたベンチマークは、「texture付きの89種類のobjectの3次元モデル」や「277K枚の学習用RGBD画像」を含む。

* [RCAA: Relational Context-Aware Agents for Person Search](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaojun_Chang_RCAA_Relational_Context-Aware_ECCV_2018_paper.html)
    * person search や person re-identification に深層強化学習（A3C）を適用した研究。大規模データセットを用いた評価実験では、mAPとCMC top-K いずれの評価尺度でもSoTAを達成。

* [DetNet: Design Backbone for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Zeming_Li_DetNet_Design_Backbone_ECCV_2018_paper.html)
    * これまでは物体検出を行うためにbackbone networkにImageNetを利用したネットワークを用いていたが、これはクラス分類により適している。そこで、物体検出に適したbackbone networkとしてDetNetを提案した。ResNetと比べて精度面で大きな改善は見られなかった。

* [Modeling Varying Camera-IMU Time Offset in Optimization-Based Visual-Inertial Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Yonggen_Ling_Modeling_Varying_Camera-IMU_ECCV_2018_paper.html)
    * rollingshutter effects のような原因のために、カメラとIMUの同期が完全ではない場合のmonocular visual inertial odometry (VIO) の手法を提案。非線形最適化によって、カメラとIMUの間の未知のtime offsetを考慮している。

* [Exploiting temporal information for 3D human pose estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Mir_Rayat_Imtiaz_Hossain_Exploiting_temporal_information_ECCV_2018_paper.html)
    * 2Dで関節位置を推定してそれらを逆投影して3D の関節位置を推定する。各フレームからの3Dポーズの推測はフレームごとに独立の誤差があるため不完全な推定になる。これを解決するためdecoderにskip connectionを取り入れたseq2seqを用いて、連続した2D入力から一貫性のある３Dポーズを予測できるようにした。

* [Joint Representation and Truncated Inference Learning for Correlation Filter based Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Yingjie_Yao_Joint_Representation_and_ECCV_2018_paper.html)
    * 

* [Learning to Zoom: a Saliency-Based Sampling Layer for Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Adria_Recasens_Learning_to_Zoom_ECCV_2018_paper.html)
    * 

* [Does Haze Removal Help Image Classification?](http://openaccess.thecvf.com/content_ECCV_2018/html/Yanting_Pei_Does_Haze_Removal_ECCV_2018_paper.html)
    * 

* [Learning Local Descriptors by Integrating Geometry Constraints](http://openaccess.thecvf.com/content_ECCV_2018/html/Zixin_Luo_Learning_Local_Descriptors_ECCV_2018_paper.html)
    * 

* [Repeatability Is Not Enough: Learning Affine Regions via Discriminability](http://openaccess.thecvf.com/content_ECCV_2018/html/Dmytro_Mishkin_Repeatability_Is_Not_ECCV_2018_paper.html)
    * local descriptor に付いての研究。局所領域の Affine 変換を推定するネットワーク AffNet と hard-negative を用いて descriptor の識別精度を高める loss (HardNegC) を提案。

* [Macro-Micro Adversarial Network for Human Parsing](http://openaccess.thecvf.com/content_ECCV_2018/html/Yawei_Luo_Macro-Micro_Adversarial_Network_ECCV_2018_paper.html)
    * RGBからセグメンテーションされた人間のポーズ画像を2つのdiscrimanatorを持つMacro-Micro Adversarial Net (MMAN)で行うように提案した。1つ目のdiscrimanatorは低解像度画像に作用し、大域的にみて人間のポーズを合理的に、体の部位を正しくさせるようにgeneraterを導く。2つ目はPatchGANと同じように高解像度画像において多数のパッチに着目し、局所的なエラーに対処する。

* [Learning Class Prototypes via Structure Alignment for Zero-Shot Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Huajie_Jiang_Learning_Class_Prototypes_ECCV_2018_paper.html)
    * Zero-shot learning (ZSL)の研究。dictionary learning と visual-semantic structures の学習をカップリングする手法を提案。visual space のもつ 識別性 と semantic space のもつ拡張性 を生かすため、それぞれの空間を共通の空間 (aligned space) に落とし込む手法を提案。新しい class の導入は aligned space への domain adaptation の問題として定式化される。aPascal & aYahoo (aPY)、Animals with Attributes (AwA)、Caltech-UCSD Birds-200-2011 (CUB) 、SUN Attribute (SUNA) の４つのbenchmarkで評価して、良好な結果を得た。

* [SphereNet: Learning Spherical Representations for Detection and Classification in Omnidirectional Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Benjamin_Coors_SphereNet_Learning_Spherical_ECCV_2018_paper.html)
    * 

* [A dataset and architecture for visual reasoning with a working memory](http://openaccess.thecvf.com/content_ECCV_2018/html/Guangyu_Robert_Yang_A_dataset_and_ECCV_2018_paper.html)
    * visual reasoning の研究。VQA等の現在の問題設定では、時間変化や記憶の概念が必要ない問題設定となっているため、時間変化する画像群、言語でのインストラクション、対応する正解を計算によって生成するデータセット、COGを作成・公開した。

* [Flow-Grounded Spatial-Temporal Video Prediction from Still Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Yijun_Li_Flow-Grounded_Spatial-Temporal_Video_ECCV_2018_paper.html)
    * Video Prediction の研究。単一の入力 Frame から将来の複数フレームを推定する問題を考える。タスクを「flow predictionの段階」と「推定されたflowからframeを生成する段階」の２つに分割し、前者に3D-cVAE、後者にはFlow2rgb（Optical Flowベースで画像をWarp）を用いている。 human action や dynamic texture など異なる種類の複数の動画に対して手法の有効性を確認した。

* [The Unmanned Aerial Vehicle Benchmark: Object Detection and Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Dawei_Du_The_Unmanned_Aerial_ECCV_2018_paper.html)
    * 複雑なシナリオを対象とした新しい Unmanned Aerial Vehicles (UAVs) のための benchmark、UAV Detection and Tracking (UAVDT) を作成・公開した。 14 種類の物体に Bounding Box と attribute のアノテーションが付いている。object detection、single object tracking、multiple object tracking のタスクにおいて SotA の手法でも UAVDT では十分な結果を達成出来ていないことを確認した。

* [Selective Zero-Shot Classification with Augmented Attributes](http://openaccess.thecvf.com/content_ECCV_2018/html/Jie_Song_Selective_Zero-Shot_Classification_ECCV_2018_paper.html)
    * Zero-Shot Classification の研究。confidence が低い時は分類を行わないことで、misclassification の可能性を低くする、Selective Classification のタスクを Zero-Shot Classification に導入して、既存手法ではこのタスクに上手く適用出来ないことを実験により確認。人手によって定義された attribute と 自動的に発見される residual attribute を組み合わせる手法を提案。

* [Action Search: Spotting Actions in Videos and Its Application to Temporal Action Localization](http://openaccess.thecvf.com/content_ECCV_2018/html/Humam_Alwassel_Action_Search_Spotting_ECCV_2018_paper.html)
    * 動画中から特定の人間の行動を探索する（action spotting）研究。人間の探索の効率の良さを学習するために、人間が動画からaction spottingをする過程の手続きを記録したデータセットHuman Searchesを作成・公開。また、RNNを用いて人間がaction spottingをするときの手続きを真似たモデルである、Action Searchを提案。提案手法はベースラインの手法と比較して約15~20％少ない観測で同等の精度を達成。また、temporal action localizationのタスクにおいてはTHUMOS14 datasetでSotAを達成。

* [A Principled Approach to Hard Triplet Generation via Adversarial Nets](http://openaccess.thecvf.com/content_ECCV_2018/html/Yiru_Zhao_A_Principled_Approach_ECCV_2018_paper.html)
    * hard possitive と hard negative との組み Hard Triplet を生成し、それを区別出来るようにすることで大域的に最適化された feature embedding network を学習させる研究。（既存の mining-based の手法は local optimum に落ちやすいという問題があった。）提案手法はCUB200-2011、CARS196、DeepFashion 、VehicleID など様々な Dataset で SotA を達成。

* [Pose Guided Human Video Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Ceyuan_Yang_Pose_Guided_Human_ECCV_2018_paper.html)
    * Human Video Synthesis の研究。姿勢の予測とVideo Frameの生成を別々に行う手法を提案。「姿勢の予測」と「frameの生成」はどちらもGANを使って学習。

* [Deep Directional Statistics: Pose Estimation with Uncertainty Quantification](http://openaccess.thecvf.com/content_ECCV_2018/html/Sergey_Prokudin_Deep_Directional_Statistics_ECCV_2018_paper.html)
    * 物体の角度推定（姿勢推定の一種）の研究。入力画像が低解像度でもロバストに推定が出来る probabilistic deep learning モデルを提案。von Mises distributions の mixture として確率的に姿勢を推定。PASCAL 3D+ benchmark を含む姿勢推定のデータセットで先行研究と同等の精度を達成すると共に、推定の尤度において確率的なモデルが有効であることを確認した。

* [Learning 3D Human Pose from Structure and Motion](http://openaccess.thecvf.com/content_ECCV_2018/html/Rishabh_Dabral_Learning_3D_Human_ECCV_2018_paper.html)
    * 単一画像からの３次元の姿勢推定の研究。人間の解剖学的な構造を考慮したロスを提案。また、２層のFCネットワークを用いて過去２０frame分の姿勢を考慮することで、運動の連続性を考慮。提案手法はHuman3.6M と MPI-INF-3DHP でそれぞれStoAを達成（両者とも10%以上の向上）。

* [Learning Dynamic Memory Networks for Object Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Tianyu_Yang_Learning_Dynamic_Memory_ECCV_2018_paper.html)
    * Template-matching ベースの object tracking の研究。追跡物体の見た目の変化に動的に対応出来るようにするため、attentional 機構を用いた LSTMのコントローラーによって最適な特徴量マップをメモリー上に記録された複数のマップの中から探索するモデルを提案。OTB や VOTなどのlarge scale datasetでreal-time動作しない高精度なobject trackingの手法と近い精度を達成。（提案手法は、off-lineでの学習が終了したら、onlineのfine-tuningは必要無いため、50FPSで動作可能。）

* [Faces as Lighting Probes via Unsupervised Deep Highlight Extraction](http://openaccess.thecvf.com/content_ECCV_2018/html/Renjiao_Yi_Faces_as_Lighting_ECCV_2018_paper.html)
    * 単一画像中の人間の顔から、シーン中の詳細な光源環境を推定する研究。non-parametric な環境マップによって先行研究よりも高精度な推定が可能。NNによって検出したスペキュラー情報を環境マップに投影することで光源の位置の推定を行う。

* [CurriculumNet: Learning from Large-Scale Web Images without Human Annotation](http://openaccess.thecvf.com/content_ECCV_2018/html/Sheng_Guo_CurriculumNet_Learning_from_ECCV_2018_paper.html)
    * web上のアノテーションのついていない大量の画像（検索用のtextのクエリはついてる）からネットワークの学習をするために、ノイジーなラベルかつ、アンバランスな大量のデータにおいて効果的に学習を行える手法を提案。特徴量空間での分布密度を用いてデータの複雑性を計測、順位付けすることで、教師なしで学習のカリキュラムを設計する。WebVision, ImageNet, Clothing1M, Food101 などの４つのベンチマークでSoTAの精度を達成。目的としているタスクの重要性と評価の結果からgoodと判断。

* [Joint Task-Recursive Learning for Semantic Segmentation and Depth Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhenyu_Zhang_Joint_Task-Recursive_Learning_ECCV_2018_paper.html)
    * semantic segmentation と depth estimation のタスクを sequencial に学習して情報をお互いに伝達することで、相互の学習をより高速なものにする Task-Recursive Learning (TRL) framework を提案。ネットワークの中でモジュールとして使用出来き、２つのタスクのインタラクションを仲介する Task-Attentional Module (TAM)を設計。 NYU Depth V2 と SUN RGBD dataset で semantic segmentation と depth estimation の両方のタスクでSotAを達成。

* [HybridFusion: Real-Time Performance Capture Using a Single Depth Sensor and Sparse IMUs](http://openaccess.thecvf.com/content_ECCV_2018/html/Zerong_Zheng_HybridFusion_Real-Time_Performance_ECCV_2018_paper.html)
    * 単一のdepth cameraとsparseに体にマウントしたIMU(4?12個)の情報からreal timeでロバストにhuman performance captureを行う手法を提案。フレーム毎のセンサーのキャリブレーションやconfidence値を考慮したadaptiveなgeometryの再構成法など複数のコントリビューションを主張。

* [Associating Inter-Image Salient Instances for Weakly Supervised Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Ruochen_Fan_Associating_Inter-Image_Salient_ECCV_2018_paper.html)
    * weakly supervised semantic segmentation の研究。弱教師である画像レベルのラベルから pixel level のラベル (proxy ground-truth) を推定する手法を提案。S^4Net を用いて salient instance を画像中から抽出し、学習データ無いの全ての salient instance の特徴量の類似度を用いて graph を構成。その graph から graph partitioning algorithm によって分割される sub-graph に対して 弱教師のラベルを割り当てる。提案手法によって生成される proxy ground-truth を用いて既存の fully-supervised な手法を学習されることが可能であり、 DeepLab を学習させたものは PASCAL VOC 2012 dataset で SotAを達成。また、Mask R-CNN と組み合わせることで keyward の弱教師のみで weakly supervised instance segmentation を学習することを可能にした。

* [Ask, Acquire and Attack: Data-free UAP generation using Class impressions](http://openaccess.thecvf.com/content_ECCV_2018/html/Konda_Reddy_Mopuri_Ask_Acquire_and_ECCV_2018_paper.html)
    * data-free で Universal Adversarial Perturbations (UAP) を作成する研究。実際のデータサンプルの効果を真似るために提案手法ではまず、“class impression”を生成する（Stage I）。Attackを行う際にはNNの生成モデルから生成されたUAPとclass impressionを足し合わせる（Stage II）。data-free な手法ではSotAを達成、data-driven な手法とも同等のfooling rateを達成。

* [A Scalable Exemplar-based Subspace Clustering Algorithm for Class-Imbalanced Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Chong_You_A_Scalable_Exemplar-based_ECCV_2018_paper.html)
    * unsupervised learning 等で使用される subspace clustering についての研究。 imbalanced や large scale データによる精度の低下を防ぐために、データ中からデータ全体を subspace で表現する際に良い標本を探す手法を提案。選ばれたサンプルは、解析的には対象性を持つ凸包で全データの射線を出来るだけ多く含むものとなる。

* [Find and Focus: Retrieve and Localize Video Events with Natural Language Queries](http://openaccess.thecvf.com/content_ECCV_2018/html/Dian_SHAO_Find_and_Focus_ECCV_2018_paper.html)
    * 自然言語のクエリを使用した Video Retrieval の研究。複雑な動画の内容を自然言語を使って表現すると、動画のある部分とクエリのある部分に局所的な対応関係が出来るはずという仮定に基づき、top level だけではなくparts ごとの対応関係を考慮したフレームワーク（Find and Forcus）を提案。提案手法は ActivityNet Captions と modified LSMDC dataset の両者で SotA を達成。

* [Graininess-Aware Deep Feature Learning for Pedestrian Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Chunze_Lin_Graininess-Aware_Deep_Feature_ECCV_2018_paper.html)
    * 歩行者検出の研究。従来手法は低解像度の特徴量マップのみを考慮するものが多数であった。提案手法では scale-aware pedestrian attention module が異なるscaleの特徴量マップから、歩行者のattention maskを作成することで、従来手法よりもロバストに歩行者検出を行うことが出来る。また、zoom-in-zoom-out module を導入することで、小さな歩行者や遮蔽されている歩行者に対しても精度の良い検出が可能となった。 提案手法は Caltech, INRIA, KITTI, MOT17Det などのデータセットで既存のSotAと同等の精度を約4倍高速な計算速度で達成。

* [Diverse Image-to-Image Translation via Disentangled Representations](http://openaccess.thecvf.com/content_ECCV_2018/html/Hsin-Ying_Lee_Diverse_Image-to-Image_Translation_ECCV_2018_paper.html) [[GitHub](http://vllab.ucmerced.edu/hylee/DRIT/)]
    * pix2pixの派生研究。pix2pixでは入力画像と変換先の画像が1by1で対応づいていたが、変換画像の対応を拡張して複数のドメインに対応させることに成功した。例えば猫と犬の変換時、犬の種類をハスキー/レトリーバーといった感じで複数の表現を可能とした。image-to-image変換系の論文では初めてのunpairedかつmultimodalな手法であると主張、ドメイン変換の実験においてもCycleGANよりも高精度であった。

* [Convolutional Networks with Adaptive Computation Graphs](http://openaccess.thecvf.com/content_ECCV_2018/html/Andreas_Veit_Convolutional_Networks_with_ECCV_2018_paper.html) [[GitHub](https://vision.cornell.edu/se3/people/andreas-veit/)]
    * 入力に対してどの畳み込み層（ConvLayer）が必要かを自動で判断して活用するConvNet-AIG (Adaptive Inference Graph)を提案した。提案手法であるConvNet-AIGを使用する/しないで同じ層数のResNet-50/-101をベースラインとして精度向上が見られた上に計算時間も20~30%程度削減した。ResNetのスキップコネクション時にgate機構を設けてスキップする/しないを自動判断。

* [Learning to Separate Object Sounds by Watching Unlabeled Video](http://openaccess.thecvf.com/content_ECCV_2018/html/Ruohan_Gao_Learning_to_Separate_ECCV_2018_paper.html) [[GitHub](http://vision.cs.utexas.edu/projects/separating_object_sounds/\n)]
    * ラベルなしのビデオから教師なしで音源の分離を実施する研究である。NeuralNetの文脈でDeep Multi-instance Multi-label Learningの枠組みを提案、音源を分離して動画像中の対象領域にマッピングすることに成功。ImageNet Pretrained ResNet-152によりTopCategoryを推定、音源はNon-negative Matrix Factorization (NMF)により分離して画像側と対応付け。

* [Light Structure from Pin Motion: Simple and Accurate Point Light Calibration for Physics-based Modeling](http://openaccess.thecvf.com/content_ECCV_2018/html/Hiroaki_Santo_Light_Structure_from_ECCV_2018_paper.html) [[GitHub](https://github.com/hiroaki-santo/light-structure-from-pin-motion)]
    * フォトメトリックステレオを実施する際のキャリブレーション法を提案。点光源（Point Light Source）を与えることで効果的にキャリブレーション可能であることを実証した。従来手法であるLambertian spheres, mirror spheres, mirror planesとは対照的に、提案手法ではLambertian spheresとsmall shadow castersを想定することで、その小さなサイズから点光源を与えることでshadow caster上の未知の位置を既知とする。提案手法を用いることで、SfMの枠組みにより動的物体と固定カメラからshadow caster位置と光源の位置と方向を推定できる。

* [Coded Two-Bucket Cameras for Computer Vision](http://openaccess.thecvf.com/content_ECCV_2018/html/Mian_Wei_Coded_Two-Bucket_Cameras_ECCV_2018_paper.html)
    * 新規の画像センサであるcoded two-bucket (C2B)を提案、プログラミング可能でピクセルごとにライトソースを操作できる。センサオリジナルの解像度で法線画像や距離画像を取得できる。

* [Programmable Triangulation Light Curtains](http://openaccess.thecvf.com/content_ECCV_2018/html/Jian_Wang_Programmable_Light_Curtains_ECCV_2018_paper.html)
    * Light Curtainと呼ばれる、距離センサ付近のみに配置された任意形状の高解像度のDepthMapを提案。現在までのDepthMapのように一律で空間情報を取得するのではなく、自動車やロボットを想定した際の目的に応じてセンシングの形式を変えていくことができるという意味で新しい。20~30mの位置に配置することができ、リソースも節約することができる。

* [Materials for Masses: SVBRDF Acquisition with a Single Mobile Phone Image](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhengqin_Li_Materials_for_Masses_ECCV_2018_paper.html) [[GitHub](https://medium.com/@neurohive/materials-for-masses-svbrdf-acquisition-with-a-single-mobile-phone-image-a7ad8bbadb32)]
    * 携帯端末カメラで撮影した画像から物体の材質、法線ベクトルや双方向反射率分布関数（BRDF）推定を実施。大規模データベースの作成と同時に、材質カテゴリの推定を行いながらSpatially-Varying BRDFと法線ベクトルを推定するCNNアーキテクチャを構築した。Dense CRFも構造の中に組み入れてrefinementを行う手法とした。

* [Zero-shot keyword search for visual speech recognition in-the-wild](http://openaccess.thecvf.com/content_ECCV_2018/html/Themos_Stafylakis_Zero-shot_keyword_search_ECCV_2018_paper.html)
    * 録音された音声と顔領域の動画からキーワード探索を行う問題であるKeyword Spotting (KWS)を提案。ゼロショット学習の文脈で手法を構築、概念を学習することにより見たことのないキーワードでも動画像（実際には携帯で読み上げ？）検索できるようになる。画像特徴の抽出にはSpatiotemporal ResNet、キーワード検索にはgrapheme-to-phonemeを実現するSeq2Seqモデルを提案。新規にLRS2 databaseを提案することにより同タスクを提供することが可能となった。

* [End-to-End Joint Semantic Segmentation of Actors and Actions in Video](http://openaccess.thecvf.com/content_ECCV_2018/html/Jingwei_Ji_End-to-End_Joint_Semantic_ECCV_2018_paper.html)
    * 人物行動認識（Human Action Recognition）とセマンティックセグメンテーション（Semantic Segmentation）の両者は従来別々に解かれてきたが、提案手法では同時に学習する。RGB/FlowのTwo-Streamの入力からEncode-Decode構造により位置（ROIs）、セグメント、行動者（Actor）、行動（Action）などを推定、マルチタスク学習により最適化。行動検出/行動セグメントにてSoTA。

* [Learning Discriminative Video Representations Using Adversarial Perturbations](http://openaccess.thecvf.com/content_ECCV_2018/html/Jue_Wang_Learning_Discriminative_Video_ECCV_2018_paper.html)
    * Adversarial Examples（AE）を時系列動画に対して拡張。動画に対してAEを挿入し、Manifold上で効果的に分離できるような空間を作成することで動画認識のロバスト性を向上させるという研究。行動認識、動的文字認識、姿勢ベース行動認識のタスクにてSoTAを達成することができた。摂動ノイズを与え、正サンプルとの分離性を考慮すると識別に有効な特徴が生成できるという意味で次の研究のinsightを与える。

* [DeepWrinkles: Accurate and Realistic Clothing Modeling](http://openaccess.thecvf.com/content_ECCV_2018/html/Zorah_Laehner_DeepWrinkles_Accurate_and_ECCV_2018_paper.html)
    * テクスチャまで含めた動的非剛体物体の再構成問題に対応。論文中では服装も含めて動的な人物の3次元形状を復元している。4D（xyzt）にてデータを取得、subspaceモデルにより形状復元、Adversarial Learningにより法線マップを復元、復元した形状と法線ベクトルを用いて3次元レンダリングを実施。

* [Massively Parallel Video Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Viorica_Patraucean_Massively_Parallel_Video_ECCV_2018_paper.html)
    * 動画認識（行動認識、キーポイント追跡）においてスループット最大化、レイテンシ最小化、クロックサイクルを低減させるような時間情報の使い方に関する調査研究を実施した。時間軸に対して並列化、コネクションモデルを考案。具体的には実時間で推論を行うと同時に時間的に先のラベルも予測的に推論、トレードオフを考慮しつつも3~4倍に高速化できることを明らかとした。

* [Unsupervised Person Re-identification by Deep Learning Tracklet Association](http://openaccess.thecvf.com/content_ECCV_2018/html/Minxian_Li_Unsupervised_Person_Re-identification_ECCV_2018_paper.html)
    * Tracklet（人物追跡の動線情報）を用いて教師なし学習の枠組みで人物再同定（Person Re-identification; ReID）のための特徴学習をEnd2Endで行う。ReIDでは通常、異なるviewpointにてカメラ間の人物を対応づける処理を行うが、提案のTracklet Association Unsupervised Deep Learning (TAUDL)ではカメラ内の対応づけやカメラ間の相関値をそれぞれ計算することで特徴学習を行う。ReID、教師なし学習におけるドメイン変換の文脈において代表的なデータセットでSoTA。

* [Instance-level Human Parsing via Part Grouping Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Ke_Gong_Instance-level_Human_Parsing_ECCV_2018_paper.html) [[GitHub](http://sysu-hcp.net/lip/)]
    * 人物の解析において、部位ごとのセマンティックセグメンテーション、インスタンスによるエッジ検出を同時に実行することで、混雑時においても人物部位推定を成功させる。この目的のために、bboxの検出を行わないという意味でDetection-freeなPart Grouping Network (PGN)を提案、multi-person parsing dataset (CIHP)にてSoTAな精度を実現した。

* [Scaling Egocentric Vision: The E-Kitchens Dataset](http://openaccess.thecvf.com/content_ECCV_2018/html/Dima_Damen_Scaling_Egocentric_Vision_ECCV_2018_paper.html) [[GitHub](https://epic-kitchens.github.io/2018)]
    * 現存のデータでは最大のFirst Person ViewのKitchen datasetであるEPIC-KITCHENを提案。32のキッチン、55時間の映像、11,500,000フレームを含むデータベースとなった。物体のアノテーション数454,200、行動数39,000を含み機械学習のための良質なデータとなった。お皿を割るところまで含まれている。

* [Predicting Gaze in Egocentric Video by Learning Task-dependent Attention Transition](http://openaccess.thecvf.com/content_ECCV_2018/html/Huang_Predicting_Gaze_in_ECCV_2018_paper.html)
    * 一人称カメラによる物体操作時の視線変化を推定する研究である。Task-dependentな物体操作時のアテンションの遷移とbottom-upな顕著性推定を統合して高精度な視線推定とした。基本的にはTwo-Stream ConvNetsとSaliencyモデルにより構築される。

* [Adversarial Geometry-Aware Human Motion Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Liangyan_Gui_Adversarial_Geometry-Aware_Human_ECCV_2018_paper.html)
    * 人物の姿勢位置を時間的に予測する問題である。GANベースの手法を用いて同問題に取り組んでおり、人間のように(1) フレーム内での空間的な配置、(2) 時系列フレームにおける時間的な変化を同時に考慮できるモデルを考案した。さらに、時空間の推定を高精度に実施するためのGeodesic Lossを考案して姿勢回帰の問題をよくした。提案のAdversarial Geometry-aware Encoder-Decoder (AGED)は姿勢予測の問題においてSoTA。

* [3D Scene Flow from 4D Light Field Gradients](http://openaccess.thecvf.com/content_ECCV_2018/html/Sizhuo_3D_Motion_Sensing_ECCV_2018_paper.html)
    * light fieldセンサーを用いて3D scene flowを計測する技術を提案。

* [Burst Image Deblurring Using Permutation Invariant Convolutional Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Miika_Aittala_Burst_Image_Deblurring_ECCV_2018_paper.html)
    * 任意のサイズ・長さの動画像に含まれた（酷い）ブラーからの画像復元を行う。提案のアーキテクチャはU-Netにより構成され、フレームごとにEncode-Decodeを行い、時系列フレーム間でMaxpoolを行う。フレーム間でエッジやテクスチャをシャープにしていくと同時に、ブラーが少ない領域をつなぎ合わせていくことで（？）より綺麗な画像復元をおこなうことに成功した。

* [Direct Sparse Odometry With Rolling Shutter](http://openaccess.thecvf.com/content_ECCV_2018/html/David_Schubert_Direct_Sparse_Odometry_ECCV_2018_paper.html)
    * direct sparse odometory(DSO)にrolling shutterモデルを組み込むことで、visual odometory(VO)の高精度化に成功した。VOでは特徴点ベースでマッチングするindirect methodと画像の輝度変化について対応点を取得するdirect methodに分類される。ローリングシャッターでは画像の行毎に時間差があるため、direct methodの場合はそれを考慮しないとキーフレームで誤差が大きくなる。そのため、ローリングシャッターモデルを組み込むことで既存手法よりも高精度となっている。モデルにはキーフレームの速度推定値を最適化で拡張し、最適化の前に一定の速度を負わせている。

* [Learning to Segment via Cut-and-Paste](http://openaccess.thecvf.com/content_ECCV_2018/html/Tal_Remez_Learning_to_Segment_ECCV_2018_paper.html)
    * 領域のCut-and-Pasteによりインスタンスセグメンテーションの学習データを増やす弱教師付き学習を提案。Cutは物体検出、マスク抽出により実現、Pasteは画像内任意の領域に貼り付け、さらにAdversarial LearningによりRealかFake（Cut-and-Paste）かを判断することで学習データがよりリアルに近いかどうかを反転して自然なデータとする。完全教師あり学習と比較して9割くらいの精度を出すに至った。

* [Weakly-supervised 3D Hand Pose Estimation from Monocular RGB Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Yujun_Cai_Weakly-supervised_3D_Hand_ECCV_2018_paper.html) [[GitHub](https://github.com/xinghaochen/awesome-hand-pose-estimation)]
    * 単眼RGBカメラからの弱教師付き学習による3Dハンドトラッキング。Kinect等により準備できる3Dにより学習のサポートを行い、テスト時には3D情報がなくても3次元ハンドトラッキングができるようにした。

* [DeepIM: Deep Iterative Matching for 6D Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yi_Li_DeepIM_Deep_Iterative_ECCV_2018_paper.html) [[GitHub](https://rse-lab.cs.washington.edu/projects/deepim/)]
    * 6D Object DetectionにおいてSoTAなモデルであるDeep Iterative Matching (DeepIM)を提案した。初期姿勢から3次元空間上で位置と回転を求めるタスクで、繰り返し最適化により誤差を修正しながら最終的な結果を出力する。DeepIMによる繰り返しの中ではズームインした画像も入力していく。

* [Jointly Discovering Visual Objects and Spoken Words from Raw Sensory Input](http://openaccess.thecvf.com/content_ECCV_2018/html/David_Harwath_Jointly_Discovering_Visual_ECCV_2018_paper.html)
    * 画像と音声の入力から、画像認識タスク（画像識別/検出/セグメンテーション）やキャプションとして音声の書き出しを実施する。

* [A Style-aware Content Loss for Real-time HD Style Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Artsiom_Sanakoyeu_A_Style-aware_Content_ECCV_2018_paper.html) [[GitHub](https://github.com/CompVis/adaptive-style-transfer)]
    * HD画像におけるStyleTransferの研究であり、HD動画においてもリアルタイムでスタイル変換を実施することができる。Gatys et al.ではなく、Johnson et al.のContent Lossを参考にEncode-Decode構造のアーキテクチャを提案した。

* [Implicit 3D Orientation Learning for 6D Object Detection from RGB Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Martin_Sundermeyer_Implicit_3D_Orientation_ECCV_2018_paper.html)
    * RGB画像の入力による物体検出と6D姿勢検出を解決する。Domain Randomizationによる3DモデルをAutoencoderにより学習した。潜在空間における姿勢情報表現により、リアルデータや詳細な姿勢によるアノテーション情報を必要とせず同タスクを解決に導く。

* [Scale-Awareness of Light Field Camera based Visual Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Niclas_Zeller_Scale-Awareness_of_Light_ECCV_2018_paper.html)
    * Light Fieldカメラによるsemi-denseな３次元点群やビジュアルオドメトリを計算。重み付けGauss-Newtonによる最適化により照明変動がある環境下においても対応点マッチングができている。さらに、連続的なフレームからキーフレームを選択して全体最適化を実施し、スケールの面でも正確性を保証できている。

* [Audio-Visual Scene Analysis with Self-Supervised Multisensory Features](http://openaccess.thecvf.com/content_ECCV_2018/html/Andrew_Owens_Audio-Visual_Scene_Analysis_ECCV_2018_paper.html)
    * 動画中の音と動画フレームには相関があるという考えのもと、それぞれをself-supervisedに学習し、動画と音のalignmentをDNNに学習させる。得られた特徴量を使用して、音源位置推定、行動認識、音源分離を行う。

* [Active Stereo Net: End-to-End Self-Supervised Learning for Active Stereo Systems](http://openaccess.thecvf.com/content_ECCV_2018/html/Yinda_Zhang_Active_Stereo_Net_ECCV_2018_paper.html)
    * active stereoによるデプスや法線などの３次元情報をend-to-endな学習によって推定する手法を提案。ground truthはなしで、self-supervisedで行う。オクルージョンや照明に頑健。局所的なコントラストに着目したリコンストラクションロスや、オクルージョンを検知しロスの計算には考慮しない、などを行なっている。他のステレオカメラに共通な問題も解いている。

* [GAL: Geometric Adversarial Loss for Single-View 3D-Object Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Li_Jiang_GAL_Geometric_Adversarial_ECCV_2018_paper.html)
    * 単眼画像から、point-based 3D modelの復元を行う手法を提案。既存研究であるpoint間を比較するロス関数の欠点を指摘し、geometric adversarial loss (GAL)を提案。GALは異なる視点からも同一形状を保つようにする項と、セマンティックに意味のあるポイントクラウドを行うようにする項の2つからなる。

* [MVSNet: Depth Inference for Unstructured Multi-view Stereo](http://openaccess.thecvf.com/content_ECCV_2018/html/Yao_Yao_MVSNet_Depth_Inference_ECCV_2018_paper.html)
    * multi-view画像から、デプスマップの推定をend-to-endに学習、推定する手法を提案。それぞれの画像から得られた特徴量マップをDifferentiable Homographyという変換によって結合し、3Dconvに入力する任意の方向から撮影された画像を入力とすることができ、実行時間において既存手法よりも数倍高速になっている。

* [PlaneMatch: Patch Coplanarity Prediction for Robust RGB-D Registration](http://openaccess.thecvf.com/content_ECCV_2018/html/Yifei_Shi_PlaneMatch_Patch_Coplanarity_ECCV_2018_paper.html)
    * RGB-D SLAMの文脈において、同一平面上（Coplanar）の対応点同士か否かをTripletにより学習。データセットを生成し、1,000万の対応点によりCoplanar/Non-coplanarをTripletLossにより学習してDense SLAMを実施した。同一平面かどうかを判定する新しいタスクも提供。

* [Deep Virtual Stereo Odometry: Leveraging Deep Depth Prediction for Monocular Direct Sparse Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Nan_Yang_Deep_Virtual_Stereo_ECCV_2018_paper.html)
    * 並行ステレオマッチングによるスケール推定や幾何情報を用いて、ビジュアルオドメトリの弱点を解消する研究。ステレオ視による情報を用いてSemi-supervised学習によりオドメトリを推定する。具体的にはDepth推定を行った画像を用いてオドメトリ計算。

* [GANimation: Anatomically-aware Facial Animation from a Single Image](http://openaccess.thecvf.com/content_ECCV_2018/html/Albert_Pumarola_Anatomically_Coherent_Facial_ECCV_2018_paper.html)
    * 顔表情を表現するActionUnitを補助情報とすることで、動画的に連続な顔表情変化を生成することに成功した。StarGANは離散的に変換するが、本論文では連続的なアニメーションを生成する点で異なる。ドメイン感を滑らかに移動しつつ動画を生成できる。

* [Unsupervised Geometry-Aware Representation for 3D Human Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Helge_Rhodin_Unsupervised_Geometry-Aware_Representation_ECCV_2018_paper.html)
    * 幾何情報を用いることで、2D単眼画像からでも3次元アノテーションなしで3次元姿勢を推定可能とした。

* [Efficient Semantic Scene Completion Network with Spatial Group Convolution](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiahui_Zhang_Efficient_Semantic_Scene_ECCV_2018_paper.html)
    * Group ConvolutionによるVoxel処理を実行しセマンティックラベルを推定、さらに同ラベルを用いることで物体ごとの3次元空間情報の補完を行うSemantic Scene Completionを実施した。スパースなボクセル空間においても効果的に畳み込みを行い、誤差を減らすことに成功した。SUN-CGにてSoTAな精度。

* [Deep Autoencoder for Combined Human Pose Estimation and Body Model Upscaling](http://openaccess.thecvf.com/content_ECCV_2018/html/Matthew_Trumble_Deep_Autoencoder_for_ECCV_2018_paper.html)
    * マルチビューカメラの設定から、3次元姿勢推定および人体形状推定を同時に実行するDeep Autoencoderを提案。キーポーズおよび人体のボリュームによる誤差関数を同時に最適化することで同タスクを解決した。

* [Highly-Economized Multi-View Binary Compression for Scalable Image Clustering](http://openaccess.thecvf.com/content_ECCV_2018/html/Zheng_Zhang_Highly-Economized_Multi-View_Binary_ECCV_2018_paper.html)
    * バイナリ圧縮により複数視点画像のクラスタリングを実施するHighly-economized Scalable Image Clustering (HSIC)を提案。バイナリの表現とクラスタリングの同時最適化を実施。l_{21}正則化の拘束により最適化を実行、XOR演算により高速化を実施。

* [Asynchronous, Photometric Feature Tracking using Events and Frames](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Gehrig_Asynchronous_Photometric_Feature_ECCV_2018_paper.html)
    * 低いレイテンシで画像内の領域を追跡（してSLAM等を）するイベントカメラを提案した。イベントカメラは時間ごとのピクセルの変化を捉えるカメラであり、非同期のイベントからフォトメトリック的な特徴抽出とトラッキングを実施。従来のヒューリスティックな手法とは異なり、直接的にピクセルから推定する手法を最尤推定的に解決。

* [Deterministic Consensus Maximization with Biconvex Programming](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhipeng_Cai_Deterministic_Consensus_Maximization_ECCV_2018_paper.html)
    * Consensus Maximizationにdeterministic optimizationを用いることでロバスト性を向上させた。  
    Consensus Maximizationに代表される手法としてRANSACがあり、その後も改良アルゴリズムが多く提案されてきた。

* [Occlusion-aware Hand Pose Estimation Using Hierarchical Mixture Density Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Qi_Ye_Occlusion-aware_Hand_Pose_ECCV_2018_paper.html)
    * 手の重なりによって発生したオクルージョン環境でのHand Pose Estimation。従来手法は特徴学習やモデル推定などでオクルージョンが発生した場合でも単一の解を導き出していた。一方提案したhierarchical mixture density networks(HMDN)は目に見える関節とオクルージョンが発生した関節を、それらのユニモーダルとマルチモーダルの特徴によってそれぞれ推定している。提案手法はオクルージョンが発生しないDSでは従来と同等の性能、オクルージョンが発生しているDSではstate-of-the-artな性能を出している。

* [Learning with Biased Complementary Labels](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiyu_Yu_Learning_with_Biased_ECCV_2018_paper.html)
    * 画像識別において、従来のラベルであるTrueLabelに加えて補助的なラベルであるComplementaryLabel（e.g. not monkey）を追加する。これにより、推移確率にバイアスがなくなる、従来の誤差関数を改変して一般化し、TrueLabelに対してもあてはまりがよくなり、精度向上が見込める。従来の識別ネットワークのSoftmax層の後にComplementaryLabelを評価する推移行列を配置してCross-entropy誤差を計算。

* [Lifting Layers: Analysis and Applications](http://openaccess.thecvf.com/content_ECCV_2018/html/Michael_Moeller_Lifting_Layers_Analysis_ECCV_2018_paper.html)
    * CNNにおける活性化関数(伝達関数)は適切な非線形性を持った線形モデルが用いられている。本論文では、リフティングと呼ばれる新しい非線形伝達関数を提案している。これは凸最適化の関連技術から着想を得た。

* [Progressive Neural Architecture Search](http://openaccess.thecvf.com/content_ECCV_2018/html/Chenxi_Liu_Progressive_Neural_Architecture_ECCV_2018_paper.html)
    * 強化学習・遺伝的アルゴリズムによりニューラルネット構造を探索するProgressive Neural Architecture Search (PNAS)の提案。従来法のNASと比較すると5倍も高速な探索アルゴリズムとなった。「探索のための探索」を行うヒューリスティックな探索を実施して簡単なものから複雑な構造への拡張を実施する。Progressive (simple to complex)な探索が効率化と高精度なモデルの発見に寄与した。図はセル（畳み込みの最小ユニットでGoogLeNetのインセプションのようなもの）とセルの組み合わせによるアーキテクチャを示す。従来法であるNASNetと類似する構造になったと主張。アーキテクチャ探索自体を人間ではなく強化学習に任せることでCIFAR/ImageNetにてstate-of-the-art。より効率的に従来法と類似する構造に行き着くことができた。

* [Robust fitting in computer vision: easy or hard?](http://openaccess.thecvf.com/content_ECCV_2018/html/Tat-Jun_Chin_Robust_fitting_in_ECCV_2018_paper.html)
    * ロバストフィッティング（つまり最適化）はコンピュータビジョンにおいて重要技術として扱われて来た。このうちConcensus Maximimzation（いかにインライアを選択して最適化するか）が重要と主張。コンピュータビジョンにおいて議論されていること、されていないことなどを考えることで、次の最適化手法のためのインサイトを与える。

* [Dual-Agent Deep Reinforcement Learning for Deformable Face Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Minghao_Guo_Dual-Agent_Deep_Reinforcement_ECCV_2018_paper.html)
    * Dual-agent deep reinforcement learning (DADRL)を提案、動画の入力から人物の顔検出や顔ランドマーク検出をインタラクティブに実施する手法とした。従来はこの２つのタスクは別々に解かれて来たが、同時に考慮、さらにMarkov Decision Process (MDP)により２つのエージェントを仮定したとき強化学習的にこの両者のタスクを解いていく問題にすると上手くいく。

* [Towards Realistic Predictors](http://openaccess.thecvf.com/content_ECCV_2018/html/Pei_Wang_Towards_Realistic_Predictors_ECCV_2018_paper.html)
    * Realistic Predictorという新しい概念の提案。基本的に機械学習ではデータとそれに対するラベルが付与されており、その訓練データに基づいて学習(例えば分類)が施されていく。しかし無理やり学習することにより、分類""できない""ことに対して意識していない。一方、人間は失敗するかもしれない分類は無理に分類しない、というRealistic Predictorが備わっている。本論文では分類困難な問題を拒絶し、良好なパフォーマンスを保証する変数を導入することでRealistic Predictorを実現している。

* [Group Normalization](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuxin_Wu_Group_Normalization_ECCV_2018_paper.html) [[GitHub](https://github.com/facebookresearch/Detectron/tree/master/projects/GN)]
    * Deep Learningの学習においてBatch Normalization（BN）に代わる技術としてGroup Normalization（GN）を提案。BNではバッチサイズが小さくなるとエラーが大きくなるが、GNではチャネルを複数のグループに分割してグループ毎に最適化を行うため、バッチサイズとは独立に最適化を行うことができる。事実、バッチサイズが小さい時にも、GNはエラーが大きくならずに学習に成功している。識別、検出、セグメンテーションなどフレームワーク依存がなく使用できる枠組みであるため、CVの研究に汎用的に使用可能である。

* [Deep Expander Networks: Efficient Deep Networks from Graph Theory](http://openaccess.thecvf.com/content_ECCV_2018/html/Ameya_Prabhu_Deep_Expander_Networks_ECCV_2018_paper.html)
    * ResNet vs. DenseNet的に効率のよいネットワークとは何か？精度と効率性のトレードオフをいかにグラフ理論を用いて解決するかを考察した。CNNのconnectivityに着目し、CS分野でよく調査されているExpander Graphの理論を導入したX-Netを提案したところ、効率性を高めながらMobileNetよりも4%精度向上した。

* [Learning SO(3) Equivariant Representations with Spherical CNNs](http://openaccess.thecvf.com/content_ECCV_2018/html/Carlos_Esteves_Learning_SO3_Equivariant_ECCV_2018_paper.html)
    * Spherical Networkを用いて、3次元のEquivariance（同変性）について調査を行った。3次元識別の文脈でデータ拡張も行い、pooling on the spectral domainについても提案した。

* [Deep Model-Based 6D Pose Refinement in RGB](http://openaccess.thecvf.com/content_ECCV_2018/html/Fabian_Manhardt_Deep_Model-Based_6D_ECCV_2018_paper.html)
    * RGBベースで画像上の物体の6D poseを推定し、refinementするネットワークを提案している。本手法では輪郭ベースの追跡から着想を得て、DNNに平行移動および回転の更新させる新しいvisual lossを提案しているため、明示的に外観モデルを定義をする必要がない。実験の結果、Depthデータを用いずとも3D ICPに近い精度で物体の姿勢を推定でき、さらにリアルタイムで実行できる。

* [ContextVP: Fully Context-Aware Video Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Wonmin_Byeon_ContextVP_Fully_Context-Aware_ECCV_2018_paper.html)
    * video predictionにおいて、過去の情報を大量に用いることで精度を向上した。既存手法ではpooling層で情報を集約してしまい、過去情報が失われてしまう。その問題に対処するため、Parallel Multi-Dimensional LSTMユニットを使用して各ピクセルにおける過去のコンテキスト全体をキャプチャしている。提案手法をチャレンジングなデータセット(Human 3.6M、Caltech Pedestrian、UCF-101)で実験した結果、state-of-the-artな結果を出した。さらに提案手法ではモデルにおけるパラメータが少なく、既存手法では前景背景分離や敵対的学習、motion flow学習に重視しているが、video predictionに関しては過去の情報を用いることが効果的であることを示している。

* [CornerNet: Detecting Objects as Paired Keypoints](http://openaccess.thecvf.com/content_ECCV_2018/html/Hei_Law_CornerNet_Detecting_Objects_ECCV_2018_paper.html)
    * top-leftとbottom-rightのキーポイントを検出するCornerNetを提案している。一般的なobject detectionでは最初に物体候補領域を推定しているが、CornerNetではそれを排除している。その代わりに、物体のコーナーをヒートマップで出力するcorner poolingを提案し、MS COCOにおいてone-stage detectorで42.1% APの精度となっている。

* [RelocNet: Continous Metric Learning Relocalisation using Neural Nets](http://openaccess.thecvf.com/content_ECCV_2018/html/Vassileios_Balntas_RelocNet_Continous_Metric_ECCV_2018_paper.html)
    * 最近傍マッチおよび連続メトリック学習に基づく特徴記述子を用いて、カメラ姿勢探索に適したconvolutional learningを提案している。

* [Museum Exhibit Identification Challenge for the Supervised Domain Adaptation.](http://openaccess.thecvf.com/content_ECCV_2018/html/Piotr_Koniusz_Museum_Exhibit_Identification_ECCV_2018_paper.html)
    * 美術展示品の画像データセットでOpen Museum Identification Challenge (Open MIC)の提案。10の異なる美術館から絵画、時計、彫刻、ガラス製品、遺物、科学展、自然史資料、陶磁器、陶器、道具、土木工芸品などの写真を携帯電話/ウェアラブルカメラで撮影した。展示品には照明、モーションブラー、オクルージョン、クラッタ、視点とスケールの変動、回転、グレア、透明性、非平面性、クリッピングなどの品質問題など、多くの課題がある。

* [Acquisition of Localization Confidence for Accurate Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Borui_Jiang_Acquisition_of_Localization_ECCV_2018_paper.html) [[GitHub](https://github.com/vacancy/PreciseRoIPooling)]
    * 物体検出タスクにおいて推定したbboxのIoUを計算してくれるIou-Netを提案。従来のNon-maximum supression（NMS）では物体ラベルの尤度に基づいてbboxを回帰してきたが、本来はbbox自体の推定尤度を出すべきであろうというところから研究がなされている。RoIPooling/RoI-Alignに対して改良版であるPreciseRoIPooling（PrRoIPooling）を提案、IoU-NetはIoU、識別尤度、bbox-regを出力する。MSCOCOにてSoTAな精度。

* [The Contextual Loss for Image Transformation with Non-Aligned Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Roey_Mechrez_The_Contextual_Loss_ECCV_2018_paper.html) [[GitHub](https://github.com/roimehrez/contextualLoss)]
    * 画像変換タスクのためのコンテキスト誤差（Contextual Loss）の提案。Pix2Pixなどはピクセル位置が合致していることが条件であるが、本論文で提案するう誤差はコンテキストやセマンティックに依存するため、多少異なる配置の顔同士でも誤差計算ができる。論文中ではリアル顔をアニメ調にしたり、異なる画像の異なる人物同士を合成、超解像や法線ベクトル推定を行った。

* [Saliency Benchmarking Made Easy: Separating Models, Maps and Metrics](http://openaccess.thecvf.com/content_ECCV_2018/html/Matthias_Kummerer_Saliency_Benchmarking_Made_ECCV_2018_paper.html)
    * 顕著性マップに関する問題を整理した。現在までの顕著性マップの評価は整合性がなく、すべての指標にて効果的なモデルなどがなかった。本論文では顕著性マップとモデルを切り離して考えることで、ベンチマーキングを有意義に行うことに成功した。

* [Multi-Attention Multi-Class Constraint for Fine-grained Image Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Ming_Sun_Multi-Attention_Multi-Class_Constraint_ECCV_2018_paper.html)
    * 詳細画像識別の問題にて、複数のアテンションを抽出できるような最適化Multi-attention multi-class constraint (MAMC)やモジュールOne-squeeze Multi-excitation (OSME)にした。

* [DeepTAM: Deep Tracking and Mapping](http://openaccess.thecvf.com/content_ECCV_2018/html/Huizhong_Zhou_DeepTAM_Deep_Tracking_ECCV_2018_paper.html)
    * キーフレームベースのカメラトラッキング＋depth推定の提案。  
    トラッキングでは現在のカメラ画像と結合画像との間のポーズ増分を推定する。

* [Convolutional Networks with Adaptive Computation Graphs](http://openaccess.thecvf.com/content_ECCV_2018/html/Andreas_Veit_Convolutional_Networks_with_ECCV_2018_paper.html)
    * 上と同じ

* [Progressive Neural Architecture Search](http://openaccess.thecvf.com/content_ECCV_2018/html/Chenxi_Liu_Progressive_Neural_Architecture_ECCV_2018_paper.html)
    * 上と同じ

* [Diverse Image-to-Image Translation via Disentangled Representations](http://openaccess.thecvf.com/content_ECCV_2018/html/Hsin-Ying_Lee_Diverse_Image-to-Image_Translation_ECCV_2018_paper.html)
    * 上と同じ

* [Lifting Layers: Analysis and Applications](http://openaccess.thecvf.com/content_ECCV_2018/html/Michael_Moeller_Lifting_Layers_Analysis_ECCV_2018_paper.html)
    * 上と同じ

* [Learning with Biased Complementary Labels](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiyu_Yu_Learning_with_Biased_ECCV_2018_paper.html)
    * 上と同じ

* [Light Structure from Pin Motion: Simple and Accurate Point Light Calibration for Physics-based Modeling](http://openaccess.thecvf.com/content_ECCV_2018/html/Hiroaki_Santo_Light_Structure_from_ECCV_2018_paper.html)
    * 上と同じ

* [Programmable Light Curtains](http://openaccess.thecvf.com/content_ECCV_2018/html/Jian_Wang_Programmable_Light_Curtains_ECCV_2018_paper.html)
    * 上と同じ

* [Learning to Separate Object Sounds by Watching Unlabeled Video](http://openaccess.thecvf.com/content_ECCV_2018/html/Ruohan_Gao_Learning_to_Separate_ECCV_2018_paper.html)
    * 上と同じ

* [Coded Two-Bucket Cameras for Computer Vision](http://openaccess.thecvf.com/content_ECCV_2018/html/Mian_Wei_Coded_Two-Bucket_Cameras_ECCV_2018_paper.html)
    * 上と同じ

* [Materials for Masses: SVBRDF Acquisition with a Single Mobile Phone Image](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhengqin_Li_Materials_for_Masses_ECCV_2018_paper.html)
    * 上と同じ

* [End-to-End Joint Semantic Segmentation of Actors and Actions in Video](http://openaccess.thecvf.com/content_ECCV_2018/html/Jingwei_Ji_End-to-End_Joint_Semantic_ECCV_2018_paper.html)
    * 上と同じ

* [Learning-based Video Motion Magnification](http://openaccess.thecvf.com/content_ECCV_2018/html/Tae-Hyun_Oh_Learning-based_Video_Motion_ECCV_2018_paper.html)
    * 上と同じ

* [Massively Parallel Video Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Viorica_Patraucean_Massively_Parallel_Video_ECCV_2018_paper.html)
    * 上と同じ

* [DeepWrinkles: Accurate and Realistic Clothing Modeling](http://openaccess.thecvf.com/content_ECCV_2018/html/Zorah_Laehner_DeepWrinkles_Accurate_and_ECCV_2018_paper.html)
    * 上と同じ

* [Learning Discriminative Video Representations Using Adversarial Perturbations](http://openaccess.thecvf.com/content_ECCV_2018/html/Jue_Wang_Learning_Discriminative_Video_ECCV_2018_paper.html)
    * 上と同じ

* [Scaling Egocentric Vision: The E-Kitchens Dataset](http://openaccess.thecvf.com/content_ECCV_2018/html/Dima_Damen_Scaling_Egocentric_Vision_ECCV_2018_paper.html)
    * 上と同じ

* [Unsupervised Person Re-identification by Deep Learning Tracklet Association](http://openaccess.thecvf.com/content_ECCV_2018/html/Minxian_Li_Unsupervised_Person_Re-identification_ECCV_2018_paper.html)
    * 上と同じ

* [Predicting Gaze in Egocentric Video by Learning Task-dependent Attention Transition](http://openaccess.thecvf.com/content_ECCV_2018/html/Huang_Predicting_Gaze_in_ECCV_2018_paper.html)
    * 上と同じ

* [Instance-level Human Parsing via Part Grouping Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Ke_Gong_Instance-level_Human_Parsing_ECCV_2018_paper.html)
    * 上と同じ

* [Adversarial Geometry-Aware Human Motion Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Liangyan_Gui_Adversarial_Geometry-Aware_Human_ECCV_2018_paper.html)
    * 上と同じ

* [Weakly-supervised 3D Hand Pose Estimation from Monocular RGB Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Yujun_Cai_Weakly-supervised_3D_Hand_ECCV_2018_paper.html)
    * 上と同じ

* [Audio-Visual Scene Analysis with Self-Supervised Multisensory Features](http://openaccess.thecvf.com/content_ECCV_2018/html/Andrew_Owens_Audio-Visual_Scene_Analysis_ECCV_2018_paper.html)
    * 上と同じ

* [Jointly Discovering Visual Objects and Spoken Words from Raw Sensory Input](http://openaccess.thecvf.com/content_ECCV_2018/html/David_Harwath_Jointly_Discovering_Visual_ECCV_2018_paper.html)
    * 上と同じ

* [DeepIM: Deep Iterative Matching for 6D Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yi_Li_DeepIM_Deep_Iterative_ECCV_2018_paper.html)
    * 上と同じ

* [Implicit 3D Orientation Learning for 6D Object Detection from RGB Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Martin_Sundermeyer_Implicit_3D_Orientation_ECCV_2018_paper.html)
    * 上と同じ

* [Direct Sparse Odometry With Rolling Shutter](http://openaccess.thecvf.com/content_ECCV_2018/html/David_Schubert_Direct_Sparse_Odometry_ECCV_2018_paper.html)
    * 上と同じ

* [3D Scene Flow from 4D Light Field Gradients](http://openaccess.thecvf.com/content_ECCV_2018/html/Sizhuo_3D_Motion_Sensing_ECCV_2018_paper.html)
    * 上と同じ

* [A Style-aware Content Loss for Real-time HD Style Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Artsiom_Sanakoyeu_A_Style-aware_Content_ECCV_2018_paper.html)
    * 上と同じ

* [Scale-Awareness of Light Field Camera based Visual Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Niclas_Zeller_Scale-Awareness_of_Light_ECCV_2018_paper.html)
    * 上と同じ

* [Burst Image Deblurring Using Permutation Invariant Convolutional Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Miika_Aittala_Burst_Image_Deblurring_ECCV_2018_paper.html)
    * 上と同じ

* [MVSNet: Depth Inference for Unstructured Multi-view Stereo](http://openaccess.thecvf.com/content_ECCV_2018/html/Yao_Yao_MVSNet_Depth_Inference_ECCV_2018_paper.html)
    * 上と同じ

* [PlaneMatch: Patch Coplanarity Prediction for Robust RGB-D Registration](http://openaccess.thecvf.com/content_ECCV_2018/html/Yifei_Shi_PlaneMatch_Patch_Coplanarity_ECCV_2018_paper.html)
    * 上と同じ

* [Active Stereo Net: End-to-End Self-Supervised Learning for Active Stereo Systems](http://openaccess.thecvf.com/content_ECCV_2018/html/Yinda_Zhang_Active_Stereo_Net_ECCV_2018_paper.html)
    * 上と同じ

* [GAL: Geometric Adversarial Loss for Single-View 3D-Object Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Li_Jiang_GAL_Geometric_Adversarial_ECCV_2018_paper.html)
    * 上と同じ

* [Deep Virtual Stereo Odometry: Leveraging Deep Depth Prediction for Monocular Direct Sparse Odometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Nan_Yang_Deep_Virtual_Stereo_ECCV_2018_paper.html)
    * 上と同じ

* [Unsupervised Geometry-Aware Representation for 3D Human Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Helge_Rhodin_Unsupervised_Geometry-Aware_Representation_ECCV_2018_paper.html)
    * 上と同じ

* [Dual-Agent Deep Reinforcement Learning for Deformable Face Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Minghao_Guo_Dual-Agent_Deep_Reinforcement_ECCV_2018_paper.html)
    * 上と同じ

* [Deep Autoencoder for Combined Human Pose Estimation and Body Model Upscaling](http://openaccess.thecvf.com/content_ECCV_2018/html/Matthew_Trumble_Deep_Autoencoder_for_ECCV_2018_paper.html)
    * 上と同じ

* [Occlusion-aware Hand Pose Estimation Using Hierarchical Mixture Density Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Qi_Ye_Occlusion-aware_Hand_Pose_ECCV_2018_paper.html)
    * 上と同じ

* [GANimation: Anatomically-aware Facial Animation from a Single Image](http://openaccess.thecvf.com/content_ECCV_2018/html/Albert_Pumarola_Anatomically_Coherent_Facial_ECCV_2018_paper.html)
    * 上と同じ

* [Deterministic Consensus Maximization with Biconvex Programming](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhipeng_Cai_Deterministic_Consensus_Maximization_ECCV_2018_paper.html)
    * 上と同じ

* [Robust fitting in computer vision: easy or hard?](http://openaccess.thecvf.com/content_ECCV_2018/html/Tat-Jun_Chin_Robust_fitting_in_ECCV_2018_paper.html)
    * 上と同じ

* [Highly-Economized Multi-View Binary Compression for Scalable Image Clustering](http://openaccess.thecvf.com/content_ECCV_2018/html/Zheng_Zhang_Highly-Economized_Multi-View_Binary_ECCV_2018_paper.html)
    * 上と同じ

* [Efficient Semantic Scene Completion Network with Spatial Group Convolution](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiahui_Zhang_Efficient_Semantic_Scene_ECCV_2018_paper.html)
    * 上と同じ

* [Asynchronous, Photometric Feature Tracking using Events and Frames](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Gehrig_Asynchronous_Photometric_Feature_ECCV_2018_paper.html)
    * 上と同じ

* [Group Normalization](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuxin_Wu_Group_Normalization_ECCV_2018_paper.html)
    * 上と同じ

* [Deep Matching Autoencoder]()
    * 上と同じ

* [Deep Expander Networks: Efficient Deep Networks from Graph Theory](http://openaccess.thecvf.com/content_ECCV_2018/html/Ameya_Prabhu_Deep_Expander_Networks_ECCV_2018_paper.html)
    * 上と同じ

* [Towards Realistic Predictors](http://openaccess.thecvf.com/content_ECCV_2018/html/Pei_Wang_Towards_Realistic_Predictors_ECCV_2018_paper.html)
    * 上と同じ

* [Learning SO(3) Equivariant Representations with Spherical CNNs](http://openaccess.thecvf.com/content_ECCV_2018/html/Carlos_Esteves_Learning_SO3_Equivariant_ECCV_2018_paper.html)
    * 上と同じ

* [CornerNet: Detecting Objects as Paired Keypoints](http://openaccess.thecvf.com/content_ECCV_2018/html/Hei_Law_CornerNet_Detecting_Objects_ECCV_2018_paper.html)
    * 上と同じ

* [RelocNet: Continous Metric Learning Relocalisation using Neural Nets](http://openaccess.thecvf.com/content_ECCV_2018/html/Vassileios_Balntas_RelocNet_Continous_Metric_ECCV_2018_paper.html)
    * 上と同じ

* [The Contextual Loss for Image Transformation with Non-Aligned Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Roey_Mechrez_The_Contextual_Loss_ECCV_2018_paper.html)
    * 上と同じ

* [Acquisition of Localization Confidence for Accurate Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Borui_Jiang_Acquisition_of_Localization_ECCV_2018_paper.html)
    * 上と同じ

* [Deep Model-Based 6D Pose Refinement in RGB](http://openaccess.thecvf.com/content_ECCV_2018/html/Fabian_Manhardt_Deep_Model-Based_6D_ECCV_2018_paper.html)
    * 上と同じ

* [DeepTAM: Deep Tracking and Mapping](http://openaccess.thecvf.com/content_ECCV_2018/html/Huizhong_Zhou_DeepTAM_Deep_Tracking_ECCV_2018_paper.html)
    * 上と同じ

* [ContextVP: Fully Context-Aware Video Prediction](http://openaccess.thecvf.com/content_ECCV_2018/html/Wonmin_Byeon_ContextVP_Fully_Context-Aware_ECCV_2018_paper.html)
    * 上と同じ

* [Saliency Benchmarking Made Easy: Separating Models, Maps and Metrics](http://openaccess.thecvf.com/content_ECCV_2018/html/Matthias_Kummerer_Saliency_Benchmarking_Made_ECCV_2018_paper.html)
    * 上と同じ

* [Museum Exhibit Identification Challenge for the Supervised Domain Adaptation.](http://openaccess.thecvf.com/content_ECCV_2018/html/Piotr_Koniusz_Museum_Exhibit_Identification_ECCV_2018_paper.html)
    * 上と同じ

* [Multi-Attention Multi-Class Constraint for Fine-grained Image Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Ming_Sun_Multi-Attention_Multi-Class_Constraint_ECCV_2018_paper.html)
    * 上と同じ

* [Depth-aware CNN for RGB-D Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Weiyue_Wang_Depth-aware_CNN_for_ECCV_2018_paper.html)
    * RGB-D Semantic Segmentationの新しい手法としてdepth-aware   
    convolutionとdepth-aware average poolingからなるCNNを提案。  
    state-of-the-artと比べ精度や計算コストの点で有利。実装も楽で計算的な

* [Object Detection in Video with Spatiotemporal Sampling Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Gedas_Bertasius_Object_Detection_in_ECCV_2018_paper.html)
    * ビデオ中の物体検出を行うためにデフォメーションを考慮したCNNを考案。時間tのフレームとサポートとしてt+kのフレームから処理を行うことで、ビデオに起きがちなブラー中においても物体検出することができる。ImageNet VIDのデータを用いて検証を行った。

* [Dependency-aware Attention Control for Unconstrained Face Recognition with Image Sets](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaofeng_Liu_Dependency-aware_Attention_Control_ECCV_2018_paper.html)
    * 顔認証に関する研究であり、強化学習を導入して個人内、個人間の特徴抽出をよくする。Markov Decision Process (MDP)を用いた潜在空間探索問題？

* [License Plate Detection and Recognition in Unconstrained Scenarios](http://openaccess.thecvf.com/content_ECCV_2018/html/Sergio_Silva_License_Plate_Detection_ECCV_2018_paper.html)
    * 自動車のナンバープレート（License Place）を検出・認識する研究である。形状変換も考慮して自動で検出、およびOCR的に文字認識してくれる。さらに、困難な場面においてもいかにアノテーションを実施するかについて言及。車検出、プレート検出、形状変換（rectification）、OCRについて一貫して実装。

* [Revisiting the Inverted Indices for Billion-Scale Approximate Nearest Neighbors](http://openaccess.thecvf.com/content_ECCV_2018/html/Dmitry_Baranchuk_Revisiting_the_Inverted_ECCV_2018_paper.html)
    * 画像検索の高速化・高度化に関する研究であり、Billion-scaleの最近傍探索（Nearest Neighbor）問題、しかもMulti-indexの問題について言及。インデックスごとに？分解可能なディープ特徴（Highly-disentangled Deep Descriptor）を提案して高度な画像検索を実施した。

* [Zero-Annotation Object Detection with Web Knowledge Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Qingyi_Tao_Zero-Annotation_Object_Detection_ECCV_2018_paper.html)
    * 物体検出についての研究。本論文では，自由に利用できるweb画像を用いて人の手によるアノテーションを必要としない物体検出手法を提案している。3つのコンポーネントによるmulti-stream networkによって構成されている。

* [Semi-supervised Adversarial Learning to Generate Photorealistic Face Images of New Identities from 3D Morphable Model](http://openaccess.thecvf.com/content_ECCV_2018/html/Baris_Gecer_Semi-supervised_Adversarial_Learning_ECCV_2018_paper.html)
    * リアルな顔画像生成の問題について扱う。生成には2つのGeneratorにより構成されるGANsを採用、入力がSimGAN的にシミュレーション画像、出力がよりリアルな顔画像である。やはりSimGAN的に学習画像としても評価を行った。オリジナル画像+GANs生成画像における実験では多少精度向上が見られ、SimGANよりも良好な精度を実現。

* [Improving Shape Deformation in Unsupervised Image-to-Image Translation](http://openaccess.thecvf.com/content_ECCV_2018/html/Aaron_Gokaslan_Improving_Shape_Deformation_ECCV_2018_paper.html)
    * Image-to-Imageの文脈で形状変換を行う研究であり、例えば犬領域を猫領域に、その逆の変換も行う研究である。コンテキストに沿った変換を行うために、セマンティックセグメンテーションやDilated Convをツールとして用い、さらにはConceptualLossをマルチスケールで計算する枠組みにして同問題を解決した。

* [K-convexity shape priors for segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Hossam_Isack_K-convexity_shape_priors_ECCV_2018_paper.html)
    * K-convexity（凸最適化において凸が複数ある問題）において、複数の極値を求めることでセグメンテーションを実施する。例えば、複数のテニスボールが重なっている状況でインスタンスごとに切り分けるような場面を想定する。

* [Visual Question Generation for Class Acquisition of Unknown Objects](http://openaccess.thecvf.com/content_ECCV_2018/html/Kohei_Uehara_Visual_Question_Generation_ECCV_2018_paper.html)
    * 画像からUnknown物体検出及び検出された物体に対し質問文を自動生成するネットワークを提案した．提案手法により，有効的にUnknown物体から情報を収集できる．

* [Sampling Algebraic Varieties for Robust Camera Autocalibration](http://openaccess.thecvf.com/content_ECCV_2018/html/Danda_Pani_Paudel_Sampling_Algebraic_Varieties_ECCV_2018_paper.html)
    * カメラのオートキャリブレーションを行い、3次元再構成を行う問題である。最適化の多項式を解くためにCconsensus maximizationを計算する。

* [Hand Pose Estimation via Latent 2.5D Heatmap Regression](http://openaccess.thecvf.com/content_ECCV_2018/html/Umar_Iqbal_Hand_Pose_Estimation_ECCV_2018_paper.html)
    * 新規の2.5次元姿勢表現を通して，単眼カメラの画像から3次元姿勢推定のための新しい手法を提案。 また可微分な損失関数を使った潜伏性のある方法によって2.5次元ヒートマップを学習するためのCNNアーキテクチャーを提案した。

* [Single-view Hair Reconstruction using Convolutional Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Yi_Zhou_Single-view_Hair_Reconstruction_ECCV_2018_paper.html)
    * DNNベースの手法により3Dヘアジオメトリをリアルタイムに生成。  
    2D画像からヘアマスク推定を行いヘア領域のオリエンテーションを  
    計算。それを入力とすることで様々な入力画像に対し滑らかで密な

* [Super-Identity Convolutional Neural Network for Face Hallucination](http://openaccess.thecvf.com/content_ECCV_2018/html/Kaipeng_Zhang_Super-Identity_Convolutional_Neural_ECCV_2018_paper.html)
    * Face Hallucination法は、 事例学習に基づき単一の低解像度顔画像から高解像度顔画像を生成する手法である。しかしながら，従来のFace　Hallucinationは低解像度から高解像度にする際に顔の個性を大きく無視している。そのため本論文では顔の個性を考慮するためにSuper-Identity Convolutional Neural Network (SICNN)を提案している

* [Receptive Field Block Net for Accurate and Fast Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Songtao_Liu_Receptive_Field_Block_ECCV_2018_paper.html)
    * Receptive Fieldを変形したカーネルを用いて畳み込みネットを行う研究である。直感的にはDilated Convのマルチスケール化？物体検出問題にて、SSDに導入したところベースラインよりも多少精度向上したことが確認された。

* [Interpretable Intuitive Physics Model](http://openaccess.thecvf.com/content_ECCV_2018/html/Tian_Ye_Interpretable_Intuitive_Physics_ECCV_2018_paper.html)
    * 物理現象の時間的予測のみならず、そのファクターなど理由づけについても実施する。例えば、物体の重さが異なるときに坂を転がる速さが変わるかどうか？などの予測や原因について推定する。Interpretabilityの研究という意味では将来的な話か。

* [Variable Ring Light Imaging: Capturing Transient Subsurface Scattering with An Ordinary Camera](http://openaccess.thecvf.com/content_ECCV_2018/html/Ko_Nishino_Variable_Ring_Light_ECCV_2018_paper.html)
    * 新規の画像検査法の提案。外界からの反射光を散乱させて変化する境界光路長と，それに比例したバウンス数に変化させるためのvariable ring light imagingを導入

* [Facial Dynamics Interpreter Network: What are the Important Relations between Local Dynamics for Facial Trait Estimation?](http://openaccess.thecvf.com/content_ECCV_2018/html/Seong_Tae_Kim_Facial_Dynamics_Interpreter_ECCV_2018_paper.html)
    * 顔の特徴の推定関する研究。本論文では，facial dynamics interpreter networkと呼ばれる顔の特徴を推定する新規の学習手法を提案。顔の特徴は、顔の局所的ダイナミクスの関係特性を関係の重要性に基づいて組み合わせることによって推定された。従来手法との比較実験によって提案された方法は、最先端の方法と比較して顔の特徴（年齢および性別）を正確に推定することができた。

* [Text2Colors: Guiding Image Colorization through Text-Driven Palette Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Wonwoong_Cho_Text2Colors__Guiding_ECCV_2018_paper.html)
    * 本論文では入力テキストの意味づけ(セマンティック)を適用して複数のカラーパレットを生成し，それを基に入力されたグレースケール画像に色付けをする新規のアプローチを提案している。

* [Sparsely Aggregated Convolutional Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Ligeng_Zhu_Sparsely_Aggregated_Convolutional_ECCV_2018_paper.html)
    * 集約リンクの複雑さをネットワーク深度で対数的にスケーリングすることにより，シンプルなCNNアーキテクチャを構築

* [Deep Attention Neural Tensor Network for Visual Question Answering](http://openaccess.thecvf.com/content_ECCV_2018/html/Yalong_Bai_Deep_Attention_Neural_ECCV_2018_paper.html)
    * テンソルベースの表現を用いて画像、質問および回答に対する共同相関を発見することができるVQAのための新規なdeep attention neural tensor network (DA-NTN)の提案

* [Diverse feature visualizations reveal invariances in early layers of deep neural networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Santiago_Cadena_Diverse_feature_visualizations_ECCV_2018_paper.html)
    * DNNの可視化．DNN内の最初から中間の畳み込み層における，隠れ層ユニットの応答における不変性を発見し，可視化．

* [Sidekick Policy Learning for Active Visual Exploration](http://openaccess.thecvf.com/content_ECCV_2018/html/Santhosh_Kumar_Ramakrishnan_Sidekick_Policy_Learning_ECCV_2018_paper.html)
    * 限定的な狭視野から，広範囲環境の再構築のために，カメラの動きを選択するアクティブなしてく探査シナリオの検討．

* [DPP-Net: Device-aware Progressive Search for Pareto-optimal Neural Architectures](http://openaccess.thecvf.com/content_ECCV_2018/html/Jin-Dong_Dong_DPP-Net_Device-aware_Progressive_ECCV_2018_paper.html)
    * Neural Architectural Search (NAS) における推理時間，メモリ使用量，電力消費量などの問題を解決し，ポータブルデバイスに応用するためのDPPNetの提案．

* [Pixel2Mesh: Generating 3D Mesh Models from Single RGB Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Nanyang_Wang_Pixel2Mesh_Generating_3D_ECCV_2018_paper.html)
    * 本論文ではRGB画像から3次元のメッシュ状のモデルを生成するend-to-endのニューラル  
    ネットワークのアーキテクチャーを提案している。GCNで表される3Dジオメトリに知覚画像の特徴を組み込んだ投影レイヤーを設計している。

* [End-to-End Incremental Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Francisco_M._Castro_End-to-End_Incremental_Learning_ECCV_2018_paper.html)
    * 新しいデータと古いクラスのサンプルに対応している教師データを使って徐々に学習するend-to-endのdeep neaural networkに取り組む。CIFAR-100およびImageNetILSVRC 2012）画像分類データセットで提案手法を比較評価し，高いスコアを示したことを確認。

* [CAR-Net: Clairvoyant Attentive Recurrent Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Amir_Sadeghian_CAR-Net_Clairvoyant_Attentive_ECCV_2018_paper.html)
    * 我々は、経路予測タスクを解決する際にシーンの大きな画像をどこで見るべきかを学習するClirvoyant Attentive Recurrent Network（CAR-Net）を提案。対象の軌跡を予測する際に実画像（例えば道路交差点）内の任意の領域または領域の組み合わせにより，軌跡の予測に影響を及ぼすナビゲーションシーンの細かいセマンティック要素を視覚化する。

* [Learning Data Terms for Image Deblurring](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiangxin_Dong_Learning_Data_Terms_ECCV_2018_paper.html)
    * 激しいノイズや外れ値を含む，大きなブレを除去するフレームワークの提案．従来のように単にデータフィッティング誤差を学習するのではなく，より柔軟で効率的なカスケード構造を使用していて，縮小関数を直接学習する．

* [Image Inpainting for Irregular Holes Using Partial Convolutions](http://openaccess.thecvf.com/content_ECCV_2018/html/Guilin_Liu_Image_Inpainting_for_ECCV_2018_paper.html)
    * Image Inpaintingの新手法としてPartial Convを提案。PatchMatchの  
    ようなホールの周辺情報から欠落部分を予測するのでなく、ホールとGTの  
    対応関係をDNNに学習させ画像を再構築する。  
    25000近いサンプルでテストを行い、既存手法と比べより自然な補間に  
    成功し、ホールの形状や大きさに対しロバストである。

* [SRDA: Generating Instance Segmentation Annotation Via Scanning, Reasoning And Domain Adaption](http://openaccess.thecvf.com/content_ECCV_2018/html/Wenqiang_Xu_SRDA_Generating_Instance_ECCV_2018_paper.html)
    * 3DスキャンやGANベースのドメインアダプテーションを組み合わせることによって，少ないサンプルからインスタンスセグメンテーションの学習データを生成する．

* [Learning Priors for Semantic 3D Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Ian_Cherabier_Learning_Priors_for_ECCV_2018_paper.html)
    * 本論文ではvariational regularizationをニューラルネットワークに組み込む新規なsemantic 3D reconstructionフレームワークを提案している。

* [Integrating Egocentric Videos in Top-view Surveillance Videos: Joint Identification and Temporal Alignment](http://openaccess.thecvf.com/content_ECCV_2018/html/Shervin_Ardeshir_Integrating_Egocentric_Videos_ECCV_2018_paper.html)
    * トップビュービデオとエコセントリックビデオの関連付け．トップビューによる自己識別と，エコセントリックによる見える人間の識別，そしてこれら2つの統合．

* [Deep Boosting for Image Denoising](http://openaccess.thecvf.com/content_ECCV_2018/html/Chang_Chen_Deep_Boosting_for_ECCV_2018_paper.html)
    * 画像のノイズ除去のための研究である。本論文では様々な畳み込みニューラルネットワークをフィードフォワード方式で統合したノイズ除去のための新規なdeep boosting framework(DBF)を提案する。実験ではDBFは既存のノイズ除去の手法よりも優れていることを確認

* [Descending, lifting or smoothing: Secrets of robust cost optimization](http://openaccess.thecvf.com/content_ECCV_2018/html/Christopher_Zach_Descending_lifting_or_ECCV_2018_paper.html)
    * コスト最小化への取り組み，算時間の短縮、局所最小値を見つけるための改善．

* [MultiPoseNet: Fast Multi-Person Pose Estimation using Pose Residual Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Muhammed_Kocabas_MultiPoseNet_Fast_Multi-Person_ECCV_2018_paper.html)
    * マルチタスク学習による複数人の姿勢推定を行うアーキテクチャ  
    MultiPoseNetを提案。  
    ResNetによって抽出された特徴マップを人物検出とキーポイント推定を  
    行うサブネットに入力。これら二つのサブネットの出力を彼らが提案する  
    Pose Residual Network(PRN)に入力し姿勢推定を行う。COCOを使った

* [TS2C: Tight Box Mining with Surrounding Segmentation Context for Weakly Supervised Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Yunchao_Wei_TS2C_Tight_Box_ECCV_2018_paper.html)
    * 物体周辺のセグメンテーションコンテキスト情報を使いった弱教師付き学習の物体検出手法．MILベースの手法において，例えば動物全体のボックスだけでなく，顔部分のボックスも信頼度が上がってしまう問題を解決する．つまり，物体候補をしっかり選別する試み．

* [End-to-End Deep Structured Models for Drawing Crosswalks](http://openaccess.thecvf.com/content_ECCV_2018/html/Justin_Liang_End-to-End_Deep_Structured_ECCV_2018_paper.html)
    * 交差点などの道路における横断歩道のエリアの検出をDNNを用いて行っている。LiDARとカメラ画像を用いて横断歩道の検出することを目的としている。複数のLiDARスイープとそれに対応する画像が与えられた場合、両方の入力を地面に投影して、シーンのトップダウンビューを生成します。次に、畳み込みニューラルネットワークを利用して、クロスウォークの位置に関する意味的きっかけを抽出する。実験では，市街地の横断歩道を96.6%の精度で検出。

* [Efficient Global Point Cloud Registration by Matching Rotation Invariant Features Through Translation Search](http://openaccess.thecvf.com/content_ECCV_2018/html/Yinlong_Liu_Efficient_Global_Point_ECCV_2018_paper.html)
    * BnBベースの点群レジストレーションを提案。並進と回転の自由度を分離  
    して最適化を行う点で従来手法と異なる。高速BnBによって並進パラメー  
    タを最適化し、これを用いて回転パラメータを計算する。このとき、新し  
    く提案された回転不変特徴量を用いる。速度と精度の両方でstate-of-

* [Large Scale Urban Scene Modeling from MVS Meshes](http://openaccess.thecvf.com/content_ECCV_2018/html/Lingjie_Zhu_Large_Scale_Urban_ECCV_2018_paper.html)
    * ラージスケールな都市景観のためのモデリング。セグメンテーションと  
    建築モデリングの２ステップから成る。ビジュアルとジオメトリの特徴  
    を融合し、MRF形式でセグメンテーションする。建築モデリングでは3D  
    モデリングを2Dラベリング問題に変換する。state-of-the-artと比べて、

* [Sub-GAN: An Unsupervised Generative Model via Subspaces](http://openaccess.thecvf.com/content_ECCV_2018/html/Jie_Liang_Sub-GAN_An_Unsupervised_ECCV_2018_paper.html)
    * 画像やビデオなどの複雑なデータにおいて，高次元空間の分布を活用したGANモデルは困難．そこで，逐次的にどのように生成モデルの学習を行うか決定する，部分空間ベースのsub-GANの提案．

* [Pseudo Pyramid Deeper Bidirectional ConvLSTM for Video Saliency Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Hongmei_Song_Pseudo_Pyramid_Deeper_ECCV_2018_paper.html)
    * 動画中の顕著性の高い物体を，高速に検出するモデルの提案．名前の通り，反復的かつ(convLSTM)，複数のスケール(pyramid)において同時に特徴を抽出することができる．

* [Practical Black-box Attacks on Deep Neural Networks using Efficient Query Mechanisms](http://openaccess.thecvf.com/content_ECCV_2018/html/Arjun_Nitin_Bhagoji_Practical_Black-box_Attacks_ECCV_2018_paper.html)
    * 譲渡性に頼らないターゲットモデルのクラス確率に対するクエリアクセスを有する敵対者に対する新規のblack-box attack勾配推定を提案。

* [Learning 3D Shape Priors for Shape Completion and Reconstruction](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiajun_Wu_Learning_3D_Shape_ECCV_2018_paper.html)
    * 単一視点からの3D形状補完と再構成．

* [Comparator Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Weidi_Xie_Comparator_Networks_ECCV_2018_paper.html)
    * 2組の顔画像が同じ人物か否かを判断．比較に特化しており，単なる分類タスクとは異なる．入力画像数が可変であることにも注目．

* [Improving Fine-Grained Visual Classification using Pairwise Confusion](http://openaccess.thecvf.com/content_ECCV_2018/html/Abhimanyu_Dubey_Improving_Fine-Grained_Visual_ECCV_2018_paper.html)
    * Fine-Grained Visual Classi?cation (FGVC) における新提案．クラス間のばらつきがや，類似性の高さといった問題に挑戦．

* [Visual-Inertial Object Detection and Mapping](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaohan_Fei_Visual-Inertial_Object_Detection_ECCV_2018_paper.html)
    * 単眼カメラと慣性センサによって，3Dシーンの物体検出とマッピングを行う．具体的には，固定された物体(自動車，建物，家具など)において，屋外/屋内関わらず，環境内の点群モデルを生成する．

* [Learning Region Features for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiayuan_Gu_Learning_Region_Features_ECCV_2018_paper.html)
    * RoIプーリングよりも優れた特徴領域抽出手法の提案．RoIやAlignと異なり，学習することができる．物体検出の精度は上がっているようだが，更なる解析・検証の余地あり？

* [Efficient Dense Point Cloud Object Reconstruction using Deformation Vector Fields](http://openaccess.thecvf.com/content_ECCV_2018/html/Kejie_Li_Efficient_Dense_Point_ECCV_2018_paper.html)
    * シングルビュー画像から密なポイントクラウドを生成．

* [Evaluating Capability of Deep Neural Networks for Image Classification via Information Plane](http://openaccess.thecvf.com/content_ECCV_2018/html/Hao_Cheng_Evaluating_Capability_of_ECCV_2018_paper.html)
    * DNN画像分類タスク評価．そして，新たなDNN評価フレームワークの提案．相互情報(2つの確率変数の相互依存の尺度を表す量)を適用することにより，損失曲線よりも有益な情報を得られ，ネットワークの選択に役立つ．

* [Shuffle-Then-Assemble: Learning Object-Agnostic Visual Relationship Features](http://openaccess.thecvf.com/content_ECCV_2018/html/XU_YANG_Shuffle-Then-Assemble_Learning_Object-Agnostic_ECCV_2018_paper.html)
    * 物体に依存しない，リレーションシップモデルのための視覚的特徴の学習．従来手法のように，物体ペアの依存関係に左右されない，視覚に依存した学習を行うことができる．

* [Zero-Shot Deep Domain Adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Kuan-Chuan_Peng_Zero-Shot_Deep_Domain_ECCV_2018_paper.html)
    * おメインアダプテーションにおいて，タスクに関連しないデータにおいても学習できるような提案．

* [Deep Imbalanced Attribute Classification using Visual Attention Aggregation](http://openaccess.thecvf.com/content_ECCV_2018/html/Nikolaos_Sarafianos_Deep_Imbalanced_Attribute_ECCV_2018_paper.html)
    * 人間の視覚的属性を学習することは，大きなクラスの不均衡と意味的/空間的な属性の注釈の欠如から逃れる複数ラベルの分類問題である。これらの課題に対処するために本論文では，visual attentionマスクを複数のスケールで出力しクラスの不均衡や高い予測分散を持つサンプルを処理するアーキテクチャを提案した。

* [Video Object Segmentation by Learning Location-Sensitive Embeddings](http://openaccess.thecvf.com/content_ECCV_2018/html/Hai_Ci_Video_Object_Segmentation_ECCV_2018_paper.html)
    * ビデオセグメンテーションタスク．最初のフレームにバウンディングボックスを与えることで，ターゲットを絞ってオブジェクトのマスクを出力できる．その後のフレームでは，前フレームの結果に基づいてバウンディングボックスのサイズを変更し，前景領域にズームインする．トリミング後，前景予測と位置予測を行い，2つの結果をマージして最終的な出力を行う．

* [Deep Multi-Task Learning to Recognise Subtle Facial Expressions of Mental States](http://openaccess.thecvf.com/content_ECCV_2018/html/Guosheng_Hu_Deep_Multi-Task_Learning_ECCV_2018_paper.html)
    * マルチタスク学習による表情認識。CNNのどのレイヤを共有するかなど、

* [Where Will They Go? Predicting Fine-Grained Adversarial Multi-Agent Motion using Conditional Variational Autoencoders](http://openaccess.thecvf.com/content_ECCV_2018/html/Panna_Felsen_Where_Will_They_ECCV_2018_paper.html)
    * 複数エージェントのトラッキング手法としてCVAEを提案。エージェントの  
    敵対性と利用可能なデータ量を考慮してバスケットボールの試合動画を

* [Video Summarization Using Fully Convolutional Sequence Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Mrigank_Rochan_Video_Summarization_Using_ECCV_2018_paper.html)
    * 入力次元の一般化によってセマンティックセグメンテーションとビデオサ  
    マリーの共通項を見出だした。時間軸に対しセマンティックな領域を抽出  
    することでビデオサマリーを可能にする。リカレントなモデルと比べGPU

* [ConceptMask: Large-Scale Segmentation from Semantic Concepts](http://openaccess.thecvf.com/content_ECCV_2018/html/Yufei_Wang_ConceptMask_Large-Scale_Segmentation_ECCV_2018_paper.html)
    * Large-Scaleなセマンティックセグメンテーションを難しくするラベル  
    の曖昧さを克服するために、異なるレベルのコンセプト（人なのか顔なの  
    かなど）を考慮した画像分割問題としてタスクを定式化。多数のコンセプ

* [Conditional Image-Text Embedding Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Bryan_Plummer_Conditional_Image-Text_Embedding_ECCV_2018_paper.html)
    * この論文では、画像内のテキストを学習するのに単一のエンドツーエンドモデルで複数のテキスト条件付き埋め込みを 学習するアプローチをしている。

* [Geolocation Estimation of Photos using a Hierarchical Model and Scene Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Eric_Muller-Budack_Geolocation_Estimation_of_ECCV_2018_paper.html)
    * 地球スケールの位置推定を行うDNNベースの手法を提案。地球を地理的な  
    セルに分割し位置推定を分類問題と考える。さらにシーンの情報も利用す  
    る。地理的なセルを分類するタスクとシーン認識のタスクをマルチタスク

* [Learning Deep Representations with Probabilistic Knowledge Transfer](http://openaccess.thecvf.com/content_ECCV_2018/html/Nikolaos_Passalis_Learning_Deep_Representations_ECCV_2018_paper.html)
    * 既存のナレッジトランスファーは分類タスクごとに調整され、他のタスク  
    に対して効果的でないが、特徴空間内のデータの確率分布をマッチさせる

* [A Trilateral Weighted Sparse Coding Scheme for Real-World Image Denoising](http://openaccess.thecvf.com/content_ECCV_2018/html/XU_JUN_A_Trilateral_Weighted_ECCV_2018_paper.html)
    * RGB同時スパースコーディングによるデノイズの提案．ガウスノイズでは表現できない実際のCCDやCMOSセンサのノイズ表現能力があると主張．3分強できれいになる．毛のような元の高周波パターンもそこそこ維持している．

* [Saliency Detection in 360$^\circ$ Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Ziheng_Zhang_Saliency_Detection_in_ECCV_2018_paper.html)
    * 球体CNN（arXiv:1801.10130，こっちは対3Dデータ）で360度パノラマ動画の顕著性をとる．

* [Learning to Blend Photos](http://openaccess.thecvf.com/content_ECCV_2018/html/Wei-Chih_Hung_Learning_to_Blend_ECCV_2018_paper.html)
    * 人手でやるとCropとかAlignmentとかプロセスが多くて時間がかかりがちな写真のブレンディングをDLで自動でやる．いい見た目になるように前景・背景の2枚の画像配置が決まるのはAttentionのノリがうまく使えている感じがしていい．

* [Escaping from Collapsing Modes in a Constrained Space](http://openaccess.thecvf.com/content_ECCV_2018/html/Chieh_Lin_Escaping_from_Collapsing_ECCV_2018_paper.html)
    * GANには，Gが潜在空間の部分分布しか表現しなくなる＝同じ画像しか出力しなくなるMode Collapseという現象があるが，BEGANにおけるこれを解決．ロス関数を追加するだけ．CelebAのダメなケースに対して，明らかに別の画像を出力するようになる．

* [Verisimilar Image Synthesis for Accurate Detection and Recognition of Texts in Scenes](http://openaccess.thecvf.com/content_ECCV_2018/html/Fangneng_Zhan_Verisimilar_Image_Synthesis_ECCV_2018_paper.html)
    * 文字検出の学習用に，妥当な色・フォントを選んで幾何的整合性を保ちながら妥当な場所に文字を合成する．

* [Layer-structured 3D Scene Inference via View Synthesis](http://openaccess.thecvf.com/content_ECCV_2018/html/Shubham_Tulsiani_Layer-structured_3D_Scene_ECCV_2018_paper.html) [[GitHub](https://shubhtuls.github.io/lsi/\n)]
    * 単画像から3Dシーンの推定をするのは遮蔽があって難しい．そこで，単画像からLDIと呼ばれる面の重なりの構造を表現できる画像群を推定することで達成する．学習データは3D合成データを用いる．

* [Perturbation Robust Representations of Topological Persistence Diagrams](http://openaccess.thecvf.com/content_ECCV_2018/html/Anirudh_Som_Perturbation_Robust_Representations_ECCV_2018_paper.html)
    * 

* [Analyzing Clothing Layer Deformation Statistics of 3D Human Motions](http://openaccess.thecvf.com/content_ECCV_2018/html/Jinlong_YANG_Analyzing_Clothing_Layer_ECCV_2018_paper.html)
    * 服を着ている人のメッシュから服と身体の特徴を分離して，服→身体→太らせる→服を戻す，のようなアプリケーションを可能にする．PCA部分空間縮退とNNによるパラメータ回帰による．

* [Learning to Solve Nonlinear Least Squares for Monocular Stereo](http://openaccess.thecvf.com/content_ECCV_2018/html/Ronald_Clark_Neural_Nonlinear_least_ECCV_2018_paper.html)
    * 今だ最小二乗法が良く使われるが，ちゃんと最適化できない場合も多いので，NNで非線形最小二乗の最適化をしてみよう，という論文．デファクトな非線形解法はヘシアンのリーズナブルな近似によるものだが，NNでやればヤコビアン全体において更新を計算できる．

* [Propagating LSTM: 3D Pose Estimation based on Joint Interdependency](http://openaccess.thecvf.com/content_ECCV_2018/html/Kyoungoh_Lee_Propagating_LSTM_3D_ECCV_2018_paper.html)
    * 単眼画像における人間の3Dポーズ推定において，関節間の連結性を伝播的に探していくLSTMで2Dポーズ推定し，さらに3Dポーズに変換する．

* [Proximal Dehaze-Net: A Prior Learning-Based Deep Network for Single Image Dehazing](http://openaccess.thecvf.com/content_ECCV_2018/html/Dong_Yang_Proximal_Dehaze-Net_A_ECCV_2018_paper.html)
    * 単画像からdark channelとtransmission mapを推定し，そのうえでディヘイズを実行するという研究があるが，そのdark channelを求めるときの更新式にproximal operatorを導入する．

* [Attend and Rectify: a gated attention mechanism for fine-grained recovery](http://openaccess.thecvf.com/content_ECCV_2018/html/Pau_Rodriguez_Lopez_Attend_and_Rectify_ECCV_2018_paper.html)
    * あるNNの複数の中間層のfeature mapからattentionを取って，それらを組み合わせることでGlobal Attention Gatesを計算．これをヒントに認識を行うというAttentionの枠組みを提案．NNの構造に依らず適用でき，シンプル．WRNにこれを適用するとResNeXtと同等の性能を30倍高速に出せる．

* [Learning to Capture Light Fields through A Coded Aperture Camera](http://openaccess.thecvf.com/content_ECCV_2018/html/Yasutaka_Inagaki_Learning_to_Capture_ECCV_2018_paper.html)
    * アパーチャーカメラ画像数枚から，ライトフィールドをNNで求める．アパーチャーパターンがそれぞれ異なっても，NNがパターンを獲得できる．

* [AMC: Automated Model Compression and Acceleration with Reinforcement Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Yihui_He_AMC_Automated_Model_ECCV_2018_paper.html)
    * GoogleのAutoMLの枠組みでモデル圧縮し，モバイル環境での可用性を高める．

* [Extreme Network Compression via Filter Group Approximation](http://openaccess.thecvf.com/content_ECCV_2018/html/Bo_Peng_Extreme_Network_Compression_ECCV_2018_paper.html)
    * フィルタグループの要素分解によって近似するという大胆な思想でモデル圧縮を行う．計算量を8割削減した．

* [Retrospective Encoders for Video Summarization](http://openaccess.thecvf.com/content_ECCV_2018/html/Ke_Zhang_Retrospective_Encoders_for_ECCV_2018_paper.html)
    * 

* [LQ-Nets: Learned Quantization for Highly Accurate and Compact Deep Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Dongqing_Zhang_Optimized_Quantization_for_ECCV_2018_paper.html) [[GitHub](https://github.com/Microsoft/LQ-Nets)]
    * モデル圧縮に役立つ量子化のパラメータを学習ベースで最適化する．他はhand-craftな量子化だったり，学習ベースでも一度決めたら固定だったりするが，これはweightとactivationに適応的な量子化を行うという指針．

* [Universal Sketch Perceptual Grouping](http://openaccess.thecvf.com/content_ECCV_2018/html/Ke_LI_Universal_Sketch_Perceptual_ECCV_2018_paper.html)
    * スケッチのストロークのセマンティックなグループとスケッチのカテゴリの推定という新たな取り組み．データセットがないのでまず作った．グルーピングはseq2seqにより行う．大局的な見えとローカルなストロークの対応によりスケッチのグルーピングを行う．未知のカテゴリのスケッチにも対応可能．

* [Uncertainty Estimates and Multi-Hypotheses Networks for Optical Flow](http://openaccess.thecvf.com/content_ECCV_2018/html/Eddy_Ilg_Uncertainty_Estimates_and_ECCV_2018_paper.html) [[GitHub](https://youtu.be/HvyovWSo8uE)]
    * オプティカルフローにおける不確実性を推定するいくつかのDL手法を提案し，評価した．また，複数仮説を表現するネットワークを提案．DLは自身の不確実性の推定が行えることを示してると主張．

* [Learning 3D Keypoint Descriptors for Non-Rigid Shape Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Hanyu_Wang_Learning_3D_Keypoint_ECCV_2018_paper.html)
    * 非剛体マッチングのための3Dキーポイント記述の学習．

* [A Joint Sequence Fusion Model for Video Question Answering and Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Youngjae_Yu_A_Joint_Sequence_ECCV_2018_paper.html)
    * VQA&検索．複数のモーダルのそれぞれのサブシーケンスの結合を考える．

* [Deformable Pose Traversal Convolution for 3D Action and Gesture Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Junwu_Weng_Deformable_Pose_Traversal_ECCV_2018_paper.html)
    * 「Pose Traversal」という概念のもとで，デフォーマブルな1次元CNNを提案．ポーズに関係する関節点のペアの関係性を見る．ポーズに関係のない部分は避けられたりしてよいらしい．５％程度性能向上．

* [Fine-Grained Visual Categorization using Meta-Learning Optimization with Sample Selection of Auxiliary Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Yabin_Zhang_Fine-Grained_Visual_Categorization_ECCV_2018_paper.html)
    * Fine-Grainedカテゴリ認識を，メタラーニングの枠組みで補助データをサンプリングすることで行う．

* [Stereo relative pose from line and point feature triplets](http://openaccess.thecvf.com/content_ECCV_2018/html/Alexander_Vakhitov_Stereo_relative_pose_ECCV_2018_paper.html)
    * ステレオカメラの2眼間姿勢推定を，2フレームにおける3つのの点あるいは線の対応関係から代数的に導く．3要素は片方の目で見えていればもう片方は欠落していても大丈夫．

* [CBAM: Convolutional Block Attention Module](http://openaccess.thecvf.com/content_ECCV_2018/html/Sanghyun_Woo_Convolutional_Block_Attention_ECCV_2018_paper.html)
    * チャンネル方向のアテンション，空間方向のアテンションと段階的に適用して中間層特徴を改善していくような，アテンションモジュールの新提案．結果を見ると，注目すべきまとまり全体にちゃんと注目するように改善できているように見える．

* [EC-Net: an Edge-aware Point set Consolidation Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Lequan_Yu_EC-Net_an_Edge-aware_ECCV_2018_paper.html)
    * それなりのセンサで計測した少々のノイズが乗っている3Dスキャンデータについて，Edge lossなどを入れて，エッジを構成する点群を明示的にとることできれいにメッシュを張れるようになるネットワークを提案．

* [Video Compression through Image Interpolation](http://openaccess.thecvf.com/content_ECCV_2018/html/Chao-Yuan_Wu_Video_Compression_through_ECCV_2018_paper.html)
    * ビデオ圧縮をDLでやる．今のところほとんど行われていないらしい．ビデオ圧縮は反復の画像補間でできるという思想で実現．MPEG4やH.264と比べてきれいにデコード可能．

* [HybridNet: Classification and Reconstruction Cooperation for Semi-Supervised Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Thomas_Robert_HybridNet_Classification_and_ECCV_2018_paper.html)
    * 識別に有効な特徴を抽出するネットワークと、それ以外の特徴を抽出するネットワークに分割したオートエンコーダを構築。2つのネットワークで復元されたものを合わせたものが元の画像の復元となるように学習をする。

* [Structure-from-Motion-Aware PatchMatch for Adaptive Optical Flow Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Maurer_Structure-from-Motion-Aware_PatchMatch_for_ECCV_2018_paper.html)
    * Patch Matchによる対応付けを利用してoptical flowの推定精度を上げる研究。隣接2フレーム間のflow推定と３フレームを用いたSFMを組み合わせる。

* [Joint & Progressive Learning from High-Dimensional Data for Multi-Label Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Danfeng_Hong_Joint__Progressive_ECCV_2018_paper.html)
    * 高次元データを識別するために、最適なsubspaceを探す手法を提案。subspaceを複数探してきて、それらを組み合わせて識別精度が高くなる空間を決定する。

* [SDC-Net: Video prediction using spatially-displaced convolution](http://openaccess.thecvf.com/content_ECCV_2018/html/Fitsum_Reda_SDC-Net_Video_prediction_ECCV_2018_paper.html)
    * 未来予測の高解像度化を行った。隣接フレーム間のflowを求めることによって，畳み込みの際に空間の時間変化を考慮する。

* [Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Liang-Chieh_Chen_Encoder-Decoder_with_Atrous_ECCV_2018_paper.html)
    * pyramid型＋encoder-decoderによりセマンティックセグメンテーションの精度を向上した。DeepLabv3という手法を発展させたものに対応する。

* [VQA-E: Explaining, Elaborating, and Enhancing Your Answers for Visual Questions](http://openaccess.thecvf.com/content_ECCV_2018/html/Qing_Li_VQA-E_Explaining_Elaborating_ECCV_2018_paper.html)
    * VQAの出力として、質問に対する答えだけでなくその答えの根拠を説明する文章を出力する手法を提案した。

* [Image Super-Resolution Using Very Deep Residual Channel Attention Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Yulun_Zhang_Image_Super-Resolution_Using_ECCV_2018_paper.html)
    * 超解像のためにCNNの層の数を増やすための手法を提案した。

* [Urban Zoning Using Higher-Order Markov Random Fields on Multi-View Imagery Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Tian_Feng_Urban_Zoning_Using_ECCV_2018_paper.html)
    * street view＋衛星写真から、都市内のエリアの識別を行う。具体的には、衛星写真中の各ピクセルにresidental, commercial, industrial, othersの4つのラベルを割り振る。

* [Clustering Convolutional Kernels to Compress Deep Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Sanghyun_Son_Clustering_Kernels_for_ECCV_2018_paper.html)
    * 畳み込みカーネルをk-meansでクラスタリングし、各カーネルを各クラスの代表カーネルで近似することでネットワークの圧縮を行う。イメージはベクトル量子化を畳み込みカーネルに適用した感じ。

* [Explainable Neural Computation via Stack Neural Module Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Ronghang_Hu_Explainable_Neural_Computation_ECCV_2018_paper.html)
    * VQAのような複雑なタスクにおける理由付けに関する研究。理由を説明するための層をstackすることで段階を追って理由付けを行う。

* [Quaternion Convolutional Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Xuanyu_Zhu_Quaternion_Convolutional_Neural_ECCV_2018_paper.html)
    * CNNをQuartenion上で取り扱えるようにした研究。画像をQuartenionに変換し、CNNの各操作を定義しなおした。通常のCNN同様にロスが減少し、精度はわずかながら向上した。

* [Lip Movements Generation at a Glance](http://openaccess.thecvf.com/content_ECCV_2018/html/Lele_Chen_Lip_Movements_Generation_ECCV_2018_paper.html)
    * 音声データ＋対象人物の画像から、音声に合わせて対象人物の口を変化させる手法を提案。従来手法との違いは、音声に合わせて口を合成するため対象人物は動画ではなく画像だけでよい

* [Toward Scale-Invariance and Position-Sensitive Object Proposal Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Hsueh-Fu_Lu_Toward_Scale-Invariance_and_ECCV_2018_paper.html)
    * スケールに頑健な物体検出手法

* [Constraints Matter in Deep Neural Network Compression](http://openaccess.thecvf.com/content_ECCV_2018/html/Changan_Chen_Constraints_Matter_in_ECCV_2018_paper.html)
    * DNNの圧縮を、特定の制約のもと行う研究。例えば、自動運転車ではトラブルに対応するためにリアルタイム性が求められる、ドローンは限られたメモリしか搭載できないなどが制約となる。

* [MRF Optimization with Separable Convex Prior on Partially Ordered Labels](http://openaccess.thecvf.com/content_ECCV_2018/html/Csaba_Domokos_MRF_Optimization_with_ECCV_2018_paper.html)
    * セマンティックセグメンテーションのように、複数のラベルを出力する問題に対する最適化問題を提案。

* [Switchable Temporal Propagation Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Sifei_Liu_Switchable_Temporal_Propagation_ECCV_2018_paper.html)
    * 連続するフレーム間の変化を伝播していく手法を提案した。

* [T2Net: Synthetic-to-Realistic Translation for Solving Single-Image Depth Estimation Tasks](http://openaccess.thecvf.com/content_ECCV_2018/html/Chuanxia_Zheng_T2Net_Synthetic-to-Realistic_Translation_ECCV_2018_paper.html)
    * 合成画像を用いてdepth推定を学習する手法を提案。リアル画像はdepthデータを用意せず単独で使用し、depthの学習は合成データによって行う。

* [ArticulatedFusion: Real-time Reconstruction of Motion, Geometry and Segmentation Using a Single Depth Camera](http://openaccess.thecvf.com/content_ECCV_2018/html/Chao_Li_ArticulatedFusion_Real-time_Reconstruction_ECCV_2018_paper.html)
    * リアルタイムで動きなどのあるシーンを復元する手法を提案する。RGB-Dカメラを入力とし、グラフを構築する。

* [NNEval: Neural Network based Evaluation Metric for Image Captioning](http://openaccess.thecvf.com/content_ECCV_2018/html/Naeha_Sharif_NNEval_Neural_Network_ECCV_2018_paper.html)
    * 画像キャプショニングの新しい評価指標を提案。生成したキャプションが人間が生成したものか機械が生成したものかを判定し、人間が生成したものに似ているほどいいものとする

* [Coreset-Based Convolutional Neural Network Compression](http://openaccess.thecvf.com/content_ECCV_2018/html/Abhimanyu_Dubey_Coreset-Based_Convolutional_Neural_ECCV_2018_paper.html)
    * CNNの圧縮に関する研究。冗長な成分を減らすことによって圧縮をする。再学習がいらないらしい。

* [Context Refinement for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhe_Chen_Context_Refinement_for_ECCV_2018_paper.html)
    * 候補領域の抽出→refineの2段階による物体検出の改善手法を提案。周囲の情報(コンテクスト)が重要と考え，周辺の候補領域の情報を組み合わせることで精度を上げる。

* [Real-time 'Actor-Critic' Tracking](http://openaccess.thecvf.com/content_ECCV_2018/html/Boyu_Chen_Real-time_Actor-Critic_Tracking_ECCV_2018_paper.html)
    * リアルタイムトラッキングを行うactor-clrticフレームワークを提案した。actorがmotionの決定を行い、criticは学習時に使われる。

* [Partial Adversarial Domain Adaptation](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhangjie_Cao_Partial_Adversarial_Domain_ECCV_2018_paper.html) [[GitHub](https://github.com/thuml/PADA)]
    * 2つのドメイン間で、クラスの数が異なる場合のドメインアダプテーションを提案。ターゲットドメインに含まれないクラスの重みを小さくすることで実現する

* [Localization Recall Precision (LRP): A New Performance Metric for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Kemal_Oksuz_Localization_Recall_Precision_ECCV_2018_paper.html)
    * 物体検出の新たな評価指標Localization Recall Precision Errorを提案。true positive, false positive, false negativeの3つを考慮した指標。

* [Improving Embedding Generalization via Scalable Neighborhood Component Analysis](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhirong_Wu_Improving_Embedding_Generalization_ECCV_2018_paper.html)
    * 学習データが少ない新たなカテゴリを識別可能なnon-parametricなアルゴリズムを提案。特徴量空間における学習データ同士の距離を求め、新たなカテゴリが加わったときに特徴量空間を最適化していく。

* [Leveraging Motion Priors in Videos for Improving Human Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yu-Ting_Chen_Leveraging_Motion_Priors_ECCV_2018_paper.html)
    * 動画を使った人物のセグメンテーションを提案。連続フレーム間でoptical flowを求めることで、人物が映っている領域(前景)を求めることで学習に使用する。

* [Recurrent Squeeze-and-Excitation Context Aggregation Net for Single Image Deraining](http://openaccess.thecvf.com/content_ECCV_2018/html/Xia_Li_Recurrent_Squeeze-and-Excitation_Context_ECCV_2018_paper.html)
    * RNNをベースに1枚の画像から雨筋を除去する研究。context aggregation networkを適用し段階的に雨筋を除去していく。特に、各段階での除去の情報を次の除去に取り入れるという点は新規性。この研究においてはstate-of-the-artを達成。

* [Statistically-motivated Second-order Pooling](http://openaccess.thecvf.com/content_ECCV_2018/html/Kaicheng_Yu_Statistically-motivated_Second-order_Pooling_ECCV_2018_paper.html)
    * second-order pooling (bilinear pooling)について、統計学的な観点からネットワークの中間表現を分析し、通常のそれよりも圧縮されたSMSO poolingを提案。いくつかの認識タスクにおいて通常のbilinear poolingやfirst-order poolingと比較しstate-of-the-artを達成。

* [SegStereo: Exploiting Semantic Information for Disparity Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Guorun_Yang_SegStereo_Exploiting_Semantic_ECCV_2018_paper.html)
    * 双眼ステレオ画像における差異の検出において、semantic cuesをさまざまな推定フレームワークに埋め込む統合的なモデルSegStereo、semantic softmax lossを提案。supervisedでもunsupervisedでも使える。

* [Small-scale Pedestrian Detection Based on Somatic Topology Localization and Temporal Feature Aggregation](http://openaccess.thecvf.com/content_ECCV_2018/html/Tao_Song_Small-scale_Pedestrian_Detection_ECCV_2018_paper.html)
    * 歩行者検出のタスクにおいて、様々なサイズの歩行者を検出するために、人間の身体のtopological line localization (TLL)と、時間的な特徴集合を統合した方法を提案した。カメラから遠く小さく映っている歩行者に対してもうまくはたらくらしい。後処理としてmarkov random fieldをベースにした方法も提案し、曖昧さを除去している。

* [Object Detection with an Aligned Spatial-Temporal Memory](http://openaccess.thecvf.com/content_ECCV_2018/html/Fanyi_Xiao_Object_Detection_with_ECCV_2018_paper.html)
    * ビデオ物体検出でSpatio-Temporal Memoryモジュール(STMM)を提案した。これは、繰り返し計算ユニットとして働き、長期間の時間的外観とモーションダイナミクスをモデル化するやつ。ImageNet VIDでSOTA達成。

* [Learning to Drive with 360° Surround-View Cameras and a Map](http://openaccess.thecvf.com/content_ECCV_2018/html/Simon_Hecker_Learning_to_Drive_ECCV_2018_paper.html)
    * 自動車の周囲に8つのカメラを搭載した360度ビューと経路プランナーを合わせた運転モデルを提案。従来の前面のみのカメラよりも人間の運転手の感覚にちかいらしい。（人間はミラーとかで確認するので）。各カメラの映像をCNNに入れて特徴をエンコードし、LSTMでその時間的な出力を統合、FC層を使って、すべてのカメラからの情報とGPSや地図の情報を統合し、運転の機動を予測。60時間の新しいデータセットを作り、新しいアルゴリズムを提案。

* [Monocular Scene Parsing and Reconstruction using 3D Holistic Scene Grammar](http://openaccess.thecvf.com/content_ECCV_2018/html/Siyuan_Huang_Monocular_Scene_Parsing_ECCV_2018_paper.html)
    * 一枚のRGB画像をパースし、確率的文法モデルを使ってCADモデルの集合により構成された全体的な3Dの外観を再構成する、統合的な手法を提案した。

* [Coded Illumination and Imaging for Fluorescence Based Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuta_Asano_Coded_Illumination_and_ECCV_2018_paper.html)
    * 物体中の物質の検出に関する研究。蛍光の励起光と発光がこのようなタスクには役立つが、この行列を捉えるにはすごく時間がかかるので、輝線が学習されコード化された光を使うアプローチをとった。物質の分類に蛍光の知識が役立つのはよく知られているが、コード化された光を使うのは初めて。

* [Modality Distillation with Multiple Stream Networks for Action Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Nuno_Garcia_Modality_Distillation_with_ECCV_2018_paper.html)
    * 訓練時はいろいろなモードの入力があるのに、テスト時には限られたモードの入力しかないという場合が多々ある。著者らは、訓練時はdepth + RGBで、テスト時はRGBのみという想定で、halluciation networkを学習し、時空間特徴を積結合を通じてdepth特徴を蒸留させた。

* [VideoMatch: Matching based Video Object Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Yuan-Ting_Hu_VideoMatch_Matching_based_ECCV_2018_paper.html)
    * video object segmentationに関して，soft matching layerを提案し，fine tuningなどの時間がかかりすぎ問題を解決した．そして，いくつかのデータセットにおいてcomparableな結果を残した．

* [Superpixel Sampling Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Varun_Jampani_Superpixel_Sampling_Networks_ECCV_2018_paper.html)
    * superpixelに関して，既存手法で問題となっていたend-to-endなネットワークに組み込めないという点を解決し，微分可能な手法を提案した．Superpixel Sampling Network(SSN)と呼ばれる．segmentationタスクにとどまらず，ほかのタスクでも有用らしい．

* [Deep Bilinear Learning for RGB-D Action Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/HU_Jian-Fang_Deep_Bilinear_Learning_ECCV_2018_paper.html)
    * modality-temporalの相互の特徴を使い，RGB-Dの動作認識を行った．提案手法はdeep bilinear learning frameworkと呼ばれ，modalityとtemporalの情報を，cube constructionとbilinear learningに分けて学習するという方法．２つのデータセットでstate-of-the-artを上回った．

* [Multi-object Tracking with Neural Gating using bilinear LSTMs](http://openaccess.thecvf.com/content_ECCV_2018/html/Chanho_Kim_Multi-object_Tracking_with_ECCV_2018_paper.html)
    * 複数物体のトラッキングを行う新手法bilinear LSTMを提案し，long-term appearance modelをrecurrent networkを通じて学習できるようにした．また，物体のトラックを見た目とモーションの両方について記録する新しいdata augmentationを提案した．MOT2016 と MOT2017のベンチマークでstate-of-the-artを達成．

* [Person Search via A Mask-guided Two-stream CNN Model](http://openaccess.thecvf.com/content_ECCV_2018/html/Di_Chen_Person_Search_via_ECCV_2018_paper.html)
    * 歩行者検出とperson re-IDのタスクからなる人物検索の問題について，検出器とre-IDの特徴抽出を分けたほうがそれを統合したモデルよりも良いパフォーマンスをすることがわかった．提案手法は，re-IDについて，前面の人間とオリジナル画像のパッチを別個にモデル化し，2つのCNNから表現を得たというもの．CUHK-SYSUとPRWデータセットにおいて5pp以上の差をつけてstate-of-the-art達成．

* [Imagine This! Scripts to Compositions to Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Tanmay_Gupta_Imagine_This_Scripts_ECCV_2018_paper.html)
    * 自然言語の文章で表現されたシーンを想像する（再現する）タスク．提案手法は，Composition, Retrieval and Fusion Network (CRAFT)で，ビデオキャプションから学習し，これを新しいキャプションにあてはめあたらしいビデオを生成するというもの．貢献は，レイアウトと見た目を合わせて訓練し，そして，検索のために構成表現を学習できるようなロス関数を提案したこと．

* [Multiresolution Tree Networks for 3D Point Cloud Procesing](#N/A)
    * 3Dの形状理解と生成タスクのために，ポイントクラウドを処理するマルチ解像度の木構造ネットワークを提案した．これは3Dの形状を，場所を保持しながら1次元のリストとして表現するものである．これにより，1次元の畳込みが効率的に行えるようになり，マルチグリッドな構造を通じて粗密な解析を行えるようにし，収束も早く，メモリ使用も小さい．形状分類タスクでも，形状生成タスクでもstate-of-the-artを達成した．

* [Quantization Mimic: Towards Very Tiny CNN for Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Yi_Wei_Quantization_Mimic_Towards_ECCV_2018_paper.html)
    * Quantization Mimicを提案し，極小なCNNで物体検出を行おうという研究．Mimicは生徒ネットワークを教師ネットワークから知識を移転することによってパフォーマンスを上げさせ，Quantizationは精度の高いネットワークから量子化ネットワークへ精度の劣化を抑えて変換するというもの．

* [Multi-scale Residual Network for Image Super-Resolution](http://openaccess.thecvf.com/content_ECCV_2018/html/Juncheng_Li_Multi-scale_Residual_Network_ECCV_2018_paper.html)
    * 超解像のために，residual blockを基礎として，異なるスケールの画像特徴を適応的に検出するために，異なるサイズのカーネルの畳込みを導入した．これらを相互に作用させ，最も意味のある画像特徴を得る．そして，大域的な特徴の統合のために，階層的な特徴としてそれを使い，最終的には再構成モジュールへと送る．

* [BodyNet: Volumetric Inference of 3D Human Body Shapes](http://openaccess.thecvf.com/content_ECCV_2018/html/Gul_Varol_BodyNet_Volumetric_Inference_ECCV_2018_paper.html)
    * 3Dの人間の形状推定について，3Dの体積損失，マルチビューの再投影損失，中間層における2Dポーズ，2Dの身体のパーツセグメンテーション，そして，3Dポーズによる教師あり学習を行うことで，パフォーマンスを向上させた．また，身体のパーツセグメンテーションも可能にしている．

* [3D Recurrent Neural Networks with Context Fusion for Point Cloud Semantic Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaoqing_Ye_3D_Recurrent_Neural_ECCV_2018_paper.html)
    * ３Dの構造化されていないポイントクラウドのセグメンテーション問題について、内在的なコンテクスト特徴を捉えられるような手法を提案。ポイントワイズなピラミッドプーリングモジュールと、双方向の階層的RNNを提案した。

* [Robust Anchor Embedding for Unsupervised Video Re-Identification in the Wild](http://openaccess.thecvf.com/content_ECCV_2018/html/Mang_YE_Robust_Anchor_Embedding_ECCV_2018_paper.html)
    * Person Re-IDでの拡張性と頑健性の問題について、異なる人物に、アフィン包をベースにしたアンカーを設定し、それを使ってCNNを初期化し、後のラベル推定につかえるような区別可能な特徴表現を得る。

* [Towards Robust Neural Networks via Random Self-ensemble](http://openaccess.thecvf.com/content_ECCV_2018/html/Xuanqing_Liu_Towards_Robust_Neural_ECCV_2018_paper.html)
    * DNNへの敵対的攻撃を防ぐための防衛アルゴリズムを提案。ランダム・ノイズ層を追加することで強力な勾配ベースの攻撃手法を防ぎ、それらをアンサンブルすることでパフォーマンスを保つというもの。よいところは、追加のメモリオーバーヘッドを要せずに、無限のノイズモデルと同等になること、さらに様々なネットワークに統合することが簡単であること。ノイズ層を各畳込みブロックの先頭に入れているようだ。

* [SpiderCNN: Deep Learning on Point Sets with Parameterized Convolutional Filters](http://openaccess.thecvf.com/content_ECCV_2018/html/Yifan_Xu_SpiderCNN_Deep_Learning_ECCV_2018_paper.html)
    * ポイントクラウドでのCNNの話。CNNにマルチスケールで階層的な構造をもたせることで、効率的に地理的特徴を得られるような新しいCNNアーキテクチャを提案した。

* [CIRL: Controllable Imitative Reinforcement Learning for Vision-based Self-driving](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaodan_Liang_CIRL_Controllable_Imitative_ECCV_2018_paper.html)
    * 自動車の運転ナビゲーションについて、自動車シミュレータのビジョン入力だけを使う制御可能な模倣教科学習を提案し、ルールベースの方法や教師あり模倣学習よりも優れた成果を出した。

* [Normalized Blind Deconvolution](http://openaccess.thecvf.com/content_ECCV_2018/html/Meiguang_Jin_Normalized_Blind_Deconvolution_ECCV_2018_paper.html)
    * ブラー画像からブラーカーネルとシャープな画像を得る問題について、シャープな画像とブラーの相対的なスケールの曖昧さについて、ぼかしの正規化の方法としてFrobeniusノルムを使うことでL1ノルムを使うよりも、精度とノイズ耐性に耐えうる手法が提案された。

* [Few-Shot Human Motion Prediction via Meta-Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Liangyan_Gui_Few-Shot_Human_Motion_ECCV_2018_paper.html)
    * 数ミリ秒での人間のモーション予測．few shot learningの流れをくんでいる．

* [Look Before You Leap: Bridging Model-Free and Model-Based Reinforcement Learning for Planned-Ahead Vision-and-Language Navigation](http://openaccess.thecvf.com/content_ECCV_2018/html/Xin_Wang_Look_Before_You_ECCV_2018_paper.html)
    * モデルレスとモデルベースの強化学習を組み合わせたビジョン言語ナビゲーションタスクである新しい計画立案ハイブリッド補強学習を提案．提案するルックアヘッドモジュールは，ルックアヘッドポリシーモデルと環境モデルを統合し，次の状態と報酬を予測する．実験の結果，提案手法がベースラインを大幅に上回り，実際のroom-to-roomデータセットで最高を達成することを示唆している．

* [HandMap: Robust Hand Pose Estimation via Intermediate Dense Guidance Map Supervision](http://openaccess.thecvf.com/content_ECCV_2018/html/Xiaokun_Wu_HandMap_Robust_Hand_ECCV_2018_paper.html)
    * 検出ベースの手法で手関節のヒートマップを予測する利点を活用することで，ヒートマップの解像度に限定されない回帰ベースのフレームワークにおいて，中間の管理によるdense feature mapを使用することを提案．提案するfeature mapは，手のジオメトリと，ローカルジョイントとグローバルハンドの空間的関係をエンコードするために細かく設計されている．提案されたフレームワークは，最近のベンチマークデータセットで2Dと3Dの両方で最先端技術を大幅に向上させる．

* [LSQ++: lower runtime and higher recall in multi-codebook quantization](http://openaccess.thecvf.com/content_ECCV_2018/html/Julieta_Martinez_LSQ_lower_runtime_ECCV_2018_paper.html)
    * マルチコードブック量子化(MCQ)の分野の最近の研究や手法では，異なるデータセットやプロトコル，計算手法を用いるため，互いに比較するのは難しい．ここで，まずMCQベースラインのシリーズを同等の基準でベンチマークし，それらのrecall-vs-runtimeパフォーマンスの分析を行う．ローカルサーチ量子化(LSQ)は，実際には競合他社よりもはるかに高速だが，すべてのケースにおいて正確な方法ではない．そこで，LSQをより正確に，より速くレンダリングする2つの改良点を紹介する．これらの改善は容易であり，MCQの新しい最先端技術を定義する．

* [Multimodal Dual Attention Memory for Video Story Question Answering](http://openaccess.thecvf.com/content_ECCV_2018/html/Kyungmin_Kim_Multimodal_Dual_Attention_ECCV_2018_paper.html)
    * 

* [Hierarchical Bilinear Pooling for Fine-Grained Visual Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Chaojian_Yu_Hierarchical_Bilinear_Pooling_ECCV_2018_paper.html)
    * 詳細画像認識は，様々なセマンティックパーツのモデリングと細かいフィーチャラーニングに大きく依存しているため困難．提案手法では第一に，レイヤ間の部分的な特徴の関係を補足するために，クロスレイヤの双線バイリニアプール法が提案され，これは他の双線近似手法と比較して優れた性能をもたらす．次に複数のクロスレイヤバイリニアフィーチャを統合して表現能力を高めるための階層的なバイリニアプーリングフレームワークを提案する．この提案手法は，広く使われている認識データセットで最高水準の結果を達成．

* [Dense Semantic and Topological Correspondence of 3D Faces without Landmarks](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhenfeng_Fan_Dense_Semantic_and_ECCV_2018_paper.html)
    * ランドマークのない3次元顔の密な対応のための一般的な枠組みを提案.テンプレートの顔面メッシュから始めて、グローバルアライメント、テンプレートワーピングによる一次対応，コンテキストメッシュリファインメントを順次実行する．FRGC v2.0で提案された方法を質的および量的に評価し、合理的かつ信頼できる結果を示した．

* [Real-Time Blind Video Temporal Consistency](http://openaccess.thecvf.com/content_ECCV_2018/html/Wei-Sheng_Lai_Real-Time_Blind_Video_ECCV_2018_paper.html)
    * 映像の時間的整合性を実現するために，深い反復的なネットワークに基づく効率的なend-to-endのアプローチを提案．提案手法は，元の未処理およびフレームごとに処理されたビデオを入力として時間的に一貫したビデオを生成する．これは，時間的安定性と知覚的類似性とのバランスをとるための知覚損失と同様に短期的および長期的な時間的損失を最小限に抑えることにより，提案モデルはオプティカルフローを計算する必要がなく，高解像度ビデオでもリアルタイムのスピードを実現する．

* [Depth Estimation via Affinity Learned with Convolutional Spatial Propagation Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Xinjing_Cheng_Depth_Estimation_via_ECCV_2018_paper.html)
    * 奥行予測のためのアフィニティ行列を学習するために有効な畳み込み空間伝搬ネットワーク(CSPN)を提案．具体的には，再帰畳み込み演算を用いて伝搬を行い，隣接画素間の親和性をCNNを介して学習する，効率的な線形伝搬モデルを採用する．

* [Hierarchical Metric Learning and Matching for 2D and 3D Geometric Correspondences](http://openaccess.thecvf.com/content_ECCV_2018/html/Mohammed_Fathy_Hierarchical_Metric_Learning_ECCV_2018_paper.html)
    * 一般的に使用されるメトリック学習手法が、畳み込みニューラルネットワーク（CNN）で幾何学的特徴マッチングのタスクの場合に学習した特徴を最適に活用していないこと実証する

* [GridFace: Face Rectification via Learning Local Homography Transformations](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhou_GridFace_Face_Rectification_ECCV_2018_paper.html)
    * この論文では，顔の幾何学的変化を低減し，認識性能を向上させるためのGridFaceと呼ばれる手法を提案．この手法では，顔修正ネットワークによって推定される局所ホモグラフィ変換によって顔を修正する．canonical views（標準的見え方）で画像生成を促進するために，自然な顔の分布に基づいて正規化を適用．修正ネットワークと認識ネットワークをend-to-endで学習．実験の結果，提案手法が幾何学的な変動を大幅に低減し，制約のない顔認識シナリオにおいて大幅な改善を示唆した．

* [Rethinking Spatiotemporal Feature Learning: Speed-Accuracy Trade-offs in Video Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Saining_Xie_Rethinking_Spatiotemporal_Feature_ECCV_2018_paper.html)
    * この論文では3つの問題を組み合わせてI3Dとして知られている最先端の3D CNN動画分類モデルを大幅に改善することができることを示した。

* [Deep Variational Metric Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Xudong_Lin_Deep_Variational_Metric_ECCV_2018_paper.html)
    * クラス内の分散を明示的にモデル化し，クラス内の不変量を解くためのdeep variational metric learning(DVML)を提案．学習されたクラス内分散の分布を用いて，頑健性を向上させるために識別サンプルを同時に生成することが出来る．

* [Multi-Class Model Fitting by Energy Minimization and Mode-Seeking](http://openaccess.thecvf.com/content_ECCV_2018/html/Daniel_Barath_Multi-Class_Model_Fitting_ECCV_2018_paper.html)
    * 入力データを、複数のクラスの複数のインスタンスから発生するノイズの多い観測の混合として解釈する問題に対して多クラス多インスタンスモデルフィッティングのためのMulti-Xと呼ばれる一般的な定式化を提案する．Multi-Xは、多様な問題に対する公開データセットでの既存の手法の精度を大幅に上回る性能を発揮．

* [A Unified Framework for Single-View 3D Reconstruction with Limited Pose Supervision](http://openaccess.thecvf.com/content_ECCV_2018/html/Guandao_Yang_A_Unified_Framework_ECCV_2018_paper.html)
    * 少量のカメラポーズアノテーションを使用して姿勢不変性および視点一貫性を算出し， 敵対的な損失と組み合わされた未ラベルの画像は、レンダリングされ生成されたモデルの現実感を引き出すために使用する．この2つを組み合わせたフレームワークを提示し，影響を半教師あり学習、マルチタスク、および転送学習の3つのパラダイムで測定し精度を検証する．

* [Diverse Conditional Image Generation by Stochastic Regression with Latent Drop-Out Codes](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_He_Diverse_Conditional_Image_ECCV_2018_paper.html)
    * GANの安定性の問題，CAVEモデルのモード混合の問題を解決するために両方の研究のメリットを組み合わせたドロップアウトコードを用いた、新規かつ効率的な確率的回帰アプローチを提案する．さらに正確性および多様性の点で最先端な手法の改善をする．

* [Orthogonal Deep Features Decomposition for Age-Invariant Face Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/yitong_wang_Orthogonal_Deep_Features_ECCV_2018_paper.html)
    * 顔認識コミュニティにおいて，年齢不変顔認識(AIFR) が依然として大きなk大である．年齢不変の深い顔の特徴を学習するための新しい手法(OE-CNN)を提案．具体的には，深い顔の特徴を2つの直交する成分に分解し，年齢関連および身元関連の特徴を表現する．その結果，AIFRには，エイジングに強いアイデンティティ関連の機能が使用される．さらに，既存のクロス・エイジ・データセットを補完し，この分野の研究を進めるために，新しい大規模クロス・エイジ・フェース・データセット(CAF)を構築する．3つの顔面老化データセットで実施した実験により，提案した手法の有効性と，構築したCAFデータセットのAIFRの価値が示唆された．

* [HiDDeN: Hiding Data with Deep Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Jiren_Zhu_HiDDeN_Hiding_Data_ECCV_2018_paper.html)
    * 提案手法では，エンコーダとデコーダのネットワークを共同して訓練する．入力メッセージとカバー画像が与えられると，エンコーダは視覚的に区別できない符号化画像を生成し，そこからデコーダが元のメッセージを復元することができる．これらのエンコーディングは，既存のデータ隠蔽アルゴリズムと競合し，さらにノイズに強くすることができることを示している．実験の結果，敵対的な訓練が符号化画像の視覚的品質を改善することを示唆した．

* [Learning and Matching Multi-View Descriptors for Registration of Point Clouds](http://openaccess.thecvf.com/content_ECCV_2018/html/Lei_Zhou_Learning_and_Matching_ECCV_2018_paper.html)
    * ポイントクラウドレジストレーションに用いられる，学習可能なマルチビューdescriptorsを提案した．具体的には，まず3Dキーポイントを記述可能で，マルチビュー画像を用いて学習可能なmulti-view local descriptorを提案した．次に，対応付けのアウトライヤーを除去できるロバストマッチング手法を提案した．いくつかデータセットで提案descriptorsとmatching方法の有効性を証明した．

* [Deep Burst Denoising](http://openaccess.thecvf.com/content_ECCV_2018/html/Clement_Godard_Deep_Burst_Denoising_ECCV_2018_paper.html)
    * バーストキャプチャ戦略を用いて，反復完全畳み込みニューラルネット(CNN)によるインテリジェントな統合を実装する．単一のフレームノイズ除去モデルに関単に追加できるように，斬新なマルチフレームアーキテクチャを構築している．得られたアーキテクチャは，任意の長さのシーケンスですべてのフレームノイズを除去する．

* [On Offline Evaluation of Vision-based Driving Models](http://openaccess.thecvf.com/content_ECCV_2018/html/Felipe_Codevilla_On_Offline_Evaluation_ECCV_2018_paper.html)
    * 自律運転モデルの評価のための様々なオンラインメトリックとオフラインメトリックの関係を調査．一般にオフライン予測は必ずしも運転品質と相関するとは限らず，同一の予測誤差を有する2つのモデルが運転性能において異なっていることがわかった．適切な検証データセットと適切なオフラインメトリックを選択することで，オフライン評価と運転品質との相関を大幅に改善できることを示す．

* [Distortion-Aware Convolutional Filters for Dense Prediction in Panoramic Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Keisuke_Tateno_Distortion-Aware_Convolutional_Filters_ECCV_2018_paper.html)
    * 単一の画像からのパノラマ深度マップ推定のための学習アプローチを提案．歪み対応の変形可能な畳み込みフィルタのおかげで，従来のパースペクティブ画像を使用して訓練を行い，パノラマ画像の深度を後退させて，注釈付きのパノラマトレーニングデータセットを作成するのに必要な作業を回避できる．

* [Salient Objects in Clutter: Bringing Salient Object Detection to the Foreground](http://openaccess.thecvf.com/content_ECCV_2018/html/Deng-Ping_Fan_Salient_Objects_in_ECCV_2018_paper.html)
    * 顕著な物体検出(SOD)モデルの包括的な評価を提供．分析に基づき，総合的でバランスの取れたデータセットが完全になるべき7つの重要な側面を特定．次に，新しい高品質のデータセットを提案し，以前の顕著性ベンチマークを更新．提案するSOCデータセットには，毎日のオブジェクトカテゴリからの顕著なオブジェクトと非顕著なオブジェクトを含むイメージが含まれている．

* [Randomized Ensemble Embeddings](http://openaccess.thecvf.com/content_ECCV_2018/html/Hong_Xuan_Randomized_Ensemble_Embeddings_ECCV_2018_paper.html)
    * 改良された結果を得るためにアンサンブルとして使用できる埋め込み関数のファミリを定義するための，新規で一般化可能かつ高速な方法を提案．各埋め込み関数は，学習ラベルをランダムに小さなサブセットに入れて学習する．

* [Conditional Prior Networks for Optical Flow](http://openaccess.thecvf.com/content_ECCV_2018/html/Yanchao_Yang_Conditional_Prior_Networks_ECCV_2018_paper.html)
    * Conditional Prior Network(CPN)と呼ばれる新しいアーキテクチャを紹介し，それを訓練して条件付き事前確率を生成する方法を示す．CPNは，シンプルなオプティカルフローアーキテクチャと組み合わせて使用すると，すべての変分法およびすべての教師なし学習ベースのアルゴリズムよりも優れている．

* [Adaptively Transforming Graph Matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Fudong_Wang_Adaptively_Transforming_Graph_ECCV_2018_paper.html)
    * 適応表現変換の観点から適応変換グラフマッチング(ATGM)法を提案．具体的には，変換公式のもとで，元のグラフと変換されたグラフとの間の誤差を最小にすることによって，2つのグラフを一致させる．実験の結果，提案手法が最先端のグラフマッチングアルゴリズムを上回った．

* [Learning 3D shapes as multi-layered height maps using 2D convolutional neural networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Kripasindhu_Sarkar_Learning_3D_shapes_ECCV_2018_paper.html)
    * 2次元CNNに適した3次元形状の新規なグローバル表現を提案．各格子位置で複数のハイトマップのインスタンスを格納することにより，いくつかのオクルージョン層の背後に隠された3D形状の多層形状ハイトマップ(MLH)を表現．

* [ISNN - Impact Sound Neural Network for Material and Geometry Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Auston_Sterling_ISNN_-_Impact_ECCV_2018_paper.html)
    * 物体の幾何学および材料を推定するために最適化されたマルチモーダルニューラルネットワークを提案．このネットワークは，記録され合成されたオブジェクトインパクトサウンドとボクセル化された形状推定のスペクトログラムを使用して，視覚ベースの再構成の機能を拡張する．

* [Visual Psychophysics for Making Face Recognition Algorithms More Explainable](http://openaccess.thecvf.com/content_ECCV_2018/html/Brandon_RichardWebster_Visual_Psychophysics_for_ECCV_2018_paper.html)
    * 本論文では、視覚心理学が、顔認識アルゴリズムをより説明可能にするための方法論であることを示唆している。CNNとhandclaft特徴ベースの手法との上に展開される、顔認識アルゴリズムが構成される

* [Show, Tell and Discriminate: Image Captioning by Self-retrieval with Partially Labeled Data](http://openaccess.thecvf.com/content_ECCV_2018/html/Xihui_Liu_Show_Tell_and_ECCV_2018_paper.html)
    * キャプションの弁別性を図るための新たなキャプショニングフレームワークを提案．フレームワークはキャプションモジュールと自己探索モジュールで構成される．キャプションモジュールでキャプションを生成し，自己探索モジュールで生成されたキャプションから画像を探索する．この2つが一致するように学習することでキャプションの品質を測定するための評価として機能し，弁別的なキャプションを生成するようにモデルを促す．

* [Using LIP to Gloss Over Faces in Single-Stage Face Detection Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Siqi_Yang_Using_LIP_to_ECCV_2018_paper.html)
    * Single-stage networkを用いて現在のSOTAな顔検出器をattack/foolできる手法を提案した．従来のadversarial perturbation手法がSOTAな顔検出器のadversarial attackに有効ではないことを実験を通して証明し，その理由としては従来は一つの顔を目標に攻撃し，画像中に小さい顔がたくさんある場合，従来のattackは成功しない．DNNのreceptive fieldとadversarial perturbationの関連性の検討から，Localized Instance Perturbation(LIP)を提案した．LIPを用いてeffective receptive field内でadversarial attackができる．

* [Variational Wasserstein Clustering](http://openaccess.thecvf.com/content_ECCV_2018/html/Liang_Mi_Variational_Wasserstein_Clustering_ECCV_2018_paper.html)
    * 最適輸送理論に基づく新しいクラスタリング手法を提案．パワーダイアグラムを調整してクラスタリングエネルギーの最小値を維持しながら，ターゲットドメインを介してクラスタセントロイドを駆動する．したがって，重心とターゲットドメインの間のクラスタリングとWasserstein距離を同時に追求し，測定値を保持するマッピングを実現．

* [ADVISE: Symbolism and External Knowledge for Decoding Advertisements](http://openaccess.thecvf.com/content_ECCV_2018/html/Keren_Ye_ADVISE_Symbolism_and_ECCV_2018_paper.html)
    * シンボリックリファレンスを使用して広告の意味をよりよく理解する方法を示す．さらに，汎用オブジェクト認識と画像キャプションの広告理解をどのようにすることで結果を改善するかを示す．広告の理解を促すタスクを，広告イメージに人間が生成したステートメントと照合して，広告が促すアクションと，そのアクションを実行するための理論的根拠を記述するものとして定式化する．

* [Weakly- and Semi-Supervised, Non-Overlapping Instance Segmentation of Things and Stuff](http://openaccess.thecvf.com/content_ECCV_2018/html/Anurag_Arnab_Weakly-_and_Semi-Supervised_ECCV_2018_paper.html)
    * セマンティックセグメンテーションとインスタンスの両方を共同して実行する弱教師ありモデルを提案．オブジェクト検出器に基づく多くの一般的なインスタンスセグメンテーションとは対照的に，提案手法は，重なり合うインスタンスを予測しない．さらに，「物」と「物」の両方のクラスを分けて，イメージのすべてのピクセルを説明することができる．Pascal VOCについては，教師学習と弱教師学習の両方で，教師学習されたパフォーマンスの95%を達成した．さらに，セマンティックセグメンテーションとインスタンスセグメンテーションの両方について，Cityscapesに関する最初の弱教師学習の結果を提示する．また，弱教師学習されたフレームワークを使用して，アノテーションの品質と予測パフォーマンスの関係を分析する．

* [Broadcasting Convolutional Network for Visual Relational Reasoning](http://openaccess.thecvf.com/content_ECCV_2018/html/Simyung_Chang_Broadcasting_Convolutional_Network_ECCV_2018_paper.html)
    * 入力画像全体のグローバルな視野から主要被写体の特徴を抽出し，地物との関係を認識するBroadcasting Convolutional Network(BCN)を提案．BCNは，有効な空間フィーチャを収集し，位置情報を埋め込み，それらをフィーチャマップ全体にブロードキャストする単純なネットワークモジュールである．さらに，BCNモジュールを利用して既存のリレーションネットワーク(RN)を改善するマルチリレーションネットワーク(multiRN)を提案．

* [A Unified Framework for Multi-View Multi-Class Object Pose Estimation](http://openaccess.thecvf.com/content_ECCV_2018/html/Chi_Li_A_Unified_Framework_ECCV_2018_paper.html)
    * 物体の姿勢推定における1つの大きな課題は，複雑背景の中で多数の多様な前景物体に対して正確かつ頑強であることである．この問題を解決するために，1つまたは複数のビューから多数のオブジェクトクラスに対して6自由度ポーズを正確に推定するためのスケーラブルなフレームワークを提案．差別的ポーズの特徴を学習するために，3次元でのユニークなテッセレーションに基づく分類と姿勢回帰の両方を組み合わせた推論スキーム，deepCNNによってクラスプライオリティのタイル化されたクラスマップを介したトレーニングプロセスの融合，およびオブジェクトマスクによる深い教師学習を用いた正規化が含まれる．

* [Fast and Accurate Point Cloud Registration using Trees of Gaussian Mixtures](http://openaccess.thecvf.com/content_ECCV_2018/html/Benjamin_Eckart_Fast_and_Accurate_ECCV_2018_paper.html)
    * ポイントクラウドの登録は，多くの重要かつチャレンジングな3D認識問題の中核に位置している．ここで，階層的ガウス混合表現を用いて最先端の速度と精度を達成する新しい登録アルゴリズムであるHGMR(Hierarchical Gaussian Mixture Registration)を提案．HGMRは，多数の小規模なデータ尤度セグメンテーションをGPU上で並行して再帰的に実行することにより，ポイントクラウドデータのトップダウンマルチスケール表現を構築する．

* [Teaching Machines to Understand Baseball Games: Large Scale Baseball Video Database for Multiple Video Understanding Tasks](http://openaccess.thecvf.com/content_ECCV_2018/html/Minho_Shim_Teaching_Machines_to_ECCV_2018_paper.html)
    * BBDBという大規模な野球の試合のビデオデータセットを提案する．このデータは4200時間の試合が含まれており，オンラインで半自動的に400kのアノテーションがされる．動画認識、ローカリゼーション、動画ハイライト生成、データ不均衡問題など、多くの動画認識タスクでに用いられることが期待される

* [Using Object Information for Spotting Text](http://openaccess.thecvf.com/content_ECCV_2018/html/Shitala_Prasad_Using_Object_Information_ECCV_2018_paper.html)
    * テキストとオブジェクトの依存関係に基づくテキストスポッティングアルゴリズムを提案．

* [Deep Domain Generalization via Conditional Invariant Adversarial Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Ya_Li_Deep_Domain_Generalization_ECCV_2018_paper.html)
    * ドメイン不変表現学習のためにディープニューラルネットワークを利用することによって，end-to-endの条件不変深部ドメイン汎化手法を提案．

* [On the Solvability of Viewing Graphs](http://openaccess.thecvf.com/content_ECCV_2018/html/Matthew_Trager_On_the_Solvability_ECCV_2018_paper.html)
    * 解決可能なビューグラフの特徴付けを研究し，すべてのカメラパラメータを回復するために適用できるいくつかの新しい結果を提示する．

* [Learning Type-Aware Embeddings for Fashion Compatibility](http://openaccess.thecvf.com/content_ECCV_2018/html/Mariya_Vasileva_Learning_Type-Aware_Embeddings_ECCV_2018_paper.html)
    * アイテムタイプを考慮したイメージ埋め込みを学習するアプローチを提案し，end-to-endモデルにおけるアイテムの類似性と互換性の概念を共同で学習する．学習されたモデルを評価するために，ユーザがPolyvoreウェブサイト上に作成した68,306の衣装をクロールした．

* [Visual Coreference Resolution in Visual Dialog using Neural Module Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Satwik_Kottur_Visual_Coreference_Resolution_ECCV_2018_paper.html)
    * 視覚的対話のためのニューラルモジュールネットワークアーキテクチャを提案．これは，より細かい単語レベルで，明示的で基礎的なコアレッション解決を行う2つの新規モジュールを導入する．このモデルはMNIST Dialogに有効である．

* [Hard-Aware Point-to-Set Deep Metric for Person Re-identification](http://openaccess.thecvf.com/content_ECCV_2018/html/Rui_Yu_Hard-Aware_Point-to-Set_Deep_ECCV_2018_paper.html)
    * ディープメトリック学習のパフォーマンスは，従来のサンプリング方法によって大きく制限される．この問題を解決するために，ソフトハードマイニング方式でハードウェアポイントツーセット(HAP2S)損失を提案．他の最先端の損失関数と比較した場合，いくつかの有利な特性がみられる．

* [Gray box adversarial training](http://openaccess.thecvf.com/content_ECCV_2018/html/Vivek_B_S_Gray_box_adversarial_ECCV_2018_paper.html)
    * ブラックボックス攻撃に関して，ⅰ)既存の評価方針の欠点を明らかにする．ⅱ)ホワイトボックス攻撃とブラックボックス攻撃から新しいグレイボックス攻撃を導入し，新しい評価方法を提案．ⅲ)中間バージョンのモデルを使用して敵を襲う”Graybox Adversarial Training”という敵対的訓練の新しい手法を提案．

* [Exploiting Vector Fields for Geometric Rectification of Distorted Document Images](http://openaccess.thecvf.com/content_ECCV_2018/html/Gaofeng_Meng_Exploiting_Vector_Fields_ECCV_2018_paper.html)
    * ハンドヘルドカメラで撮影した歪みのある文書画像を幾何学的に整形するセグメントフリーの方法を提案する。本方法は、画像の固有ベクトル場を利用することによって3Dページ形状を回復することができる。カールしたページ形状が一般的な円柱面であると仮定して、カメラフィールドと3D形状モデルに関連するパラメータをベクトルフィールド上の加重多数決によって推定する。次に、オイラー法を用いて常微分方程式（ODE）を解くことにより、表面の空間的な方向性を復元する。最後に、推定された3Dページ表面を平面上に平坦化することによって、画像の幾何学的歪みを修正することができる。

* [Revisiting RCNN: On Awakening the Classification Power of Faster RCNN](http://openaccess.thecvf.com/content_ECCV_2018/html/Bowen_Cheng_Revisiting_RCNN_On_ECCV_2018_paper.html)
    * Faster RCNNの分類能力を向上させることにタスクの重きをおいた研究．通常のFaster-RCNNモジュールにDecoupled Classification Refinement(DCR)モジュールを追加し，間違った確信度の高いものをサンプリングしていき，分類器を学習させ強力にする

* [On Regularized Losses for Weakly-supervised CNN Segmentation](http://openaccess.thecvf.com/content_ECCV_2018/html/Meng_Tang_On_Regularized_Losses_ECCV_2018_paper.html)
    * MRF/CRFの正規化項を統合した様々な損失を提案し，実験的に比較する．提案手法は，正式な損失を早期の提案生成手法と並行して処理する．このアプローチは，ほぼ完全な教師品質を備えたセマンティックセグメンテーションにおける最先端の精度を達成．

* [ShapeCodes: Self-Supervised Feature Learning by Lifting Views to Viewgrids](http://openaccess.thecvf.com/content_ECCV_2018/html/Dinesh_Jayaraman_ShapeCodes_Self-Supervised_Feature_ECCV_2018_paper.html)
    * 単一形状の画像表現に3D形状情報を埋め込む教師学習されない特徴学習アプローチを導入．ネットワークは，未知カテゴリーおよび未知視点の入力画像を潜在空間に写像し，そこからデコンボリューション・デコーダは画像をその全視野角物体を示す完全な視野グリッドに最良に「持ち上げる」ことができる．

* [A Minimal Closed-Form Solution for Multi-Perspective Pose Estimation using Points and Lines](http://openaccess.thecvf.com/content_ECCV_2018/html/Pedro_Miraldo_A_Minimal_Closed-Form_ECCV_2018_paper.html)
    * 多視点カメラのために点と線の両方を用いて姿勢推定のための最小限の解を提案．

* [Interaction-aware Spatio-temporal Pyramid Attention Networks for Action Classification](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Du_Interaction-aware_Spatio-temporal_Pyramid_ECCV_2018_paper.html)
    * 注意マップを学習するためにPCAに触発された効果的な相互作用認識セルフアテンションモデルを提案．さらに，深いネットワークの異なるレイヤーは異なるスケールのフィーチャマップをキャプチャするため，これらのフィーチャマップを使用して空間ピラミッドを作成し，マルチスケール情報を使用してより正確なアテンションスコアを取得する．

* [Towards Privacy-Preserving Visual Recognition via Adversarial Training: A Pilot Study](http://openaccess.thecvf.com/content_ECCV_2018/html/Zhenyu_Wu_Towards_Privacy-Preserving_Visual_ECCV_2018_paper.html)
    * スマートカメラアプリケーションにおいて要求される特徴であるプライバシー保護視覚認識を，ユニークな敵対的な訓練フレームワークを策定することによって改善することを目指している．提案されたフレームワークは，目標とされたタスクの性能と，劣化したビデオ上の関連プライバシー・バジェットとの間のトレードオフを最適化するために，元のビデオ入力にたいする劣化変換を明示的に学習する．

* [Polarimetric Three-View Geometry](http://openaccess.thecvf.com/content_ECCV_2018/html/Lixiong_Chen_Polarimetric_Three-View_Geometry_ECCV_2018_paper.html)
    * この論文では，偏光と三面図形の間の接続を理論化している．これは，3台のカメラからなるシステムの相対的な姿勢を調整する偏光誘起拘束を提示する．スペキュラリットの対応関係を用いた相互検証メカニズムは，混合偏光によって引き起こされるあいまい性を効果的に解決することが出来る．

* [SketchyScene: Richly-Annotated Scene Sketches](http://openaccess.thecvf.com/content_ECCV_2018/html/Changqing_Zou_SketchyScene_Richly-Annotated_Scene_ECCV_2018_paper.html)
    * 最大規模な最初のシーンスケッチのデータセットであるSketchySceneのオブジェクトとシーンの両方の認識をする目的の研究． SketchySceneには、29,000以上のシーンレベルのスケッチ、7,000以上のシーンテンプレートと写真のペア、および11,000以上のオブジェクトスケッチが含まれる．画像検索や色塗り，キャプション生成をすることでデータセットの可能性を検証する

* [Bi-Real Net: Enhancing the Performance of 1-bit CNNs with Improved Representational Capability and Advanced Training Algorithm](http://openaccess.thecvf.com/content_ECCV_2018/html/zechun_liu_Bi-Real_Net_Enhancing_ECCV_2018_paper.html)
    * 1－bit CNN(ウェイトと活性化関数がバイナリ)に関する研究．従来の1－bit CNNは大規模なデータセットにおいて普通のCNNより精度の差が大きい．1－bit CNNと普通のCNNの性能ギャップを縮小する新たなネットワーク構造Bi-Real netを提案した．Bi-Real netは1－bit conv, batchnorm layerの後に普通の活性化関数を用いる．Bi-Real netは1－bit CNNの性能を大幅に増強した．また，いくつかの1－bit CNNネットワークに用いられるテクニックを紹介した．Bi-Real netの34層バージョンはImageNetにおいて62.2%のトップ１精度を得られた．

* [Deep Continuous Fusion for Multi-Sensor 3D Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Ming_Liang_Deep_Continuous_Fusion_ECCV_2018_paper.html)
    * LIDARとカメラのデータから高精度で3次元物体を検出できる検出器の提案．LIDARセンサーのデータとRGB画像を異なる解像度でfuseするend-to-endなcontinuous convolutionsを利用したネットワーク構造を提案した．提案のcontinuous convolutions layerが離散的な画像特徴と連続的な幾何情報を両方encodeできる，これによりマルチセンサーの情報のfusionを可能にした．KITTI,及びほかの3次元物体検出用データセットで従来手法より良い精度を達成した．

* [Focus on the Hard Things: Dynamic Task Prioritization for Multitask Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Michelle_Guo_Focus_on_the_ECCV_2018_paper.html)
    * Multitask learningに用いられる動的タスク優先順位をつける(dynamic task prioritization)手法を提案した．提案手法がトレーニング中にダイナミックで困難タスクを見つめて困難なタスクから学習を行う（curriculum学習と逆）．いくつかの実験を用いて困難タスクを優先的に学習することの重要性を示した．タスクのロス関数のウェイトを動的に変化させることによりタスクの優先順位を調整する．COCO, MPIIデータセットで従来のmultitask learningより良い性能，single task learningと匹敵するパフォーマンスを得られた．

* [Domain transfer through deep activation matching](http://openaccess.thecvf.com/content_ECCV_2018/html/Haoshuo_Huang_Domain_transfer_through_ECCV_2018_paper.html)
    * セマンティックセグメンテーションに用いられるlayer-wiseな無監督Domain adaptationの新たな手法を提案した．従来のDomain adaptationは主に出力の分布をマッチングにより行い，この文章で中間層の分布に対してもalignを行う．このようなやり方は①最適化問題がより良好にconditioned②covariate shiftを軽減できる．提案手法はGANを用いて分布のalignを行う．GTA->Cityscapes, SYNTHIA->Cityscapes, USPS, MNIST-> 画像分類の3つの実験でSOTAなDomain adaptationパフォーマンスを得られた．

* [Joint Blind Motion Deblurring and Depth Estimation of Light Field](http://openaccess.thecvf.com/content_ECCV_2018/html/Dongwoo_Lee_Joint_Blind_Motion_ECCV_2018_paper.html)
    * サブアパーチャ画像、カメラの動き、およびぼやけた4Dライトフィールドからのシーン深度などのすべてのぼけモデル変数を推定するための新しいアルゴリズムを提案した．

* [Learning to Look around Objects for Top-View Representations of Outdoor Scenes](http://openaccess.thecvf.com/content_ECCV_2018/html/Samuel_Schulter_Learning_to_Look_ECCV_2018_paper.html)
    * 新規な問題設定：“室外道路シーンのtop-view occusion-reasonedセマンティックシーンレイアウトを推定する”を提案した．この問題設定には：3次元幾何，セマンティック推定，オクルージョン領域のセマンティック推定の3つを同時に解決する．前景である車／人などを見まわすことによりオクルージョン領域のシーンレイアウトを推定するネットワークを提案した．また，top-view視点が学習過程によりより豊かなpriorsを学習できることをしめした．KITTI, Cityscapesデータセットで提案手法の評価を行った．

* [Data-Driven Sparse Structure Selection for Deep Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Zehao_Huang_Data-Driven_Sparse_Structure_ECCV_2018_paper.html)
    * CNNの構造を適応的学習できるData-drivenなSparse Structure Selection (SSS)を提案した．新たなCNNパラメータscaling factorを提案し，これを用いることによりneurons, groupsとresidual blocksの出力をscaleできる．scaling factorsにスパース正規化を加える．scaling factorをコントロールすることにより不要な構造の削除ができる．提案のネットワークを用いてトレーニングのパラメータ調整の工夫を軽減できる．ソースコード公開中

* [Reconstruction-based Pairwise Depth Dataset for Depth Image Enhancement Using CNN](http://openaccess.thecvf.com/content_ECCV_2018/html/Junho_Jeon_Reconstruction-based_Pairwise_Depth_ECCV_2018_paper.html)
    * 安価なRGBDカメラで撮ったデータから三次元リコンストラクションを良好に行えるデプス画像enhancement手法の提案．デンス3次元サーフェスリコンストラクションからimage-depth画像ペアを自動生成する方法を提案した．サーフェスリコンストラクションしながら，filteringにより低質なペアを除去する．また，マルチスケールlaplacian pyramidベースなNN及び構造保持ロス関数を用いてcoarse-to-fineでノイズとホールを除去する．提案手法を用いて修正したデプス画像で三次元リコンストラクションのパフォーマンスが良い．

* [A Geometric Perspective on Structured Light Coding](http://openaccess.thecvf.com/content_ECCV_2018/html/Mohit_Gupta_A_Geometric_Perspective_ECCV_2018_paper.html)
    * 高性能構造光（SL）符号化方式の解析と設計のための数学的枠組みを提示する。グローバルイルミネーションを扱うための高い空間周波数を有するパターンのような特定の望ましい特性を有するハミルトニアンコーディングパターンを設計するための一般的なレシピを提案する。我々は、提案されたアプローチを評価するためにいくつかの実験を行い、暗いアルベド、強い周囲光、および相互反射を含むシーンを含む挑戦的なシナリオにおいて、ハミルトニアン符号化に基づくSLが既存の方法より優れていることを示す。

* [3D Ego-Pose Estimation via Imitation Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Ye_Yuan_3D_Ego-Pose_Estimation_ECCV_2018_paper.html)
    * 物理シミュレーションと模倣学習を用いて人の動きをモデル化し、自我姿勢推定のためのビデオ調整された制御方針を学習するための新しい制御ベースのアプローチを提案する。模倣学習フレームワークは、シミュレーションデータに基づいて訓練されたポリシーを実世界のデータに移行するためのドメイン適合を実行することを可能にする。

* [Unsupervised Learning of Multi-Frame Optical Flow with Occlusions](http://openaccess.thecvf.com/content_ECCV_2018/html/Joel_Janai_Unsupervised_Learning_of_ECCV_2018_paper.html)
    * 複数フレームにわたるオプティカルフローとオクルージョンの教師なし学習の枠組みを提案．より具体的には、3つのフレームの最小構成を利用して測光損失を強化し，明示的にオクルージョンの理由を説明．

* [Dynamic Conditional Networks for Few-Shot Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Fang_Zhao_Dynamic_Conditional_Networks_ECCV_2018_paper.html)
    * 本論文では、条件付き少数訓練を扱うための新しい動的条件付き畳み込みネットワーク（Dynamic Conditional Convolutional Network、DCCN）を提案．すなわち、各条件に対して少数の訓練サンプルしか利用できない。 DCCNはデュアルサブネットで構成されています.DyConvNetには、基本フィルタのバンクを持つ動的畳み込みレイヤーが含まれる． CondiNetは、基本フィルタを線形結合するために、条件付き入力から一連の適応重みを予測する．マルチモーダル画像分類、フレーズグラウンディング、アイデンティティベースの顔生成など、条件付きモデル学習として定式化できる4つのタスクについてDCCNを評価．

* [3DFeat-Net: Weakly Supervised Local 3D Features for Rigid Point Cloud Registration](http://openaccess.thecvf.com/content_ECCV_2018/html/Zi_Jian_Yew_3DFeat-Net_Weakly_Supervised_ECCV_2018_paper.html)
    * 弱監督なポイントクラウドレジストレーションに用いられる3次元特徴抽出器3DFeat-Netを提案した．GPS/INSから収集した3次元ポイントクラウドを対象に，アライメントとattentionメカニズムを利用した弱監督な３次元マッチングを実現した．室外のLidarデータセットを用いて提案の3DFeat-Netの有効性を検証した．

* [Learning to Forecast and Refine Residual Motion for Image-to-Video Generation](http://openaccess.thecvf.com/content_ECCV_2018/html/Long_Zhao_Learning_to_Forecast_ECCV_2018_paper.html)
    * 画像2枚からビデオに変換するタスクを行う．運動をモデル化するために現在のフレームと将来のフレームとの間の残差運動を学習するようにネットワークを使用し，無関係な体の動きを学習しないようにした．

* [Learn-to-Score: Efficient 3D Scene Exploration by Predicting View Utility](http://openaccess.thecvf.com/content_ECCV_2018/html/Benjamin_Hepp_Learn-to-Score_Efficient_3D_ECCV_2018_paper.html)
    * 未来のビューの有用性を予測する手法の提案．ドローンが環境を観測し，環境の3Dマップを作成する際に，情報量が少ないビューなども大量に含めている．従来この分野主にhandcraftedな関数によってそれぞれのビューの有用性を評価しているが，この文章で3DCNNにより未来のビューの有用性を予測するネットワークを提案した．いくつかurban scenesの従来のデータセットで提案手法の有用性を示した．

* [Deep Co-Training for Semi-Supervised Image Recognition](http://openaccess.thecvf.com/content_ECCV_2018/html/Siyuan_Qiao_Deep_Co-Training_for_ECCV_2018_paper.html)
    * Semi-supervised画像認識手法の提案．Deep Co-Trainingネットワークを提案した．Deep Co-Trainingは，異なる視点を認識するマルチネットワークをトレーニングし，またadversarial examplesを探索して視点の違いをencourageする．Deep Co-Trainingを用いて学習データからより全面的な情報を得られる．SVHN,CIFAR-10/100などのデータセットで従来のSemi-supervised手法より良い性能を得られた．

* [Attention-aware Deep Adversarial Hashing for Cross Modal Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Xi_Zhang_Attention-aware_Deep_Adversarial_ECCV_2018_paper.html)
    * アテンションに基づいた敵対的なハッシング手法の提案．ハッシュモジュールとアテンションモジュールで構成されていて，マルチモーダルデータの類似性を保持することを学習する．アテンションモジュールでは，ハッシング・モジュールが何もない部分の特徴の類似性を保存を保存しないようにして敵対的に学習する．

* [Remote Photoplethysmography Correspondence Feature for 3D Mask Face Presentation Attack Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Siqi_Liu_Remote_Photoplethysmography_Correspondence_ECCV_2018_paper.html)
    * 顔認識の3D mask face presentation attack問題を対応する新たな特徴量を提案した．従来のrPPGがノイズ信号に対してロバスト性が低いことから，ノイズのrPPGデータからheartbeat vestigeを検出できる特徴量CFrPPGを提案した．更に，global noiseとCFrPPG特徴を組み合わせる新たな学習策を提案した．従来のデータセットで3D mask attacksを有効的に防ぐほか，暗い環境やカメラモーションにもロバストで対応できる．

* [Semi-Supervised Generative Adversarial Hashing for Image Retrieval](http://openaccess.thecvf.com/content_ECCV_2018/html/Guanan_Wang_Semi-Supervised_Generative_Adversarial_ECCV_2018_paper.html)
    * Self-supervised learningに用いられる画像をspatial-temporalで順序を付ける手法を提案した．従来のself-supervised order付けに，主にpreselected setからランダムに選択する方が多い．この研究では、DRNをベースとしたsampling policyを提案し，CNN特徴更新の場合の有用性によりpermutationsに新たなorder付けを行う．

* [Improving Spatiotemporal Self-Supervision by Deep Reinforcement Learning](http://openaccess.thecvf.com/content_ECCV_2018/html/Uta_Buchler_Improving_Spatiotemporal_Self-Supervision_ECCV_2018_paper.html)
    * Semi-supervisedなGANを用いたhashing手法SSGANを提案した．GANとDeep hashing modelをminimax two-playerゲームにより結合し，小型なlabeledデータと大量なunlabeledデータから学習を行う．また，新規なsemi-supervised ranking lossとadversary ranking lossを提案した．

* [AutoLoc: Weakly-supervised Temporal Action Localization in Untrimmed Videos](http://openaccess.thecvf.com/content_ECCV_2018/html/Zheng_Shou_AutoLoc_Weakly-supervised_Temporal_ECCV_2018_paper.html)
    * weakly-supervisedなビデオからTemporal Action Localizationを行う手法AutoLocを提案した．AutoLocがビデオからactionの時系列boundaryを検出できる．新たなOuter-Inner-Contrastive (OIC)ロスを提案した．OICによりトレーニングデータからsegment-levelな監督信号を得られる．THUMOS’14とActivityNetデータセットにおいて大幅にmAPを向上できた．

* [Revisiting Autofocus for Smartphone Cameras](http://openaccess.thecvf.com/content_ECCV_2018/html/Abdullah_Abuolaim_Revisiting_Autofocus_for_ECCV_2018_paper.html)
    * ?コントラスト検出や位相差検出など、AFシステムで使用される基礎となるアルゴリズムは十分に確立されている．しかし、特定の場面に最適な焦点を合わせる方法に関する高いレベルで目標を決定することは明確に示されていない．本研究では，時系列の各時点でフルフォーカルスタックへのアクセスを提供する新しい4Dデータセットのキャプチャをする．

* [Contour Knowledge Transfer for Salient Object Detection](http://openaccess.thecvf.com/content_ECCV_2018/html/Xin_Li_Contour_Knowledge_Transfer_ECCV_2018_paper.html)
    * 輪郭を検出し，顕著性の高い部分を検出するネットワーク(C2S-Net)を提案する．輪郭ブランチで輪郭を推定し，顕著性マスクを生成する．顕著性ブランチでは，顕著性認識をし，輪郭ラベルを出力する．輪郭ブランチと顕著性ブランチをフィードバックする．

* [Deep Volumetric Video From Very Sparse Multi-View Performance Capture](http://openaccess.thecvf.com/content_ECCV_2018/html/Zeng_Huang_Deep_Volumetric_Video_ECCV_2018_paper.html)
    * PassiveでスパースなマルチビューキャプチャーシステムでDNNによりパフォーマンスをキャプチャーできる手法を提案した．従来のパフォーマンスキャプチャーシステムがprescannedモデル，大量なカメラ及びactiveなセンサーなどが必要．この研究で3つのRGBカメラからtemplate-free, per-frame 3Dサーフェスをリコンストラクションを可能にした．具体的にはRGB画像を3Dボリューム空間に変換できるマルチビューCNN構造を提案した．CGデータでトレーニングして，リアルパフォーマンスをキャプチャーできる．様々なVR,ARシステムで提案手法を応用できる．

* [Person Re-identification with Deep Similarity-Guided Graph Neural Network](http://openaccess.thecvf.com/content_ECCV_2018/html/Yantao_Shen_Person_Re-identification_with_ECCV_2018_paper.html)
    * 従来のperson Re-ID手法が異なるprobe-gallery pairs関の関連性をあまり検討していない．そのため，hard samplesの類似性分析の精度が低くなりやすい．この問題を克服するため，Similarity-Guided Graph NN(SGGNN)を提案した．Probe imageとgallery imagesをSGGNNに入力し，SGGNNがprobe-gallery pairsの関係をグラフにより表示し，その関係を利用してprobe-gallery の関係特徴を更新する．3つのperson Re-IDデータセットで提案手法の有効性を検証した．

* [Deep Component Analysis via Alternating Direction Neural Networks](http://openaccess.thecvf.com/content_ECCV_2018/html/Calvin_Murdock_Deep_Component_Analysis_ECCV_2018_paper.html)
    * 伝統的なcomponent分析とDNNのgapに橋掛けるDeep Component Analysis(DeepCA)を提案した．DeepCAがComponent分析の表現能力をディープモデルに介して高くしたモデルの提案である．様々なタスクで提案構造の有効性を検証した，例えば単眼画像デプス推定．

* [Understanding Perceptual and Conceptual Fluency at a Large Scale](http://openaccess.thecvf.com/content_ECCV_2018/html/Meredith_Hu_Understanding_Perceptual_and_ECCV_2018_paper.html)
    * 大規模なlogoデータセットを提案した(543,758画像，39工業カテゴリ，216国)．いくつか異なるDCNN構造を用いて，そういった構造や具体的なネットワークパラメータがいかにデザインの評価と予測の効果に影響するかを実験した．また，デザインのperceptual distinctiveness及びambiguity in meaningの2つの指標を抽出または評価できる手法を提案した．
