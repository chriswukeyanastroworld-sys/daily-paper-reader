---
title: "Implicitly Guided Design with PropEn: Match your Data to Follow the Gradient"
title_zh: 隐式引导设计方法PropEn：匹配数据以跟随梯度
authors: "Natasa Tagasovska, Vladimir Gligorijevic, Kyunghyun Cho, Andreas Loukas"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=dhFHO90INk"
tags: ["query:mdd-regen"]
score: 4.0
evidence: 面向数据稀缺场景的引导设计框架，可应用于数据稀缺的可持续材料设计。
tldr: 针对传统引导设计模型依赖大数据的局限，PropEn通过匹配样本与属性更好的相似样本来隐式指明改进方向，无需训练判别器。在多个科学设计任务中，该方法在数据有限时表现优越，为资源受限的可持续设计等场景提供了新思路。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1196, \"height\": 692, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1254, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1395, \"height\": 264, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1402, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1363, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1282, \"height\": 354, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1430, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 655, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1441, \"height\": 234, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-dhfho90ink/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1441, \"height\": 421, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1436, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 197, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1456, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 875, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1458, \"height\": 2436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-dhfho90ink/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1457, \"height\": 2393, \"label\": \"Table\"}]"
motivation: 科学设计常面临数据有限与复杂景观，传统数据驱动模型效率低。
method: 通过匹配每个样本与属性更佳的相似样本，构建增强数据集以隐式引导优化。
result: 在有限数据下，多个设计任务中表现优于传统方法。
conclusion: 提供了一种无需大数据的隐式引导设计框架，广泛适用于科学发现。
---

## Abstract
Across scientific domains, generating new models or optimizing existing ones while meeting specific criteria is crucial. Traditional machine learning frameworks for guided design use a generative model and a surrogate model (discriminator), requiring large datasets. However, real-world scientific applications often have limited data and complex landscapes, making data-hungry models inefficient or impractical. We propose a new framework, PropEn, inspired by ``matching'', which enables implicit guidance without training a discriminator. By matching each sample with a similar one that has a better property value, we create a larger training dataset that inherently indicates the direction of improvement. Matching, combined with an encoder-decoder architecture, forms a domain-agnostic generative framework for property enhancement. We show that training with a matched dataset approximates the gradient of the property of interest while remaining within the data distribution, allowing efficient design optimization. Extensive evaluations in toy problems and scientific applications, such as therapeutic protein design and airfoil optimization, demonstrate PropEn's advantages over common baselines. Notably, the protein design results are validated with wet lab experiments, confirming the competitiveness and effectiveness of our approach. Our code is available at https://github.com/prescient-design/propen.

---

## 论文详细总结（自动生成）

好的，作为资深学术论文分析助手，以下是对论文《Implicitly Guided Design with PropEn: Match your Data to Follow the Gradient》的结构化深入总结。

### 1. 论文的核心问题与整体含义

*   **核心问题**：在许多科学领域（如材料科学、药物设计），研究人员需要通过迭代优化来改进某个设计的特定属性（如蛋白质的结合亲和力、机翼的升阻比）。传统机器学习引导设计的方法（“显式引导”）通常依赖两个模型：一个生成新设计的生成模型，一个预测属性好坏的判别器/代理模型。然而，这些模型往往是“数据饥渴”的，需要大量标注数据才能可靠工作，这与现实世界中数据稀缺且获取成本高昂的现状相矛盾。
*   **整体含义**：本文挑战了这一范式，提出了一种名为 **PropEn (Property Enhancer)** 的全新“隐式引导”框架。其核心思想是，无需单独训练一个判别器，而是通过对现有数据进行“匹配”，构造出一个内在地指示改进方向的增强数据集，从而在小数据场景下也能实现有效的设计优化。这为数据匮乏的科学发现提供了一种更高效、更鲁棒的新路径。

### 2. 论文提出的方法论

*   **核心思想**：从因果推断的“匹配”方法中汲取灵感，将“拥有更优属性值的样本”视为“实验组”，将其与“属性值较低的相似样本”（对照组）进行配对。这样形成的配对数据集本身就蕴含了从“优化前”到“优化后”的演进方向。

*   **关键技术细节与流程**：
    1.  **匹配数据集**：给定初始数据集 `D = {(x_i, y_i)}`（`x` 为设计，`y` 为目标属性），PropEn 构建一个匹配数据集 `M`。`M` 中的每个元素 `(x, x')` 满足：`x'` 是 `x` 的一个近邻（`||x' - x||_2 ≤ Δx`），并且其属性值更好（`0 < g(x') - g(x) ≤ Δy`）。这极大地扩充了训练数据量（复杂度可达 `O(n^2)`）。
    2.  **隐式梯度近似**：利用匹配好的数据集 `M`，训练一个编码器-解码器网络 `f_θ`，优化目标是最小化“匹配重建损失”`ℓ(f_θ(x), x')`（如均方误差）。**理论证明（定理1）** 表明，该优化过程的最优解 `f*` 会学习到一个与目标属性函数 `g(x)` 的梯度 `∇g(x)` 同向的向量场，即 `f*(x)` 的输出方向近似指向属性提升最快的方向。
    3.  **隐式引导优化**：训练完成后，从任意初始设计 `x_0` 开始，可迭代地进行自回归优化：`x_t = f_θ(x_{t-1})`，直到收敛到不动点 `f_θ(x_t) = x_t`。整个过程无需显式评估属性预测器，而是通过模型学到的“方向”直接推进。**理论证明（定理2）** 还保证，生成的候选设计的概率密度不会显著低于原始训练数据的分布，从而避免了生成不合理或“出界”的设计。

*   **算法变体**：论文探讨了不同变体，例如是否同时重建属性值 (`xy2xy`)，以及是否加入一个将输出拉近原始输入的混合正则化项 (`mixup`)，以提高保守性。

### 3. 实验设计

*   **数据集/场景**：
    *   **合成数据 (Toy problems)**：2D 的“风车”和“8-高斯”数据集，通过随机等距嵌入扩展至高维 (`d ∈ {10, 50, 100}`)，考验模型在高维空间的能力。目标属性为基于核密度估计（KDE）的对数似然。
    *   **工程优化 (Airfoil optimization)**：NACA 4-位数系列翼型数据，目标是在保持形状合理性的前提下，优化翼型的升阻比 (Cl/Cd)。升阻比由深度学习模拟器 NeuralFoil 计算。
    *   **治疗性蛋白设计 (Therapeutic protein design)**：针对三种抗原（包括HER2）的抗体序列数据，目标是优化抗体的结合亲和力（pKD）。蛋白设计结果包含了通过表面等离子共振（SPR）实验进行的**湿实验验证**，是本文的一大亮点。

*   **Benchmark 与对比方法**：
    *   **合成数据与翼型实验**：
        *   与 **显式引导 (Explicit guidance)** 基线对比，该基线使用相同架构的自编码器（AE）加上一个在潜空间进行引导的多层感知机（MLP）判别器。
        *   翼型实验还额外对比了扩散模型（Diffusion Models）。
    *   **蛋白设计实验**：与多个最先进方法对比，包括 **Walk-Jump Sampler**、 **LaMBO**（引导式）以及两种基于 **扩散模型** 的方法（一种为普通扩散，另一种为加入引导的扩散）。

*   **评估指标**：根据任务不同，指标包括 **改进率**（改进样本占总样本比例）、**对数似然值**（衡量样本是否在分布内）、**唯一性**（生成设计中的独特比例）、**新颖性**（不在训练集中的比例）以及抗体实验中的**结合率**和**亲和力提升值**。

### 4. 资源与算力

*   论文**未明确说明**其所使用的具体GPU型号、数量以及总训练时长。仅在附录B.6给出了部分实验的超参数，如训练周期数（Toy: 500 epochs, Airfoil: 1000 epochs, Proteins: 300 epochs）和批次大小（batch size），但未提及其背后的计算资源消耗。

### 5. 实验数量与充分性

*   **实验数量**：实验较为丰富，共计三大类、十余组实验：
    *   **合成实验**：2种形状 × 3-4种维度 × 2种样本量 × 4种PropEn变体 ≈ 数十种设定，并进行了10次重复实验。
    *   **翼型实验**：不同训练集大小，并针对匹配阈值 `Δx`, `Δy` 进行了详细的**消融研究**。
    *   **蛋白实验**：针对3种抗原的8个种子设计，与4个强大的基线方法进行对比，并产生总计超过300个设计进行**湿实验验证**。
*   **充分性与客观性**：实验设计较为充分且客观。
    *   **覆盖全面**：从合成数据到真实世界的工程和生命科学问题，从连续数据到离散序列，验证了方法的通用性。
    *   **对比公平**：与当前主流方法（显式引导、扩散模型等）进行了直接比较，且在蛋白设计任务中连接了昂贵的湿实验，结果极具说服力。
    *   **消融严谨**：对PropEn的多个变体和匹配阈值进行了消融，有助于理解各组件的贡献。

### 6. 论文的主要结论与发现

*   **隐式引导有效且鲁棒**：PropEn能在不训练任何判别器的情况下，有效引导设计向属性更优的方向进化。尤其是在**有限数据和面对分布外（OOD）初始设计**时，其鲁棒性显著优于传统的显式引导方法。
*   **理论保证实用**：证明了该方法能够隐式地近似目标属性的梯度，同时保证生成样本大概率落在数据分布内，这为生成设计的合理性提供了保障。
*   **真实世界任务表现优越**：在抗体优化的湿实验中，PropEn以最高的结合率（94.6%）和最高的亲和力改进比例（34.4%）超越了所有基线方法，证明其在小数据、高风险的生物医药领域有巨大潜力。

### 7. 优点

*   **方法论创新**：巧妙地将因果推断中的“匹配”概念引入生成式设计，开辟了一条无需独立预测模型的“隐式引导”新路径，是方法学上的重要贡献。
*   **坚实的理论基础**：提供了两个定理，分别证明了对属性梯度的近似能力和生成设计的分布内概率下界，使方法不再是“黑箱”。
*   **端到端且领域无关**：框架简单，仅需编码器-解码器架构，可应用于连续和离散数据，域适应性强。
*   **实验验证说服力强**：包含了罕见的**湿实验（in vitro）验证**，直接证明了方法在制药领域的实际竞争力，这是纯计算模拟无法比拟的优势。

### 8. 不足与局限

*   **匹配过程的计算开销**：论文承认，匹配步骤的计算复杂度为 `O(n^2)`，当数据集规模扩大时会产生可观的额外计算负担，尽管当前聚焦于小数据场景。
*   **距离度量选择依赖领域知识**：`Δx` 的设定需要选择合适的相似度度量（如欧氏距离、编辑距离），这要求研究者对特定应用场域有一定理解，可能会引入一定的领域偏见。
*   **多属性优化未解决**：当前框架针对单一属性进行优化，但科学设计常需折中多个甚至相互冲突的属性，论文指出这是未来工作方向。
*   **缺乏计算资源报告**：未提供任何实验的算力详情（GPU型号、运行时间），难以评估其整体计算效率和在不同硬件条件下的可复现性。

（完）
