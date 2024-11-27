# Story Generation in Roman Urdu

## 1. Introduction

This project focuses on generating a coherent story in **Roman Urdu** using **n-gram language models** (unigram, bigram, and trigram). Leveraging the **spaCy** library for text preprocessing, the generated story consists of three paragraphs, each containing 5–10 sentences. The story is created word by word using the n-gram model, trained on a corpus of classic Urdu short stories.

---

## 2. Objectives

The main objectives of this project are:
1. Load and preprocess the story corpus.
2. Develop **n-gram language models** (unigram, bigram, and trigram).
3. Generate a coherent three-paragraph story using the models.
4. Compare the outputs of different n-gram models.

---

## 3. Challenges

### Implementation Challenges:
- **Next Word Prediction**: Selecting the most probable next word using the n-gram models.
- **Conditional Frequency Distribution (CFD)**: Using CFD to calculate probabilities for the next word.
- **Maintaining Coherence**: Ensuring narrative consistency across sentences and paragraphs.

### Urdu-Specific Challenges:
- Handling Roman Urdu complexities, such as variations in spelling and sentence structures.
- Building robust n-gram models that capture the unique linguistic patterns of Urdu.

---

## 4. Implementation Steps

### Step 1: Load and Preprocess the Corpus
- Load the Roman Urdu story corpus (`urdu_stories.csv`), which contains classic Urdu short stories.
- Use the **spaCy** library to tokenize the text, split sentences, and process the data.

### Step 2: Develop n-gram Models
- **Unigram Model**: Counts the frequency of individual words.
- **Bigram Model**: Counts the frequency of word pairs (current word → next word).
- **Trigram Model**: Counts the frequency of word triplets (current two words → next word).
- Conditional Frequency Distribution (CFD) is used to calculate the probability of the next word.

### Step 3: Generate Story
- Generate sentences using the n-gram models:
  - Randomly select a starting word.
  - Use the selected n-gram model to predict the most probable next word.
  - Repeat until the sentence reaches a random length (5–19 words).
- Combine sentences to create a paragraph.
- Combine three paragraphs to generate the final story.

---

### Step 6: Generate Sentences and Paragraphs
- Sentence Generation:
-A sentence is generated using the n-gram models with the following steps:

- Randomly select the first word from the corpus's starting words.
- Use the n-gram model to predict the most probable next word based on previously generated words.
- Repeat until the sentence reaches a random length (5–19 words).
- Add Urdu punctuation (۔) at the end of the sentence.
- Paragraph Generation:
- Each paragraph consists of 5–10 sentences generated sequentially. Sentences in a paragraph aim to maintain narrative flow and coherence.

- Story Generation:
The story consists of three paragraphs, separated by an empty line. Each paragraph has a randomly determined number of sentences.

### 7. Results and Outputs
- Unigram Model
The unigram model generates sentences based on individual word probabilities.
Results may lack coherence and grammatical structure, as it does not account for context or relationships between words.
- Bigram Model
The bigram model improves upon the unigram model by considering word pairs.
Sentences are more coherent, but the narrative flow between sentences remains limited.
- Trigram Model
The trigram model produces the best results by considering word triplets.
Sentences and paragraphs are more contextually relevant and grammatically correct, creating a more cohesive narrative.
