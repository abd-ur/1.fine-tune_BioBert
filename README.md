# 1.fine-tune_BioBert (Assignment 1)

Here, we have used pretrained BioBERT model v1.1 from Transformers. Goal is to fine-tune it using provided genomic variants(variants.json).

Part 1
1. Loaded JSON data into python (Hugging Face Dataset)
2. Created training pairs between input: Query and output: Label
3. Split data into train/val/test sets (30%/15%/15%) with balanced cancer subtypes. However, due to odd number of variants in test+val set, val set contains one variant more than set test
4. Tokenzied the data using BioBert tokenizer with max_len=128

Part 2
1. Loaded BioBERT from Transformers
2. Implemented trainer API for sequence classification
3. Hyperparameters introduced as instructed - LR=2e-5, epochs=3, batch=16
4. Tested separately with LoRA for efficiency
5. Trained the setup on Google Colab T4 GPU

Important Points to Consider:
1. Didnt go for T5-style generation, it would introduce hallucination given shortage of dataset
2. NoteBook preview doesnt appears due to metadata error. Download or visit notebook @ https://colab.research.google.com/drive/1tfSbsaHb54EdOE2QorwpGppnRFlLnFyr?usp=sharing
3. Trained model pushed to HF @ https://huggingface.co/abd-ur/results
