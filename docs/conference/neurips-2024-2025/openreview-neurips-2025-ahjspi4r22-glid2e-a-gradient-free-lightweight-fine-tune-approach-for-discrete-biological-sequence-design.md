---
title: "GLID$^2$E: A Gradient-Free Lightweight Fine-tune Approach for Discrete Biological Sequence Design"
title_zh: GLID^2E：一种用于离散生物序列设计的无梯度轻量级微调方法
authors: "Hanqun Cao, Haosen Shi, Chenyu Wang, Sinno Jialin Pan, Pheng-Ann Heng"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=AHjspi4R22"
tags: ["query:mdd-regen"]
score: 4.0
evidence: 用于生物序列设计的无梯度微调方法，可应用于可持续材料中交联酶的优化。
tldr: 针对生物序列设计中现有方法在离散优化时不稳定或计算成本高的问题，本文提出GLID^2E，一种基于强化学习的无梯度微调方法，通过扩散模型实现多目标序列设计。该方法在多个生物序列生成任务中表现了高效优化能力，为功能生物分子设计提供了实用工具。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ahjspi4r22/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1413, \"height\": 402, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1381, \"height\": 480, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1320, \"height\": 556, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1271, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1273, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 609, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 521, \"height\": 419, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 659, \"height\": 691, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 917, \"height\": 143, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ahjspi4r22/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 566, \"height\": 381, \"label\": \"Table\"}]"
motivation: 离散生物序列设计对工程有益，但现有优化方法在稳定性与效率上存在不足。
method: 采用强化学习微调扩散模型，无需梯度计算，实现稳定的离散序列多目标优化。
result: 在生物序列生成中展示高效多目标优化，超越现有方法。
conclusion: 为数据有限的生物序列设计提供了一种稳定且计算高效的微调策略。
---

## Abstract
The design of biological sequences is essential for engineering functional biomolecules that contribute to advancements in human health and biotechnology. Recent advances in diffusion models, with their generative power and efficient conditional sampling, have made them a promising approach for sequence generation. To enhance model performance on limited data and enable multi-objective design and optimization, reinforcement learning (RL)-based fine-tuning has shown great potential. However, existing post-sampling and fine-tuning methods either lack stability in discrete optimization when avoiding gradients or incur high computational costs when employing gradient-based approaches, creating significant challenges for achieving both control and stability in the tuning process.
To address these limitations, we propose GLID$^2$E, a gradient-free RL-based tuning approach for discrete diffusion models. Our method introduces a clipped likelihood constraint to regulate the exploration space and implements reward shaping to better align the generative process with design objectives, ensuring a more stable and efficient tuning process. 
By integrating these techniques, GLID$^2$E mitigates training instabilities commonly encountered in RL and diffusion-based frameworks, enabling robust optimization even in challenging biological design tasks. In the DNA sequence and protein sequence design systems, GLID$^2$E achieves competitive performance in function-based design while maintaining computational efficiency and a flexible tuning mechanism.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：设计具有特定功能的生物序列（如DNA增强子、热稳定蛋白）是蛋白质工程与合成生物学的核心任务。扩散模型虽能有效建模序列分布，但在数据有限、目标多指标且存在冲突的情况下，如何将预训练模型适配到具体的功能优化任务仍面临挑战。
- **核心问题**：现有方法存在明显的“权衡困境”。基于梯度的微调方法（如DRAKES）需要反向传播整个生成轨迹，计算和内存开销极大；而无梯度方法在离散空间中训练不稳定。这种权衡严重限制了上述方法在生物设计中的实用性。
- **整体含义**：论文旨在提出一种**轻量级、无梯度的强化学习微调框架**，以在保持计算效率的同时实现稳定高效的离散扩散模型优化，从而为功能驱动的生物序列优化提供实用解决方案。

### 2. 论文提出的方法论
- **核心思想**：将扩散模型的微调重新定义为**策略优化**问题。将生成过程视为智能体与环境的交互，仅对策略参数计算轻量级梯度，避免了通过完整轨迹进行反向传播。
- **关键技术细节**：
    - **截断似然约束 (Clipped Likelihood Constraint)**：
        - 摒弃传统的散度正则化，将合理性视为硬约束。利用预训练模型评估样本似然，仅允许在其高似然区域内探索。
        - 实现：通过校准集计算对数似然的均值 $\mu$ 和标准差 $\sigma$，设置阈值 $c = \mu - k\sigma$。修改奖励函数 $\tilde{r}(x) = r(x) + \beta \min\left( \frac{\log p_{prior}(x) - \mu}{\sigma} + k, 0 \right)$，对低于阈值的序列施加惩罚，从而避免生成不合理序列。
    - **奖励塑形 (Reward Shaping)**：
        - 解决标准强化学习中仅在序列完全生成后才给予奖励导致的信号稀疏问题。
        - 将采样过程建模为马尔可夫决策过程，采用势函数 $\Phi(s_t)$ 为中间步骤提供奖励。对于含 `MASK` 令牌的中间状态，通过蒙特卡洛抽样补全序列并预估奖励，使优化过程在早期即获得指导。
    - **基于PPO的策略优化**：
        - 采用混合参考策略 $\log \pi_{ref} = \eta \log \pi_{prior} + (1-\eta) \log \pi_{\theta}$ 作为“软锚”，平衡探索与先验保留。
        - 使用PPO的截断代理目标，结合广义优势估计和熵奖励，在不计算昂贵散度的情况下稳定更新策略。
- **算法流程**：整体构成一个集成了奖励塑形、似然惩罚和PPO更新的轻量级训练循环。

### 3. 实验设计
- **数据集与任务**：
    - **DNA设计**：使用约70万条200碱基对的增强子数据集，以Enformer架构作为奖励预言机预测活性。
    - **蛋白质设计**：使用基于PDB结构预训练的ProteinMPNN模型，以Megascale数据集训练的模型预测热力学稳定性（$\Delta\Delta G$）作为奖励。
- **基准方法**：对比了预训练扩散模型、条件采样方法（CG、SMC、TDS、CFG）、基于MCTS的PepTune以及基于梯度的微调方法DRAKES。
- **评估指标**：
    - **DNA**：功能（预测活性、ATAC染色质可及性）与自然度（3-mer相关性、对数似然）。
    - **蛋白质**：稳定性（预测ddG、稳定序列百分比）、结构天然度（自洽性RMSD、scRMSD<2百分比）以及综合的成功率。

### 4. 资源与算力
- **硬件配置**：所有实验均在**单张NVIDIA A40 GPU (20GB显存)** 上完成。为进行不同随机种子的并行运行，使用了多个GPU。
- **训练时长**：文中报告了每轮训练时间，所提方法GLID$^2$E为 **13.54 ± 0.04 秒/epoch**，而对比的梯度方法DRAKES为 **23.28 ± 0.14 秒/epoch**，实现了显著的效率提升。

### 5. 实验数量与充分性
- **实验数量**：共完成了约**6组核心实验**，包括：
    - 2个主要任务的全面对比实验（DNA与蛋白质设计）。
    - 2组消融实验（分别移除奖励塑形M1和似然约束M2）以验证核心模块贡献。
    - 2组超参数分析实验（截断比率 $k$ 和混合比率 $\eta$ 的影响）。
    - 此外，还包括序列多样性分析和训练时间对比。
- **充分性与客观性**：实验设计较为**充分**。对比了多个类别的SOTA方法，覆盖功能和自然度指标；消融实验清晰证实了两个创新组件的必要性；超参数分析揭示了方法性能的稳健区间，分析客观。

### 6. 论文的主要结论与发现
- GLID$^2$E在DNA增强子设计任务上取得**最优功能性能**，活性指标较梯度方法DRAKES提升30%，且计算效率显著更高。
- 在蛋白质稳定性设计任务上，GLID$^2$E取得**有竞争力的结果**（成功率76.7%），逼近甚至在某些指标上超越梯度方法。
- 消融实验证实，**奖励塑形对优化功能性至关重要**，而**截断似然约束则有效保持了生成序列的分布合理性**并防止了训练崩溃。
- 该框架成功在离散扩散模型的微调中平衡了**效率与稳定性**。

### 7. 优点
- **方法创新**：巧妙地将扩散模型微调转化为轻量级的RL策略优化，以截断似然约束替代昂贵的KL散度计算，想法新颖且实用。
- **计算高效**：无需求导通过完整轨迹，训练速度和内存占用均优于基于梯度的方法，部署门槛低。
- **性能卓越**：在多个基准测试上取得领先或极具竞争力的结果，尤其是在不牺牲太多自然度的情况下大幅提升DNA活性。
- **实验扎实**：包含充分的消融和超参数分析，细粒度地揭示了各组件的作用和方法的鲁棒性，分析深刻。

### 8. 不足与局限
- **理论保证缺失**：作为一种启发式RL方法，缺乏像DRAKES那样的理论收敛保证，微调过程的稳定性依赖于超参数调节。
- **生物验证局限**：所有评估均基于计算机模拟，尚未通过湿实验验证生成序列的真实体内活性或稳定性。
- **任务覆盖范围**：当前仅在DNA增强子和单体蛋白稳定性任务上验证，其在更复杂的生物系统（如酶-底物结合、抗体设计）上的泛化能力有待检验。
- **自然度偏差风险**：在DNA任务中，3-mer相关性指标较低，表明该方法可能过度偏离了传统序列统计学规律，其生物真实意义需进一步探讨。

（完）
