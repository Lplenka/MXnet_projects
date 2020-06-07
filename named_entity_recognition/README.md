## Running the code

1. Clone this repo
2. Train the model: `$ cd src && python ner.py`

To reproduce the preprocessed training data:

1. Download and unzip the data: https://www.kaggle.com/abhinavwalia95/entity-annotated-corpus/downloads/ner_dataset.csv
2. Move ner_dataset.csv into `./data`
3. `$ cd src && python preprocess.py`
