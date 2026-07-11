# Progress Log

## July 2026

### Week 1

#### Dev Environment (PC2 - Arch Linux)
- Set up KVM/QEMU with Ubuntu Server 24.04 LTS VM
  - 12GB RAM, 6 vCPUs, 700GB thin-provisioned qcow2
  - Static IP setup
- Configured SSH key authentication to VM from iphone (via terminus), and PC2 
- Configured SSH key authentication to Pi5 from iphone (via terminus), and PC2 
- Set up VS Code Remote-SSH to VM and pi5
- Installed Ollama with qwen2.5-coder:7b for local LLM inference
- Installed Continue.dev VS Code extension connected to local Ollama

#### Networking
- Tailscale mesh architecture for remote access
  - Pi 5 as exit node
  - iPhone as client
  - Covers SSH, Navidrome streaming, general privacy

#### Self-Hosting (Raspberry Pi 5)
- Navidrome music streaming server
- Tailscale exit node configuration

#### Portfolio
- Created this homelab GitHub repository