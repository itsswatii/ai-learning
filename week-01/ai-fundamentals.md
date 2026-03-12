# AI Fundamentals

## Overview

This document covers the foundational concepts behind Artificial Intelligence — what it is, how it evolved, and how modern systems like large language models actually work under the hood. Understanding these fundamentals is what separates someone who uses AI tools from someone who can think critically about them.

---

## A Century of Predictions

In 1925, a British engineer named Archibald Low wrote a book predicting what life would look like in 2025. He imagined wall-mounted televisions, climate-controlled rooms, and instantaneous access to global information. Nearly everything he predicted came true.

What he got wrong? He thought every man in 2025 would be bald from wearing hats too often.

The point isn't that he was a prophet — it's that *transformative technology often arrives sooner than sceptics expect and differently than optimists imagine*. AI is no different.

---

## A Timeline of AI Milestones

AI didn't emerge overnight. It was built across decades of incremental breakthroughs — grouped below into four distinct eras:

```mermaid
%%{init: { 'theme': 'base', 'themeVariables': { 'fontSize': '18px', 'cScale0': '#6b9fb8', 'cScale1': '#7daa8a', 'cScale2': '#9b86b8', 'cScale3': '#c4956a' } } }%%
timeline
    title The Evolution of Artificial Intelligence

    section The Foundations
        1943 : McCulloch & Pitts Neural Model
        1950 : Turing Test Proposed
        1955 : Logic Theorist — First AI Program
        1956 : Term AI Coined by John McCarthy

    section Early Intelligence
        1958 : Perceptrons Introduced
        1965 : ELIZA Chatbot
        1969 : Shakey the Robot

    section Rise of Machine Learning
        1997 : Deep Blue Defeats Kasparov
        2011 : IBM Watson Wins Jeopardy
        2012 : Google Brain Identifies Cats

    section The Generative Era
        2017 : Attention Is All You Need
        2020 : GPT-3 Released
        2022 : ChatGPT Launches
```

The table below expands on what each milestone actually meant:

| Year | Milestone | Significance |
|---|---|---|
| 1943 | McCulloch & Pitts Neural Model | First mathematical model of a neuron |
| 1950 | Turing Test Proposed | Set the benchmark: can a machine think? |
| 1955 | Logic Theorist | First AI program — proved machines can reason |
| 1956 | Term "AI" Coined | John McCarthy formalises the field |
| 1958 | Perceptrons Introduced | Machines could learn from data, not just rules |
| 1965 | ELIZA Chatbot | Early NLP — users were fooled into thinking it was human |
| 1997 | Deep Blue Defeats Kasparov | AI beat the world chess champion |
| 2011 | IBM Watson Wins Jeopardy | AI handled unstructured, ambiguous language |
| 2017 | "Attention Is All You Need" | Transformer architecture introduced |
| 2020 | GPT-3 Released | Foundation models become viable at scale |
| 2022 | ChatGPT Launches | Generative AI goes mainstream |

There were also *AI winters* — periods in the 1970s–80s when funding dried up and progress stalled, mostly because hardware wasn't powerful enough and data wasn't plentiful enough. The lesson: good ideas still need the right infrastructure to flourish.

---

## What Is Artificial Intelligence?

At its core, AI is **the simulation of human intelligence in machines** — building systems that can learn from experience, reason about problems, and adapt to new situations.

A useful analogy: imagine you've been asked to learn and explain a topic you've never studied before — say, aerospace engineering. You'd read books, search for articles, synthesize notes, and then explain the concept in your own words. You wouldn't copy-paste; you'd genuinely generate an understanding. That's what AI aims to replicate.

---

## Traditional AI vs. Generative AI

This distinction is critical to understand, especially for career positioning.

| | Traditional AI | Generative AI |
|---|---|---|
| **Era** | Pre-2022 mainstream | Post-2022 mainstream |
| **Scope** | One model per task | One model, many tasks |
| **Access** | Requires programming skills | Natural language interface |
| **Output** | Predictions and classifications | New content — text, images, code, audio |
| **Example** | Fraud detection model | ChatGPT drafting, summarising, translating |

The shift from Traditional to Generative AI is what made **prompt engineering** the new power skill. You no longer need to code a model; you need to know how to communicate with one.

---

## How the Brain Inspired Neural Networks

The human brain has roughly 100 billion neurons. Each neuron receives signals, processes them, and passes output to the next neuron. Connections strengthen or weaken based on experience — that's how learning happens. Artificial Neural Networks mirror this structure directly.

```mermaid
flowchart LR
    subgraph IL[Input Layer]
        I1([Input 1])
        I2([Input 2])
        I3([Input 3])
    end

    subgraph HL[Hidden Layers]
        H1([Neuron A])
        H2([Neuron B])
        H3([Neuron C])
        H4([Neuron D])
    end

    subgraph OL[Output Layer]
        O1([Result])
    end

    I1 --> H1
    I1 --> H2
    I2 --> H2
    I2 --> H3
    I3 --> H3
    I3 --> H4
    H1 --> O1
    H2 --> O1
    H3 --> O1
    H4 --> O1
```

The more hidden layers a network has, the "deeper" it is — hence the term **Deep Learning**. Deep networks can model complex, non-linear patterns in data that shallow networks cannot.

> **Key stat:** GPT-3 has 175 billion parameters — the adjustable weights across all connections. That exceeds the estimated 100 billion neurons in a human brain, though the comparison isn't perfectly apples-to-apples.

**Real-world example — Tesla Autopilot:**
Camera input → Deep neural network → Identifies lanes, pedestrians, traffic signs → Calculates steering, braking, and acceleration — all within milliseconds.

---

## How AI Learns: Three Training Paradigms

Understanding how models are trained helps you use them more intelligently.

```mermaid
flowchart LR
    D[Training Data] --> SL[Supervised Learning]
    D --> UL[Unsupervised Learning]
    D --> SSL[Self-Supervised Learning]

    SL --> SL1[Labeled input-output pairs]
    SL1 --> SL2[Spam filters, Sentiment analysis]

    UL --> UL1[No labels — finds patterns]
    UL1 --> UL2[Customer segmentation, Anomaly detection]

    SSL --> SSL1[Data labels itself from context]
    SSL1 --> SSL2[LLM pre-training, Next-word prediction]
```

**1. Supervised Learning** — The model trains on labeled examples, like a student studying with an answer key. Powerful but expensive — requires humans to label thousands or millions of data points.

**2. Unsupervised Learning** — The model finds patterns without being told what to look for. Think of sorting a mixed bag of items by similarity without knowing their names.

**3. Self-Supervised Learning** — The model generates its own labels from raw data. The surrounding text in a sentence *is* the label. This is how LLMs are pre-trained and why they can learn from virtually unlimited data without expensive human annotation.

---

## Generative Models — How AI Creates

The question many people ask: is AI just copy-pasting from its training data? The answer is no.

Generative models learn the *underlying patterns* of data, not specific examples. Once trained, they produce entirely new outputs that fit those patterns.

**Analogy:** Show a child hundreds of photos of animals. After a while, ask the child to draw an animal they've never seen. They'll draw something plausible — four legs, fur, eyes — because they've internalized the *rules*, not the *images*. AI works the same way.

**Two key generative architectures before Transformers:**

**GANs (Generative Adversarial Networks)** — Two neural networks compete against each other to produce increasingly realistic outputs.

```mermaid
flowchart LR
    RD([Real Data]) --> DM([Discriminator])
    GN([Generator]) --> DM
    DM -->|Real| OUT([Realistic Output])
    DM -->|Fake — improve| GN
```

The Generator creates fake samples. The Discriminator decides if each sample is real or fake. When caught, the Generator adjusts and improves. This loop repeats until the Generator produces outputs convincing enough to fool the Discriminator.

Famous example: [thispersondoesnotexist.com](https://thispersondoesnotexist.com) — every face shown is AI-generated from scratch using a GAN.

**VAEs (Variational Autoencoders)** — The Encoder compresses an input into a compact representation; the Decoder reconstructs it. Used in image compression, anomaly detection, and drug discovery.

---

## Transformers — The Architecture Behind Modern AI

The 2017 Google paper *"Attention Is All You Need"* changed everything. It introduced the **Transformer architecture**, which underpins virtually every major LLM today: ChatGPT, Claude, Gemini, Llama, and more.

Older models (RNNs) processed text sequentially — one word at a time. Transformers process the entire input simultaneously, making them dramatically faster and far better at capturing long-range context.

```mermaid
flowchart LR
    A([Input Text]) --> B([Tokenization])
    B --> C([Embeddings])
    C --> D([Positional Encoding])
    D --> E([Encoder])
    E --> F([Decoder])
    F --> G([Output Text])
```

**How each step works:**

| Step | What Happens |
|---|---|
| **Input Text** | Raw text entered by the user |
| **Tokenization** | Text is split into tokens, each mapped to a number — this is what the model actually sees |
| **Embeddings** | Each token becomes a vector encoding its meaning — similar words have similar vectors |
| **Positional Encoding** | Word order is added to embeddings so the model knows the position of each word |
| **Encoder — Self-Attention** | Each word weighs its relationship to every other word, capturing context and dependencies |
| **Decoder** | Generates output one token at a time using the full encoded context |
| **Output Text** | Tokens are converted back to readable words |

**Self-attention in plain terms:** In "The trophy didn't fit in the suitcase because *it* was too big," self-attention determines that "it" refers to the trophy, not the suitcase — by weighing the relationship between all words simultaneously.

---

## Understanding LLMs

LLMs (Large Language Models) are a specific category within Generative AI, focused on text understanding and generation. At their core, LLMs do one thing: **predict the next most likely token** given everything that came before.

| Type | Description | Examples |
|---|---|---|
| **Base Model** | Pre-trained on raw text; cannot be chatted with directly | GPT-2, early BERT |
| **Instruction-Tuned** | Fine-tuned to follow specific instructions | Llama-3-Instruct |
| **Dialogue-Tuned** | Fine-tuned for natural back-and-forth conversation | ChatGPT, Claude, Gemini |

**Why don't LLMs always give the same answer?**
By design. LLMs sample from a probability distribution rather than always selecting the single most likely word. This is controlled by a **temperature** setting — lower temperature produces more deterministic responses; higher temperature produces more creative and varied ones.

---

## Limitations to Know

| Limitation | What It Means | Mitigation |
|---|---|---|
| **Hallucinations** | Confidently states false or fabricated information | Verify critical facts independently |
| **Knowledge Cutoff** | Only knows events up to when training data was collected | Use web-enabled modes for recent events |
| **Math and Logic Gaps** | Unreliable at complex arithmetic without external tools | Delegate calculations to code execution |
| **Inherited Bias** | Reflects biases present in the training data | Evaluate outputs critically for sensitive topics |

---

## Key Takeaways

1. **AI is pattern recognition at scale**, not magic. Understanding how neural networks learn makes you a sharper user and a more credible communicator of AI's capabilities and limits.

2. **The shift from Traditional to Generative AI is a shift in accessibility.** The barrier moved from coding skills to communication skills.

3. **Transformers are the backbone of modern AI.** The self-attention mechanism is what allows models to understand context across an entire input — not just word by word.

4. **LLMs are probabilistic, not deterministic.** They don't look up answers — they generate the most statistically likely continuation of your input.

---

## Resources

- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — Visual walkthrough of the Transformer architecture
- [Transformer Explainer](https://poloclub.github.io/transformer-explainer/) — Interactive animation
- [OpenAI Tokenizer](https://platform.openai.com/tokenizer) — See how text becomes tokens in real time
- [ArtificialAnalysis.ai](https://artificialanalysis.ai) — Compare LLM performance, speed, and cost

---

*Week 1 — AI Fundamentals*
