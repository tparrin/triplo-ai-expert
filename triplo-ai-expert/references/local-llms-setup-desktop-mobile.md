# Local LLMs Setup (Desktop and Mobile)

## Overview

Triplo AI can route requests to **local LLMs** running on your hardware, providing privacy, offline capability, and cost savings. This guide covers setting up local models on desktop and accessing them from mobile devices.

## Desktop Setup

### Step 1: Choose Your Inference Engine

**Popular options**:

| Engine | Best For | Difficulty | Features |
|--------|-----------|-------------|-----------|
| **Ollama** | Beginners, ease of use | Easy | Simple CLI, auto-download |
| **llama.cpp** | Performance, efficiency | Medium | Fast, optimized |
| **vLLM** | GPU performance, production | Hard | High performance |
| **Text Generation WebUI** | Visual interface | Easy | Web UI, many features |

**Recommendation**: Start with Ollama for simplicity, then explore others.

### Step 2: Install Inference Engine

**Ollama (Recommended for beginners)**:

**Windows**:
1. Download from [ollama.ai](https://ollama.ai)
2. Run installer
3. Open Command Prompt
4. Test: `ollama --version`

**macOS**:
1. Download from [ollama.ai](https://ollama.ai)
2. Install .dmg
3. Open Terminal
4. Test: `ollama --version`

**Linux**:
```bash
curl -fsSL https://ollama.ai/install.sh | sh
```

**llama.cpp**:

1. Clone repository: `git clone https://github.com/ggerganov/llama.cpp`
2. Build following README instructions
3. Download model weights
4. Run inference server

### Step 3: Download Models

**Using Ollama**:
```bash
# Download Llama 3 8B
ollama pull llama3:8b

# Download Mistral 7B
ollama pull mistral:7b

# Download Phi-3 Mini
ollama pull phi3:mini
```

**Using llama.cpp**:
1. Download model weights from Hugging Face
2. Place in models directory
3. Convert to GGUF format if needed
4. Configure for inference

### Step 4: Start Local Server

**Ollama**:
```bash
# Start server (default port 11434)
ollama serve

# Start on specific port
ollama serve --port 8080
```

**llama.cpp**:
```bash
# Start server
./server --model path/to/model.gguf --port 8080
```

**Verify server is running**:
- Check that server is listening on configured port
- Test with curl or browser
- Example: `http://localhost:11434`

### Step 5: Configure Triplo AI

**Connect Triplo to local model**:

1. Open Triplo AI
2. Go to Settings → Models
3. Select "Local Models" or "Custom Endpoint"
4. Enter endpoint URL:
   - Ollama: `http://localhost:11434`
   - Custom: Your server URL
5. Select model name
6. Test connection
7. Save settings

**Configuration options**:
- **Endpoint URL**: Where local server is running
- **Model name**: Which model to use
- **Temperature**: Response randomness
- **Max tokens**: Response length limit

### Step 6: Test Integration

**Test workflow**:
1. Select local model in Triplo
2. Trigger Triplo with a simple prompt
3. Verify response from local model
4. Check performance and quality
5. Adjust settings if needed

**Test prompts**:
- "Hello, can you hear me?"
- "What is 2+2?"
- "Summarize this text: [short text]"

## Mobile Setup

### Option 1: Mobile-Optimized Local Models

**Run local models directly on mobile**:

**iOS**:
1. Download local LLM app (e.g., MLC LLM, Draw Things)
2. Download model weights
3. Configure model settings
4. Use app's interface

**Android**:
1. Download local LLM app (e.g., MLC LLM, AICP)
2. Download model weights
3. Configure model settings
4. Use app's interface

**Limitations**:
- Smaller models only (3B-7B)
- Slower performance
- Limited features
- Battery drain

### Option 2: Access Desktop Local Model from Mobile

**Route mobile requests to desktop local model**:

**How it works**:
1. Desktop runs local model server
2. Desktop exposes server to network
3. Mobile app connects to desktop server
4. Requests routed through network

**Setup steps**:

**1. Expose Desktop Server**:

**Ollama**:
```bash
# Listen on all interfaces
OLLAMA_HOST=0.0.0.0 ollama serve

# Or modify ollama config
```

**2. Configure Network**:
- Allow port through firewall
- Use static IP or DNS
- Consider VPN for security

**3. Configure Triplo Mobile**:
1. Open Triplo mobile app
2. Go to Settings → Models
3. Select "Custom Endpoint"
4. Enter desktop URL:
   - Local network: `http://192.168.1.X:11434`
   - External: `http://your-domain.com:11434`
5. Test connection
6. Save settings

**Security considerations**:
- Use strong authentication
- Use HTTPS if exposing externally
- Consider VPN for remote access
- Monitor access logs

### Option 3: Cloud-Hosted Local Model

**Host local model on cloud VPS**:

**Setup**:
1. Rent VPS with GPU
2. Install inference engine (Ollama, etc.)
3. Download and run model
4. Expose via HTTPS
5. Configure Triplo to use cloud endpoint

**Benefits**:
- Access from anywhere
- Better performance than mobile
- Still "local" (your instance)
- Privacy maintained

**Providers**:
- RunPod
- Lambda Labs
- Vast.ai
- Google Cloud, AWS, Azure

## Advanced Configuration

### Multiple Models

**Run multiple models simultaneously**:

**Ollama**:
```bash
# Download multiple models
ollama pull llama3:8b
ollama pull mistral:7b
ollama pull phi3:mini

# All models available via same endpoint
```

**Configure in Triplo**:
- Switch between models in settings
- Use different models for different tasks
- Set default model per device

### Model Quantization

**Reduce VRAM requirements**:

**Ollama**:
```bash
# Pull quantized version
ollama pull llama3:8b-q4_K_M

# Available quantizations: q4, q5, q8
```

**Benefits**:
- Run larger models on smaller GPUs
- Faster inference
- Lower memory usage

**Trade-offs**:
- Slightly lower quality
- May affect certain tasks

### Performance Tuning

**Optimize for speed**:
- Use GPU acceleration
- Quantize model
- Reduce context window
- Use smaller models

**Optimize for quality**:
- Use larger models
- Higher precision (FP16)
- Larger context window
- Adjust temperature

**Monitor performance**:
- GPU/VRAM usage
- Inference speed (tokens/second)
- Memory consumption
- Temperature and power

## Troubleshooting

### Desktop Issues

**Issue: Server won't start**
- **Solution**: Check port availability, verify installation
- **Check**: Firewall, permissions, dependencies

**Issue: Triplo can't connect**
- **Solution**: Verify endpoint URL, test with curl
- **Check**: Server is running, correct port, firewall

**Issue: Out of memory**
- **Solution**: Use smaller model, quantize more
- **Check**: VRAM usage, model size

**Issue: Slow performance**
- **Solution**: Use GPU, quantize model, reduce context
- **Check**: Hardware acceleration, model size

### Mobile Issues

**Issue: Can't connect to desktop**
- **Solution**: Verify network, check firewall, test URL
- **Check**: Desktop server running, network accessible

**Issue: Connection drops**
- **Solution**: Check network stability, use VPN
- **Check**: Wi-Fi signal, router settings

**Issue: Mobile local model slow**
- **Solution**: Use smaller model, close other apps
- **Check**: Device performance, battery mode

**Issue: Poor quality on mobile**
- **Solution**: Use larger model, adjust parameters
- **Check**: Model capabilities, prompt quality

## Best Practices

### For Desktop Setup

1. **Start simple**
   - Use Ollama for easy setup
   - Start with smaller models
   - Test thoroughly

2. **Secure your setup**
   - Don't expose externally without auth
   - Use firewall rules
   - Monitor access

3. **Optimize for your hardware**
   - Match model to VRAM
   - Use quantization if needed
   - Monitor performance

4. **Document configuration**
   - Record model versions
   - Note settings
   - Track performance

### For Mobile Setup

1. **Choose right approach**
   - Mobile local: Simple but limited
   - Desktop routing: Better performance
   - Cloud hosting: Best but costs money

2. **Consider network**
   - Local network: Faster, more secure
   - External: Slower, security concerns
   - VPN: Secure but overhead

3. **Test thoroughly**
   - Test connection stability
   - Verify performance
   - Check battery impact

### For Security

1. **Protect your endpoints**
   - Use authentication
   - Use HTTPS for external access
   - Monitor access logs

2. **Understand data flow**
   - Where does data go?
   - Is it truly local?
   - Any external calls?

3. **Keep software updated**
   - Update inference engines
   - Update Triplo AI
   - Monitor for vulnerabilities

## Performance Benchmarks

### Expected Performance

**By Hardware**:

| Hardware | Model | Speed (tokens/s) | Quality |
|----------|--------|-------------------|----------|
| **RTX 3060 (12GB)** | Llama 3 8B (4-bit) | 50-70 | Good |
| **RTX 3070 (8GB)** | Llama 3 8B (4-bit) | 60-80 | Good |
| **RTX 3080 (10GB)** | Llama 3 8B (8-bit) | 40-60 | Very Good |
| **RTX 3090 (24GB)** | Llama 3 70B (4-bit) | 20-30 | Very Good |
| **M1/M2 Mac** | Llama 3 8B (4-bit) | 15-25 | Good |
| **CPU Only** | Phi-3 Mini | 2-5 | Fair |

**Note**: Actual performance varies by configuration and quantization.

## Next Steps

- **Learn about local model strengths**: [`local-models-strengths.md`](local-models-strengths.md)
- **Understand model selection**: [`models-allowances-and-byok.md`](models-allowances-and-byok.md)
- **Explore OpenRouter models**: [`openrouter-models-strengths.md`](openrouter-models-strengths.md)

---

**Official Documentation**: [documentation.triplo.ai/using-triplo-ai/local-llms](https://documentation.triplo.ai/using-triplo-ai/local-llms)
