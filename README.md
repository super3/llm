# WebLLM Chat

A fully browser-based chat interface powered by [WebLLM](https://github.com/mlc-ai/web-llm). Run large language models completely locally in your browser with no server required.

## Features

- **100% Local & Private** - Everything runs in your browser, no data sent to servers
- **WebGPU Accelerated** - Fast inference using WebGPU for hardware acceleration
- **Multiple Chats** - Create and manage multiple conversation threads
- **Persistent Storage** - Conversations saved locally in browser storage
- **Modern UI** - Clean, dark-themed interface inspired by ChatGPT
- **Collapsible Sidebar** - Space-efficient layout with icon-only collapsed state
- **Offline Capable** - Works completely offline after initial model download

## Model

Currently uses **Phi-3-mini-4k-instruct** (~2.5GB) - a compact, high-quality model perfect for general chat applications.

## Requirements

- **WebGPU-capable browser**:
  - Chrome/Edge 113+
  - Safari (latest)
  - Firefox with WebGPU enabled
- **~3GB RAM** available
- **Internet connection** (first load only, to download model)

## Usage

Simply open `index.html` in a WebGPU-capable browser:

```bash
open index.html
```

**First Load:**
- The model will download (~2.5GB) - this may take a few minutes
- Progress is shown in the status bar
- Model is cached locally for subsequent visits

**After Loading:**
- Create new chats with the "New chat" button
- Switch between chats in the sidebar
- Collapse sidebar for more space
- All chats persist across browser sessions

## How It Works

This application uses:
- **WebLLM** - Browser-based LLM inference engine
- **WebGPU** - For hardware-accelerated model execution
- **localStorage** - For persisting chat history
- Pure HTML/CSS/JavaScript - No build tools required

## Browser Compatibility

| Browser | Support | Notes |
|---------|---------|-------|
| Chrome 113+ | ✅ Full | Best performance |
| Edge 113+ | ✅ Full | Best performance |
| Safari (latest) | ✅ Full | Good performance |
| Firefox | ⚠️ Partial | Requires WebGPU flag |

## Privacy

All inference happens locally in your browser. No data is sent to external servers. Chat history is stored only in your browser's localStorage.

## License

MIT