# Deep-Space Image Restoration via Physics-Informed Conditional GAN (PI-cGAN)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-orange)
![Dataset](https://img.shields.io/badge/Dataset-NASA%20FITS-blueviolet)

# 本研究為旺宏科學獎（Macronix Science Awards）之參賽作品。

## 專案簡介 (Abstract)
本研究針對深度學習技術應用於深空影像重建時，在極低信噪比（SNR）環境下因過度
擬合所產生之「幻覺偽影」及物理能量失真等核心問題，提出相應解決方案。現有多數純視
覺導向模型雖能提升影像解析度，卻可能生成缺乏物理依據之假結構，甚至違背光通量守恆
原則，影響天文觀測之科學真實性。
 為改善上述問題，本研究提出融合天文物理先驗知識之生成對抗網路（Physics-Informed
Conditional GAN, PI-cGAN），以 cGAN 為基礎結合物理損失函數，並使用 NASA 公開 FITS
天文影像資料建構訓練資料集，透過多版本模型迭代優化物理約束策略。研究以 PSNR、
SSIM、Phase Consistency Error 與 Linear Flux Error 等指標進行模型評估與參數調整。
 實驗結果顯示，相較於傳統 Basic cGAN，本研究提出之 PI-cGAN 可有效抑制幻覺偽
影，並將光通量誤差由平均 214.66% 降低至 4.65%，在提升影像細節復原能力的同時，兼顧
物理一致性與科學合理性，提供一套具備工程應用潛力之深空影像重建方法。

## 專案架構 (Repository Structure)
.
├── Data dealing tool/                   # 天文影像數據預處理模組
│   └── astro cGAN dataset dealing auto.ipynb
├── Model/                               # 核心模型架構與各階段訓練歷程
│   ├── basic cGAN model.ipynb           # 基準測試模型 (Baseline)
│   ├── PI-cGAN model I.ipynb            # PI-cGAN 演進版本 I
│   ├── PI-cGAN model II.ipynb           # PI-cGAN 演進版本 II
│   ├── PI-cGAN model III.ipynb          # PI-cGAN 演進版本 III
│   ├── PI-cGAN model IV.ipynb           # PI-cGAN 演進版本 IV
│   ├── PI-cGAN model IV.1.ipynb         # PI-cGAN 演進版本 IV.1 
│   └── PI-cGAN model V.ipynb            # PI-cGAN 演進版本 V
├── .gitignore                           # Git 忽略檔案設定
└── README.md                            # 專案總說明文件
