___
# TOKEN
Links: [[Natural Language Processing (NLP)]]
Status: #🌳 
Tags: [[ChatGPT]] [[Let's build GPT - from scratch, in code, spelled out.]]

<!--- Created on: 2023.10.23, 20:30 --->

> Tokens in NLP are individual units of text, which can be words, subwords, or characters, used for processing and analyzing natural language text in various NLP tasks.
- Tokenization: Convert text to sequence of integers.


1. **Word Tokens:** In many NLP applications, text is tokenized at the word level, meaning that each word in a sentence is treated as a separate token. For example, in the sentence "I love NLP," the word tokens are "I," "love," and "NLP."
2. **Subword Tokens:** Some NLP models, such as subword-based models like BERT, tokenize text into subword units. This is particularly useful for handling languages with complex morphology. For instance, the word "unhappiness" might be tokenized into subword tokens like "un," "happiness."
3. **Character Tokens:** In character-level tokenization, each character in the text is treated as a separate token. For example, the word "apple" would be tokenized into the character tokens "a," "p," "p," "l," "e."

> [!info]
> Longer encodings such as work tokens lead to larger vocabularies (dictionaries), but can represent text with less integers.
> - Charakter Token for `hello`: `[1, 2, 3, 3, 4]`
> - Word Token for `hello`: `[3176]`
> In practice, subword Tokens are usually used.
