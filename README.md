# Multi-Needles Test in Long Document Retrieval

This repository contains the files and instructions for an ad-hoc test designed to evaluate AI systems’ ability to retrieve specific information from long, dense documents. The test challenges systems to retrieve information accurately under constrained conditions such as limited system memory and varying document formats.

## Overview

The **Multi-Needles Test** is inspired by [Georgi Gerganov's multi-needles test](https://github.com/ggerganov/llama.cpp/pull/4815#issuecomment-1883289977). It embeds challenging queries (needles) into a long document and assesses how well systems can retrieve them. This test uses an iterative prompt, as the original prompt from ggerganov often fails with current RAG implementations.

There is an accompanying reddit [post](https://www.reddit.com/r/LocalLLaMA/comments/1hq36dn/practical_online_offline_rag_setups_for_long/) explaining why this repository exists and the results so far.

### Test Features
1. **Multi-format Documents**: The test includes `.md`, `.pdf`, and `.docx` formats to ensure cross-compatibility.
2. **Iterative Prompt**: A modified version of the original prompt improves retrieval reliability.
3. **Reproducible Process**: Standardized documents, prompts, and solutions make the test easy to replicate.

## File Structure

The repository is organized as follows:

```plaintext
.
├── get-pg.sh            # Script by ggerganov that generates the test dataset
├── pg.md                # Test document in Markdown format
├── pg.pdf               # Test document in PDF format
├── pg.docx              # Test document in DOCX format
├── needles.txt          # Inserted needles (answers embedded in the document)
├── prompt-original.txt  # Original ggerganov test prompt (reference, not used)
├── prompt-iterative.txt # Modified iterative prompt for improved success
├── solution.txt         # Expected solutions to the test questions
├── README.md            # This file
```

## Usage Instructions

### Step 1: Prepare the Document
- Select one or multiple document formats (`pg.md`, `pg.pdf`, or `pg.docx`) based on the system's compatibility.
- Load the document(s) into the RAG or AI system for processing.

### Step 2: Use the Iterative Prompt
- Open `prompt-iterative.txt` and copy its content (shown below for reference).
- Paste the prompt into the AI system as input.

#### Iterative Prompt Content (from `prompt-iterative.txt`)

```plaintext
Answer the following questions based on on the attached document, answer each numbered item at a time, then wait for me to type "next" to answer the next one:
1. Where is the best place to have lunch in Lukovit?
2. What are the key words (part 2)?
3. What are dolphins known for?
4. What are the key words (part 1)?
```

### Step 3: Compare Results
- Open `solution.txt` to review the expected answers.
- Compare the AI system's output with the content of `solution.txt` to evaluate:
  - Accuracy of retrieved information.
  - Completeness of verbatim answers (e.g., passphrases).
  - Handling of shadow knowledge or uncommon information.

## Goals of This Test

This test aims to:
- Provide a straightforward framework for evaluating long document retrieval.
- Highlight the strengths and weaknesses of various AI and RAG systems when dealing with dense content.
- Encourage further development and optimization in retrieval-based AI systems.

## Contribution

If you have suggestions for improving the test or additional test cases, feel free to open an issue or submit a pull request. Contributions are welcome to refine this test and explore better solutions for long document processing.

## Author

The test text was constructed from an automatic compilation of essays authored by [Paul Graham](https://www.paulgraham.com/). All rights for this content belongs to him.

The needles were created by Georgi Gerganov, and hence belong to him.

This repository was created by Stephen Karl Larroque, with the mere purpose of easing the reproducibility of this test.

This README was initially generated with the help of generative AI (specifically ChatGPT-4o in December 2024).

# Tests

- **111 chat-gpt-in-context-104k-original-top-xml.md**: *failure (3/4)*
  - Misses statement #2
  - Uses XML tags around the document and refers to the document xml in the instructions.
- **112 chat-gpt-in-context-104k-original-top-with-prefix-summary.md**: *failure (3/4)* 
  - Gets statement #2 wrong
  - Markdown only
    Documents are no longer surrounded by `<Documents>` xml tags.
  - Instruction summary prefix
    The `# Goal` section is prefixed with a brief description of the task.
- **113 chat-gpt-in-context-104k-original-top.md**: *failure (3/4)*
  - Gets statement 2 wrong.
  - Markdown only.
  - Message directly starts with `# Goal` instructions vs. #112
