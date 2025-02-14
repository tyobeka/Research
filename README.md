# Research

## Investigating Subword Tokenization Strategies for the Translation of English to Low-Resource South African Languages

Structure of Folder:
*tgt = nso, nde, tso

### Raw text files
- eng_to_*tgt_readme.txt
- eng.txt
- *tgt.txt

### Notebooks:
- preprocessing_for_eng_to_*tgt.ipynb: Code for data splitting, cleaning training and validation corpora
- standard-subword-tok-eng-to-*tgt.ipynb: Code for tokenizing training and validation corpora using the standard subword tokenization methods + converting tokenized sentences to numerical representations for modelling
- subword-reg-eng-to-*tgt.ipynb: Code for tokenizing training and validation corpora using the subword regularization methods + converting tokenized sentences to numerical representations for modelling.
- training-target-tokenizer.ipynb: Code for training task-specific tokenizer for target language
- mlm-tok.ipynb: Code for tokenizing target language using the trained task-specific tokenizer for target language.
- task-subword-tok.ipynb: Code for converting tokenized sentences in the third experiment to numerical representations for modelling.
- training-nmt.ipynb: Code for training translation models for all experiments.
- cleaning_test_sets.ipynb: Code for cleaning global test set, i.e., removing  string that indicates which document the sentences were sourced from.
- evaluating-nmt.ipynb: Code for generating predictions and evaluating predictions on test and global test corpora.
- significance test.ipynb: Code for conducting significance test on post-processed predictions.

### Folders:
- Autshumato-Evaluation-Set: Contains raw text files for global test corpora
- bpe: Contains the trained model folder for BPE experiment, the folder includes trained translation model, predictions, and the joint vocabulary.
- ulm: Contains the trained model folder for ULM experiment, the folder includes trained translation model, predictions, and the joint vocabulary.
- bpeDROP: Contains the trained model folder for BPE-Dropout experiment, the folder includes trained translation model, predictions, and the joint vocabulary..
- ulmSR: Contains the trained model folder for ULM with subword regularization experiment, the folder includes trained translation model, predictions, and the joint vocabulary..
- target-tok: Contains the trained model folder for task-specific tokenizer experiment, includes trained translation model, trained target language tokenizer, predictions, and the joint vocabulary.
