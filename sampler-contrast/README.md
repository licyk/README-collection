# 采样算法对比
## 简介
对不同采样算法和采样算法的调度器做个简单的对比

## 参数
- 正向提示词
```
1girl,cherry blossoms,hair flower,hair ribbon,cat ears,animal ear fluff,blue eyes,grey hair,short hair,bangs,hair between eyes,eyebrows visible through hair,blush,open mouth,light smile,neck ribbon,white sleeveless dress,crease,frilled_collar,detached_sleeves,flat chest,legs,
upper body,looking at viewer,sitting near river,hand on own chest,fist,
outdoors,flower,day,tree,grass,bridge,river,road,water,nature,sun,field,
foot out of frame,close-up,from_above,
```

- 反向提示词
```
nsfw,lowres,bad anatomy,bad hands,text,error,missing fingers,extra digit,fewer digits,cropped,worst quality,low quality,normal quality,jpeg artifacts,signature,watermark,username,blurry,bad feet,
```

- 提示词引导系数：7
- CLIP 停止层数：2
- 分辨率：1024x768
- 采样步数：20
- 种子：743776728
- 大模型：[cetusMix_Whalefall2](https://civitai.com/models/6755?modelVersionId=105924)
- VAE 模型：[vae-ft-mse-840000-ema-pruned](https://huggingface.co/stabilityai/sd-vae-ft-mse-original/blob/main/vae-ft-mse-840000-ema-pruned.ckpt)
- SD WebUI 版本：v1.9.0-15-gff6f4680
- 测试的采样算法：
  - DPM++ 2M
  - DPM++ SDE
  - DPM++ 2M SDE
  - DPM++ 2M SDE Heun
  - DPM++ 2S a
  - DPM++ 3M SDE
  - Euler a
  - Euler
  - LMS
  - Henu
  - DPM2
  - DPM2 a
  - DPM fast
  - DPM adaptive
  - Restart
  - DDIM
  - PLMS
  - UniPC
  - LCM
  - Euler_Dy
  - Eular_Max
  - Eular_Smea_Dy
  - Eular_Smea
- 测试的调度器：
  - Uniform
  - Karras
  - Exponential
  - Polyexponential
  - SGM Uniform

>[!NOTE]  
>`Euler_Dy`，`Eular_Max`，`Eular_Smea_Dy`，`Eular_Smea`采样算法需安装 [advanced_euler_sampler_extension](https://github.com/licyk/advanced_euler_sampler_extension) 扩展

## 对比图
- DPM++ 2M
![img](img/xyz_grid-0033-20240414_113801_cetusMix_Whalefall2-fp16-no-ema_DPM++_2M.png)

- DPM++ SDE
![img](img/xyz_grid-0034-20240414_113954_cetusMix_Whalefall2-fp16-no-ema_DPM++_SDE.png)

- DPM++ 2M SDE
![img](img/xyz_grid-0035-20240414_114059_cetusMix_Whalefall2-fp16-no-ema_DPM++_2M_SDE.png)

- DPM++ 2M SDE Heun
![img](img/xyz_grid-0036-20240414_114203_cetusMix_Whalefall2-fp16-no-ema_DPM++_2M_SDE_Heun.png)

- DPM++ 2S a
![img](img/xyz_grid-0037-20240414_114349_cetusMix_Whalefall2-fp16-no-ema_DPM++_2S_a.png)

- DPM++ 3M SDE
![img](img/xyz_grid-0038-20240414_114503_cetusMix_Whalefall2-fp16-no-ema_DPM++_3M_SDE.png)

- Euler a
![img](img/xyz_grid-0039-20240414_114607_cetusMix_Whalefall2-fp16-no-ema_Euler_a.png)

- Euler
![img](img/xyz_grid-0040-20240414_114710_cetusMix_Whalefall2-fp16-no-ema_Euler.png)

- LMS
![img](img/xyz_grid-0041-20240414_114921_cetusMix_Whalefall2-fp16-no-ema_LMS.png)

- Henu
![img](img/xyz_grid-0042-20240414_115107_cetusMix_Whalefall2-fp16-no-ema_Heun.png)

- DPM2
![img](img/xyz_grid-0043-20240414_115255_cetusMix_Whalefall2-fp16-no-ema_DPM2.png)

- DPM2 a
![img](img/xyz_grid-0044-20240414_115442_cetusMix_Whalefall2-fp16-no-ema_DPM2_a.png)

- DPM fast
![img](img/xyz_grid-0045-20240414_115545_cetusMix_Whalefall2-fp16-no-ema_DPM_fast.png)

- DPM adaptive
![img](img/xyz_grid-0046-20240414_120126_cetusMix_Whalefall2-fp16-no-ema_DPM_adaptive.png)

- Restart
![img](img/xyz_grid-0047-20240414_120312_cetusMix_Whalefall2-fp16-no-ema_Restart.png)

- DDIM
![img](img/xyz_grid-0048-20240414_120416_cetusMix_Whalefall2-fp16-no-ema_DDIM.png)

- PLMS
![img](img/xyz_grid-0049-20240414_120527_cetusMix_Whalefall2-fp16-no-ema_PLMS.png)

- UniPC
![img](img/xyz_grid-0050-20240414_120632_cetusMix_Whalefall2-fp16-no-ema_UniPC.png)

- LCM
![img](img/xyz_grid-0051-20240414_120734_cetusMix_Whalefall2-fp16-no-ema_LCM.png)

- Euler_Dy
![img](img/xyz_grid-0052-20240414_120841_cetusMix_Whalefall2-fp16-no-ema_Euler_Dy.png)

- Eular_Max
![img](img/xyz_grid-0053-20240414_120942_cetusMix_Whalefall2-fp16-no-ema_Euler_Max.png)

- Eular_Smea_Dy
![img](img/xyz_grid-0054-20240414_121128_cetusMix_Whalefall2-fp16-no-ema_Euler_Smea_Dy.png)

- Eular_Smea
![img](img/xyz_grid-0055-20240414_121236_cetusMix_Whalefall2-fp16-no-ema_Euler_Smea.png)

***

2024.6.9

在 SD WebUI 的 dev 分支更新了 KL Optimal 和 Align Your Steps 调度器后，对我常用的算法测试了一遍效果。

- Restart
![img](img/xyz_grid-0000-20240609_235024_animagine-xl-3.1_Restart.png)

- UniPC
![img](img/xyz_grid-0002-20240610_000331_animagine-xl-3.1_UniPC.png)

- Euler_Dy_Negative
![img](img/xyz_grid-0003-20240610_000910_animagine-xl-3.1_Euler_Dy_Negative.png)

- Euler_Smea_Dy
![img](img/xyz_grid-0004-20240610_001330_animagine-xl-3.1_Euler_Smea_Dy.png)

- DPM++ 2M SDE
![img](img/xyz_grid-0005-20240610_001825_animagine-xl-3.1_DPM++_2M_SDE.png)

- Euler a
![img](img/xyz_grid-0006-20240610_002506_animagine-xl-3.1_Euler_a.png)

- Heun
![img](img/xyz_grid-0007-20240610_003237_animagine-xl-3.1_Heun.png)

- DPM++ 2M SDE Heun
![img](img/xyz_grid-0008-20240610_003824_animagine-xl-3.1_DPM++_2M_SDE_Heun.png)

***

2024.7.6

SD WebUI 更新了 DDIM CFG++ 采样器和 Simple、Normal、DDIM 调度器，顺手测试了一下效果。

- DDIM CFG++
![img](img/xyz_grid-0000-20240706_182431_animagine-xl-3.1_DDIM_CFG++.png)

- TCD
![img](img/xyz_grid-0001-20240706_182834_animagine-xl-3.1_TCD.png)

- Euler_Dy_Negative
![img](img/xyz_grid-0002-20240706_183409_animagine-xl-3.1_Euler_Dy_Negative.png)

- Euler_Negative
![img](img/xyz_grid-0003-20240706_183837_animagine-xl-3.1_Euler_Negative.png)

- Euler_Smea_Dy
![img](img/xyz_grid-0004-20240706_184422_animagine-xl-3.1_Euler_Smea_Dy.png)

- UniPC
![img](img/xyz_grid-0005-20240706_184746_animagine-xl-3.1_UniPC.png)

- Restart
![img](img/xyz_grid-0006-20240706_185510_animagine-xl-3.1_Restart.png)

- DPM++ 2M SDE
![img](img/xyz_grid-0007-20240706_190811_animagine-xl-3.1_DPM++_2M_SDE.png)

- Euler a
![img](img/xyz_grid-0008-20240706_191239_animagine-xl-3.1_Euler_a.png)

- DPM++ 2M SDE Heun
![img](img/xyz_grid-0009-20240706_191746_animagine-xl-3.1_DPM++_2M_SDE_Heun.png)

- Heun
![img](img/xyz_grid-0000-20240706_193536_animagine-xl-3.1_Heun.png)