# Welcome to E-Utilities (site in progress)

E-Utilities is an Application Program Interface (API) that helps you gather data from most of the 40 NCBI databases (with greater than 1 billion records) residing at the NCBI. The databases include a variety of biomedical data, including biomedical literature nucleotide and protein sequences, gene records, gene expression, genotype and biological assay studies with data, chemical information, and three-dimensional molecular structures. There are about 25 million E-Utilities calls sent to our servers daily from about 100,000 different IP addresses.

Here are a few examples of what E-Utilities can do for you:

•	Search PubMed with a term and retrieve PMIDs (Add link here to ID)
•	Search MedGen with a SnoMedCI ID, then link over to GTR and retrieve their Summary info
•	Save a list of Gene IDs and fetch their full records
•	Save a PubChem Compound CID and retrieve the SDF-formatted record to showthe 3D coordinates in the Molecules App (ADD LINK HERE)

Users can access E-utilities by writing API queries and pasting them into any internet browser. 


## Quick Start

## Reference

## PubMed User Guide

Use our interactive API tester:

[Launch API Explorer](swagger-ui/index.html)


### This Site is a MkDocs Site
For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

! * `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
