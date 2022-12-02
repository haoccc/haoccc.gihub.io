---
title: Pytorch-Tips
date: 2022-12-02 10:52:29
tags:
---

## torchvision.transforms as T

1. T.ToTensor()
   - 如果输入为np.ndarray，会自动转置transpose((2, 0, 1)
   - 如果输入为np.unit8(图片格式), 会自动 /255 进行归一化
