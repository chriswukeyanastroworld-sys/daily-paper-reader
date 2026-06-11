---
title: A Computational Framework for Domain Insertion into Type IV Pili for Bacterial Display and Living Material Assembly
title_zh: 将结构域插入IV型菌毛的计算框架用于细菌展示和活性材料组装
authors: "Tesoriero, R. F., Harris, N. E., Suggs, O. D., Ajo-Franklin, C. M."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.731259v1.full.pdf"
tags: ["query:mdd-regen"]
score: 6.0
evidence: 通过细菌菌毛工程的计算设计方法开展活材料设计，与可持续生物基材料开发方向相符
tldr: 细菌表面展示系统宿主范围窄，IV型菌毛（TFP）普遍保守但展示潜力未挖掘。本研究开发计算框架预测主要菌毛蛋白稳定展示插入位点，以蓝细菌PilA1验证。融合SpyCatcher003的细胞悬浮水平较C端展示提升8倍，增大货物仍改善TFP组装；实现SpyTag003蛋白共价连接，活材料装载量提高四倍且无损材料性质。该框架为TFP工程和跨物种可编程表面展示提供通用方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有细菌表面展示系统宿主范围窄，限制跨物种应用；IV型菌毛（TFP）普遍保守，但展示潜力未被挖掘。
method: 利用AlphaFold3分析PilA1单体和多聚体，识别非界面溶剂可及柔性位点，并测试SpyCatcher003融合。
result: 融合菌株细胞悬浮水平较C端展示提高8倍，增大货物仍改善TFP组装；实现SpyTag003蛋白共价连接，活材料装载量提升4倍且无损材料性质。
conclusion: 这项工作为IV型菌毛工程提供了预测性计算框架，并开启了在广泛细菌物种中进行可编程表面展示的大门。
---

## 摘要
细菌表面结构已实现多种展示系统，在生物技术领域产生广泛影响，但其狭窄的宿主范围限制了它们在多种物种中的应用。相反，IV型菌毛（TFP）是存在于各种细菌中的普遍且结构保守的附属结构，但很少被探索用于展示。在此，我们描述了一个计算框架，用于预测主要菌毛蛋白中可行的插入位点，以实现稳定的TFP介导展示，并将其应用于蓝细菌Synechocystis sp. PCC 6803的主要菌毛蛋白PilA1，以便共价结合到活性材料上。通过分析AlphaFold3生成的PilA1单体以及已知的多聚TFP结构，我们的流程识别了非界面、溶剂可及且灵活的位点，以进行最佳的PilA1展示。我们使用全长和截短的SpyCatcher003在两种不同的表达水平下探测这些位点。我们发现，表达这些PilA1-SpyCatcher003融合蛋白的细胞比之前的C端PilA1展示平台维持高达8倍水平的细胞悬浮，表明尽管货物大小增加了两倍以上，TFP组装仍然得到改善。此外，我们在工程菌株中验证了SpyCatcher003的反应性，使得含有SpyTag003的蛋白质能够共价附着在Synechocystis表面。最后，我们利用这种共价图案化实现了Synechocystis在活性材料中加载量增加四倍，而不影响其粘弹性或机械性能。总之，这项工作为TFP工程提供了一个预测框架，并开启了在广泛的细菌物种中进行可编程表面展示的大门。

## Abstract
Bacterial surface structures have enabled display systems with broad impact across biotechnology, but their narrow host range limits their deployment into diverse species. Conversely, Type IV Pili (TFP) are ubiquitous, structurally conserved appendages found across bacteria, but have been minimally explored for display. Here, we describe a computational framework for predicting viable insertion sites in major pilins for stable TFP-mediated display, which we apply to the major pilin PilA1 of the cyanobacterium Synechocystis sp. PCC 6803 to enable covalent binding to living materials. By analyzing an Alphafold3-generated PilA1 monomer alongside known multimeric TFP multimers, our pipeline identifies non-interfacial, solvent-accessible, and flexible sites for optimal PilA1 display. We probe these sites with both full-length and truncated SpyCatcher003 at two different expression levels. We show that cells expressing these PilA1-SpyCatcher003 fusions maintain up to 8-fold higher levels of cell suspension than previous C-terminal PilA1 display platforms, suggesting improved TFP assembly despite more than a two-fold increase in cargo size. Additionally, we validate SpyCatcher003 reactivity across the engineered strains, enabling covalent attachment of SpyTag003-containing proteins on the Synechocystis surface. Lastly, we utilize this covalent patterning to achieve a four-fold increase in Synechocystis loading into a living material without compromising its viscoelastic or mechanical properties. Taken together, this work provides a predictive framework for TFP engineering, and opens the door towards programmable surface display across the breadth of bacterial species.