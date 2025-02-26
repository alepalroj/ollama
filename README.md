# Ollama v0.5.12 Release Notes

## Overview

**Ollama** is a tool designed to help you get up and running with large language models. With this release, we've introduced new models, improved performance, and fixed various issues to enhance your experience.

For installation, download the appropriate package for your system:
- [Download Ollama for Linux (amd64)](https://github.com/ollama/ollama/releases/download/v0.5.12/ollama-linux-amd64.tgz)

For more details, visit the full release page:
- [Ollama v0.5.12 Release Page](https://github.com/ollama/ollama/releases/tag/v0.5.12)

## New Models

### Perplexity R1 1776
- A version of the DeepSeek-R1 model that has been **post-trained** to remove its refusal to respond to some sensitive topics, expanding its capabilities for a broader range of use cases.

## What's Changed

- **OpenAI-Compatible API**: The API now returns `tool_calls` if the model calls a tool, making it easier to track and debug tool interactions.
- **Intel Xeon Processor Performance**: Performance issues on certain Intel Xeon processors have been restored, providing improved stability and speed.
- **Linux Installation Fixes**:
  - Fixed permission denied issues that could occur after installing Ollama on Linux.
  - Resolved the inclusion of unnecessary CPU libraries in the `arm64` Linux installation.
  - The model now runs without errors on Linux systems where Ollama was installed in a path containing UTF-8 characters.
- **Progress Bar**: The progress bar during `ollama pull` will no longer flicker, providing a smoother user experience.
- **OpenAI API Header Support**: `X-Stainless-Timeout` is now accepted as a header in the OpenAI API endpoints, allowing for more customized interactions.

## Installation

1. Download the appropriate package for your system:
   - [Linux (amd64)](https://github.com/ollama/ollama/releases/download/v0.5.12/ollama-linux-amd64.tgz)
   
2. Extract and install the package:
   ```bash
   tar -xvzf ollama-linux-amd64.tgz
   sudo mv ollama /usr/local/bin/
