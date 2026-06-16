---
title: "Context-Aware Hydrophobicity Modeling: HydroMap and FastHydroMap"
title_zh: 上下文感知的疏水性建模：HydroMap 和 FastHydroMap
authors: "Lobo, S., Najafi, S., Shea, J.-E., Shell, M. S."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.07.730647v1.full.pdf"
tags: ["query:mdd-regen"]
score: 6.0
evidence: 从蛋白表面上下文预测疏水性，可用于明胶基材料特性分析。
tldr: 传统疏水性尺度未考虑表面集体溶剂响应，直接计算去润湿自由能(Fdewet)耗时长。本研究从短期全原子模拟中提取局部水结构特征与势能，训练HydroMap预测残基级Fdewet，并构建图神经网络FastHydroMap免去溶剂模拟。模型在α-突触核蛋白纤维、钙调蛋白和Protein G上捕获了上下文依赖疏水性变化，揭示隐藏结合位点及折叠动态。Fdewet因此成为廉价描述符，可快速评分界面相互作用与动态过程。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统序列疏水性尺度忽略溶剂化集体效应，直接分子模拟计算Fdewet虽准确但速度过慢，限制实际应用。
method: 从廉价全原子模拟提取水结构签名和残基-水势能作为特征，训练HydroMap预测Fdewet；基于其输出训练GNN得到快速代理FastHydroMap，无需溶剂模拟。
result: 模型在多个蛋白体系中展示上下文敏感疏水性：识别纤维隐藏结合位点、钙调蛋白Ca2+结合时疏水性重分布、追踪蛋白G折叠轨迹。
conclusion: HydroMap与FastHydroMap使Fdewet成为计算廉价、物理准确的疏水性描述符，可用于界面预测、材料设计与动态过程分析。
---

## 摘要
疏水性支配着从蛋白质-蛋白质相互作用到纳米材料组装等广泛的现象，并且可以通过分子或表面的去润湿自由能（Fdewet）得到严格量化。然而，疏水性仍被广泛视为氨基酸身份的可加和性质，掩盖了水的响应是表面的集体性质这一事实，该性质由曲率、化学图案和邻近残基所塑造。通过专门的分子模拟直接计算Fdewet可以捕捉这种集体行为，但速度极慢，从而使广泛使用的、已有数十年历史的基于序列的疏水性标度得以沿用，这些标度忽略了溶剂化的物理学。在这里，我们展示了残基水平的Fdewet可以从一组紧凑的局部水特征（水结构特征和残基-水势能）中预测，这些特征是从一个简短且计算成本低廉的全原子模拟中提取的。我们将这一见解嵌入到两个模型中：HydroMap，它直接从水特征预测Fdewet；以及FastHydroMap，一个计算成本低廉的图神经网络代理模型，该模型在HydroMap上训练而成，无需溶剂模拟。HydroMap和FastHydroMap捕捉到了经典仅基于序列的疏水性标度所遗漏的上下文依赖的疏水性。我们在三个蛋白质系统中展示了这一点：在α-突触核蛋白淀粉样纤维上，强去润湿界面与未指派的肽密度对齐，揭示了隐藏的结合位点；在钙调蛋白中，疏水性在Ca2+结合时重新分布；对于蛋白G，时间分辨的疏水性变化追踪了折叠轨迹。总之，这些模型使Fdewet成为蛋白质、膜和其他表面的一种计算成本低廉的描述符，从而能够为材料设计进行快速评分，并为蛋白质折叠等动态疏水介导的过程提供时间分辨的视图。

意义声明：疏水性，即表面排斥水的倾向，驱动着蛋白质如何折叠以及分子如何相互识别。几十年来，它被广泛视为氨基酸或化学基团的固定属性，但实际上水响应的是表面的整体形状和化学性质（例如蛋白质所呈现的），而不是其孤立组分的。通过分子模拟测量这种集体响应是严格的，但速度极慢。我们展示了它可以从一组描述表面附近水结构和相互作用的紧凑特征中推断出来，并利用这一见解构建了能够快速并以残基分辨率预测疏水性的模型，从而使基于物理的疏水介导相互作用的实用设计成为可能。

## Abstract
Hydrophobicity governs a vast range of phenomena, from protein-protein interactions to nanomaterial assembly, and can be rigorously quantified by the dewetting free energy (Fdewet) of a molecule or surface. However, hydrophobicity remains widely treated as an additive property of amino acid identity, obscuring the fact that waters response is a collective property of the surface, shaped by curvature, chemical patterning, and neighboring residues. Direct calculation of Fdewet via specialized molecular simulations captures this collective behavior but is prohibitively slow, leaving in place broadly-used, decades-old sequence-based hydropathy scales that neglect the physics of solvation. Here we show that residue-level Fdewet can be predicted from a compact set of local water features (water structural signatures and residue-water potential energy) extracted from a brief and inexpensive all-atom simulation. We embed this insight in two models: HydroMap, which predicts Fdewet directly from water features, and FastHydroMap, a computationally inexpensive graph neural network surrogate trained on HydroMap that requires no solvent simulation. HydroMap and FastHydroMap capture context-dependent hydrophobicity that classical, sequence-only hydropathy scales miss. We demonstrate this across three protein systems: on an -synuclein amyloid filament, strongly dewetting interfaces align with unassigned peptide densities, revealing hidden binding sites; in calmodulin, hydrophobicity redistributes upon Ca2+ binding; and for Protein G, time-resolved hydrophobicity changes track the folding trajectory. Together, these models make Fdewet a computationally inexpensive descriptor for proteins, membranes, and other surfaces, enabling rapid scoring for materials design and a time-resolved view of dynamic hydrophobic-mediated processes such as protein folding.

Significance StatementHydrophobicity, the tendency of surfaces to expel water, drives how proteins fold and how molecules recognize one another. For decades, it has widely been treated as a fixed property of an amino acid or chemical group, but water actually responds to the collective shape and chemistry of a surface, such as that presented by a protein, not to its components in isolation. Measuring this collective response from molecular simulation is rigorous but prohibitively slow. We show that it can instead be inferred from a compact set of features describing water structure and interactions near a surface, and we use this insight to build models that predict hydrophobicity rapidly and at residue resolution, enabling practical, physically grounded design of hydrophobic-mediated interactions.