# LLMs and Data Research

## What are LLMs?

LLMs (Large Language Models) are a type of artificial intelligence model trained on large-scale text data to generate human language based on learned patterns.

---

## Are LLMs just a big database?

LLMs are not databases — they do not store and retrieve facts, they generate text by predicting patterns learned during training.

### Key differences

❌ Database
- stores exact information  
- retrieves stored records  
- does not generate new text  

**Example:**
“What is 2+2?” → returns stored value if it exists  

---

✅ LLM (Large Language Model)
- does NOT store facts as records  
- stores learned patterns in weights (parameters)  
- generates new text each time  
- produces answers by predicting the next token

**Example:**
“What is 2+2?”

An LLM would:
- generate the answer “4”  
- based on learned patterns in training data  
- not by retrieving a stored entry

---

## Examples of different LLMs?

- OpenAI: GPT models (GPT-4, GPT-4o, GPT-3.5)  
- Anthropic: Claude models (Claude 3, Claude 3.5)  
- Google: Gemini models (Gemini 1.0, Gemini 1.5)  
- Meta: LLaMA models (LLaMA 2, LLaMA 3)  
- Mistral AI: Mistral models (Mistral 7B, Mixtral)  
- DeepSeek: DeepSeek models (DeepSeek-V2, DeepSeek-R1)  
- Alibaba: Qwen models  
- Baidu: ERNIE models

---

## What can you give LLMs for their training?

LLMs are trained on large-scale datasets of text and code. The main types of data include:

- Books and academic texts  
- Websites and publicly available articles  
- Code repositories  
- Documentation and technical manuals  
- Conversational data (such as chat transcripts or forums)  
- Multilingual text data  

### Key idea

The quality and diversity of training data strongly influence the model’s performance, robustness, and ability to generalise across tasks.

---

## What, at a base level, are LLMs trying to do?

At a base level, LLMs are trying to **predict the next token** in a sequence of text.

Given some input context, the model assigns probabilities to possible next tokens and selects the most likely one. This process repeats step by step to generate full sentences and longer responses.

### Key idea

LLMs do not retrieve answers or “think”. They generate text by repeatedly predicting the next most probable token based on patterns learned during training data.

---

## Explain the concept of "Prediction, not understanding" in regard to AI and LLMs

LLMs generate text through **prediction**, not human-like understanding.

They take an input context and compute the probability of possible next tokens. The output is built step by step by selecting the most likely next token at each stage.

### What “prediction” means

- The model learns statistical patterns from large datasets  
- It estimates which token is most likely to come next  
- It builds responses by repeating this process many times  

### What it does NOT mean

- No awareness or consciousness  
- No beliefs or intentions  
- No real-world understanding of meaning  
- No reasoning in a human sense  

### Key idea

LLMs can produce outputs that *look like understanding*, but internally they are performing large-scale pattern-based prediction of language, not comprehension.

---

## Examples of LLM predictions producing accurate answers

1. **Math completion**  
Prompt: “What is 15 × 12?”  
Output: “180”

2. **Language translation**  
Prompt: “Translate ‘good morning’ to French”  
Output: “bonjour”

3. **Text completion**  
Prompt: “The capital of France is …”  
Output: “Paris”

4. **Code prediction**  
Prompt: “Write a Python function to add two numbers”  
Output: returns a correct function such as:
```python
def add(a, b):
    return a + b
```
5. **General knowledge question**  
Prompt: “Who wrote Romeo and Juliet?”  
Output: “William Shakespeare”

---

## What are Tokens?

Tokens are the basic units of text that an LLM processes.

A token can be:
- a whole word (e.g. “cat”)  
- part of a word (e.g. “un”, “believ”, “able”)  
- punctuation (e.g. “.”, “,”)  
- numbers or symbols  

### Example

Text: “I love AI”  
Tokens: ["I", "love", "AI"]

Text: “unbelievable”  
Tokens: ["un", "believ", "able"]

### Key idea

LLMs do not read text as full sentences. They process and generate text one token at a time, predicting the next token based on context.

---

## What is Tokenisation?

Tokenisation is the process of breaking text into smaller units called tokens so that an LLM can process it.

These tokens can be whole words, parts of words, numbers, or punctuation.

### Example

Text: “I love AI”

Tokenisation:
["I", "love", "AI"]

Text: “unbelievable”

Tokenisation:
["un", "believ", "able"]

### Why it is used

- It converts raw text into a format that models can process  
- It allows efficient handling of large vocabularies  
- It helps models work with words they have never seen before by splitting them into smaller parts  

### Key idea

Tokenisation is the first step that converts human language into machine-readable pieces (tokens) for LLMs to process and predict.

---

## Why do tokens matter?

Tokens matter because LLMs do not process text as whole words or sentences — they process tokens.

### 1. They define how the model “reads” text
- Text is split into tokens before processing  
- The model works token by token, not word by word  

### 2. They affect cost and limits
- LLM usage is measured in tokens (input + output)  
- More tokens = higher cost and longer processing time  
- Models have a maximum token limit (context window)

### 3. They influence performance
- Different tokenisations can change how well a model understands input  
- Rare words may be split into multiple tokens  

### 4. They determine output length
- The model generates responses one token at a time  
- Output length is controlled by token limits  

### Key idea

Tokens are the basic unit of computation in LLMs, so everything — cost, speed, input size, and output — depends on them.

---

## What is the “context window” in relation to LLMs?

The context window is the maximum number of tokens an LLM can process at one time.

It includes:
- the input (your prompt)
- the conversation history
- the model’s generated output (during generation)

### What it means in practice

If a model has a context window of 8,000 tokens, it can only “see” and use the most recent 8,000 tokens when generating a response.

Anything beyond that is not accessible to the model.

### Why it matters

- Limits how much text a model can handle at once  
- Affects long conversations and large documents  
- Determines how much past information the model can use  

### Key idea

The context window is the model’s short-term memory: it defines how much text the LLM can actively consider at any given moment.

---

## What are some ways to mitigate or get around context windows?

There are several engineering strategies used to handle the limitations of fixed context windows in LLMs:

- **Chunking** → splitting large documents into smaller parts before processing  
- **Summarisation** → compressing earlier information into shorter summaries to retain key meaning  
- **RAG (Retrieval-Augmented Generation)** → retrieving relevant information from external storage and adding it to the prompt  
- **Sliding window** → keeping only the most recent tokens and dropping older content  
- **Tool use / external memory** → storing information outside the model (such as in files, databases, or APIs) and retrieving it when needed

---

## What are hallucinations and why do they happen?

Hallucinations in LLMs are outputs where the model generates information that is incorrect, misleading, or not grounded in real data, but is presented in a confident and fluent way.

---

### Why hallucinations happen

- **Next-token prediction:** LLMs generate text by predicting the most likely next token, not by checking facts  
- **No built-in fact database:** The model does not verify information against a source of truth during generation  
- **Pattern completion:** The model fills gaps based on learned patterns, even when it has insufficient or ambiguous context  
- **Training data limitations:** Errors, gaps, or outdated information in training data can influence outputs  
- **Overgeneralisation:** The model may apply learned patterns too broadly to new situations  

### Key idea

Hallucinations occur because LLMs are optimised for producing plausible text, not for guaranteeing factual accuracy.

---

## Training vs Retrieval

Training and retrieval are two fundamentally different ways of providing knowledge to an LLM-based system.

### Training

Training is the process where an LLM learns patterns from large datasets.

- Data is used to adjust the model’s internal parameters (weights)  
- Knowledge becomes “baked into” the model  
- Happens before the model is used (offline process)  
- Does not store exact documents, but learns statistical patterns  

**Key idea:**  
The model learns *how language works*, not a searchable database of facts.

### Retrieval

Retrieval is the process of fetching relevant information at runtime from an external source.

- Uses databases, documents, or search systems  
- Information is not stored in the model itself  
- Happens during inference (when the model is being used)  
- Often used in RAG systems (Retrieval-Augmented Generation)  

**Key idea:**  
The model is given *relevant external information* to use in its response.

### Key difference

- **Training** → learning from data to build the model  
- **Retrieval** → fetching information to support the model at runtime  

---

## Why does data external to the model’s training data matter so much?

External data matters because LLMs only contain knowledge from their training data and do not automatically know new, private, or changing information.

Using external data allows LLMs to:

- Access up-to-date information that was not included in training  
- Reduce hallucinations by grounding responses in real sources  
- Use private or organisation-specific data (such as company documents)  
- Extend capabilities without retraining the model  
- Work with information that changes over time  

### Key idea

Training data is fixed, while external data allows LLMs to stay current, accurate, and relevant in real-world use cases.

---

## What is RAG?

RAG (Retrieval-Augmented Generation) is an approach that improves LLM outputs by combining a language model with an external retrieval system.

Instead of relying only on training data, the model first retrieves relevant information from an external source (such as a database or document store) and then uses that information to generate a response.

### How RAG works

1. A user asks a question  
2. The system retrieves relevant documents or data  
3. The retrieved information is added to the prompt  
4. The LLM generates an answer using both the question and retrieved context  

### Why RAG is used

- Provides up-to-date information  
- Reduces hallucinations  
- Allows access to private or domain-specific data  
- Avoids the need to retrain the model  

### Key idea

RAG enhances LLMs by grounding their responses in external, relevant information at runtime.

---

## Basic flow of an LLM prompt response with RAG

When Retrieval-Augmented Generation (RAG) is used, the response process combines retrieval and generation steps.

### 1. User prompt
The user submits a question or instruction.

### 2. Query processing
The system processes the input and converts it into a searchable format (often embeddings).

### 3. Retrieval
Relevant information is fetched from an external knowledge source (such as a database, document store, or vector database).

### 4. Context augmentation
The retrieved information is added to the original prompt as additional context.

### 5. LLM generation
The LLM generates a response using:
- the user’s prompt  
- the retrieved context  

### 6. Final output
The system returns a response that is grounded in both the model’s knowledge and the external data.

### Key idea

RAG systems improve LLM responses by inserting relevant external knowledge into the prompt before generation.





