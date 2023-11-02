# iTMU798

We present our workflow for the reconstruction a genome-scale metabolic model (GSMM) of _T. muris_ (__iTMU798__) using [COBRApy](https://cobrapy.readthedocs.io/en/latest/) (Python). _C. elegans_ GSMMs ([WormJam](https://github.com/wormjam-consortium) and [iCEL1314](http://wormflux.umassmed.edu/download.php)) were used as templates. The reconstruction process consists of 5 main steps and manual curation.

### Reconstruction of a genome-scale metabolic model for _Trichuris muris_ (Reconstruction)

The notebook `DraftModelReconstruction.ipynb` utilizes [WormJam](https://github.com/wormjam-consortium) as a reference model and creates a preliminary model by mapping _C. elegans_ - _T. muris_ orthologs obtained from [BioMart](https://parasite.wormbase.org/biomart/martview/928f0949ef9a613d72a820f3e62bb5e9). The notebook `MetaboliteNameCorrectionChEBIPubChem.ipynb` organizes metabolite information in the draft model using [ChEBI](https://www.ebi.ac.uk/chebi/) & [PubChem](https://pubchem.ncbi.nlm.nih.gov/) databases. `SearchRHEA.ipynb` is responsible for searching additional reactions in [RHEA](https://www.rhea-db.org/) using EC numbers from the _T. muris_ genome sourced from [UniProt](https://www.uniprot.org/proteomes/UP000046395).
Subsequently, a manual refinement process takes place, which includes organizing the biomass according to [iCEL1314](http://wormflux.umassmed.edu/download.php) and incorporating subsystems from [KEGG](https://www.genome.jp/kegg/). To identify blocked reactions (`BlockedReactionIdentification.ipynb`) and dead-end metabolites (`DeadEndMetaboliteIdentification.ipynb`) for gap-filling, FVA (Flux Variability Analysis) is employed. The final outcome of this iterative curation process is the creation of iTMU798.

### Identification of essential genes and comparison of __iTMU798__ with [iCEL1314](http://wormflux.umassmed.edu/download.php), [Worm1](https://github.com/SysBioChalmers/Worm-GEM) & [iDC625](https://github.com/ParkinsonLab/Brugia_metabolic_network) (Analysis)

The notebook `ModelContentComparison.ipynb` performs a comparative analysis between __iTMU798__ and the most recent genome-scale metabolic models (GSMMs) of _C. elegans_ ([iCEL1314](http://wormflux.umassmed.edu/download.php) & [Worm1](https://github.com/SysBioChalmers/Worm-GEM)) and _Brugia malayi_ ([iDC625](https://github.com/ParkinsonLab/Brugia_metabolic_network)). Additionally, the notebook `GeneEssentiality_and_Comparison.ipynb` is employed to predict essential genes in __iTMU798__ and compare them with essential genes present in both _C. elegans_ models and the [OGEE](https://v3.ogee.info/#/browse/6239/Caenorhabditis%20elegans) (Online Gene Essentiality) database. 

In the notebook `ExpressionData.ipynb`, the expression data from larvae and adult worms (from [WormBase ParaSite](https://parasite.wormbase.org/expression/trichuris_muris_prjeb126/index.html) & [Duque-Correa, M.A. et al, 2022](https://rdcu.be/disK9)) are integrated with the relevant essential genes predicted by iTMU798. `MetabolomeChart.ipynb` undertakes a comparison between the metabolites found in iTMU798 and the identified metabolites from two separate studies ([Wangchuk, P. et al, 2019](https://rdcu.be/disPs) & [Yeshi, K. et al, 2020](https://www.mdpi.com/881754))

### Cite

[A genome-scale metabolic model of parasitic whipworm. Nat Commun 14, 6937 (2023).](https://doi.org/10.1038/s41467-023-42552-4)

### Contact

omer.bay@manchester.ac.uk
