# ⚙️ Setting up CAI (Cybersecurity AI) on Linux

CAI is an open‑source framework for benchmarking, evaluating, and automating infosec workflows with local LLMs.  
Follow these steps to install and run CAI in a clean Python environment.

```bash
sudo apt-get update && \
    sudo apt-get install -y git python-pip python3-venv
```

# Clone the git
```bash
git clone https://github.com/aliasrobotics/cai.git
cd ~/cai
```

# Create the virtual environment
```bash
python3 -m venv cai_env
```

# Install the package from the local directory
```bash
source cai_env/bin/activate && pip install -e .
```

# Generate a .env file and set up with defaults
```bash
echo -e 'OPENAI_API_KEY="sk-1234"\nANTHROPIC_API_KEY=""\nOLLAMA=""\nPROMPT_TOOLKIT_NO_CPR=1' > .env
```

# Alternatively you can use mine as an example:
```bash
# ------------ API / MODEL ------------

OPENAI_API_KEY="sk-123"                        
OPENAI_API_BASE="http://YOUR_HOST_MACHINE_IP:1234/v1"
OPENAI_API_TYPE="openai" #ALWAYS SET openai here if you are running LM Studio
CAI_MODEL="openai/qwen3-coder-30b-a3b-instruct" # you'll need your exact model name here
#CAI_MDOEL="openai/mistralai/ministral-3-14b" # another example of exact model name

# Support agent (optional but supported)
#CAI_SUPPORT_MODEL="openai/lily-cybersecurity-7b-v0.2"
CAI_SUPPORT_INTERVAL=5

# ------------ AGENT (COMPATIBLE) ------------

CAI_AGENT_TYPE="redteam_agent"
CAI_PARALLEL=2                      # 3 redteam agents running in parallel (same agent)

# ------------ LIMITS ------------

CAI_TOOL_TIMEOUT=180
CAI_RETRIES=2
CAI_MAX_TURNS=60
CAI_MAX_INTERACTIONS=100

# ------------ MEMORY / CONTEXT ------------

CAI_MEMORY=true
CAI_MEMORY_MODE="episodic"
CAI_ENV_CONTEXT=true
CAI_TELEMETRY=false

# ------------ OUTPUT ------------

CAI_DEBUG=1
CAI_STREAM=true
CAI_BRIEF=false
CAI_GUARDRAILS=false
```

# Launch CAI
```bash
cai  # first launch it can take up to 30 seconds
```
