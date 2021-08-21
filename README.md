<h1 align="center">  Welcome to Team drug_development_b, HackBio 2021 </h1>

![HBimage](https://user-images.githubusercontent.com/88287648/128190365-2beca13a-9c53-41b0-83cc-185ae3d8a43c.png)

# Multiple Ligand Docking and MD Simulation Tutorial on leucine-rich repeat kinase 2 using compounds of Safflower plant as a therapeutic agent for Parkinson’s Disease

## Introduction
 
 
  This tutorial is on the use of PyRx to conduct multiple ligand docking and also the use of Galaxy to run Moleular Dynamics (MD) simulation. The study was carried out taking as **reference this **[Youtube Tutorial](https://www.youtube.com/watch?v=UIk6ISuS5Lk) for the PyRx tutorial.** The work flow is as shown below.
  
  ## 🧬Workflow for Multiple Ligand docking
  In this tutorial, we will cover:
  
  1. Download data       
  2. Separating protein and unique ligand structures using [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
  4. Docking using [PyRx](https://sourceforge.net/projects/pyrx/)
  5. Visualization using [Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
 
 ### 🧬Download data 
  1. Get the target protein (mutated LRRK2) from the [PDB Protein data bank](https://www.rcsb.org/)
  2. Get the standard (Lrrk2-IN--1) and Ligands (15 Safflower compounds) from the [PubChem database](https://pubchem.ncbi.nlm.nih.gov/)
    
 ### 🧬Get the target protein
  1. Go to Protein Data Bank - **PDB**.
  2. Download the PDB file of ["**7LI3**"](https://www.rcsb.org/structure/7LI3) - Structure of the LRRK2 G2019S mutant  
  
  
 ### 🧬Get the standard (Lrrk2-IN--1) and Ligands (15 Safflower compounds)
  1. Go to PubChem Database.
  2. Search for ["**LRRK2-IN-1**"](https://pubchem.ncbi.nlm.nih.gov/compound/46843906) (PubChem ID: 46843906)
  3. List of ["**Journal source of Safflower compounds**"](https://pubmed.ncbi.nlm.nih.gov/24288028/)
  4. Search for the Safflower ligands from PubChem and download the SDF file.
  
 ### 🧬Separating protein and unique ligand structures
  1. Simply filter the original PDB twice: once for lines which do not match, which returns a PDB file 
  containing only protein.
  2. And once for lines which match, which returns a PDB  file containing only the unique ligand.

 ### 🧬Preparing the target protein
  1. open the protein in [Biovia Discovery Studio](https://discover.3ds.com/discovery-studio-visualizer-download)
  2. click on view and hirarchy for better analyzation
  3. remove water and HETATM molecules by clicking on edit and delete one after the other
  4. Add hydrogen atom "click on chemistry, hydrogen, add".
  5. Save the file in PDB format. 
 
 ### 🧬Docking on PyRx
  1. Docking was done on [PyRx](https://sourceforge.net/projects/pyrx/)
  2. Load the prepared protein
  3. Right click on the name of the protein, click on autodock and make macromolecule. It converts from PDB to PDBQT format
  4. Use Open babel in PyRx to import the ligands one after the other
  5. Minimize the energy for all the ligand
  6. Convert the ligands to PDBQT format
  7. Click on Vina wizard, select the protein and ligand
  8. Click on forward and the docking starts
  9. Save docking result in Excel

 ### 🧬Analysis of docking result using discovery studio
  1. open the docked protein
  2. click on ligand interactions on the left side of the panel
  3. study the 2D and 3D diagram generated 
  4. On the leftside panel to view all types of interactions occuring between the protein and the ligand.
  5. Repoart the findings.
  
  

 ## 🧬Example of docking in PyRx
  
  ![3D6T- 442428 - docked](https://user-images.githubusercontent.com/83166836/130231238-c2a2f372-ec53-49a2-b46b-7417c60bdf56.png)
  
  ![3](https://user-images.githubusercontent.com/83166836/130233175-9ffec29f-513b-496d-9545-9c52c51e30d8.png)
  
  **Fig 1.** 3D structure of ligand at target protein binding site

 ## 🧬Example of visualization in Discovery studio

  ![2](https://user-images.githubusercontent.com/83166836/130231438-1cc8c7da-2a6f-4ccd-ad33-71e174aa0234.png)
  
  **Fig 2.** 3D structure ligand and target protein 

  ![4](https://user-images.githubusercontent.com/83166836/130233210-3ab1f93b-98c4-4c4a-b699-ab3aba54f8ee.png)
  
  **Fig 3.** 2D structure ligand and target protein
  
  
## 🧬Using Galaxy for protein MD simulations
Even though molecular docking gives a comprehensive insight about the non-covalent interactions between a small molecule ligand and the target receptor; it is still not enough to accurately validate the nature of binding between them. As it doesn't consider the cell's environment with the water molecules it includes in the cytosol and how it affects the local minimum binding free energy. For this reason molecular dynamics simulations are needed to accurately calculate the binding energies in the cellular environment using simplified molecular mechanics calculations by iterative application of Newton’s laws of motion.
  
## 🧬Workflow for Galaxy
1. The following workflow (https://usegalaxy.eu/u/shadwa_7/h/md) was executed using LRRK2 (PDB: 7LI3) and PDB: 1AKI. 
2. This workflow was extracted from the following Galaxy tutorial: https://training.galaxyproject.org/training-material/topics/computational-chemistry/tutorials/md-simulation-gromacs/tutorial.html#process 
  
  
## 🧬Setup 
1. In the setup step, a topology for the protein structure is prepared which contains all the information required to describe the molecule for the purposes of simulation (atom  masses, bond lengths and angles, charges).
2. Then, a GRO structure file is created, storing the structure of the protein. 
3. Finally, a ‘position restraint file’ is created which will define the unit cell where the simulation will take place. After that, protein solvation is executed to add water molecules and ions to the simulation box.

### 🧬Energy minimization
1. To remove any steric clashes or unusual geometry which would artificially raise the energy of the system, we must relax the structure by running an energy minimization (EM) algorithm.

### 🧬Equilibration
1. At this point equilibration of the solvent around the solute (i.e. the protein) is necessary. 
2. This is performed in two stages: equilibration under an NVT ensemble, followed by an NPT ensemble. 
3. NVT ensemble maintains constant number of particles, volume and temperature, while NPT ensemble maintains constant number of particles, pressure and temperature. 
4. Additionally, we use the position restraint file again to hold the protein in place while the solvent is allowed to move freely around it.

### 🧬Production simulation
After the previous steps, results of the MD simulation are now ready in the form of .GRO file which are visualized using NGL viewer. Below is an example of what is displayed on galaxy.

**Fig 4.** MD simulation for the protein ![Capture](https://user-images.githubusercontent.com/88459663/130258966-14c10463-593f-44f2-955d-b8545c9c4f86.PNG)


## 🧬Summary
1. This tutorial aimed to conduct an in silico study , which involves using computer software to analyze biological data in vitro by mimicking what happens in vivo and using the plant as an alternative therapy, with a reduced side effect.
2. When using the LRRK2 (PDB ID: 7LI3) protein in galaxy, the GROMACS tool gives an error message that details to: "This job was terminated because it used more memory than it was allocated." as shown in figure 5. Instead the lysozyme protein workflow was regenerated to describe realistic molecular motion of the system.
3. We believe this is a limitation to using GROMACS from galaxy. 

**Fig 5.** ![image](https://user-images.githubusercontent.com/88295292/130263657-7d87f51a-4c68-432d-936e-3b1ddef87710.png)


## 🧬Video Tutorial for protein-ligand binding studies
[Click over here for part 1 and 2](https://drive.google.com/drive/folders/171VjcD1O0qPpaUL9w5POX_nSfSe3Za65?usp=sharing)


## 🧬List of contributors 
1. Data Collection: 
    1. @Pharmahy071 
    2. @Halton 
    3. @Nour
    4. @OnlyOneDamola 
    5. @Aderinsola
    6. @Malak

2. PyRx:
    1.  @Sefunmi-Peace 
    2.  @Modinat
    3.  @Pravithaks 
    4.  @kawthar

3. Github repo: 
    1. @LuisaC 
    2. @Marwank 
    3. @Bukola888 
    4. @AnusuiyaBora_08

4. Galaxy workflow:
    1.  @Tafa 
    2.  @Noha 
    3.  @Shadwa 
    4.  @Zahraa



## 🧬References
 
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



