# Deep dive in "Neural Networks: Zero to Hero"

At this repo i try deep dive in to ["Neural Networks: Zero to Hero"](https://karpathy.ai/zero-to-hero.html) course from Andrej Karpathy

Short description of the course:

A course by Andrej Karpathy on building neural networks, from scratch, in code.
We start with the basics of backpropagation and build up to modern deep neural networks, like GPT. In my opinion language models are an excellent place to learn deep learning, even if your intention is to eventually go to other areas like computer vision because most of what you learn will be immediately transferable. This is why we dive into and focus on languade models.
Prerequisites: solid programming (Python), intro-level math (e.g. derivative, gaussian).

The github repo for the course: https://github.com/karpathy/nn-zero-to-hero

---

[ ] [The spelled-out intro to neural networks and backpropagation: building micrograd](https://www.youtube.com/watch?v=VMj-3S1tku0&ab_channel=AndrejKarpathy) 2h 25m

> This is the most step-by-step spelled-out explanation of backpropagation and training of neural networks. It only assumes basic knowledge of Python and a vague recollection of calculus from high school.

---

[ ] [The spelled-out intro to language modeling: building makemore](https://www.youtube.com/watch?v=PaCmpygFfXo&ab_channel=AndrejKarpathy) 1h 57m

> We implement a bigram character-level language model, which we will further complexify in followup videos into a modern Transformer language model, like GPT. In this video, the focus is on (1) introducing torch.Tensor and its subtleties and use in efficiently evaluating neural networks and (2) the overall framework of language modeling that includes model training, sampling, and the evaluation of a loss (e.g. the negative log likelihood for classification).

---

[ ] [Building makemore Part 2: MLP](https://www.youtube.com/watch?v=TCH_1BHY58I&ab_channel=AndrejKarpathy) 1h 15m

> We implement a multilayer perceptron (MLP) character-level language model. In this video we also introduce many basics of machine learning (e.g. model training, learning rate tuning, hyperparameters, evaluation, train/dev/test splits, under/overfitting, etc.).

---

[ ] [https://www.youtube.com/watch?v=P6sfmUTpUmc&ab_channel=AndrejKarpathy](Building makemore Part 3: Activations & Gradients, BatchNorm) 1h 55m

> We dive into some of the internals of MLPs with multiple layers and scrutinize the statistics of the forward pass activations, backward pass gradients, and some of the pitfalls when they are improperly scaled. We also look at the typical diagnostic tools and visualizations you'd want to use to understand the health of your deep network. We learn why training deep neural nets can be fragile and introduce the first modern innovation that made doing so much easier: Batch Normalization. Residual connections and the Adam optimizer remain notable todos for later video.

---

[ ] [Building makemore Part 4: Becoming a Backprop Ninja](https://www.youtube.com/watch?v=q8SA3rM6ckI&ab_channel=AndrejKarpathy) 1h 55m

> We take the 2-layer MLP (with BatchNorm) from the previous video and backpropagate through it manually without using PyTorch autograd's loss.backward(): through the cross entropy loss, 2nd linear layer, tanh, batchnorm, 1st linear layer, and the embedding table. Along the way, we get a strong intuitive understanding about how gradients flow backwards through the compute graph and on the level of efficient Tensors, not just individual scalars like in micrograd. This helps build competence and intuition around how neural nets are optimized and sets you up to more confidently innovate on and debug modern neural networks.

---

[ ] [Building makemore Part 5: Building a WaveNet](https://www.youtube.com/watch?v=t3YJ5hKiMQ0&ab_channel=AndrejKarpathy) 56m

> We take the 2-layer MLP from previous video and make it deeper with a tree-like structure, arriving at a convolutional neural network architecture similar to the WaveNet (2016) from DeepMind. In the WaveNet paper, the same hierarchical architecture is implemented more efficiently using causal dilated convolutions (not yet covered). Along the way we get a better sense of torch.nn and what it is and how it works under the hood, and what a typical deep learning development process looks like (a lot of reading of documentation, keeping track of multidimensional tensor shapes, moving between jupyter notebooks and repository code, ...).

---

[ ] [Let's build GPT: from scratch, in code, spelled out.](https://www.youtube.com/watch?v=kCc8FmEb1nY&ab_channel=AndrejKarpathy) 1h 56m

> We build a Generatively Pretrained Transformer (GPT), following the paper "Attention is All You Need" and OpenAI's GPT-2 / GPT-3. We talk about connections to ChatGPT, which has taken the world by storm. We watch GitHub Copilot, itself a GPT, help us write a GPT (meta :D!) . I recommend people watch the earlier makemore videos to get comfortable with the autoregressive language modeling framework and basics of tensors and PyTorch nn, which we take for granted in this video.

---

[ ] [Let's build the GPT Tokenizer](https://www.youtube.com/watch?v=zduSFxRajkE&ab_channel=AndrejKarpathy)

> The Tokenizer is a necessary and pervasive component of Large Language Models (LLMs), where it translates between strings and tokens (text chunks). Tokenizers are a completely separate stage of the LLM pipeline: they have their own training sets, training algorithms (Byte Pair Encoding), and after training implement two fundamental functions: encode() from strings to tokens, and decode() back from tokens to strings. In this lecture we build from scratch the Tokenizer used in the GPT series from OpenAI. In the process, we will see that a lot of weird behaviors and problems of LLMs actually trace back to tokenization. We'll go through a number of these issues, discuss why tokenization is at fault, and why someone out there ideally finds a way to delete this stage entirely.

---

The target:

- [ ] gaining experience in nn, understand how it works
- [ ] gaining experience using uv
- [ ] ability to use python, uv and jupyter

Useful links:

- https://karpathy.ai/
- https://www.youtube.com/@AndrejKarpathy/videos
- https://github.com/karpathy/micrograd
