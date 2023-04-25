# video-embeddings
In principle, you should be able to combine an Automatic Speech Recognition model like [Whisper](https://github.com/openai/whisper), an image captioning model like [Mini-GPT4](https://minigpt-4.github.io/), and just about any kind of gpt-3.5-quality LLM to get near-human-level understanding of videos. The formula would be something like:
1. Download video
1. Run Whisper to transcribe what's being said in the video
1. Run Mini-GPT4 image captioning on frames extracted from the video every 15 seconds or so
1. Interleave the audio transcriptions and image captions in text
1. Use an LLM to summarize and understand what's going on in the video
1. (optional) encode the LLM's summary with any sort of text embeddings to do things like classification of the videos

I see no reason why the resulting encodings would not be state of the art, specifically for the purposes of *understanding* videos.
