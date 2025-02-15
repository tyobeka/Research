# Investigating Subword Tokenization Strategies for the Translation of English to Low-Resource South African Languages

A description of the structure of each folder labelled: "eng-to-*tgt"
- *tgt = nso, nde, tso

## Raw text files:
- eng_to_*tgt_readme.txt
- eng.txt
- *tgt.txt
from https://hdl.handle.net/20.500.12185/572, https://hdl.handle.net/20.500.12185/406

## Notebooks:
The notebooks used for data cleaning include:
- `preprocessing_for_eng_to_*tgt.ipynb`: Code for data splitting, cleaning training and validation corpora
- `cleaning_test_sets.ipynb`: Code for cleaning global test set, i.e., removing  string that indicates which document the sentences were sourced from.

The notebooks used for tokenization:
- `standard-subword-tok-eng-to-*tgt.ipynb`: Code for tokenizing training and validation corpora using the standard subword tokenization methods, and converting tokenized sentences to numerical representations for modelling
- `subword-reg-eng-to-*tgt.ipynb`: Code for tokenizing training and validation corpora using the subword regularization methods, and converting tokenized sentences to numerical representations for modelling.
- `training-target-tokenizer.ipynb`: Code for training task-specific tokenizer for target language
- `mlm-tok.ipynb`: Code for tokenizing target language using the trained task-specific tokenizer for target language.
- `task-subword-tok.ipynb`: Code for converting tokenized sentences in the third experiment to numerical representations for modelling.

The notebooks used for NMT model training:
- `training-nmt.ipynb`: Code for training translation models for all experiments. 

The notebooks used for model evaluation:
- `evaluating-nmt.ipynb:` Code for generating predictions from test and global test corpora.
- `significance test.ipynb`: Code for computing BLEU scores and significance tests on post-processed predictions.

**Please note:** Recent updates in Google Colab have caused compatibility issues with the Fairseq toolkit, preventing the toolkit from running with the specified configuration in the notebooks. However, I have tried to include logs in the notebooks as evidence that models did indeed run.

## Folders:
The following folder contains the raw text file
- `Autshumato-Evaluation-Set`: Contains raw text files for global test corpora from https://repo.sadilar.org/handle/20.500.12185/506.

In the following folders you will find the outputs for each experiment:
- `bpe`: Contains the trained model folder for the BPE experiment, the folder includes the trained translation model, predictions, and the joint vocabularies.
- `ulm`: Contains the trained model folder for the ULM experiment, the folder includes the trained translation model, predictions, and the joint vocabularies.
- `bpeDROP`: Contains the trained model folder for the BPE-Dropout experiment, the folder includes the trained translation model, predictions, and the joint vocabularies.
- `ulmSR`: Contains the trained model folder for the ULM with subword regularization experiment, the folder includes the trained translation model, predictions, and the joint vocabularies.
- `target-tok`: Contains the trained model folder for task-specific tokenizer experiment, includes the trained translation model, trained target language tokenizer, predictions, and the joint vocabularies.
