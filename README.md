# Visualizing nanopore sequencing data using circos plots

A Jupyter notebook to convert methylation data and SNPs obtained with ONT into 
circos plots using [pyCircos](https://github.com/ponnhide/pyCircos) 
library.

## Installation

To install the mamba environment with the necessary programs for plotting, use 
the following commands:

```sh
# Get the source code
git clone https://github.com/villena-francis/ONT-circos
cd ONT-circos
# Create a conda environment 
mamba install env/pyCircos.yalm
```

## Usage

There are several ways, but a user-friendly approach is to use Jupyter Notebook 
from VS Code through its official extension and select the mamba environment as 
kernel.

To generate the plots, the output files from Modkit, Clair3, and ClairS are 
required, distributed as follows:

```sh
.
├── data
│   ├── GANDALF_CART_after
│   │   ├── met
│   │   │   └── ModKit_outfile.bed
│   │   ├── SNPs_germ
│   │   │   └── Clair3_outfile.vcf
│   │   └── SNPs_som
│   │       └── ClairS_outfile.vcf
│   ├── hg38_chromosome_cytoband.csv
│   └── hg38_chromosome_general.csv
├── pyCircos_ONT.ipynb
├── README.md
└── results
    └── GANDALF_CART_after.pdf
```
The final step before running the code is to specify the name of the sample 
directory. The scripts will take care of searching for the files within the 
directory and generating the plot.

```py
sample = f'GANDALF_CART_after'
```
