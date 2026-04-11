# Cynaptics_Induction_2
Built my own GPT and Fine-Tuned a pre-trained GPT 

**TASK 1** 

**GPT-Style Language Model (Tiny Shakespeare Dataset)**

**Overview**

This project implements a decoder-only Transformer (GPT-style model) trained on the Tiny Shakespeare dataset to generate text. My GPT-2 consists of 2.1 M parameters. 

**Features**
- Used GPT-2’s pretrained BPE tokenizer, which has a ~50k subword vocabulary
- Multi-head self-attention
- Transformer blocks with residual connections
- Warmup Cosine learning rate scheduler
- Autoregressive text generation

**Architecture**
- Token + Positional Embeddings
- Stacked Transformer Blocks
  - Multi-Head Self-Attention
  - Feedforward Network
  - Layer Normalization + Residual Connections
- Final Linear layer (LM Head)

**Training Details**
- Loss: CrossEntropyLoss
- Optimizer: AdamW
- Scheduler: Warmup + Cosine Decay
- Dataset: Tiny Shakespeare

**Generation**
- Sampling: Multinomial sampling
- Temperature-controlled randomness
- Autoregressive token generation

**Sample Output**

GLOUCESTER:
My pardon our feigned hard, madam.
Your target you, 'tis past twenty
Than, and beautify your disposition, great ages unparallel'd.

ISABELLA:
Truly, sir, tempting more sixteen our foul journey,
After show have warmth with succor a sweet?
Ah, PETRUCHIO Then that in the nose stand o' that told him.
Now, Like pain fellow?

JULIET:
Well, is same friends wife's that not must:
See, who sure palms;
Affection, Made deed,
Grace my state of refined
And kings shall move me I, to your hat stand for;
He never ne'er make wine his waving than, thrice thou queen:
What shall appeach I am charged with blasphemy in a blood,
Nor your pleading but a blow of Exeter;
Good Even hour but behind the elflocks of our old pleasing
And stole upon the white thing, what short or.
Speak Show art on your father
Our daintiest I did.'


**TASK 2**

**GPT-2 Fine-Tuning (Alpaca Dataset)**

**Overview**

This project performs Supervised Fine-Tuning (SFT) of a pretrained GPT-2 model on the Alpaca instruction dataset to generate instruction-following responses.

**Features**
- Instruction-based prompt formatting (Alpaca style)
- Fine-tuning pretrained GPT-2 with 124M parameters.
- Mixed precision training (FP16) using autocast
- Gradient accumulation for memory efficiency
- Periodic checkpoint saving

**Dataset**
- Source: Alpaca dataset
- Format: Instruction → Input → Response

**Architecture**
- Pretrained GPT-2 (decoder-only Transformer)
- Token embeddings + positional embeddings
- Causal self-attention with masking
- Language modeling head for token prediction

**Training Details**
- Loss: CrossEntropyLoss 
- Optimizer: AdamW
- Learning Rate: 5e-5
- Epochs: 1
- Mixed Precision: Enabled (faster + memory efficient)

**Prompt Design**
Structured format:
- Instruction
- Input (optional)
- Response
Helps model learn instruction-following behavior

**Output**
- Fine-tuned model saved locally (./gpt2-alpaca)
- Generates human-like responses to instructions
