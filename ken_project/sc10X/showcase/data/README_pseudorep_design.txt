06 pseudobulk DEG 伪重复设计说明
--------------------------------
现实约束: 每基因型仅 1 个生物学样本(n=1), 无法估计组间生物学方差, 不存在正式统计。
策略: 每样本每细胞类型细胞随机拆 3 份(seed=42) -> 每组 3 个伪重复单元; edgeR filterByExpr+TMM -> limma-voom -> 4 对比。
p 值解读: 来自样本内拆分, 系统性偏乐观(伪重复), 仅作探索性排序, 不可作最终结论;
  正式结论须补送生物学重复(n>=2/组)后在 00_config.R SAMPLE_TABLE 追加样本重跑。
阈值: DEG_FDR=0.05, DEG_LOGFC=0.25; direction: up_in_<group> 表示在组1/组2中升高。
对比设计: KO_vs_WT KO-vs-WT ; A1_Het_vs_WT A1_Het-vs-WT ; A1_Rescue_vs_KO A1_Rescue-vs-KO ; A1_Rescue_vs_A1_Het A1_Rescue-vs-A1_Het ; A1_Rescue_vs_WT A1_Rescue-vs-WT
注: A1_Rescue_vs_KO 为设计性挽救对比(回补库 vs KO 背景); 勘误后 genotype KO = 原 A1-Het 文库。
