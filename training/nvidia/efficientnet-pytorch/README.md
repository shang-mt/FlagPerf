### 测试数据集下载
[测试数据集下载](../../benchmarks/efficientnet/README.md#数据集)

### Nvidia GPU配置与运行信息参考
#### 环境配置
- ##### 硬件环境
    - 机器型号: NVIDIA DGX A100(40G) 
    - 加速卡型号: NVIDIA_A100-SXM4-40GB
    - CPU型号: AMD EPYC7742-64core@1.5G
    - 多机网络类型、带宽: InfiniBand，200Gb/s
- ##### 软件环境
   - OS版本：Ubuntu 20.04
   - OS kernel版本: 5.4.0-113-generic     
   - 加速卡驱动版本：470.129.06
   - Docker 版本：20.10.16
   - 训练框架版本：pytorch-1.8.0a0+52ea372
   - 依赖软件版本：无


### 运行情况
| 训练资源 | 配置文件        | 运行时长(s) | 目标精度 | 收敛精度 | Steps数 | 性能（samples/s) |
| -------- | --------------- | ----------- | -------- | -------- | ------- | ---------------- |
| 单机1卡  | config_A100x1x1 |      |       |    |     |             |
| 单机2卡  | config_A100x1x2 |      |       |    |     |             |
| 单机4卡  | config_A100x1x4 |      |       |    |     |             |
| 单机8卡  | config_A100x1x8 |   328383.49   |   82.672  |  82.672  |  750600  |    2340.6    |
| 两机8卡  | config_A100x2x8 |      |       |    |     |             |

[官方精度](https://github.com/pytorch/vision/blob/main/torchvision/models/efficientnet.py#L669)为84.228，按照[官方配置](https://github.com/pytorch/vision/blob/main/references/classification/README.md)，训完得到的精度为82.672，后续排期优化

