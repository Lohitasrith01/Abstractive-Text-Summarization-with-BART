# 🧠 Abstractive Text Summarization with BART

This project fine-tunes Facebook's `bart-base` model on the [BillSum](https://huggingface.co/datasets/billsum) dataset for abstractive summarization. It includes data preprocessing, tokenization, model training, and evaluation using metrics like ROUGE, BLEU, and BERTScore.

## 🧰 Stack
- 🤗 Hugging Face Transformers & Datasets
- 🦾 BART (facebook/bart-base)
- 📊 Weights & Biases for tracking
- 📈 Evaluation: ROUGE, BLEU, BERTScore

## 🚀 Workflow
- Load & explore BillSum
- Tokenize with BART tokenizer (max_len=1024 for inputs, 256 for outputs)
- Fine-tune with `Seq2SeqTrainer` using mixed precision
- Evaluate with:
  - ROUGE scores (1, 2, L)
  - BLEU
  - BERTScore
- Visualize training and validation loss

## ⚙️ Results
Model trained for 3 epochs on 10k training samples + 1k test samples.

**Final scores:**
- ROUGE-1: ~19.3
- ROUGE-2: ~15.8
- ROUGE-L: ~18.8
- BLEU: ~2.8
- BERTScore (F1): ~85.48

## 📉 Challenges
- Input truncation due to token limits
- Inconsistent reference summary lengths

## 📎 Notes
- Tokenized dataset saved locally for efficiency
- WANDB tracking enabled for all runs

## 🛠️ Future Work
- Test on MultiNews dataset
- Try `facebook/bart-large` or `flan-t5-base`
- Integrate Pegasus or LongT5 for longer sequences

---
