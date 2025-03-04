# somascan analysis
A pipeline for the analysis of somascan readouts


# Files
Data doawnloaded from:  https://github.com/SomaLogic/SomaLogic-Data

```
library("SomaDataIO")

soma_obj <- read_adat("example_data.adat")
analyte_info <- getAnalyteInfo(soma_obj)
measurements <- as.data.frame(soma_obj)

write.table(analyte_info, file= "example_data_analyte.tsv", sep = "\t", row.names = FALSE)
write.table(measurements, file= "example_data_measurements.tsv", sep = "\t", row.names=FALSE)
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
