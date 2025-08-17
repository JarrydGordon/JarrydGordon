# JarrydGordon

[![GitHub](https://img.shields.io/badge/GitHub-JarrydGordon-blue?style=flat-square&logo=github)](https://github.com/JarrydGordon)
[![Python](https://img.shields.io/badge/Python-3.6+-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)](https://jupyter.org/)

Welcome to my personal GitHub repository! This repository contains tools and tutorials for AI/ML development, particularly focused on large language model deployment and infrastructure.

## 🚀 Projects

### DeepSeek R1 14B with Ollama & Nginx Setup

A comprehensive Jupyter notebook that automates the setup of the DeepSeek R1 14B language model using Ollama, with Nginx reverse proxy and Ngrok tunneling for public access.

**File:** `deepseek-r1-14b-ollama-nginx.ipynb`

#### 🎯 What it does

This notebook provides a complete, automated setup for running the DeepSeek R1 14B model locally with professional-grade infrastructure:

- **Model Deployment**: Downloads and configures DeepSeek R1 14B via Ollama
- **Reverse Proxy**: Sets up Nginx for production-ready request handling
- **Public Access**: Creates secure tunnels using Ngrok for external access
- **Environment Configuration**: Optimizes settings for performance and compatibility

#### 📋 Prerequisites

Before running the notebook, ensure you have:

- Python 3.6 or higher
- Sufficient disk space (DeepSeek R1 14B requires ~8GB)
- Internet connection for model download
- Ngrok account and auth token ([Get one here](https://ngrok.com/))
- Root/sudo access (for Nginx installation)

#### 🛠️ Setup Instructions

1. **Clone this repository**
   ```bash
   git clone https://github.com/JarrydGordon/JarrydGordon.git
   cd JarrydGordon
   ```

2. **Install required Python packages**
   ```bash
   pip install jupyter pyngrok
   ```

3. **Get your Ngrok auth token**
   - Sign up at [ngrok.com](https://ngrok.com/)
   - Copy your auth token from the dashboard

4. **Run the notebook**
   ```bash
   jupyter notebook deepseek-r1-14b-ollama-nginx.ipynb
   ```

5. **Follow the prompts**
   - Enter your Ngrok auth token when requested
   - Wait for the automated setup to complete

#### 🔧 What gets installed

The notebook automatically installs and configures:

- **Ollama**: Local LLM server
- **DeepSeek R1 14B**: The language model
- **Nginx**: Web server and reverse proxy
- **Ngrok**: Secure tunneling service

#### 📡 Usage

Once setup is complete:

1. The notebook will display a public URL (e.g., `https://xxxxx.ngrok-free.app`)
2. Access your DeepSeek R1 model via the Ollama API:
   ```bash
   curl -X POST https://your-ngrok-url.ngrok-free.app/api/generate \
        -H "Content-Type: application/json" \
        -d '{"model": "deepseek-r1:14b", "prompt": "Hello, world!"}'
   ```

#### 🏗️ Architecture

```
Internet → Ngrok Tunnel → Nginx (Port 80) → Ollama (Port 11434) → DeepSeek R1 14B
```

#### ⚠️ Important Notes

- **Security**: The Ngrok tunnel makes your model publicly accessible. Monitor usage and consider authentication for production use.
- **Resources**: DeepSeek R1 14B requires significant computational resources. Performance may vary based on hardware.
- **Costs**: Ngrok free tier has usage limits. Consider upgrading for heavy usage.

#### 🐛 Troubleshooting

**Common Issues:**

1. **"Ollama command not found"**
   - Restart the kernel and re-run the installation cells
   - Ensure `/usr/local/bin` is in your PATH

2. **Nginx permission errors**
   - Make sure you're running with sudo privileges
   - Check that port 80 is not already in use

3. **Ngrok tunnel fails**
   - Verify your auth token is correct
   - Check your Ngrok account limits

4. **Model download timeout**
   - Ensure stable internet connection
   - The 14B model is large (~8GB) and may take time to download

## 🤝 Contributing

Contributions are welcome! If you have improvements or bug fixes:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📬 Contact

- GitHub: [@JarrydGordon](https://github.com/JarrydGordon)
- Feel free to open an issue for questions or suggestions!

---

⭐ If you find this repository helpful, please consider giving it a star!