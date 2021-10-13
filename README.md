# Using Clinical Drug Representations for Improving Mortality and Length of Stay Predictions



## Usage

1. Clone the code to local.   
```
https://github.com/tanlab/MIMIC-III-Clinical-Drug-Representations.git
cd MIMIC-III-Clinical-Drug-Representations
```
2. Run MIMIC-Extract Pipeline as explained in https://github.com/MLforHealth/MIMIC_Extract.   

3. Copy the output file of MIMIC-Extract Pipeline named `all_hourly_data.h5` to `mimic-extract` folder.

4. Copy the `ADMISSIONS.csv`, `PRESCRIPTIONS.csv`, `ICUSTAYS.csv` files into `mimic-iii` folder.

5. Run `01-MIMIC-III-Drugs-Names-To-Pubchem-ID.ipynb` to convert MIMIC-III Drug names into Pubchem ID.

6. Download drug information via FDA. https://www.fda.gov/drugs/drug-approvals-and-databases/national-drug-code-directory. 

7. Run `02-Create-Cohort.ipynb` to select correct drugs for patients and create the final cohort.

8. Run `03-Embeddings.ipynb` to get embeddings of drugs.

9. Run `04-Timeseries.ipynb` to run timeseries baseline model to predict 4 different clinical tasks.

10. Run `05-ECFP-1024-TimeSeries.ipynb` to run ECFP multimodal baseline to predict 4 different clinical tasks.

11. Run `6-Smiles-Transformer-TimeSeries.ipynb` to run Transformers multimodal baseline to predict 4 different clinical tasks.


## References

Download the MIMIC-III dataset via https://mimic.physionet.org/

MIMIC-Extract implementation: https://github.com/MLforHealth/MIMIC_Extract

