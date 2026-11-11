# Computational Identification and Therapeutic Targeting of NUSAP1 in Breast Cancer

**Pathogenic nsSNPs Characterization, Structural Analysis, and Dual
Virtual Screening of Chemical and Phytochemical Compounds**

## Project Overview

This project uses computational bioinformatics and virtual-screening
approaches to investigate **NUSAP1 (Nucleolar and Spindle-Associated
Protein 1)** as a potential therapeutic target in breast cancer. The
study characterizes selected non-synonymous single-nucleotide
polymorphisms (nsSNPs), evaluates protein structure, stability and
dynamics, and screens chemical and phytochemical libraries to identify
potential lead compounds.



## Objectives

-   Collect breast-cancer hub genes reported in published literature.
-   Screen hub genes for the absence of known therapeutic drug targets.
-   Construct protein--protein interaction (PPI) networks and identify
    candidate hub genes.
-   Select a candidate gene based on breast-cancer and pan-cancer
    expression.
-   Computationally characterize deleterious nsSNPs in NUSAP1.
-   Evaluate protein stability, structure, flexibility and evolutionary
    conservation.
-   Identify potential lead compounds through virtual screening of
    chemical and phytochemical libraries.


## Methodology

The computational workflow included the following stages:

1.  **Gene collection and differential-expression analysis**
    -   GEO datasets were used to identify significant genes.
    -   Venny was used to identify common differentially expressed genes
        (DEGs).
2.  **PPI network and hub-gene identification**
    -   STRING was used to construct the protein--protein interaction
        network.
    -   Cytoscape and the CytoHubba plugin were used to identify hub
        genes with the MCC algorithm.
3.  **Therapeutic-target screening and candidate selection**
    -   The 87 reported hub genes were screened against TTD.
    -   The 36 genes without known drug targets were examined.
    -   GEPIA2 expression analysis supported the selection of NUSAP1.
4.  **nsSNP analysis**
    -   NUSAP1 variants were collected from UniProtKB.
    -   MetaRNN was used for pathogenicity ranking.
    -   MUpro and I-Mutant 2.0 were used to assess protein-stability
        changes.
    -   HOPE was used to examine variant-level structural and functional
        effects.
5.  **Evolutionary conservation**
    -   Evolutionary Trace analysis was used to compare conservation
        patterns in the wild-type protein and selected variants.
6.  **3D structure modelling and validation**
    -   AlphaFold was used for structure modelling.
    -   GalaxyRefine was used for structure refinement.
    -   SAVES was used for structure validation.
7.  **Protein dynamics**
    -   iMODS was used to assess deformability, B-factor, eigenvalue,
        variance, covariance and elastic-network model patterns.
8.  **Binding-pocket prediction and virtual screening**
    -   PrankWeb was used to identify binding pockets.
    -   Chemical compounds were screened from the Mcule library.
    -   Phytochemical compounds were screened from the IMPPAT database.
    -   AutoDock Vina was used for docking.
    -   SwissADME was used to assess ADME-related properties.
    -   ProTox 3.0 was used for toxicity prediction.

## Tools and Resources

  Purpose                               Tools / databases
  ------------------------------------- ----------------------
  Gene expression datasets              GEO
  Common DEGs                           Venny
  PPI network                           STRING
  Network visualization and hub genes   Cytoscape, CytoHubba
  Therapeutic-target screening          TTD
  Expression analysis                   GEPIA2
  Variant information                   UniProtKB
  Pathogenicity prediction              MetaRNN
  Protein stability                     MUpro, I-Mutant 2.0
  Variant effect analysis               HOPE
  Evolutionary conservation             Evolutionary Trace
  Protein structure prediction          AlphaFold
  Structure refinement                  GalaxyRefine
  Structure validation                  SAVES
  Protein dynamics                      iMODS
  Binding-pocket prediction             PrankWeb
  Chemical compound library             Mcule
  Phytochemical compound library        IMPPAT
  Molecular docking                     AutoDock Vina
  ADME prediction                       SwissADME
  Toxicity prediction                   ProTox 3.0

## Key Results

   ### Hub-gene analysis and NUSAP1 selection

    -   Total reported hub genes: **87**
    -   Hub genes with known drug targets: **51**
    -   Hub genes without known drug targets: **36**
    -   NUSAP1 was selected as the candidate gene based on its hub-gene
         recurrence and expression analysis.

   ### NUSAP1 variant analysis

   Four variants were evaluated:

    ------------------------------------------------------------------------
    Variant      Amino-acid          MUpro ΔΔG I-Mutant 2.0    MetaRNN score
               change                        stability    
    ------------ ------------ ---------------- ------------ ----------------
    R434M        Arg → Met              -0.539 Decrease                0.823

    K404E        Lys → Glu              -0.343 Decrease                0.727

    N386S        Asn → Ser              -1.332 Decrease                0.335

    T114N        Thr → Asn              -0.407 Decrease                0.039
   ------------------------------------------------------------------------

   The pathogenicity ranking reported in the presentation was:

 **R434M \> K404E \> N386S \> T114N**

   All four variants showed negative ΔΔG values and were predicted to decrease protein stability.

### Structure validation

The presentation reports the following structure-validation results:

  Structure          ERRAT score   Ramachandran favored
  ---------------- ------------- ----------------------
  Wild type (WT)          92.82%                  95.9%
  R434M variant           97.16%                  95.6%
  T114N variant           94.57%                  93.6%

All three structures were reported as having good structural quality.

### Protein dynamics

The reported native-dynamics preservation ranking was:

**WT \> R434M \> T114N**

The analysis described R434M as having a moderate dynamic effect and
T114N as causing greater disruption to protein motion and residue
communication.

### Binding-pocket prediction

PrankWeb identified three binding pockets. Pocket 1 had the highest
reported score and probability:

  Pocket       Score   Probability
  ---------- ------- -------------
  Pocket 1      2.22         0.054
  Pocket 2      1.54         0.022
  Pocket 3      1.34         0.016

Pocket 1 was selected for virtual screening. The reported binding-site
center was:

-   X: -19.2576
-   Y: -10.2263
-   Z: -15.8069

The reported binding-site dimensions were 20.0 Å × 20.0 Å × 20.0 Å.

### Virtual screening results

The project reports four non-toxic lead compounds from each library,
giving **eight computationally selected leads**.

**Mcule chemical library**

  Compound ID              Binding energy (kcal/mol)
  ---------------------- ---------------------------
  MCULE-3003239086-0-1                        -7.628
  MCULE-4544406282-0-1                        -6.483
  MCULE-6557310118-0-1                        -6.826
  MCULE-6724108984-0-1                        -7.171

**IMPPAT phytochemical library**

  Compound                  Binding energy (kcal/mol)
  ----------------------- ---------------------------
  Corylin                                      -6.555
  Puerarone                                    -6.666
  Sophoracoumestan A                           -6.639
  Steroid-like compound                        -7.084

The presentation reports favorable screening properties for the selected
leads, including zero Lipinski violations, zero PAINS alerts, zero Brenk
alerts, high gastrointestinal absorption and a bioavailability score of
0.55.

## Conclusion

The study's computational workflow identified NUSAP1 as a potential
therapeutic target for breast cancer and characterized four
destabilizing nsSNPs. The wild-type and variant structures were reported
to have good validation scores, while protein-dynamics analysis
indicated changes in flexibility and residue communication. Virtual
screening of Mcule and IMPPAT libraries identified eight non-toxic
candidate lead compounds with favorable predicted ADME properties.

These findings are computational predictions and require experimental
validation before any therapeutic conclusions can be drawn.

## Future Scope

-   Perform molecular-dynamics simulations using **GROMACS**.
-   Analyse RMSD for overall structural stability.
-   Analyse RMSF to identify flexible protein regions.
-   Calculate radius of gyration to assess protein compactness.
-   Conduct full-trajectory analysis for WT, R434M and T114N.
-   Validate promising compounds in NUSAP1-overexpressing breast-cancer
    cell lines.
-   Conduct suitable animal-model studies for promising candidates.
-   Experimentally validate the computational predictions.

## References

The following references were included in the project presentation:

1.  Zheng, H., et al. (2023). Comprehensive pan-cancer analysis reveals
    NUSAP1 is a novel predictive biomarker for prognosis and
    immunotherapy response. *International Journal of Biological
    Sciences, 19*(14), 4689--4708.
2.  McLaren, W., et al. (2016). The Ensembl Variant Effect Predictor.
    *Genome Biology, 17*(1), 122.
3.  Islam, M. S., Tanha, T. H., Zarin, N., Haque, S., Shiddiky, M. J.
    A., Lam, A. K., & Gopalan, V. (2025). Computational analysis and
    molecular dynamics insights into deleterious SNPs of the HFE gene.
    *Journal of Biomolecular Structure & Dynamics*, 1--24.
    https://doi.org/10.1080/07391102.2025.2593504
4.  Zeng, X., Shi, G., He, Q., & Zhu, P. (2021). Screening and predicted
    value of potential biomarkers for breast cancer using bioinformatics
    analysis. *Scientific Reports, 11*(1), 20799.
    https://doi.org/10.1038/s41598-021-00268-9
5.  Liu, Z., Liang, G., Tan, L., Su, A. N., Jiang, W., & Gong, C.
    (2017). High-Efficient Screening Method for Identification of Key
    Genes in Breast Cancer Through Microarray and Bioinformatics.
    *Anticancer Research, 37*(8), 4329--4335.
    https://doi.org/10.21873/anticanres.11826
6.  Wu, Y., Jin, J., Zhang, Y., Huang, X., Wang, H., Huang, Y., &
    Xie, H. (2026). Downregulation of the lncRNA PGM5P4-AS1 predicts
    poor prognosis and drives breast cancer progression through
    miR-3664-5p/KLF9. *Cancer Biology & Therapy, 27*(1), 2606474.
    https://doi.org/10.1080/15384047.2025.2606474
7.  Fang, E., & Zhang, X. (2017). Identification of breast cancer hub
    genes and analysis of prognostic value using integrated
    bioinformatics. *Cancer Biomarkers, 21*(1), 373--381.
8.  Torgovnick, A., & Schumacher, B. (2015). DNA repair mechanisms in
    cancer development and therapy. *Frontiers in Genetics, 6*, 157.
    https://doi.org/10.3389/fgene.2015.00157

------------------------------------------------------------------------

**Project:** Computational identification and therapeutic targeting of
NUSAP1 in breast cancer\
**Student:** Satya Sri Kranthi\
**Roll Number:** DY22SBBU0BID020\
**Guide:** Dr. A. Krishna Chaitanya
