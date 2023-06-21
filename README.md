# SpeechToText_NLP

## Problem statement and solution
In companies that audit their promotional calls, employees have to manually listen to all the recorded calls and decide whether all the promotional offers are detailed correctly to the customer. But this process is time-consuming and involves lots of manual intervention. So the best solution is to use Natural Language Understanding and develop a product that deals with processing audio calls, converting the speech into text, identifying intent and entities from the text, and generating the summary for the audio calls. This automated process reduces human error, and saves time and effort, thus making the above-mentioned process seamless.

## Analysis of code
Initially, we use an open-sourced model Wav2Vec2, and transcribe the given audio file. The entire project is based on transformers under which we use the Wav2Vec2ForCTC and Wav2Vec2Tokenizer to fine-tune the Wav2Vec2 model and facilitate the tokenization and preprocessing of audio data.

Next, we use Rasa, an open-source machine learning framework to automate text and voice-based conversation that classifies intents and recognizes entities in the transcribed audio file and presents them in a JSON format.

We then generate the summary of the call with a transformer model, Pegasus that uses a tokenizer called Pegasus Tokenizer. With this, you preprocess your text data, tokenize it appropriately, and encode it into numerical representations that can be fed into the Pegasus model for text summarization.
