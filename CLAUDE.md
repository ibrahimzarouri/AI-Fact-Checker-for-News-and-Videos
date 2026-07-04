- Add to memory, Keep in mind the overall workflow and goal of this extension: its purpose is to analyze a video by extracting its audio, sending the audio to Whisper for transcription, processing the resulting text through a GPT model along with ClaimBuster for fact-checking, and finally displaying the analysis results in the UI. Always remember this process when reasoning about how the extension works or when implementing, debugging, or improving it.

- > **Add to memory:**
> This extension primarily works with **four main files**:
>
> 1. `manifest.json`
> 2. `background.js`
> 3. `content.js`
> 4. `styles.css`
>
> All other files are not relevant to the core functionality.

- Add to memory, And the APIs are stored in config file for both OpenAI(Whisper and gpt-4.1-nano) & ClaimBuster