# Omnia

## v1.8.1
### Changelog
- Default to MS Zira voice for all languages if available
- Add support for system calls using .AIMO files. 
AIMO is our new tool that can record your desktop actions. 
Place these files in the actions folder and you can trigger them when talking to the assistant by saying for example: "System call, start X"

## v1.7.4
### Changelog
- Improve parsing of triggers and support to set the value directly
Examples:  "osc_parameter_triggers": [["activate summer dress", "/avatar/parameters/Outfit", 5], ["Mute me", "/avatar/parameters/MuteSelf", True]]

## v1.7.3
### Changelog
- Namechange to Omnia

## v1.7.2
### Changelog
- Improved parsing of wake up word
- Small improvements

## v1.7
### Changelog
- Fix autostart of recording
- Fix mp3 playback for elevenlabs

## v1.6
### Changelog
- Updated README
- Improved parsing of OSC parameter triggers. One Two, Three get parsed as 1,2,3 correctly. Fixes issues with transcription being too literal.
- Fixed bug with elevenlabs audio
- Added support for wake up message that triggers the assistant. Default: Pineapple (works best)

Welcome to Omnia-VRC!
This is a tool that allows you to use GPT-3 and GPT-4 to generate text and audio. You can use tools like VoiceMeeter to route the audio to VRChat. https://vb-audio.com/Voicemeeter/banana.htm
It is currently in beta, so please report any bugs you find to me on Discord: aria_aurora, God⛧ on VRChat, Parzival on ChilloutVR or through the form on my website https://suro.One

Feel free to donate if you are satisfied. 
Donate: https://www.paypal.com/donate/?hosted_button_id=2X2NBB4AA3CFC
----------------------------------------------------------
Settings description:
- openai: mandatory, your OpenAI API key
- gpt_model_number: mandatory, 3 for GPT-3, 4 for GPT-4
- use_elevenlabs: optional, highly recommended! If you want to use ElevenLabs for text-to-speech, set to true and add your API key in the elevenlabs field
- elevenlabs: optional, your ElevenLabs API key. Only needed if you want to use ElevenLabs for text-to-speech
- context_length: optional, how many messages to use as context. This is the amount of messages that will be remembered by the assistant. Lower is cheaper, higher is better, default 5
- play_sounds: optional, if you want to play sounds when you send a message, default true
- assistant_prompt: optional, the prompt for GPT-3, default is the VRChat assistant prompt. Remove this line if you want to use the default prompt for our assistant, Aria.
- osc_output: optional, if you want to send the output to OSC in VRChat. Note, follow this guide on how to enable it: https://docs.vrchat.com/docs/osc-overview#enabling-it , default true
- jailbreak: optional, if you want to use the jailbreak version of the  model, default false. DAN is something else...
- elevenlabs_voice_id: optional, the voice id for ElevenLabs, default is the default voice. You can find a list of voice ids here: https://api.elevenlabs.io/v1/voices
- silence_duration: optional, how long to wait for silence to stop recording, default 3
- verbose: optional, if you want to see the verbose output of GPT-VRC, default false
- disable_language_model: optional, if you want to disable the language model (useful if you only want the OSC parameter triggers), default false
- osc_parameter_triggers: optional, if you want to use OSC parameter triggers, default false. Format: [["trigger sentence", "/path/to/parameter", "int"/"float"/"bool"], ["trigger2 sentence", "/path/to/parameter2", "int"/"float"/"bool"]]
    Example: "osc_parameter_triggers": [["set speed", "/avatar/parameters/Speed", "int"], ["set mute", "/avatar/parameters/MuteSelf", "bool"]] 
    To activate: say "set speed 50" or "set mute on" or "set mute true"
    The above showed you the generic ways of setting an OSC parameter. You can now also set the value directly:
    Example:  "osc_parameter_triggers": [["activate summer dress", "/avatar/parameters/Outfit", 5], ["Mute me", "/avatar/parameters/MuteSelf", True]]
- wake_up_word: optional, if you want to use a wake up word, default "Pineapple", remember to set wake_up_mode to true
- wake_up_duration: optional, how long to wait for the wake up word, default 3
- wake_up_timeout: optional, how long to wait after the wrong wake up word has been said, default 10
- wake_up_mode: optional, if you want to use a wake up word, default false
- disable_speech: optional, disables the language model's speech and only outputs text

----------------------------------------------------------
# Requirements
- Windows
- Internet
- OpenAI API key

# Running the application
- Click on omnia-vrc.exe

# Features
- GPT-3 and 4 support in VRChat and on your desktop

- Voice control including wake up word(s) (Default: Pineapple)

- OSC -> Sends data to VRChat to display the assistant's message in your textbox.

- Elevenlabs voices -> Natural sounding voices, enable this in the settings.txt by setting the value use_elevenlabs to true and placing your elevenlabs API key in the setting: "elevenlabs" where it says "YOUR_11LABS_KEY_HERE".

- Trigger OSC parameters. You can switch outfits, etc. with your voice. Set up your trigger sentence, the path to the parameter, and pick one of the types. Make sure to only pick one. 
Example: "osc_parameter_triggers": [["trigger sentence", "/avatar/parameters/MyParameter", "int"]]
Read this to learn about avatar parameters (it's super easy): https://docs.vrchat.com/docs/osc-avatar-parameters
To add your own parameters to the application:
-- Go to: C:\Users\YOUR_USERNAME\AppData\LocalLow\VRChat\VRChat\OSC\
-- Find select the file with your user id, go to avatars. Select your avatar's ID and you'll see the parameters available for your avatar and the types.
-- Now you can add parameters you want to trigger to settings.txt

- Create your own custom assistant by setting the `assistant_prompt` in the settings.

- AIMO is our new tool that can record your desktop actions, and it generates .AIMO files https://suro.gumroad.com/l/aimo
    Place these .AIMO files in the "actions" folder of omnia and you can trigger them when talking to the assistant by saying for example: "System call, start X"

If you need help, message me on discord: aria_aurora and I'll be glad to assist you.
Join our discord: https://discord.gg/WFGvAXWpfY

Cheers!

