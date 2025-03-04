# somascan analysis
A pipeline for the analysis of somascan readouts


# Files
Data downloaded from:  https://github.com/SomaLogic/SomaLogic-Data

here is the R code used to save the two files, analyte info and measurements. 

```
library("SomaDataIO")

soma_obj <- read_adat("example_data.adat")
analyte_info <- getAnalyteInfo(soma_obj)
measurements <- as.data.frame(soma_obj)

write.table(analyte_info, file= "example_data_analyte.tsv", sep = "\t", row.names = FALSE)
write.table(measurements, file= "example_data_measurements.tsv", sep = "\t", row.names=FALSE)
```

# Import

CSV importer was used to import both files

```
example_data_analyte.tsv
example_data_measurements.tsv
```

During import, the advanced button was used to gather the colmuns with pattern `seq`
The following was used as the names and values of the gathered columns.

```
seqId_value
seqId_name
```


# Preprocessing

* log10

# Differential Analysis

* limma


# Biological Analysis

Reactome Pathways Download
https://reactome.org/download/current/UniProt2Reactome.txt

* GSEA

# Export

* Limma Results
* Pathway NES Results
