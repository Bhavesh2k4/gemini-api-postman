# Postman Gemini API Collection 🚀

This repository contains Postman collections for interacting with the **Google Gemini API**. It provides ready-to-use requests for various Gemini API capabilities.

## 📌 Features

* **Chat Conversations** - Simple and multi-turn chat interactions
* **Code Generation & Analysis** - Generate, explain, and debug code
* **Text Generation** - Basic and advanced text generation with parameter control
* **Embedding Generation** - Create text embeddings for semantic search
* **System Instructions** - Customize AI behavior with system prompts
* **Streaming Responses** - Stream text generation and chat responses
* **Multimodal Capabilities** - Process and analyze images
* **Structured Output** - Generate responses in structured formats like JSON
* **Function Calling** - Define and use tools for enhanced capabilities

## 🔧 Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Bhavesh2k4/gemini-api-postman.git
   ```

2. **Import into Postman**
   * Open **Postman**
   * Go to **File > Import**
   * Select the downloaded collection JSON files

3. **Set Up Environment Variables**
   * Configure the following variables in your Postman environment:
     * `GOOGLE_API_KEY` - Your Gemini API key 
     * `API_BASE_URL` - API base URL (default: https://generativelanguage.googleapis.com/v1beta)
     * `MODEL_VERSION` - Gemini model version (default: gemini-1.5-flash)
     * `BASE64_IMAGE` - Base64-encoded image for multimodal requests (optional)
     * `BASE64_IMAGE1` - Additional base64-encoded image (optional)

## 🗂️ Collection Overview

| Collection | Description |
|------------|-------------|
| **Chat** | Simple and multi-turn conversation examples |
| **Code** | Code generation, explanation, and debugging |
| **Text Generation** | Basic and advanced text generation with parameters |
| **Embedding** | Text embedding generation |
| **System Instructions** | Examples using system prompts |
| **Streaming** | Stream text generation and chat responses |
| **Multimodal** | Process and analyze images |
| **Structured Output** | Generate structured JSON responses |
| **Function Calling** | Define and use tools for enhanced capabilities |

## 🛠️ Usage Examples

### Simple Chat Request
```json
{
  "contents": [
    {
      "role": "user",
      "parts": [{
        "text": "Hello, I'm learning to use the Gemini API"
      }]
    }
  ]
}
```

### Code Generation
```json
{
  "contents": [{
    "parts":[{
      "text": "Write a Python function that gets the prime numbers within a certain range"
    }]
  }],
  "generationConfig": {
    "temperature": 0.2,
    "topK": 1,
    "topP": 0.8,
    "maxOutputTokens": 1000
  }
}
```

### Processing Images
```json
{
  "contents": [{
    "parts":[
      {"text": "Describe what you see in this image in detail."},
      {
        "inline_data": {
          "mime_type":"image/jpeg",
          "data": "{{BASE64_IMAGE}}"
        }
      }
    ]
  }]
}
```

## 📢 Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the collection.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🔒 Security

This collection does not include sensitive API keys. Make sure to:
- Keep your API keys private
- Never commit sensitive information to public repositories
- Use environment variables for all sensitive data

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.
