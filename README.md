
# lysergicai.com Client

This script is an installer GUI that automatically configures your computer to interface with lysergicai.com privately. It consists of three core applications:
1. [lysergicai.com client](https://github.com/lysergicai/lysergic-ai-client)
2. [Kohya_ss](https://github.com/bmaltais/kohya_ss)
3. [Stable diffusion webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui)

## Server requirements

- NVIDIA GPU
- [CUDA 11.8](https://developer.nvidia.com/cuda-11-8-0-download-archive?target_os=Linux)
- SSD with 30GB free

## Setup Instructions

### Ngrok Setup

1. Sign up at [ngrok](https://dashboard.ngrok.com/signup)
2. Get your [free ngrok static domain](https://dashboard.ngrok.com/cloud-edge/domains)

### Server Setup

1. Create a server at [lysergicai.com](https://lysergicai.com/servers?s=createnew)
2. Copy/Paste your ngrok domain URL into the URL field
3. Click 'Next'

### lysergic-ai-client Installation

1. Open a terminal and clone this repository (lysergic-ai-client):
   ```bash
   git clone https://github.com/lysergicai/lysergic-ai-client.git
   ```

2. Install python, pip, venv, tkinter, psutil - then launch the installer GUI:
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip python3.10-venv python-is-python3 python3-tk
   python -m pip install --upgrade pip
   pip install --upgrade psutil
   cd lysergic-ai-client && python install.py
   ```

3. Copy your ngrok authtoken, ngrok domain & server ID into the installer GUI.

4. Click the 'Install' button and wait for the installation to finish (takes about 10-15 minutes).

5. Click the 'Launch' button, or close the installer GUI and run:
   ```bash
   python launch.py
   ```

6. Click the 'Start' buttons next to the 'kohya_ss' and 'sd_webui' modules and wait for the launch to finish.
   - Note: The first launch takes about 5-10 minutes. Subsequent launches will only take a few seconds.

7. Click the Lysergic_ai 'Start' button.

## Tested on

- Linux (Ubuntu 22.0.4.1), macOS Ventura, Windows 10
- 3090 Ti (24 GB VRAM)
- 48 GB RAM

## Notes

- Use any SDXL checkpoint by adding it to your 'lysergic-ai-client/stable-diffusion-webui/models/Stable-diffusion/XL' directory
- Windows users will need to manually confirm a few GPU settings at the end of the installation process within Windows PowerShell

