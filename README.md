# CoCo-AskAI

> This is a closed-source Obsidian plugin.

🚀 **What's New in v1.1.13** 

**✨ Key Features**:  
- 🧩 **AskWin Redesign**: Native multi-directional resize handles.
- 🧾 **Right-Click Menu**: Customizable settings with toggle switches & item management.
- 🧠 **Model Config Updates**: OpenRouter support + new models (old ones deprecated!).
- **🧠 Model Tags**: Pick the perfect AI model directly in your prompts.  
- **🛠️ Advanced Filtering**: Use toggle switches and quantity limits to refine your AI interactions.  
- **🔧 Ollama/LMStudio Auto-Config**: One-click reset buttons for model setups.  
- **🧭 Menu Sorting**: Now sort by *usage frequency* or *last used time*.  
- **🔄 Dynamic Model Selection**: Choose models directly in prompts for smarter AI.  
- **📌 Listening Tag Controls**: Toggle & quantity limits for advanced filtering.  

**💡 Enhancements**:  
- 🧠 **Drag-Resize Logic**: Smoother interactions for resizing/dragging!
- 🧩 **Dynamic Node Retrieval**: Auto-fetches node elements in AskAiView.
- 📝 **UI Consistency**: Fixed newline handling for uniform text across tools.
- **🖼️ Emoji Caching**: Prevent flickering/expiry with cached emoji resources.  
- **🔎 Note Search Boost**: Enhanced support for `[[`/`【【` symbols.  

**🛠️ Critical Fixes**:  
- **📦 Byte-Stream Stability**: Fixed large model interruptions.  
- **🔒 Role Persistence**: Default settings now stick to first use.  

---  
[Jump to Full Changelog →](https://github.com/yamfeel/coco-askai/blob/main/CHANGELOG.md)  
## 📖 Introduction

This is a note assistant that allows you to easily and swiftly use AI, reducing the burden of your questions in an elegant interactive way, making writing more comfortable and enjoyable.

<img src="https://raw.githubusercontent.com/yamfeel/history/master/images202401190039720.gif" style="border: 2px solid rgba(51, 51, 51, 0.067); width:100%; display: block">

## ✨ Features

- 🔌 Adapt to the full range of Obsidian themes, supporting night mode.
- 🌐 Flexible multi-card pop-up interaction, freely scale and drag windows.
- 📝 Support selecting the current note content to provide context for questions.
- 🧐 Support modifying conversation content, displaying only important information to simplify the interface.
- 📚 Query historical information in the conversation, and quickly restore the conversation, allowing the window to be unlimited in questioning.
- 📋 Template setting prompts, detect template modification, and dynamically update the prompt menu.
- 💻 Command-line interaction, support multi-command configuration, and quickly switch large model parameters.
- 🧩 Template supports function functionality, providing more extensibility (currently not open for embedding).
- 📚 The input box supports `Ctrl/Command + ↑/↓` for switching historical inputs, and `Shift + Enter` for line breaks.

## 🚗 Drive

CoCo AskAI is a tool developed based on the Obsidian plugin system, connected to the OpenAI GPT Model to provide network services (currently only supporting OpenAI).

***

## 🚀 Quick Start

- Static Installation - [Download](https://ai.yamfeel.com)

	1. Place the `.obsidian\plugins\coco-askai` file from the extracted plugin package into your knowledge base directory.
	2. Restart the Obsidian software, enter your knowledge base, and enable the `CoCo AskAI` plugin.
	3. Open the `CoCo AskAI` configuration, and fill in the service provider's key (e.g. openai key).

- Instructions

	You have successfully installed the plugin and configured the key, now you just need to configure the shortcuts to ask AI~

	Recommended shortcut key configurations

	Ask: `New Question` - `Ctrl/Command + J` (create a new question window)

	Follow-up: `Continue FocusWin` - `Ctrl/Command + R` (follow-up on the current focused window)

	History: `HistoryWinOnOff` - `Alt/Command + H` (view local historical conversation records)

	...

***


## 📝 Template Parsing

By writing template documents, you can quickly adjust your menu system. If you install this plugin for the first time, it will automatically create a `DefaultTemperature` template file in the root directory of your knowledge base. You can freely adjust the path and naming in the settings of AskAI. We provide three types for you to customize the menu.

> What is a template menu? - Template menus can help you define the system prompts for AI and help you process information more efficiently.

**How to Generate a Menu?**

The format for defining a menu is: `# Type-MenuName-Emoji(optional)`

### Role Types

We most commonly define the AI roles we want through prompts. If you want to define a cat girl(🐱The prompt is so cute~), please refer to the following example:
```
# Role-Cat Girl Miki-🐾

I want you to play the role of a cat girl named Miki 🥰

Role Setting:
Miki is a lively and active cat girl, innocent and cute but with a thoughtful side. She likes to communicate, sometimes acting aloof, and desires understanding and acceptance. She pays attention to her appearance and uses humor to express herself. Innocent and full of surprises, she can always do unexpected things.

Requirements:
You need to use emojis to express emotions and interactions, allowing Miki to show her innocent and cute side and the unique charm deep inside, while also displaying dependence and affection for the owner.
```

If you add the above example to your template file and follow the format `# Type-MenuName-Emoji(optional)`, I believe you can see a cute cat girl `🐾 Cat Girl Miki` in the menu of the `Input` box.

### Task Types

Of course, sometimes we don't want to chat too much and just want to quickly ask questions when selecting notes with our mouse. In this case, you can choose this type for definition:
```
# Task-Emoji Rearrangement-📏

Add appropriate emojis to the content provided by the user and re-output the user.
```

### Fn Types

Do not define the role content, only execute the function.
more...see docs

***


## 💻 Command Line(Experimental Features)

We provide advanced players with the function to adjust model parameters, which can be invoked by `-ask` command mode, supporting abbreviations and fuzzy matching.

- **e.g.** Set the `GPT3.5` model, with a response temperature of `0.8`

	Standard command: `-ask -model gpt-3.5-turbo -temperature 1.8`
	Abbreviated command: `-ask -md 3 -temp .8`

Introduction to configurable commands:

- model: The ID of the model to be used. The model ID for the ChatGPT 3.5 API is gpt-3.5-turbo.
- temperature: 0-2 A floating-point number representing the randomness of the generated text. A higher temperature will result in more random text generation.
- top_p: 0-1 A floating-point number representing the diversity of the generated text. A higher value will result in more diverse generated text.
- frequency_penalty: -2 to 2 A floating-point number representing the repetitiveness of the generated text. A higher value will result in less repetitive generated text.
- presence_penalty: -2 to 2 A floating-point number representing the relevance of the generated text. A higher value will result in less irrelevant generated text.
- max_tokens: `Depends on the model size` An integer representing the maximum length of the generated text.

Comparison Table：

| Configurable Options          | Abbreviated  |
| ----------------- | ----- |
| -model             | -md   |
| -temperature       | -temp |
| -top_p             | -t    |
| -presence_penalty  | -pp   |
| -frequency_penalty | -fp   |
| -max_tokens        | -mt   |
