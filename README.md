# diffexpr # 
[![CI](https://github.com/wckdouglas/diffexpr/workflows/CI/badge.svg)](https://github.com/wckdouglas/diffexpr/actions) [![codecov](https://codecov.io/gh/wckdouglas/diffexpr/branch/master/graph/badge.svg)](https://codecov.io/gh/wckdouglas/diffexpr)


A python package using ```rpy2``` to port [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html) into python.

## INSTALL ##
Dependencies are ```pandas``` (python), ```rpy2``` (python), and ```DESeq2``` (R)
Best way to build dependencies should be via conda. 

```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
conda create -q -n diffexpr python=3.6 \
    pandas tzlocal rpy2 biopython ReportLab pytest-cov \
    bioconductor-deseq2 codecov
conda activate diffexpr # activate diffexpr environment
Rscript setup.R #to install DESeq2 correctly 
python setup.py install
```

## Example ##
An example of running DESeq2 in *python* using ```diffexp``` package is provided [here](https://github.com/wckdouglas/diffexp/blob/master/example/deseq_example.ipynb).


## Citation ##
:bangbang: Please cite the original [DESeq2 paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-014-0550-8) if you used this package in your work:

```
@article{Love2014,
  doi = {10.1186/s13059-014-0550-8},
  url = {https://doi.org/10.1186/s13059-014-0550-8},
  year = {2014},
  month = dec,
  publisher = {Springer Science and Business Media {LLC}},
  volume = {15},
  number = {12},
  author = {Michael I Love and Wolfgang Huber and Simon Anders},
  title = {Moderated estimation of fold change and dispersion for {RNA}-seq data with {DESeq}2},
  journal = {Genome Biology}
}
```
