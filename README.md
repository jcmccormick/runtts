# RunTTS
POSIX-compliant shell utility for working with local LLM + voice models

# Requirements

1. Whisper CLI e.g. `sudo apt-get install whisper`
2. Ollama CLI e.g. `sudo apt-get install ollama`
3. TTS CLI e.g. `sudo apt-get install tts`

Configure whatever models you want to use with Ollama and TTS, noting their model name as you would use a la `ollama run xxxx` or `tts --model_name xxxx`. Upon running RunTTS for the first time, go into the configuration menu and enter in the model names you are using.

# Install

1. Clone the repo into `~/runtts`.
2. `chmod +x ~/runtts/runtts`
3. `~/runtts/runtts` to start the program.

# About

This tool is a mashup of the whisper + tts + ollama CLIs in order to have a local utility for interacting with AI models. It keeps track of a running context as you continue prompting it, and when needed conversations can be saved for later prompting. Because of the variability of situations where models can be run, it utilizes streaming responses in order to produce audio clips as soon as newline-delimited content is ready. As well, it will handle markdown style triple-backtick blocks, setting them aside to not be read aloud, but can be viewed as received.
