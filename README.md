# Gender_Stereotyping_Artists

This repository contains codes to reproduce the results of the research paper "X". I have used Python to collect and clean data, and both Python and RStudio for text analysis. I have mentioned the runtime of each computationally expensive codes on top of it and the reproduction of the research requires following the file sequence in the `01_notebooks_&_py_files` folder. 

The following mermaid plot illustrates the data journey,

```mermaid
flowchart TD
    A[01_notebooks_&_py_files/01_data_collection.ipynb] -->|constructs raw data| B[(data)]
    B -->|Data goes for handcoding| C[[Handcoding]]
    C -->|Gender coded complete raw data| D[(01_notebooks_&_py_files/02_data_prep_sentiment.ipynb)]
    D -->|Prepares data for text analysis and saves the data| B
    D -->|Fitted plots| E((plot))
    D -->|Keyness, wordclouds, and corpus characteristics| F[(01_notebooks_&_py_files/03_exploratory.rmd)]
    F --> |Other plots|E
    F --> G[(01_notebooks_&_py_files/04_stm.rmd)]
    G --> |STM plots|E

```
