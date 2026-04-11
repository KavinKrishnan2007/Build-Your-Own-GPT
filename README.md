# Cynaptics_Induction_2
Built my own GPT and Fine-Tuned a pre-trained GPT 

**TASK 1** 

**GPT-Style Language Model (Tiny Shakespeare Dataset)**

**Overview**

This project implements a decoder-only Transformer (GPT-style model) trained on the Tiny Shakespeare dataset to generate text.

**Features**
- Custom tokenization using regex
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
