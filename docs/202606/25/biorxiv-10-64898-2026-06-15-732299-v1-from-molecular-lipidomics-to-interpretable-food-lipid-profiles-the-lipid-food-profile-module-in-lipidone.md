---
title: "From molecular lipidomics to interpretable food lipid profiles: the Lipid Food Profile module in LipidOne"
title_zh: 从分子脂质组学到可解读的食品脂质谱：LipidOne中的Lipid Food Profile模块
authors: "Frongia Mancini, D., Alabed, H. B. R., Pellegrino, R. M."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732299v1.full.pdf"
tags: ["query:mdd-regen"]
score: 7.0
evidence: 提供一种脂质组学数据分析工具，可用于表征三文鱼基材料的脂质谱。
tldr: LC/MS食品脂质组学提供详细脂质分子信息，但数据难以直接解释为食品品质指标。Lipid Food Profile模块采用计算机模拟水解，重构酰基链并保留脂质类信息，生成食品相关脂质指数。在三个已发表数据集中，LFP不仅复现了原有结论，还提供了饱和度平衡、氧化稳定性等额外食品导向信息。该模块为复杂脂质组学数据增添了解释层，支持食品成分、加工效应及溯源分析。
source: biorxiv
selection_source: fresh_fetch
motivation: LC/MS 食品脂质组学数据难以直接提供食品品质、加工和真实性相关的可解释指标。
method: LFP模块应用计算机模拟水解，从LC/MS数据重建脂质链并保留脂类来源，继而计算脂质品质、饱和度平衡、氧化稳定性等指数。
result: 在微藻、鱼子和骆驼奶数据集中，LFP均复现原有结论，并额外揭示饱和度平衡、氧化稳定性等食品品质信息，结果以更少指数呈现。
conclusion: LFP为LC/MS食品脂质组学提供解释层，补充传统脂肪酸分析，并可通过LipidOne平台免费访问。
---

## 摘要
基于LC/MS的食品脂质组学提供了关于完整脂质分子的详细信息，但所得数据集往往难以转化为对食品质量、加工、营养谱和真实性评估直接有用的概念。在此，我们介绍Lipid Food Profile（LFP），这是LipidOne平台的一个模块，旨在将经注释的LC/MS脂质组学数据转化为可解读的与食品相关的脂质指数。LFP采用计算机模拟水解策略，从完整的脂质分子中重建酰基链、烷基链和烯基链，同时保留其脂质类别来源。然后将重建的信息归纳为与食品脂质质量、组成平衡、omega平衡、氧化稳定性、链重塑和醚连接链贡献相关的指数类别。

利用三个已发表的食品脂质组学数据集评估了LFP的解读价值，这些数据集涉及不同的分析问题：X射线诱导的普通小球藻脂质重塑、鲻鱼干鱼籽的空间脂质异质性以及骆驼奶的地理来源评估。在这些案例研究中，LFP重现了原始脂质组学研究的主要结论，包括与处理相关的脂质重塑、干鱼籽的内外层差异以及骆驼奶的地区差异。重要的是，LFP将这些发现重新组织为少数几个面向食品的指数，提供了关于饱和平衡、氧化敏感性、链架构和分类潜力的额外信息。

总体而言，LFP为基于LC/MS的食品脂质组学提供了一个解读层，补充了传统的脂肪酸分析和基于分子物种的解读。通过将复杂的脂质组学表格转化为结构化的脂质指数谱，该模块可支持对食品成分、加工效应、脂质质量和探索性溯源应用进行更易获取且化学意义明确的分析。LFP可通过LipidOne网络平台（LipidOne.eu）免费获取。

亮点
• Lipid Food Profile将LC/MS食品脂质组学转化为可解读的脂质指数。
• 该工作流程在不进行化学水解的情况下保留链和脂质类别信息。
• 已发表的案例研究表明，LFP重现并扩展了先前的解读。
• LFP支持食品质量、加工以及探索性来源/真实性评估。
• 该模块补充了传统的脂肪酸分析和分子脂质组学。

## Abstract
LC/MS-based food lipidomics provides detailed information on intact lipid species, but the resulting datasets are often difficult to translate into concepts directly useful for food quality, processing, nutritional profiling and authenticity assessment. Here, we present Lipid Food Profile (LFP), a module of the LipidOne platform designed to convert annotated LC/MS lipidomics data into interpretable food-relevant lipid indices. LFP applies an in silico hydrolysis strategy to reconstruct acyl, alkyl and alkenyl chains from intact lipid species while preserving their lipid-class origin. The reconstructed information is then summarized into index categories related to food lipid quality, compositional balance, omega balance, oxidative stability, chain remodelling and ether-linked chain contribution.

The interpretative value of LFP was evaluated using three published food lipidomics datasets addressing different analytical questions: X-ray-induced lipid remodelling in Chlorella vulgaris, spatial lipid heterogeneity in Mugil cephalus bottarga, and geographical-origin assessment of camel milk. Across these case studies, LFP recovered the main conclusions of the original lipidomics investigations, including treatment-associated lipid remodelling, inner-outer layer differences in bottarga and regional variation in camel milk. Importantly, LFP reorganized these findings into a smaller number of food-oriented indices, providing additional information on saturation balance, oxidative susceptibility, chain architecture and classification potential.

Overall, LFP provides an interpretative layer for LC/MS food lipidomics that complement conventional fatty-acid analysis and molecular-species-based interpretation. By translating complex lipidomic tables into structured lipid index profiles, the module may support more accessible and chemically meaningful analysis of food composition, processing effects, lipid quality and exploratory traceability applications. LFP is freely accessible through the LipidOne web platform (LipidOne.eu).

HighlightsO_LILipid Food Profile translates LC/MS food lipidomics into interpretable lipid indices.
C_LIO_LIThe workflow preserves chain and lipid-class information without chemical hydrolysis.
C_LIO_LIPublished case studies show that LFP recovers and extends previous interpretations.
C_LIO_LILFP supports food quality, processing and exploratory origin/authenticity assessment.
C_LIO_LIThe module complements conventional fatty-acid analysis and molecular lipidomics.
C_LI