
# Sig_COVID19 <img src="logo.png" align="right" width="120" />

Sig_COVID19 is a repository to share mutational signature data constructed from evolution of virus sequences (mainly SARS-CoV-2). Because virus genomes are often single stranded, this signature consists of 192-context, which is twice that of the COSMIC signature. This Repository also provides mutational signatures of various viruses in addition to SARS-CoV-2. The full lists of mutations and phylogenetic tree is also available.

You can download

* selected data
* all data of therepository

```
# Download phylogenetic tree data

wget https://github.com/ju-lab/SC2_evol_signature/raw/master/data/msa_0117.tree.gz
gzip -d msa_0117.tree.gz


# Download single base substitution

gwet https://github.com/ju-lab/SC2_evol_signature/raw/master/data/SBS.tsv


# Download all data

git clone https://github.com/ju-lab/SC2_evol_signature.git

```

If you use Sig_COVID19 please cite: (will be updated)
Yi K. et al, 2020, Mutational spectrum of SARS-CoV-2 during the global pandemic, XXXXXXXXX XXX-XXXX
