Emma Thomas & Matt Cefalu
12/15/2020

# Project name

This repo is intended as a template for research projects to ensure code is clearly documented and all outputs are reproducible. 
This is a suggested structure only and not intended to be comprehensive or the final word on reproducible workflow!

The information below should be updated to reflect the specifics of your project.

See [SETUP.md](SETUP.md) for instructions on how to initialize a new project repository using this template.

## Project description

Add a description of your project here!

## Directories

The basic directories included with this template are described below. If you have a lot of files, it may be useful to create additional subdirectories (e.g., data/raw and data/processed, results/figures and results/tables, e.t.c).

**Important Note:** all files in the [data](data) and [logs](logs) directories will be ignored (with the exception of any README.md files). In other words, changes to these files will not be tracked by git, and copies of these files will not be stored on gitlab. See the section on the .gitignore file below.

### [code](code)

Contains all code related to the project, including data cleaning and analysis. The names of code files should reflect the order in which they should be run: e.g., 0_processing_data.R, 1_analysis.R, 2_tables_and_figures.R, and so on. The [README.md](code/README.md) file in this directory should be used to give any further details necessary to replicate the analysis.

Folders can be created within the code directory to separate code for different sub-tasks.

### [data](data)

Contains all raw and processed data used in analysis. By default, the files in this directory are not tracked by git, and so will not be pushed to any remote host (e.g., GitHub). 
It is recommended that you *do not* store any data in other directories so that you do not accidentally push them to the remote host.

The [README.md](data/README.md) *is* tracked and should be used to describe the data files, including which raw files were copied over for this project, from where, and on what date. The intention is that a future reader should easily be able to find and copy over the data in order to replicate your analysis.

### [results](results)

Stores any and all outputs of the analysis, including print-outs, models, tables, figures, e.t.c.

### [logs](logs)

Contains any logs produced while running code (e.g., error logs). By default, the files in this directory are not tracked by git. 

## [.gitignore](.gitignore) file

The following is the default [.gitignore](.gitignore) file included in this directory. You can add lines to this file to ignore additional files or file types, or add new .gitignore files to specific directories; this may be particularly useful for large results files. However, it is recommended that you do not delete any of the lines below. In particular, *remember never to push sensitive data to GitHub*!

    data/*
    logs/*
    **/*.csv
    **/*.xlsx
    **/*.Rdata
    **/*.fst
    **/*.dta
    **/*.sas7bdat
    **/*.Rprofile
    **/*.Rproj
    **/*.DS_store
    !**/README.md

The above means that all files in the data and logs directories, other than any README.md files (last line), will be ignored by git. As such, copies of these files will not be stored on gitlab. In addition, common data types (.csv, .xlsx, .Rdata, .fst, .dta, and .sas7bdat) are automatically ignored just in case they appear in other directories. However, it is recommended to store all data, both raw and processed, in the data directory.

Typically, files that are ignored will be large and/or sensitive data files that should not be stored on GitHub, or large products of analysis that can be reproduced by running the code in the code directory.
