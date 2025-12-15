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

# Launch CAI
```bash
cai  # first launch it can take up to 30 seconds
```
