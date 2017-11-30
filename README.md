# TF_targets
Script to find TF regulators for a given input gene file.

# Dependencies
Requires Python 2.7 and SciPy. Both of which can be installed using Anaconda(https://www.anaconda.com/download/).

# Running program
Usage: find_TF_regulators.py --input FILE --output FILE

Options:
  -h, --help            show this help message and exit
  -i FILE, --input=FILE
                        input gene list (symbols)
  -o FILE, --output=FILE
                        file to dump output

# Input file
Text file with gene symbols on each line:

Gene1
Gene2
Gene3
...

# Output file
A comma separated values (CSV) file with the following columns:

TF - Motif name (specified by database)
TF Symbol - Gene symbol for motif that might be regulating genes in input list
TF Family - TF family for motif TF (http://tfclass.bioinf.med.uni-goettingen.de/) that might be regulating genes in input list
TF Family Members - Expanded list of gene symbols for TF family members that might be regulating genes in input list
Overlap - Number of genes overlapping between input list and TF target genes
Overlapping - Gene symbols of overlapping genes
All Genes - Number of genes in complete TF target gene set
Mapped Input Gene List - Number of input gene list symbols that were mapped to Entrez IDs
TF Targets - Number of TF target genes
P-Value - Hypergeometric CDF for enrichment of input gene list with TF target genes

# Example run
python find_TF_regulators.py --input=input.txt --output=out.csv

