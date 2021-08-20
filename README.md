<h1 align="center">  Welcome to Team drug_development_b, HackBio 2021 </h1>

![HBimage](https://user-images.githubusercontent.com/88287648/128190365-2beca13a-9c53-41b0-83cc-185ae3d8a43c.png)

# Multiple Ligand Docking Tutorial on leucine-rich repeat kinase 2 using compounds of safflower plant as a therapeutic agent for Parkinson’s Disease

## Introduction
 
  One of the most debilitating diseases of the brain is Parkinson's disease (PD), despite the availability of symptomatic treatments. The biochemical, pathological, and genetic studies have identified 18 types of PD caused by various genes such as α-Syn, LRRK2, parkin, and tau. These genes are involved in the pathogenesis of PD and can promote cognitive impairment in PD patients (Irwin et al., 2013). Leucine Rich Repeat Kinase 2 also called LRRK2 (Fig. 1) is a protein coding gene known to cause Parkinson Disease 8, Autosomal Dominant, and Hereditary Late-Onset Parkinson Disease (Tolosa et al., 2020). Mutations in leucine-rich repeat kinase 2 (LRRK2) are commonly implicated in the pathogenesis of both familial and sporadic Parkinson's disease (PD) (Myasnikov et al., 2021). 
  
  
  
![Fig 1. 3D structure of Target protein (mutant LRRK2) ](https://github.com/Lu-17/drug_development_b/blob/main/Results/3D%20structure%20of%20target%20protein%20(mutant%20LRRK2).png)

**Fig 1.** 3D structure of Target protein (mutant LRRK2)
  
  To date, only symptomatic therapies with the minimum satisfactory effects are known against PD, and no treatment has been known to decelerate the disease progression (Rai et al., 2021). There is a need to develop an effective, efficient, and etiological treatment to fulfill the medical requirement of persons with Parkinson's disease. The lack of resources, including appropriate model animals, well-known biomarkers, and limitations in clinical trial design restricts the complete understanding of PD pathogenesis, which obstructs the development of its potential neuroprotective therapies (Bezard et al., 2013).
  
  This tutorial aimed to conduct an in silico study , which involves using computer software to analyze biological data in vitro by mimicking what happens in vivo and using the plant as an alternative therapy, with a reduced side effect. The use of in silico technique is faster and reduces laboratory costs. The plant of interest is "Safflower". Safflower (*Carthamus tinctorius* L.) has long been used to treat cerebrovascular diseases in China. This plant contains flavonoids, which are effective in models of neurodegenerative disease (Ablat et al., 2016). 
  
   The study was carried out taking as reference this [Youtube Tutorial](https://www.youtube.com/watch?v=UIk6ISuS5Lk) and performed by downloading the target protein (mutated LRRK2) (PDB ID- 7L13) from the PDB database.  There are four (4) mutations on the protein. Mutated form of the protein was downloaded because mutation on this gene (LRRK2) is what triggers pathogenesis of PD. An established standard (Lrrk2-IN--1) which is an inhibitor of the Parkinson's disease kinase LRRK2 was also obtained from PubChem database. Fifteen (15) compounds extracted using hot water from safflower seed (Yu et al., 2013) were used as test compounds against the target protein. The structure of the compounds was obtained from the PubChem database. The target protein was prepared by removing water molecules, metal ion using the [Biovia Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download).  Docking was done on [PyRx](https://sourceforge.net/projects/pyrx/) while [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download) was used to carry out the visualization study. 

## Workflow
  In this tutorial, we will cover:
  
  1. Download data  
      1. Get the target protein (mutated LRRK2) from the [PDB Protein data bank](https://www.rcsb.org/)
      2. Get the standard (Lrrk2-IN--1) and Ligands (15 Safflower compounds) from the [PubChem database](https://pubchem.ncbi.nlm.nih.gov/)      
  2. Separating protein and unique ligand structures using [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
  4. Docking using [PyRx](https://sourceforge.net/projects/pyrx/)
  5. Visualization using [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
 
 ## Download data 
 Download the dataset as mentioned:
    
 ### Get the target protein
  1. Go to Protein Data Bank - **PDB**.
  2. Download the .pdb file of ["**7LI3**"](https://www.rcsb.org/structure/7LI3) - Structure of the LRRK2 G2019S mutant  
  
  
 ### Get the standard (Lrrk2-IN--1) and Ligands (15 Safflower compounds)
  1. Go to PubChem Database.
  2. Search for ["**LRRK2-IN-1**"](https://pubchem.ncbi.nlm.nih.gov/compound/46843906) (PubChem ID: 46843906)
  3. List of ["**Journal source of Safflower compounds**"](https://pubmed.ncbi.nlm.nih.gov/24288028/)
  4. Search for the Safflower ligands from PubChem:
     -2-Amino-3,4-dimethylbenzoic acid - PubChem ID: 282450
     -Hydroxybenzhydrazide - PubChem ID: 
  
  
 ## Separating protein and unique ligand structures
  
  
 ## Docking

  ![3D6T- 442428 - docked](https://user-images.githubusercontent.com/83166836/130231238-c2a2f372-ec53-49a2-b46b-7417c60bdf56.png)
  
  ![3](https://user-images.githubusercontent.com/83166836/130233175-9ffec29f-513b-496d-9545-9c52c51e30d8.png)
  
  **Fig 2.**: 3D structure of hit ligand 5280343 at target protein binding site

 ## Visualization

  ![2](https://user-images.githubusercontent.com/83166836/130231438-1cc8c7da-2a6f-4ccd-ad33-71e174aa0234.png)
  
  **Fig 3.**:3D structure of hit ligand 65064 and target protein complex

  ![4](https://user-images.githubusercontent.com/83166836/130233210-3ab1f93b-98c4-4c4a-b699-ab3aba54f8ee.png)
  
  **Fig 4.**:2D structure of hit ligand 65064 and target protein complex



## Video Tutorial for protein-ligand binding studies

[Click over here for part 1](https://drive.google.com/drive/folders/171VjcD1O0qPpaUL9w5POX_nSfSe3Za65?usp=sharing)

[Click over here for part 2](https://drive.google.com/file/d/17IBhekFHaGNz_y503WcuUWwgU02INYs7/view?usp=sharing)



## References <h1>
 
Ablat N, Lv D, Ren R, Xiaokaiti Y, Ma X, Zhao X, Sun Y, Lei H, Xu J, Ma Y, Qi X, Ye M, Xu F, Han H, Pu X. Neuroprotective Effects of a Standardized Flavonoid Extract from Safflower against a Rotenone-Induced Rat Model of Parkinson's Disease. Molecules. 2016 Aug 24;21(9):1107. 
 
Bezard E, Yue Z, Kirik D, Spillantini MG (2013) Animal models of Parkinson’s disease: limits and relevance to neuroprotection studies. Mov Disord 28:61-70.
 
Emamzadeh FN, Surguchov A (2018) Parkinson’s disease: biomarkers, treatment, and risk factors. Front Neurosci 12:612.

Fields CR, Bengoa-Vergniory N, Wade-Martins R (2019) Targeting alpha-synuclein as a therapy for Parkinson’s disease. Front Mol Neurosci 12:299.

Irwin DJ, Lee VM, Trojanowski JQ (2013) Parkinson’s disease dementia: convergence of α-synuclein, tau and amyloid-β pathologies. Nat Rev Neurosci 14:626-636.

Myasnikov A, Zhu H, Hixson P, Xie B, Yu K, Pitre A, Peng J, Sun J. (2021). Structural analysis of the full-length human LRRK2. Cell. 24;184(13):3519-3527.e10. doi: 10.1016/j.cell.2021.05.004. Epub 2021 Jun 8. PMID: 34107286.

Rai SN, Singh, P, Varchney R, Chaturvedi VK, Vamanu, E, Singh MP, Singh BK (2021). Promising drug targets and associated therapeutic interventions in Parkinson’s disease. Neural Regen Res, 16:1730-9.

Salat D, Tolosa E (2013) Levodopa in the treatment of Parkinson’s disease: current status and new developments. J Parkinson’s Dis 3:255-269.

Tolosa, E., Vila, M., Klein, C. & Rascol, O. (2020). LRRK2 in Parkinson disease: challenges of clinical trials. Nat Rev Neurol 16, 97–107. https://doi.org/10.1038/s41582-019-0301-2 - automatic!

Zhu ZG, Sun MX, Zhang WL, Wang WW, Jin YM, Xie CL (2017b) The efficacy and safety of coenzyme Q10 in Parkinson’s disease: a meta-analysis of randomized controlled trials. Neurol Sci 38:215-224.



