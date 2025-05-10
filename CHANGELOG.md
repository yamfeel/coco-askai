## [1.1.19-Beta](https://github.com/yamfeel/coco-askai/releases/tag/1.1.19) (2025-05-10)

### ⚡ Performance Upgrades
- **Null Safety**: Components now handle missing data more gracefully
- **Text Selection**: Smoother highlighting experience in input fields
- **Emoji Performance**: Frequently used emojis load faster with new caching

### 🛠️ Under the Hood
- **Data Models**: Optimized core structures for better efficiency

### 🐛 Important Fixes
- **Selection Issues**: Resolved text highlighting inconsistencies
- **Code Cleanup**: Removed deprecated functions

## [1.1.13-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.1.13) (2025-05-03)  
### **Features**
- **AskWin Redesign**: Native multi-directional resize handles implemented (removed `interactjs` dependency)  
- **Right-Click Menu**: Added customizable settings with toggle switches and item management  
- **Model Configuration**: Updated OpenRouter support with new models and deprecated model removals  

### **Enhancements**  
- **Drag-Resize Logic**: Optimized event handling for smoother resizing and dragging interactions  
- **Dynamic Node Retrieval**: Refactored `AskAiView` to dynamically fetch node elements 
- **UI Consistency**: Fixed newline handling in `AskAIRequest` and `TextTool` for uniform text processing 
### **Bug Fixes**  
- **Role Persistence**: Ensured default role settings apply only on first call (prevents mid-conversation overrides)  
- **Overflow Control**: Hidden overflow on task box and replaced last line node with `<p>` element 
## [1.1.9-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.1.9) (2025-04-13)
### Enhancements
- **OpenRouter Integration**: Full support for OpenRouter in model handling pipeline
- **Model Configuration**: Added dynamic GPTParams interface parameters for fine-grained control
- **Text Processing**: Improved newline handling consistency in AskAIRequest and TextTool
- **UI Optimization**: Adjusted textarea minimum height in model config for better visual hierarchy
- **Reasoning Engine**: Enhanced streaming data processing logic in LMStudioRequest and OpenAIRequest
- **Role Management**: Implemented default role preference settings persistence

### Bug Fixes
- **Role Selection**: 🐛 Fixed default role application logic to only trigger on first call (prevent mid-conversation overrides)
- **Error Handling**: Strengthened error fallback mechanisms in AskAIRequest pipeline

## [1.1.3-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.1.3) (2025-03-31)
### Bug Fixes

- **Model Config Validation**: [🐛 Fix: Improve model config validation and error handling] Extended support for OpenAI, O1, O3 models.

## [1.1.2-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.1.2) (2025-03-29)

### Enhancements

- **Menu Rendering Optimization**: Introduced `MenuItemPool` for efficient reuse, improving menu creation/recycling performance by ~40%
- **Session Model Persistence**: Automatically restores the previously selected AI model (e.g. Llama2/gpt-4o) when reopening conversation windows

## [1.1.0-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.1.0) (2025-03-27)

### Enhancements

- Automated configuration retrieval for **Ollama** and **LMStudio** Reset buttons to streamline model setups.
- Introduced two new **menu sorting options**: sort by *usage frequency* or *last used timestamp*.
- Added **model tag functionality** in Prompts to dynamically select models for flexible configurations.
- Implemented toggle and quantity limit features for *listening tags* to enhance customization.
- Optimized **menu style interaction** for smoother animations and user experience.
- Caching emoji resources to prevent duplication and flickering caused by expiration.
- Refactored configuration code into simplified groups for easier maintainability.
- Enabled search via `[[`/`【【` symbols and optimized the **index algorithm** to boost search efficiency.

### Bug Fixes

- Fixed byte stream discontinuation in large model flow data processing (prevents data loss).
## [1.0.30-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.0.30) (2025-02-26)

### Enhancements

- Added support for encapsulating the thinking module to support thinking models.
- Added support for LM Studio configuration.
- Optimized window scrolling so it only auto-scrolls when reaching the bottom.

### Bug Fixes

- Fixed an issue where Ollama byte streams could cause data loss.
- Optimized code size by removing dependencies on emoji.

## [1.0.27-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.0.27) (2024-12-05)

### Enhancements

- Improved continuation logic to reduce errors in the continuation feature.
- Optimized menu interaction for smoother user experience.
- Rebuilt single service with factory design pattern to support additional services, including Ollama.

### Bug Fixes

- Addressed an issue with the template menu file creation to prevent duplicate creations.
- Addressed an error in component rendering when no window is present.

## [1.0.25-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.0.25) (2024-08-14)

### Enhancements

- Added top-mounted window logo.
- Optimized Chinese words for display.
- Optimized English words for display.
- Optimized template path.
- Updated to the latest GPT-4-mini parameters.

### Bug Fixes

- Fixed the issue where text could not be selected in the pinned window.

## [1.0.23-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.0.23) (2024-05-08)

### Enhancements

- Improved path normalization and ensured markdown file extension for templates.

## [1.0.22-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.0.21) (2024-04-30)

### Bug Fixes

- Fix the problem that the path was created in the root directory.

## [1.0.21-Alpha](https://github.com/yamfeel/coco-askai/releases/tag/1.0.21) (2024-04-28)

### Bug Fixes

- Fix some startup problems.