# Model-eos6oli: Soltrannet-Aqueous-Solubility-Model

## Overview:
This repository houses all codes and datasets employed in the tasks of checking for bias, validating and reproducing the aqueous solubility model, eso6oli, which is a regression model that predicts the Log of solubility(LogS). 

## Abstract:
- Ersilia eso6oli is the SolTransNet model of SolTranNet−A Machine Learning Tool for Fast Aqueous Solubility Prediction [paper](https://pubmed.ncbi.nlm.nih.gov/34038123/) by Francoeur er al.
- SolTranNet is a molecule attention transformer MAT to predict aqueous solubility from a molecule's SMILES representation. It is a Regression model, that predicts LogS (log of the solubility) in order to help filter out insoluble compounds! The fine tuning of this mode is done with pertained model MAT, which applies self attention to a molecular graph representation of the molecule.
  

## Model Information:
- Eos Model ID: eos6oli
- Slug: soltrannet-aqueous-solubility
- Task: regression
- Input: Compound(canonicalsmiles)
- Output: Experimental value
- Interpretation: Predicted LogS (log of the solubility)

## Installation
- To deploy Ersilia to Google Colab; fetch, serve, and run predictions with a model, follow the steps listed [here](https://github.com/ersilia-os/ersilia/blob/master/notebooks/ersilia-on-colab.ipynb]).
- To install SolTranNet on Google Colab, test, and run predictions with it, follow the steps listed [here](https://github.com/gnina/SolTranNet/blob/main/README.md)

## Structural organisation:
This repository is organised by folders:
- **data**: Contains the raw data, processed data and Model predictions.
- **figures**: Contains a collection of visualizations presented in PNG format..
- **Notebooks**: Houses the jupyter notebook files where most of the developmen took place.
- **src**: Contains important functions I will re-use throughout the repository, to avoid typing them each time.


## Steps to Reproduce The Solutions to These Tasks:
### Task 1 (Model's(eos6oli) Bias Evaluation):
- From the list of the models provided in the [Ersilia Book](https://ersilia.gitbook.io/ersilia-book/contributors/internships/outreachy-summer-2024), I selected tthe model of my choice which is [Aqueous Solubility Model](https://github.com/ersilia-os/eos6oli), especially because the model's publication, aim, and methodology resonated with me.
- I then went on to create a repository that contained all the files and datasets needed for the project.
- For my task 1, I downloaded the [dataset](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/solubility-dataset.csv) from the public repository of [Harvard Dataverse](https://dataverse.harvard.edu/). With this [dataset](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/solubility-dataset.csv), I was able, through random sampling, to generate the [1000 molecules](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/1000_molecules.csv) after proper data cleaning and preprocessing steps.
- I then went on to deploy Ersilia Model Hub to Google Colab, fetched and served the model, eso6oli. After serving the model, I ran prediction on the model [1000 molecules](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/1000_molecules.csv) using the model to generate these [Predictions](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/1000_molecules_predictions.csv).
- With the [Predictions](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/1000_molecules_predictions.csv), I was able to look into the model bias through the insights gathered from these [visualisations](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/tree/main/figures/Task(1)%20figures).
- The notebook containing the solution to task 1 can be found [here](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/Notebooks/Week2_Task1.ipynb).

## Task 2(Model's Reproducibilty):
- I installed, and tested the functionality of SolTranNet on Google Colab.
- After confirming that the model was working properely, I went on to run prediction on the [1000 molecules](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/1000_molecules.csv) and thereafter, saved the [predictions](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/Soltranet_pred.csv).
- I went on to evaluate the [predictions](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/data/Soltranet_pred.csv); employing these [visualisations](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/tree/main/figures/Task(2)%20figures/Model%20Bias%20vis) to gather insights from the model's performance and suprisingly to me, it corresponded with what I got earlier when eos6oli from the Ersilia Model Hub acted on the same dataset, thus, confirming the reproducibility of the model, eos6oli.
- To further confirm this reproducibility, I compared directly the predictions from both SolTranNet and eos6oli from the Ersilia Model Hub by merging the both predictions into a single DataFrame. With the use of [scatter plot](https://github.com/Nwuguru-Chidiebere-Sullivan/Outreachy-Ersilia-Project-Week2-Tasks/blob/main/figures/Task(2)%20figures/reproducibility%20viz/repro_scatter_plot.png)  and the 




  
