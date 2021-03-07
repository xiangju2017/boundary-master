
## Pre-trained Models
Download the pre-trained models from 
* [SpanBERT (large & cased)](https://dl.fbaipublicfiles.com/fairseq/models/spanbert_hf.tar.gz): 24-layer, 1024-hidden, 16-heads, 340M parameters
 and put it in bert_base_en file

## Fine-tuning


```bash
python code/train.py \
  --train_file train-v1.1.json \
  --dev_file dev-v1.1.json \
  --train_batch_size 32 \
  --eval_batch_size 32  \
  --learning_rate 2e-5 \
  --num_train_epochs 4 \
  --max_seq_length 512 \
  --doc_stride 128 \
  --eval_metric f1 \
  --output_dir squad_output \
  --fp16
```

