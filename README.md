## Passenger flow prediction

This repository contains code, data, and results for generating security checkpoint data using a Tabular Variational Autoencoder (TVAE). It includes data preprocessing and visualization, model training, synthesization and downstream tasks analysis.

### Repository Structure

- **data_processing.ipynb**  
  Notebook for initial data cleaning, feature engineering, and prepping downstream datasets.

- **descriptives.ipynb**  
  Exploratory data analysis and descriptive statistics of the security checkpoint data.

- **tvae_train.ipynb**  
  Training workflow for the Tabular Variational Autoencoder model on the training data.

- **downstream_tasks.ipynb**  
  Implements downstream analyses (regression) using real and synthetic data.

- **security_checkpoint_data.xlsx**  
  Raw security checkpoint data (Excel) with passenger and screening station metadata.

- **train_data_tvae.csv**  
  Preprocessed training dataset used as input to the TVAE.

- **processed_data.csv**  
  Final processed dataset after feature engineering, joins, and cleaning.

- **tvae_only_project/**  
  Directory containing additional scripts or submodules specific to the TVAE implementation.

- **tvae_synthesizer.pkl**  
  Pickled synthesizer object used to generate synthetic samples from the TVAE latent space.

- **requirements.txt**  
  List of Python dependencies and their versions required to run the notebooks and scripts.

### Installation

**Prerequisites**

- Python 3.12 or higher

1. **Clone the repository**

   ```bash
   git clone https://github.com/SynthAIr/passengerflow.git
   cd passengerflow
   ```

2. **Create and activate a Python environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install requirements**

   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. **Data Preprocessing**  
   Open and run `data_processing.ipynb` to load raw data, perform cleaning, feature engineering, and export `processed_data.csv`.

2. **Descriptive Analysis**  
   Use `descriptives.ipynb` for exploratory analysis of processed data, including plots and summary tables.

3. **Model Training**  
   Execute `tvae_train.ipynb` to train the TVAE on `train_data_tvae.csv`. The trained model will be saved as `trained_tvae.pkl`.

4. **Synthetic Data Generation**  
   Load `tvae_synthesizer.pkl` in `downstream_tasks.ipynb` or custom scripts to generate synthetic samples.

5. **Downstream Evaluation**  
   Run `downstream_tasks.ipynb` to evaluate classification or regression tasks using both real and synthetic data.

## Attributions

- **TVAE implementation** adapted from [sdv-dev/CTGAN](https://github.com/sdv-dev/CTGAN), licensed under MIT.


### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
