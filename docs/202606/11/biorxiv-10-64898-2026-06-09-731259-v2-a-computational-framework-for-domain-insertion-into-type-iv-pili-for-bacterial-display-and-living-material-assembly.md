---
title: A Computational Framework for Domain Insertion into Type IV Pili for Bacterial Display and Living Material Assembly
title_zh: 细菌 IV 型菌毛结构域插入的计算框架：用于细菌展示与活性材料组装
authors: "Tesoriero, R. F., Harris, N. E., Suggs, O. D., Ajo-Franklin, C."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.731259v2.full.pdf"
tags: ["query:mdd-regen"]
score: 6.0
evidence: 通过细菌菌毛工程的计算设计方法开展活材料设计，与可持续生物基材料开发方向相符
tldr: 在生物技术中，细菌表面展示系统已广泛应用，但多数平台受宿主限制。IV型菌毛(TFP)普遍存在于细菌中，但作为展示工具开发不足。本研究建立计算框架，利用AlphaFold3预测主要菌毛蛋白PilA1中适合展示的插入位点，要求非界面、溶剂可及且柔性。实验表明，插入全长或截短SpyCatcher003的工程菌株悬浮性比C端展示高8倍，且保持反应性，能共价连接SpyTag003蛋白。最终将该蓝藻负载量提升4倍而不损害活体材料的机械性能，为TFP工程提供了预测框架，开启跨物种可编程表面展示的新途径，有望拓展至多种细菌。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有细菌展示平台局限于少数物种，IV型菌毛虽高度保守但缺乏工程化展示手段，限制其在多物种中的应用。
method: 利用AlphaFold3预测PilA1单体和TFP多聚体结构，识别非界面、溶剂可及、柔性位点，并插入SpyCatcher003进行测试。
result: 相较C端展示，工程菌株悬浮性提高8倍，且保持反应活性，可共价连接SpyTag003蛋白；蓝藻负载量提升4倍而不损害材料性能。
conclusion: 该框架为IV型菌毛展示提供预测性设计原则，成功在蓝藻中实现负载提升，推动活体材料组装和跨物种可编程展示。
---

## 摘要
细菌表面结构已赋能应用广泛的展示系统，但其宿主范围狭窄限制了它们在多种物种中的应用。相反，IV 型菌毛（TFP）广泛存在于细菌中、结构保守，但用于展示的研究甚少。在此，我们提出一种计算框架，用于预测主要菌毛蛋白中可实现稳定 TFP 介导展示的可行插入位点，并应用于蓝细菌集胞藻 PCC 6803 的主要菌毛蛋白 PilA1，以实现与活性材料的共价结合。通过分析 AlphaFold3 生成的 PilA1 单体以及已知的 TFP 多聚体，我们的流程识别出非界面、溶剂可及且柔性的位点，用于优化 PilA1 展示。我们在两个不同表达水平下，用全长和截短的 SpyCatcher003 探测这些位点。结果表明，表达这些 PilA1-SpyCatcher003 融合蛋白的细胞，其悬浮水平比以前的 C 端 PilA1 展示平台高出多达 8 倍，提示尽管货物尺寸增加了一倍以上，TFP 组装仍得到改善。此外，我们验证了工程菌株中 SpyCatcher003 的反应活性，使得含 SpyTag003 的蛋白质能够共价附着在集胞藻表面。最后，我们利用这种共价图案化，将集胞藻在活性材料中的负载量提高了四倍，且不影响其粘弹性或力学性能。综上所述，本工作为 TFP 工程提供了一个预测框架，并为在广泛的细菌物种中实现可编程表面展示打开了大门。

## Abstract
Bacterial surface structures have enabled display systems with broad impact across biotechnology, but their narrow host range limits their deployment into diverse species. Conversely, Type IV Pili (TFP) are ubiquitous, structurally conserved appendages found across bacteria, but have been minimally explored for display. Here, we describe a computational framework for predicting viable insertion sites in major pilins for stable TFP-mediated display, which we apply to the major pilin PilA1 of the cyanobacterium Synechocystis sp. PCC 6803 to enable covalent binding to living materials. By analyzing an Alphafold3-generated PilA1 monomer alongside known multimeric TFP multimers, our pipeline identifies non-interfacial, solvent-accessible, and flexible sites for optimal PilA1 display. We probe these sites with both full-length and truncated SpyCatcher003 at two different expression levels. We show that cells expressing these PilA1-SpyCatcher003 fusions maintain up to 8-fold higher levels of cell suspension than previous C-terminal PilA1 display platforms, suggesting improved TFP assembly despite more than a two-fold increase in cargo size. Additionally, we validate SpyCatcher003 reactivity across the engineered strains, enabling covalent attachment of SpyTag003-containing proteins on the Synechocystis surface. Lastly, we utilize this covalent patterning to achieve a four-fold increase in Synechocystis loading into a living material without compromising its viscoelastic or mechanical properties. Taken together, this work provides a predictive framework for TFP engineering, and opens the door towards programmable surface display across the breadth of bacterial species.