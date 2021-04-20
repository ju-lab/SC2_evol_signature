
# Sig_COVID19 <img src="logo22.png" align="right" width="120" />

Sig_COVID19 is a repository to share mutational signature data constructed from evolution of virus sequences (mainly SARS-CoV-2). Because virus genomes are often single stranded, this signature consists of 192-context, which is twice that of the COSMIC signature. This Repository also provides mutational signatures of various viruses in addition to SARS-CoV-2. The full lists of mutations and phylogenetic tree is also available.

You can download

* selected data
* all data of therepository

```
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

The phylogenetic tree file is in the **`newick`** format with sample IDs (tip labels) and node names. These names are useful for indexing the mutation data. The tree file can be loaded on R with  `read.tree` function in the `ape` package.

```{R}
library(ape)
tree <- read.tree("msa_0117.tree")
plot(tree)
```



## Citation

If you use Sig_COVID19 please cite: (will be updated)

Yi K. et al, 2020, Mutational spectrum of SARS-CoV-2 during the global pandemic, XXXXXXXXX XXX-XXXX
