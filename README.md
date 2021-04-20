
# Sig_COVID19 <img src="logo2.png" align="right" width="120" />

Sig_COVID19 is a repository to share mutational signature data constructed from evolution of virus sequences (mainly SARS-CoV-2). Because virus genomes are often single stranded, this signature consists of 192-context, which is twice that of the COSMIC signature. This Repository also provides mutational signatures of various viruses in addition to SARS-CoV-2. The full lists of mutations and phylogenetic tree is also available.

You can download

* selected data
* all data of therepository

```bash
# Download phylogenetic tree data

wget https://github.com/ju-lab/SC2_evol_signature/raw/master/data/msa_0117.tree.gz
gzip -d msa_0117.tree.gz


# Download per sample information

wget https://github.com/ju-lab/SC2_evol_signature/raw/master/data/Per_sample_mutation_list.csv.gz
wget https://github.com/ju-lab/SC2_evol_signature/raw/master/data/GISAID_metadata.csv
wget https://github.com/ju-lab/SC2_evol_signature/raw/master/data/loglikelihood_to_be_root_and_outgroup_distance.csv


# Download annotated mutation information

wget https://github.com/ju-lab/SC2_evol_signature/raw/master/data/All_mutation_information.csv.gz


# Download all data

git clone https://github.com/ju-lab/SC2_evol_signature.git

```

## Data format

The phylogenetic tree file is in the **`newick`** format with sample IDs (tip labels) and node names. These names are useful for indexing the mutation data. The tree file can be loaded on R with  `read.tree` function in the `ape` package. The tree object can be further explored using `ape`, `phangorn`, and other `R` packages and softwares. 

```R
library(ape)
tree <- read.tree("msa_0117.tree")
plot(tree)
```

The mutation data is catalogued in `Per_sample_mutation_list.csv.gz` and `All_mutation_information.csv.gz`. And the specific mutations can be explored by their unique identifers matched through the dataset including the tree file.

```
# Per_sample_mutation_list.csv.gz

|ID             |Sampling_date |Country |...|Mutation_IDs 
|:--------------|:-------------|:-------|...|:-------------------------------------------------------------
|EPI_ISL_507764 |2020-03-26    |USA     |   |sbs_1059_AC>TC_351794_351743,sbs_25563_AG>TA_351795_351794, ..
|EPI_ISL_495656 |2020-04-16    |USA     |   |sbs_23374_CT>CT_351538_2,sbs_1059_AC>TC_351794_351743,sbs_2 ..
|EPI_ISL_483143 |2020-04-21    |Germany |...|ind_24685_T>-_351539_3,sbs_13011_AC>TA_351538_351539,sbs_18 ..
|EPI_ISL_483144 |2020-04-21    |Germany |   |sbs_13011_AC>TA_351538_351539,sbs_18326_GC>TT_351538_351539 ..
|EPI_ISL_738254 |2020-04-14    |USA     |   |sbs_1059_AC>TC_351794_351743,sbs_25563_AG>TA_351795_351794, ..
|EPI_ISL_507762 |2020-03-27    |USA     |   |sbs_1059_AC>TC_351794_351743,sbs_25563_AG>TA_351795_351794, ..



# All_mutation_information.csv.gz

|mutID                      |type |status 1   |status 2                                                                   |...
|:--------------------------|:----|:----------|:--------------------------------------------------------------------------|
|sbs_10_TT>GT_633183_329639 |SBS  |node281658 |hCoV-19/USA/LA-EVTL071/2020|EPI_ISL_451232|2020-05-04&|NorthAmerica        |
|sbs_11_TT>CA_357288_6016   |SBS  |node5763   |hCoV-19/USA/UT-UPHL-2012146142/2020|EPI_ISL_746962|2020-12-01|NorthAmerica |
|sbs_13_AT>AA_649653_348274 |SBS  |node298128 |hCoV-19/USA/CA-CSMC203/2020|EPI_ISL_824612|2020-12-27|NorthAmerica         |...
|sbs_13_AT>CA_631201_327314 |SBS  |node279676 |hCoV-19/USA/LA-EVTL1196/2020|EPI_ISL_768465|2020-12-11|NorthAmerica        |
|sbs_13_AT>CA_611678_611679 |SBS  |node260153 |node260154                                                                 |
|sbs_13_AT>CA_622041_317640 |SBS  |node270516 |hCoV-19/USA/LA-EVTL1375/2020|EPI_ISL_779041|2020-12-11|NorthAmerica        |

```

## Citation

If you use Sig_COVID19, please cite: (will be updated)
```
Yi K. et al, 2020, Mutational spectrum of SARS-CoV-2 during the global pandemic, XXXXXXXXX XXX-XXXX
```
