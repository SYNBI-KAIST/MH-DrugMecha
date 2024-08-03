# DrugMecha: A Knowledge Graph Database of Drug Mechanisms via Text Mining

## Overview
DrugMecha is a knowledge graph database designed to capture the mechanisms of drugs through text mining.<br>
It integrates various biological entities such as genes, cell lines, tissues, organisms, and biological functions to provide a comprehensive resource for understanding drug actions and their effects.

## Table of Contents
1. [Introduction](#introduction)
2. [Database Schema](#database-schema)
3. [Installation](#installation)

## Introduction
DrugMecha is developed by the Synergistic Bioinformatics Laboratory at the Korea Advanced Institute Science and Technology (KAIST).<br>
The database utilizes text mining techniques to extract and organize information about drug mechanisms from PubChem Bioassay Database.

## Database Schema
The database consists of several interconnected tables, each representing a different biological entity or relationship.<br>
Below is a brief description of each table and its columns:

![Schema of DrugMecha](https://github.com/SYNBI-KAIST/MH-DrugMecha/raw/main/DrugMecha/DrugMecha-Schema.png)

## DRUG_MECHANISM_FRAG

- **DRUG_MECHANISM_FRAG_ID**: Unique identifier for each drug mechanism fragment.
- **AID**: Assay identifier.
- **REGULATION**: Type of regulation (e.g., Upregulates, Regulates(Associates), Downregulates).
- **GENE_ID**: Gene identifier.
- **GENE_NAME**: Name of the gene.
- **FUNCTION_ID**: Function identifier.
- **FUNCTION_NAME**: Name of the function.
- **FUNCTION_TYPE**: Type of function.
- **CELL_LINE_ID**: Cell line identifier.
- **CELL_LINE_NAME**: Name of the cell line.
- **TISSUE_ID**: Tissue identifier.
- **TISSUE_NAME**: Name of the tissue.
- **ORGANISM_ID**: Organism identifier.
- **ORGANISM_NAME**: Name of the organism.

## SUBSTANCE_ACTIVITY

- **SID**: Substance identifier.
- **AID**: Assay identifier.
- **ACTIVITY**: Activity measure of the substance.

## ASSAY_ACTIVITY

- **AID**: Assay identifier.
- **SUBSTANCE_LIST**: List of substances tested in the assay.
- **ACTIVITY_LIST**: List of activity measures for the substances.
- **ACTIVITY_SCORE**: Overall activity score.

## GENE

- **GENE_ID**: Unique identifier for each gene.
- **GENE_NAME**: Name of the gene.
- **UMLS_ID**: Unified Medical Language System identifier.
- **UMLS_NAME**: UMLS name.
- **UNIPROT_GENE_NAME**: UniProt gene name.
- **NCBI_GENE_ID**: NCBI gene identifier.

## CELL_LINE

- **CELL_LINE_ID**: Unique identifier for each cell line.
- **CELL_LINE_NAME**: Name of the cell line.
- **PUBCHEM_ID**: PubChem identifier.
- **CELLOSAURUS_ID**: Cellosaurus identifier.
- **UMLS_ID**: Unified Medical Language System identifier.
- **CELL_ONTOLOGY_ID**: Cell Ontology identifier.

## TISSUE

- **TISSUE_ID**: Unique identifier for each tissue.
- **TISSUE_NAME**: Name of the tissue.
- **UMLS_ID**: Unified Medical Language System identifier.

## ORGANISM

- **ORGANISM_ID**: Unique identifier for each organism.
- **ORGANISM_NAME**: Name of the organism.
- **NCBI_TAXONOMY_ID**: NCBI Taxonomy identifier.

## FUNCTION_MAIN

- **FUNCTION_ID**: Unique identifier for each function.
- **FUNCTION_NAME**: Name of the function.
- **FUNCTION_TYPE**: Type of function.
- **GO_ID**: Gene Ontology identifier.
- **GO_TYPE**: Gene Ontology type.
- **UMLS_ID**: Unified Medical Language System identifier.
- **UMLS_TYPE**: UMLS type.
- **KEGG_ID**: KEGG pathway identifier.

## FUNCTION_OTHERS

- **FUNCTION_ID**: Unique identifier for each function.
- **FUNCTION_NAME**: Name of the function.
- **FUNCTION_TYPE**: Type of function.
- **PATHWAY_TYPE**: Type of pathway.
- **REACTOME_ID**: Reactome pathway identifier.
- **PUBCHEM_PATHWAY_ID**: PubChem Pathway identifier.
- **PATHBANK_ID**: PathBank identifier.
- **PANTHER_ID**: PANTHER pathway identifier.
- **BIOCYC_ID**: BioCyc identifier.
- **WIKIPATHWAYS_ID**: WikiPathways identifier.
- **SMPDB_ID**: Small Molecule Pathway Database identifier.
- **PATHWAY_INTERACTION_DATABASE_ID**: Pathway Interaction Database identifier.
- **PLANT_REACTOME_ID**: Plant Reactome pathway identifier.
- **PLANTCYC_ID**: PlantCyc identifier.
- **PATHWAY_COMMON_ID**: Pathway Commons identifier.
- **PANTHER_PATHWAY_ID**: PANTHER Pathway identifier.
- **CHEMFONT_ID**: ChemFont pathway identifier.
- **PHARMGKB_ID**: PharmGKB identifier.
- **LIPID_MAPS_ID**: LIPID MAPS pathway identifier.
- **BIOCARTA_ID**: BioCarta pathway identifier.
- **NETPATH_ID**: NetPath pathway identifier.

## Installation
To install DrugMecha, clone the repository from GitHub (except SUBSTANCE_ACTIVITY & ASSAY_ACTIVITY):

```sh
git clone https://github.com/your-repo/MH-DrugMecha.git
cd MH-DrugMecha
```

*SUBSTANCE_ACTIVITY and ASSAY_ACTIVITY files can be downloaded in each folder
