---
title: Reconstructing living materials as a computable design space with multi-agent reasoning
title_zh: 利用多智能体推理将活体材料重构为可计算设计空间
authors: "Xiao, Y., Zeng, X., Yang, Z., Gu, J., Lu, Y., Wang, Y., Wen, H., Chen, M., Huang, Z., Hu, J., Liu, J., Sha, C., Xie, J., Li, H., Zhu, X., Zheng, S., Zhang, J., Zong, W., He, Z., Xu, Y., Zhou, X., Li, F., Liu, H., He, Q., Liu, L., Yu, Z."
date: 2026-06-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.15.705954v2.full.pdf"
tags: ["query:mdd-regen"]
score: 6.0
evidence: 多智能体框架为活体材料创建可计算设计空间，支持生物基材料的材料驱动设计
tldr: "活体材料设计涉及细胞、基质、工艺和评估条件的复杂耦合，传统人工智能方法难以处理。为此，本文提出LiveMat，一种多智能体推理框架，将非结构化文献转化为可计算设计空间。它标准化了34,215条活体材料记录，并整合了16,769种微生物和17,446种聚合物，构建了知识图谱。通过基准测试发现跨域特征集成是主要瓶颈，LiveMat采用约束分解、出处感知提取、一致性检查和专家锚定排序等机制克服了这一限制。在伤口愈合前瞻性任务中，该框架优先出四组分设计，取得了最先进的体内性能。这为可解释、循证的活体材料发现建立了可扩展的基础设施。"
source: biorxiv
selection_source: fresh_fetch
motivation: 活体材料功能由细胞、基质、工艺和评估条件的上下文依赖耦合决定，现有AI难以建模其涌现行为。
method: 提出LiveMat多智能体框架，从文献提取并标准化3.4万条记录，构建微生物-聚合物知识图谱，结合约束分解、出处感知提取、一致性检查和专家锚定排序实现跨域推理。
result: 跨五个大语言模型基准测试表明，跨域特征集成是活体材料推理的主要瓶颈，LiveMat成功克服；在伤口愈合前瞻性任务中，优先出的四组分设计实现了最先进的体内性能。
conclusion: LiveMat通过多智能体推理与知识图谱，为可解释、循证的活体材料发现提供了可扩展基础设施。
---

## 摘要
人工智能正越来越多地用于加速科学发现，但大多数成功框架都运行在定义明确的分子、蛋白质或材料空间内。活体材料带来了更艰巨的计算难题，因为其功能源于细胞、基质、制造过程和评估条件之间上下文依赖的耦合。本文介绍 LiveMat，一个多智能体推理框架，它将非结构化文献转化为活体材料的可计算设计空间。LiveMat 对 34,215 条活体材料记录进行了标准化，将 16,769 个微生物条目和 17,446 个聚合物条目集成到一个知识图谱中，连接了活体组分、非生物基质、功能输出、评估上下文和性能指标。在五个大型语言模型上的基准测试表明，活体材料推理的主要限制在于跨领域特征整合，而非粗粒度分类。LiveMat 通过约束分解、来源感知抽取、一致性检查和专家锚定排序克服了这一局限。在一项前瞻性伤口愈合任务中，它优先考虑了一种四组分设计，展现出最先进的体内性能，为可解释、基于证据的活体材料发现建立了可扩展的基础设施。

## Abstract
Artificial intelligence is increasingly used to accelerate scientific discovery, but most successful frameworks operate within well-defined molecular, protein or materials spaces. Living materials present a more formidable computational problem because functions emerge from context dependent coupling among cells, matrices, fabrication processes and evaluation conditions. Here we introduce LiveMat, a multi-agent reasoning framework that transforms unstructured literature into a computable design space for living materials. LiveMat standardizes 34,215 living material records, integrating 16,769 microorganism and 17,446 polymer entries into a knowledge graph linking living components, abiotic matrices, functional outputs, evaluation contexts and performance metrics. Benchmarking across five large language models shows that living material reasoning is limited mainly by cross-domain feature integration rather than coarse classification. LiveMat overcomes this limitation through constraint decomposition, provenance-aware extraction, consistency checking and expert-anchored ranking. In a prospective wound-healing task, it prioritizes a four-component design with state-of-the-art in vivo performance, establishing a scalable infrastructure for interpretable, evidence-grounded living material discovery.