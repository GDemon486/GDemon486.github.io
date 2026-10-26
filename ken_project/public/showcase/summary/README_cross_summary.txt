08 cross-dataset summary (SIRT6 KO vs WT), two layers
----------------------------------------------------
Layer A (Global, showcase sec 6), unit order (MEF adjacent):
  sc_10x Global -> GSE109280 (MEF) -> GSE28585 (MEF array) -> GSE13207 (MEF array)
  -> GSE64642 early (hMSC) -> GSE64642 late (hMSC).
Layer B (celltype, showcase sec 7), 15 units = 10 sc_10x cell types (no TA Cells:
  KO sample had <30 cells in 06; Global excluded as it is layer A) + the same 5 public units.
Pathway heatmaps are ANCHORED on sc_10x:
  A: top20 terms of sc_10x Global per kind/direction (rows), cells = -log10(padj) in every unit;
  B: terms enriched in >=2 sc_10x cell types (top30), cells shown for all 15 units.
  grey = not enriched (padj>=0.05 or absent) in that unit.
Gene alignment: GSE64642 (human) mapped to mouse orthologs by Title-case rule (approximate);
  KEGG ids stripped of species prefix (hsa/mmu -> digits).
Significance: direction column (up_in_KO/up_in_WT); sc_10x p-values are pseudoreplicate-based
  (exploratory); public bulk formal/array-main per their own 06 designs.
UpSet: bitmask enumeration of all non-empty intersections, top 15 combos shown.
Outputs: Summary_* (layer A), CT_* (layer B), shared_DEGs_* wide tables (>=2 units).
