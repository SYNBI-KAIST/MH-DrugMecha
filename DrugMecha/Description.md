# DrugMecha: An Ontology-based Knowledge Graph Database of Drug Mechanisms via Text Mining

## Overview
DrugMecha is an ontology-based knowledge graph database designed to capture the mechanisms of drugs through text mining. 
It integrates various biological entities such as genes, cell lines, tissues, organisms, and biological functions to provide a comprehensive resource for understanding drug actions and their effects.

## Table of Contents
1. [Introduction](#introduction)
2. [Database Schema](#database-schema)
3. [Installation](#installation)
4. [Usage](#usage)
5. [License](#license)
6. [Contributing](#contributing)
7. [Acknowledgements](#acknowledgements)

## Introduction
DrugMecha is developed by the Synergistic Bioinformatics Laboratory at the Korea Advanced Institute Science and Technology (KAIST). The database utilizes text mining techniques to extract and organize information about drug mechanisms from various biomedical literature sources.

## Database Schema
The database consists of several interconnected tables, each representing a different biological entity or relationship. Below is a brief description of each table and its columns:

![Architecture of DrugMecha](https://github.com/SYNBI-KAIST/DrugMecha/blob/main/Overview.png)

### DRUG_MECHANISM
- **DRUG_MECHANISM_ID**: Unique identifier for each drug mechanism entry.
- **AID**: Assay ID associated with the drug mechanism.
- **REGULATION**: Type of regulation (e.g., upregulates, downregulates).
- **GENE_ID**: Unique identifier for the associated gene.
- **GENE_NAME**: Name of the associated gene.
- **FUNCTION_ID**: Unique identifier for the associated biological function.
- **FUNCTION_NAME**: Name of the associated biological function.
- **FUNCTION_TYPE**: Type of biological function (e.g., molecular function, biological process).
- **CELL_LINE_ID**: Unique identifier for the associated cell line.
- **CELL_LINE_NAME**: Name of the associated cell line.
- **TISSUE_ID**: Unique identifier for the associated tissue.
- **TISSUE_NAME**: Name of the associated tissue.
- **ORGANISM_ID**: Unique identifier for the associated organism.
- **ORGANISM_NAME**: Name of the associated organism.

### GENE
- **GENE_ID**: Unique identifier for the gene.
- **GENE_NAME**: Name of the gene.
- **UMLS_ID**: Unified Medical Language System ID.
- **UMLS_NAME**: UMLS name.
- **UNIPROT_GENE_NAME**: UniProt gene name.
- **NCBI_GENE_ID**: NCBI gene ID.

### CELL_LINE
- **CELL_LINE_ID**: Unique identifier for the cell line.
- **CELL_LINE_NAME**: Name of the cell line.
- **PUBCHEM_ID**: PubChem ID.
- **CELLOSAURUS_ID**: Cellosaurus ID.
- **UMLS_ID**: UMLS ID.
- **CELL_ONTOLOGY_ID**: Cell Ontology ID.

### TISSUE
- **TISSUE_ID**: Unique identifier for the tissue.
- **TISSUE_NAME**: Name of the tissue.
- **UMLS_ID**: UMLS ID.

### ORGANISM
- **ORGANISM_ID**: Unique identifier for the organism.
- **ORGANISM_NAME**: Name of the organism.
- **NCBI_TEXONOMY_ID**: NCBI Taxonomy ID.

### BIOLOGICAL_FUNCTION
- **FUNCTION_ID**: Unique identifier for the biological function.
- **FUNCTION_NAME**: Name of the biological function.
- **FUNCTION_TYPE**: Type of biological function.
- **GO_ID**: Gene Ontology ID.
- **GO_TYPE**: Type of Gene Ontology term.
- **UMLS_ID**: UMLS ID.
- **UMLS_TYPE**: Type of UMLS entry.
- **PATHWAY_TYPE**: Type of pathway.
- **REACTOME**: Reactome pathway ID.
- **PUBCHEM_PATHWAY_ID**: PubChem pathway ID.
- **PATHBANK**: PathBank ID.
- **PANTHER**: PANTHER pathway ID.
- **BIOCYC**: BioCyc pathway ID.
- **WIKIPATHWAYS**: WikiPathways ID.
- **SMPDB**: Small Molecule Pathway Database ID.
- **KEGG**: KEGG pathway ID.
- **PLANT_REACTOME**: Plant Reactome ID.
- **PLANTCYC**: PlantCyc ID.
- **PATHWAY_COMMON**: Pathway Commons ID.
- **PANTHER_PATHWAY**: PANTHER pathway ID.
- **CHEMFONT**: ChemFont pathway ID.
- **PHARMGKB**: PharmGKB pathway ID.
- **LIPID_MAPS**: LIPID MAPS ID.
- **BIOCARTA**: BioCarta pathway ID.
- **NETPATH**: NetPath ID.

### SUBSTANCE_ACTIVITY
- **SID**: Substance ID.
- **AID**: Assay ID.
- **METAPATH_ID**: Metapath ID.
- **ACTIVE**: Active status.
- **INACTIVE**: Inactive status.
- **ACTIVITY_SCORE**: Activity score.

## Installation
To install DrugMecha, clone the repository from GitHub:

```sh
git clone https://github.com/your-repo/MH-DrugMecha.git
cd MH-DrugMecha
