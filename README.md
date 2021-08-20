<h1 align="center">  Welcome to Team drug_development_b, HackBio 2021 </h1>

![HBimage](https://user-images.githubusercontent.com/88287648/128190365-2beca13a-9c53-41b0-83cc-185ae3d8a43c.png)

# Multiple Ligand Docking Tutorial on leucine-rich repeat kinase 2 using compounds of Safflower plant as a therapeutic agent for Parkinson’s Disease

## Introduction
 
  One of the most debilitating diseases of the brain is Parkinson's disease (PD), despite the availability of symptomatic treatments. The biochemical, pathological, and genetic studies have identified 18 types of PD caused by various genes such as α-Syn, LRRK2, parkin, and tau. These genes are involved in the pathogenesis of PD and can promote cognitive impairment in PD patients (Irwin et al., 2013). Leucine Rich Repeat Kinase 2 also called LRRK2 (Fig. 1) is a protein coding gene known to cause Parkinson Disease 8, Autosomal Dominant, and Hereditary Late-Onset Parkinson Disease (Tolosa et al., 2020). Mutations in leucine-rich repeat kinase 2 (LRRK2) are commonly implicated in the pathogenesis of both familial and sporadic Parkinson's disease (PD) (Myasnikov et al., 2021). 
  
  
  
![Fig 1. 3D structure of Target protein (mutant LRRK2) ](https://github.com/Lu-17/drug_development_b/blob/main/Results/3D%20structure%20of%20target%20protein%20(mutant%20LRRK2).png)

**Fig 1.** 3D structure of Target protein (mutant LRRK2)
  
  To date, only symptomatic therapies with the minimum satisfactory effects are known against PD, and no treatment has been known to decelerate the disease progression (Rai et al., 2021). There is a need to develop an effective, efficient, and etiological treatment to fulfill the medical requirement of persons with Parkinson's disease. The lack of resources, including appropriate model animals, well-known biomarkers, and limitations in clinical trial design restricts the complete understanding of PD pathogenesis, which obstructs the development of its potential neuroprotective therapies (Bezard et al., 2013).
  
  This tutorial aimed to conduct an in silico study , which involves using computer software to analyze biological data in vitro by mimicking what happens in vivo and using the plant as an alternative therapy, with a reduced side effect. The use of in silico technique is faster and reduces laboratory costs. The plant of interest is "Safflower". Safflower (*Carthamus tinctorius* L.) has long been used to treat cerebrovascular diseases in China. This plant contains flavonoids, which are effective in models of neurodegenerative disease (Ablat et al., 2016). 
  
   The study was carried out taking as reference this [Youtube Tutorial](https://www.youtube.com/watch?v=UIk6ISuS5Lk) and performed by downloading the target protein (mutated LRRK2) (PDB ID- 7L13) from the PDB database. There are four (4) mutations on the protein. Mutated form of the protein was downloaded because mutation on this gene (LRRK2) is what triggers pathogenesis of PD. An established standard (Lrrk2-IN--1) which is an inhibitor of the Parkinson's disease kinase LRRK2 was also obtained from PubChem database. Fifteen (15) compounds extracted using hot water from Safflower seed (Yu et al., 2013) were used as test compounds against the target protein. The structure of the compounds was obtained from the PubChem database. The target protein was prepared by removing water molecules, metal ion using the [Biovia Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download).  Docking was done on [PyRx](https://sourceforge.net/projects/pyrx/) while [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download) was used to carry out the visualization study. 

## Workflow
  In this tutorial, we will cover:
  
  1. Download data       
  2. Separating protein and unique ligand structures using [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
  4. Docking using [PyRx](https://sourceforge.net/projects/pyrx/)
  5. Visualization using [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
 
 ## Download data 
  1. Get the target protein (mutated LRRK2) from the [PDB Protein data bank](https://www.rcsb.org/)
  2. Get the standard (Lrrk2-IN--1) and Ligands (15 Safflower compounds) from the [PubChem database](https://pubchem.ncbi.nlm.nih.gov/)
    
 ### Get the target protein
  1. Go to Protein Data Bank - **PDB**.
  2. Download the PDB file of ["**7LI3**"](https://www.rcsb.org/structure/7LI3) - Structure of the LRRK2 G2019S mutant  
  
  
 ### Get the standard (Lrrk2-IN--1) and Ligands (15 Safflower compounds)
  1. Go to PubChem Database.
  2. Search for ["**LRRK2-IN-1**"](https://pubchem.ncbi.nlm.nih.gov/compound/46843906) (PubChem ID: 46843906)
  3. List of ["**Journal source of Safflower compounds**"](https://pubmed.ncbi.nlm.nih.gov/24288028/)
  4. Search for the Safflower ligands from PubChem and download the SDF file:
 
 
|S.No.        | Name of ligand | PubChem ID | 
|-------------|-------------|-------------|
|1.           | 2-Amino-3,4-dimethylbenzoic acid  | [PubChem ID: 282450](https://pubchem.ncbi.nlm.nih.gov/compound/282450)|
|2.           | 4-Hydroxybenzohydrazide| [PubChem ID: 1742](https://pubchem.ncbi.nlm.nih.gov/compound/1742)|
|3.           | 4-Hydroxycinnamic acid| [PubChem ID: 637542](https://pubchem.ncbi.nlm.nih.gov/compound/637542)|
|4.           | Chlorogenic acid| [PubChem ID: 1794427](https://pubchem.ncbi.nlm.nih.gov/compound/1794427)|
|5.           | Epigallocatechin gallate| [PubChem ID: 65064](https://pubchem.ncbi.nlm.nih.gov/compound/65064)|
|6.           | Epigallocatechin| [PubChem ID:	72277](https://pubchem.ncbi.nlm.nih.gov/compound/72277)|
|7.           | Ferulic acid| [PubChem ID: 445858](https://pubchem.ncbi.nlm.nih.gov/compound/445858)|
|8.           | Gallocatechin| [PubChem ID: 65084](https://pubchem.ncbi.nlm.nih.gov/compound/65084)|
|9.           | kaempferol| [PubChem ID: 5280863](https://pubchem.ncbi.nlm.nih.gov/compound/5280863)|
|10.          | Luteolin| [PubChem ID: 5280445](https://pubchem.ncbi.nlm.nih.gov/compound/5280445)|
|11.          | Naringin| [PubChem ID: 442428](https://pubchem.ncbi.nlm.nih.gov/compound/442428)|
|12.          | Quercetin dihydrate| [PubChem ID: 5284452](https://pubchem.ncbi.nlm.nih.gov/compound/5284452)|
|13.          | Rutin hydrate| [PubChem ID: 45479757](https://pubchem.ncbi.nlm.nih.gov/compound/45479757)|
|14.          | Syringic acid| [PubChem ID: 10742](https://pubchem.ncbi.nlm.nih.gov/compound/10742)|
|15.          | trans-Chalcone| [PubChem ID: 637760](https://pubchem.ncbi.nlm.nih.gov/compound/637760)|
  
 ## Separating protein and unique ligand structures
  We simply filter the original PDB twice: once for lines which do not match, which returns a PDB file containing only protein; and once for lines which match, which returns a PDB file containing only the unique ligand.
  
 ## Docking

  ![3D6T- 442428 - docked](https://user-images.githubusercontent.com/83166836/130231238-c2a2f372-ec53-49a2-b46b-7417c60bdf56.png)
  
  ![3](https://user-images.githubusercontent.com/83166836/130233175-9ffec29f-513b-496d-9545-9c52c51e30d8.png)
  
  **Fig 2.** 3D structure of hit ligand 5280343 at target protein binding site

 ## Visualization

  ![2](https://user-images.githubusercontent.com/83166836/130231438-1cc8c7da-2a6f-4ccd-ad33-71e174aa0234.png)
  
  **Fig 3.** 3D structure of hit ligand 65064 and target protein complex

  ![4](https://user-images.githubusercontent.com/83166836/130233210-3ab1f93b-98c4-4c4a-b699-ab3aba54f8ee.png)
  
  **Fig 4.** 2D structure of hit ligand 65064 and target protein complex
  
 ## Using GROMACS for LRRK2 protein docking and visualization
Even though molecular docking gives a comprehensive insight about the non-covalent interactions between a small molecule ligand and the target receptor; it is still not enough to accurately validate the nature of binding between them. As it doesn't consider the cell's environment with the water molecules it includes in the cytosol and how it affects the local minimum binding free energy. For this reason molecular dynamics simulations are needed to accurately calculate the binding energies in the cellular environment using simplified molecular mechanics calculations by iterative application of Newton’s laws of motion. Multiple packages exist for performing MD simulations. One of the most popular visualization tools is the open-source GROMACS.

When using the 7L13 protein in galaxy, the GROMACS tool gives an error message that details to: "This job was terminated because it used more memory than it was allocated." as shown in figure 5. We believe this is a limitation to using GROMACS from galaxy. 

**Fig 5.** ![image](https://user-images.githubusercontent.com/88295292/130263657-7d87f51a-4c68-432d-936e-3b1ddef87710.png)


Instead the lysozyme protein workflow was regenerated to describe realistic molecular motion of the system.  

## Workflow
The following workflow (https://usegalaxy.eu/u/shadwa_7/h/md) was executed using PDB: 1AKI as shown in the figure below. This workflow was extracted from the following Galaxy tutorial: https://training.galaxyproject.org/training-material/topics/computational-chemistry/tutorials/md-simulation-gromacs/tutorial.html#process 

**Fig 6.** workflow ![worflow](https://user-images.githubusercontent.com/88459663/130258174-60e498fd-4677-497c-9b53-40d06d319110.PNG)

1. Setup (loading data, solvation i.e. addition of water and ions).
2. Energy minimization of the protein.
3. Equilibration of the solvent around the protein (with two ensembles, NVT and NPT)
4. Production simulation.

## Setup 
In the setup step, a topology for the protein structure is prepared which contains all the information required to describe the molecule for the purposes of simulation (atom masses, bond lengths and angles, charges). Then, a GRO structure file is created, storing the structure of the protein. Finally, a ‘position restraint file’ is created which will define the unit cell where the simulation will take place. After that, protein solvation is executed to add water molecules and ions to the simulation box.

## Energy minimization
To remove any steric clashes or unusual geometry which would artificially raise the energy of the system, we must relax the structure by running an energy minimization (EM) algorithm.

## Equilibration
At this point equilibration of the solvent around the solute (i.e. the protein) is necessary. This is performed in two stages: equilibration under an NVT ensemble, followed by an NPT ensemble. NVT ensemble maintains constant number of particles, volume and temperature, while NPT ensemble maintains constant number of particles, pressure and temperature. Additionally, we use the position restraint file again to hold the protein in place while the solvent is allowed to move freely around it.

## Production simulation
After the previous steps, results of the MD simulation are now ready in the form of .GRO file which are visualized using NGL viewer.

**Fig 7.** MD simulation for the protein ![Capture](https://user-images.githubusercontent.com/88459663/130258966-14c10463-593f-44f2-955d-b8545c9c4f86.PNG)


# Video Tutorial for protein-ligand binding studies

[Click over here for part 1 and 2](https://drive.google.com/drive/folders/171VjcD1O0qPpaUL9w5POX_nSfSe3Za65?usp=sharing)


## Summary
From the docking study using PyRx, Epigallocatechin gallate (PDB Id- 65064) and Quercetin (PDB Id- 5280343) has the highest binding affinity compared to other compounds and the standard. They both produced nine (9) poses while the standard had one (1) pose. Visualization study showed compound 65064 to have best interaction. unfavorable acceptor-acceptor interaction exist on 5280343 and the standard compound also has unfavorable bump. Galaxy was futher used to carry out molecular simulation on the target protein but failed.



## References
 
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



