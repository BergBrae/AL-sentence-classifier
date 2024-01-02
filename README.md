# Active learning Sentence Classifier
*Automated Data Mining for LLM/GPT use cases*

1. Retreive articles from NewsAPI
2. Chunk text into smaller lengths
3. Use `all-MiniLM-L6-v2` from HuggingFace to embed texts
4. Train a SVM classifier to identify relevant texts.
    - An interactive Active Learning loop is used to minimize the number of labels that need to be labeled.
5. With chunks that were classified as relevant, use `distilbert-base-cased-distilled-squad` from HuggingFace to identify text that answers "*What is the AI supposed to do?*".
7. Export LLM use cases and their corresponding sources.

**Valid newsapi and OpenAI API keys are required.**