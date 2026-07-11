# gemma2_tuned

I built a QLoRA fine tuning project for Google's Gemma 2B Instruct model.

My project currently looks like this:

Base model: google/gemma-2-2b-it/n
Task: Supervised Fine Tuning (SFT), instruction tuning
Method: QLoRA
Quantization: 4-bit NF4 using BitsAndBytes
Trainer: trl.SFTTrainer
PEFT: LoRA adapters
Precision: FP16
Gradient checkpointing: Enabled
Batch size: 1 with gradient accumulation of 8
Target: Push the fine tuned model to your Hugging Face account (ciphermosaic/gemma-2-2b-sft)

The pipeline Iam implementing is roughly:

Load Gemma 2B Instruct.
Quantize it to 4-bit using BitsAndBytes.
Prepare it for k-bit (QLoRA) training.
Attach LoRA adapters.
Tokenize your instruction dataset.
Fine tune using SFTTrainer.
Evaluate the model.
Save the LoRA adapter.
Push the trained adapter to Hugging Face.
Publish the project on GitHub.


Star the repo if u liked it...
