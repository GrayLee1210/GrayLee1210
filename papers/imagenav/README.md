# 🧭 Image-Goal Navigation 论文清单 (Literature)

> 按**发表年份**排序的 Image-Goal Navigation (ImageNav / Instance-ImageNav) 论文清单。
> 每篇含:论文链接、一句话简介、官方开源代码。精读笔记后续逐篇补充。
> 代码栏 "—" 表示暂未找到官方开源实现。

**任务定义**:给定一张目标位置拍摄的图像 (goal image),智能体在未知环境中仅凭自身 RGB(-D) 观测导航到该图像的拍摄位置。

---

## 2018

- **SPTM** — Semi-Parametric Topological Memory for Navigation (ICLR 2018)
  📄 [arXiv:1803.00653](https://arxiv.org/abs/1803.00653) | 💻 [nsavinov/SPTM](https://github.com/nsavinov/SPTM)
  非参数拓扑图记忆 + 参数化检索网络,无需度量地图即可定位与规划,ImageNav 拓扑记忆路线的源头工作。

## 2020

- **NTS** — Neural Topological SLAM for Visual Navigation (CVPR 2020)
  📄 [arXiv:2005.12256](https://arxiv.org/abs/2005.12256) | 💻 [项目页](https://devendrachaplot.github.io/projects/Neural-Topological-SLAM)(代码未开源)
  语义特征拓扑节点 + 粗几何关系 + 学习式建图/规划,模块化 ImageNav 的代表作,比此前方法相对提升 50%+。

## 2021

- **VGM** — Visual Graph Memory with Unsupervised Representation for Visual Navigation (ICCV 2021)
  📄 [CVF Open Access](https://openaccess.thecvf.com/content/ICCV2021/papers/Kwon_Visual_Graph_Memory_With_Unsupervised_Representation_for_Visual_Navigation_ICCV_2021_paper.pdf) | 💻 [rllab-snu/Visual-Graph-Memory](https://github.com/rllab-snu/Visual-Graph-Memory)
  用无监督图像表征在导航过程中**增量**构建视觉图记忆,GCN + 注意力读取,不依赖位姿信息。

- **NRNS** — No RL, No Simulation: Learning to Navigate without Navigating (NeurIPS 2021)
  📄 [arXiv:2110.09470](https://arxiv.org/abs/2110.09470) | 💻 [meera1hahn/NRNS](https://github.com/meera1hahn/NRNS)
  不用 RL、不用仿真,从被动漫游视频自监督学距离函数与目标预测,层级模块化 ImageNav 强基线。

## 2022

- **Mem-Aug** — Memory-Augmented Reinforcement Learning for Image-Goal Navigation (IROS 2022)
  📄 [arXiv:2101.05181](https://arxiv.org/abs/2101.05181) | 💻 [官方数据集](https://github.com/facebookresearch/image-goal-nav-dataset)(模型代码未开源)
  自监督状态嵌入构建情景记忆 + 注意力策略,纯 RGB 端到端,Gibson 上当时 SOTA;其发布的 Gibson ImageNav episode 数据集成为后续工作的标准评测设置。

- **ZER** — Zero Experience Required: Plug & Play Modular Transfer Learning for Semantic Visual Navigation (CVPR 2022)
  📄 [arXiv:2202.02440](https://arxiv.org/abs/2202.02440) | 💻 [项目页](https://vision.cs.utexas.edu/projects/zsel/)
  以 ImageNav 为源任务学通用语义搜索策略,零样本即插即用迁移到 ObjectNav / RoomNav / AudioNav。

- **ZSON** — Zero-Shot Object-Goal Navigation using Multimodal Goal Embeddings (NeurIPS 2022)
  📄 [arXiv:2206.12403](https://arxiv.org/abs/2206.12403) | 💻 [gunagg/zson](https://github.com/gunagg/zson)
  把目标图像编码进 CLIP 多模态语义空间训练 SemanticNav,ImageNav 训练 → 开放词汇零样本 ObjectNav。

- **TSGM** — Topological Semantic Graph Memory for Image-Goal Navigation (CoRL 2022, oral)
  📄 [arXiv:2209.08274](https://arxiv.org/abs/2209.08274) | 💻 [rllab-snu/TopologicalSemanticGraphMemory](https://github.com/rllab-snu/TopologicalSemanticGraphMemory)
  地点节点 + 物体节点的双层拓扑语义图,跨图混合模块提取上下文,SR +5.0~9.0%、SPL +7.0~23.5%,并有真机演示。

- **OVRL** — Offline Visual Representation Learning for Embodied Navigation (arXiv 2022)
  📄 [arXiv:2204.13226](https://arxiv.org/abs/2204.13226) | 💻 [ykarmesh/OVRL](https://github.com/ykarmesh/OVRL)
  两阶段范式:大规模室内图像离线自监督预训练 + 在线微调,ImageNav 29.2%→54.2%,预训练表征路线的开端。

## 2023

- **OVRL-v2** — A Simple State-of-art Baseline for ImageNav and ObjectNav (arXiv 2023)
  📄 [arXiv:2303.07798](https://arxiv.org/abs/2303.07798) | 💻 [ykarmesh/OVRL](https://github.com/ykarmesh/OVRL)
  ViT + 压缩层 + LSTM 的极简无地图架构,首次展示视觉导航的正向 scaling law,ImageNav 54.2%→82.0%。

- **FGPrompt** ⭐ — Fine-grained Goal Prompting for Image-Goal Navigation (NeurIPS 2023)
  📄 [arXiv:2310.07473](https://arxiv.org/abs/2310.07473) | 💻 [XinyuSun/FGPrompt](https://github.com/XinyuSun/FGPrompt) · [项目页](https://xinyusun.github.io/fgprompt-pages)
  用目标图像的细粒度高分辨率特征图作为 prompt 对观测编码器做条件化(早/中期融合),Gibson SR +8% 且模型缩小 50 倍。**(我研究方向上的关键参考工作)**

## 2024

- **DEBiT** — End-to-End (Instance)-Image Goal Navigation through Correspondence as an Emergent Phenomenon (ICLR 2024)
  📄 [arXiv:2309.16634](https://arxiv.org/abs/2309.16634) | 💻 —
  双目 ViT + 两个预文本任务(跨视图补全、目标检测/可见性),视觉对应关系作为涌现现象,ImageNav 与 Instance-ImageNav 双 SOTA。

- **MemoNav** — Working Memory Model for Visual Navigation (CVPR 2024)
  📄 [arXiv:2402.19161](https://arxiv.org/abs/2402.19161) | 💻 [ZJULiHongxin/MemoNav](https://github.com/ZJULiHongxin/MemoNav)
  仿工作记忆机制:短期记忆(动态节点)+ 遗忘模块 + 长期记忆(全局聚合)三类记忆协同,多目标 ImageNav 显著提升。

- **NoMaD** — Goal Masked Diffusion Policies for Navigation and Exploration (ICRA 2024, Best Paper)
  📄 [arXiv:2310.07896](https://arxiv.org/abs/2310.07896) | 💻 [robodhruv/visualnav-transformer](https://github.com/robodhruv/visualnav-transformer)
  目标掩码 + 扩散策略,单一策略统一"无目标探索"与"图像目标到达",真机部署,导航基础模型路线(GNM/ViNT 续作)。

- **PSL** — Prioritized Semantic Learning for Zero-shot Instance Navigation (ECCV 2024)
  📄 [arXiv:2403.11650](https://arxiv.org/abs/2403.11650) | 💻 [XinyuSun/PSL-InstanceNav](https://github.com/XinyuSun/PSL-InstanceNav)
  优先语义训练策略 + 语义扩展推理,从 ImageNav 预训练走向零样本 InstanceNav,并提出 HM3D InstanceNav 任务设定。

## 2025

- **REGNav** — Room Expert Guided Image-Goal Navigation (AAAI 2025)
  📄 [arXiv:2502.10785](https://arxiv.org/abs/2502.10785) | 💻 [leeBooMla/REGNav](https://github.com/leeBooMla/REGNav)
  无监督预训练"房间专家"判断目标图与当前观测是否同一房间,房间关系知识引导策略,缓解跨房间游荡。

- **NavigateDiff** — Visual Predictors are Zero-Shot Navigation Assistants (ICRA 2025)
  📄 [arXiv:2502.13894](https://arxiv.org/abs/2502.13894) | 💻 [项目页](https://21styouth.github.io/NavigateDiff/)
  VLM + 扩散网络组成视觉预测器,持续预测下一步潜在观测来辅助零样本导航,提升跨场景泛化与真机迁移。

- **RFSG** — Image-Goal Navigation Using Refined Feature Guidance and Scene Graph Enhancement (IROS 2025)
  📄 [arXiv:2503.10986](https://arxiv.org/abs/2503.10986) | 💻 [nubot-nudt/RFSG](https://github.com/nubot-nudt/RFSG)
  空间-通道注意力细粒度融合目标/观测特征 + 自蒸馏 + 图像-物体两级场景图,轻量架构 RTX3080 上 53.5 FPS。

- **UniGoal** — Towards Universal Zero-shot Goal-oriented Navigation (CVPR 2025)
  📄 [arXiv:2503.10630](https://arxiv.org/abs/2503.10630) | 💻 [bagh2178/UniGoal](https://github.com/bagh2178/UniGoal)
  统一图表示 + LLM 图匹配推理,单模型零样本覆盖 ObjectNav / Instance-ImageNav / TextNav 三类目标。

- **RSRNav** — Reasoning Spatial Relationship for Image-Goal Navigation (IEEE TCSVT 2025)
  📄 [arXiv:2504.17991](https://arxiv.org/abs/2504.17991) | 💻 —
  用目标-观测间的相关性建模空间关系(细粒度互相关 + 方向感知相关)替代纯语义特征,对"用户拍摄视角不一致"的设定更鲁棒。

- **What does really matter in image goal navigation?** (arXiv 2025)
  📄 [arXiv:2507.01667](https://arxiv.org/abs/2507.01667) | 💻 —
  NAVER LABS 大规模分析:late fusion / channel stacking / cross-attention 等架构选择如何影响端到端 RL 中相对位姿估计能力的涌现,并指出部分近期方法的性能受益于仿真捷径。

- **IGL-Nav** — Incremental 3D Gaussian Localization for Image-goal Navigation (ICCV 2025)
  📄 [arXiv:2508.00823](https://arxiv.org/abs/2508.00823) | 💻 [项目页](https://gwxuan.github.io/IGL-Nav/)
  增量式 3DGS 场景表示 + 离散匹配粗定位 + 可微渲染精解 6-DoF 目标位姿,支持 free-view 目标图像,可用手机拍照真机部署。

- **SIGN** — Safety-Aware Image-Goal Navigation for Autonomous Drones via Reinforcement Learning (arXiv 2025)
  📄 [arXiv:2508.12394](https://arxiv.org/abs/2508.12394) | 💻 —(论文称录用后开源)
  无人机 ImageNav:连续速度控制端到端 RL + 自监督辅助任务 + 深度碰撞概率安全模块,无需外部定位,sim-to-real 零微调。

## 2026

- **HRNav** — Think before Go: Hierarchical Reasoning for Image-goal Navigation (arXiv 2026, 标注 ACL 2026)
  📄 [arXiv:2604.17407](https://arxiv.org/abs/2604.17407) | 💻 —
  快慢分层:VLM 慢规划器生成短程语义计划("出门/沿走廊"),RL 快执行器跟随,游荡抑制惩罚 (WSP),仿真+真机验证。

- **AnyImageNav** — Any-View Geometry for Precise Last-Meter Image-Goal Navigation (arXiv 2026, 标注 CVPR 2026)
  📄 [arXiv:2604.05351](https://arxiv.org/abs/2604.05351) | 💻 —
  training-free:把目标图像当**几何查询**,语义相关性图引导探索 + 3D 多视图基础模型注册恢复精确 6-DoF 目标位姿,把 ImageNav 从"1m 内成功"推向精确定位。

---

## 📎 附录:文件夹内被筛除的非 ImageNav 文献

来源文件夹 `visual goal navigation` 中以下论文为基础设施/其他任务,未列入上表:

| 文件 | 类别 | 筛除原因 |
|---|---|---|
| Active Neural SLAM | 探索 / PointNav | 模块化探索策略,非图像目标 |
| DD-PPO (ICLR 2020) | PointNav / RL 基建 | 分布式 RL 训练框架 |
| Habitat / HM3D / MP3D | 仿真器与数据集 | 平台类,精读时作为环境背景 |
| GRU / ViT / Attention(ResNet) | 基础架构 | 通用网络组件 |
| FILM | 语言指令任务 | 属 VLN / 指令跟随方向 |

> 持续更新中;每篇的精读笔记将以单独文件加入本目录。
