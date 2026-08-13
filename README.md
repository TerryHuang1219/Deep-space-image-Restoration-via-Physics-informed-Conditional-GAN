# Deep-space-image-Restoration-via-Physics-informed-Conditional-GAN
本研究探討深度學習應用於深空影像重建時，在極低信噪比（SNR）環境下因過度擬合產生幻覺偽影與物理能量失真之問題。為此提出融合天文物理先驗知識之生成對抗網路（Physics-Informed Conditional GAN, PI-cGAN），於cGAN中加入物理損失函數，並以NASA公開FITS天文影像建立訓練資料集，透過模型迭代優化物理約束。研究以PSNR、SSIM、Phase Consistency Error及Linear Flux Error評估。結果顯示，PI-cGAN可有效抑制幻覺偽影，並將平均光通量誤差由214.66%降至4.65%，在提升影像細節復原能力的同時維持物理一致性與科學合理性。
