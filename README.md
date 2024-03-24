# hse_hw3_chromhmm

## Colab
[ссылка](https://colab.research.google.com/drive/1XXUbdWo--8thwTWiSKGfCPAcDKWm8bnV?usp=sharing)

## Гистоновые Метки
File | Name
--- | ---
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k27acStdAlnRep1.bam | H3K27ac.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k27me3StdAlnRep1.bam | H3K27me3.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k36me3StdAlnRep1.bam | H3K36me3.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k79me2StdAlnRep1.bam | H3K79me2.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k09me3StdAlnRep1.bam | H3K9me3.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH4k20me1StdAlnRep1.bam | H4K20me1.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k9acStdAlnRep1.bam | H3K9ac.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k4me1StdAlnRep1.bam  | H3K4me1.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k4me2StdAlnRep1.bam  | H3K4me2.bam
http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneH1hescH3k4me3StdAlnRep1.bam  | H3K4me3.bam


## cellmarkfiletable.txt

Клеточная линия | Гистоновая метка | Файл с гистоновой меткой | Файл с контролем
--- | --- | --- | ---
H1hesc | H3K9me3 | H3K9me3.bam | Control.bam
H1hesc | H3K4me1 | H3K4me1.bam | Control.bam
H1hesc | H3K27me3 | H3K27me3.bam | Control.bam
H1hesc | H3K27ac | H3K27ac.bam | Control.bam
H1hesc | H4K20me1 | H4K20me1.bam | Control.bam
H1hesc | H3K4me2 | H3K4me2.bam | Control.bam
H1hesc | H3K36me3 | H3K36me3.bam | Control.bam
H1hesc | H3K4me3 | H3K4me3.bam | Control.bam
H1hesc | H3K79me2 |H3K79me2.bam | Control.bam
H1hesc | H3K9ac | H3K9ac.bam | Control.bam


## ChromHMM

Emission | Overlap | Transition 
 --- | --- | ---
![Image](/data/charts/states.png) | ![Image](/data/charts/regions.png) | ![Image](/data/charts/transitions.png)

### RefSeqTES
![Image](/data/charts/enrichment.png)

## Эпигенетические типы
№ | Название | Описание
 --- | --- | ---
1 | Active Promoter | <ul><li> выражен в H3K27me3 </li><li> Чаще всего находятся на RefSeqTES </li>
2 | Weak enhancer/Weak transcribed | <ul><li> выражен в H3K27me3, H3K4me2 </li><li> Чаще всего находятся на RefSeqTES, CpGIsland, RefSeqExon </li>
3 | Strong enhancer/Transcriptional elogation | <ul><li> выражен в H3K27me3, H3K4me2, H3K4me3 </li><li> Чаще всего находятся на RefSeqTSS, CpGIsland, RefSeqExon </li>
4 | Active Promoter | <ul><li> выражен в H3K4me2, H3K4me3 </li><li> Чаще всего находятся на RefSeqTSS, CpGIsland, RefSeqExon и RefSeqTSS2Kb </li>
5 | Active Promoter | <ul><li> выражен в H3K9ac, H3K4me2, H3K4me3 </li><li> Чаще всего находятся на RefSeqTSS, CpGIsland, RefSeqExon и RefSeqTSS2Kb </li>
6 | Weak enhancer | <ul><li> выражен в H3K4me2 </li><li> Чаще всего находятся на RefSeqTES </li>
7 | Weak enhancer | <ul><li> выражен в H3K4me2, H3K79me2 </li><li> Чаще всего находятся на RefSeqGene, RefSeqTSS2Kb </li>
8 | Weak enhancer | <ul><li> выражен в H3K79me2 </li><li> Чаще всего находятся на RefSeqGene </li>
9 | Weak enhancer | <ul><li> выражен в H3K79me2 </li><li> Чаще всего находятся на RefSeqGene </li>
10 | Weak transcribed | <ul><li> Не выражен </li><li> Чаще всего находятся на RefSeqGene </li>
11 | Weak transcribed | <ul><li> выражен в H3K36me3 </li><li> Чаще всего находятся на RefSeqGene, а также на RefSeqTES и RefSeqExon, но реже </li>
12 | Weak transcribed | <ul><li> выражен в H3K9me3, H3K36me3 </li><li> Чаще всего находятся на RefSeqExon, а также на RefSeqTES, но реже </li>
13 | Repressed | <ul><li> выражен в H3K9me3</li><li> Чаще всего находятся на ядерной ламине, то есть попадает на участок репрессированного гетерохроматима </li><li> Не попадает на ген </li>
14 | Heterochromatin | <ul><li> Не выражен </li><li> Чаще всего находятся на ядерной ламине и всем геноме, то есть попадает на участок репрессированного гетерохроматима </li><li> Не попадает на ген </li>
15 | Heterochromatin | <ul><li> выражен в H3K4me1 </li><li> Чаще всего находятся на ядерной ламине, RefSeqGene и RefSeqTES </li>

## Картинки из браузера
![Image](/data/browser/6-4-10-1-2-3-13-14.png)
![Image](/data/browser/5-7-8-9-10.png)
![Image](/data/browser/11-15.png)
 
 ## Бонус
 ```
from google.colab import files
import os

states = ['Active_Promoter',
          'Weak_Enhancer',
          'Strong_Enhancer',
          'Active_Promoter',
          'Active_Promoter',
          'Weak_Enhancer',
          'Weak_Enhancer',
          'Weak_Enhancer',
          'Weak_Enhancer',
          'Weak_Transcribed',
          'Weak_Transcribed',
          'Weak_Transcribed',
          'Repressed',
          'Heterochromatin',
          'Heterochromatin']

with open(f'data/H1hesc_15_dense.bed', 'r') as old_f:
  with open(f'H1hesc_15_dense_new.bed', 'a') as new_f:
    lines = old_f.readlines()
    new_f.write(lines[0])
    for line in lines[1:]:
        l = line.split('\t')
        l[3] = l[3] + '_' + states[int(l[3]) - 1]
        new_f.write('\t'.join(l))
 ```
 
H1hesc_15_dense_new.bed - итоговый файл
