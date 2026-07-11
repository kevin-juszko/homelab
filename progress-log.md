# Progress Log

## July 2026

### Week 1

#### Initial Decisions
- Chose to add 1TB HDD for ubuntu server VM instead of sharing an SSD and HDD between the Arch install and VM using a LV (logical volume).
- I chose arch as it forces the most hands-on and complex understanding of linux.
- I chose a VM instead of a old laptop for a server so it can have access to more power, and be easily managed from the Arch host. Also it lets me learn virtulization, and network passthrough.
- Arch PC will also be used for Wii and other game emulation.

#### Dev Environment (PC2 - Arch Linux)
- Set up QEMU with Ubuntu Server 24.04 LTS VM
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
  - Allows remote SSH, Navidrome streaming

#### Self-Hosting (Raspberry Pi 5)
- Navidrome music streaming server
- Tailscale exit node configuration

#### KVM Setup
- My KVM setup allows me to switch what controls my two monitors, keyboard, mouse, speakers, headphones, microphone, and any other peripherals. (Switch between PC1, PC2, PS5, Xbox). And the output of the kvm swith to monitor 1 is duplicated through a splitter and transmitted over ethernet (HDBaseT) to output on my TV. Resulting in me seamlessly switching from gaming on my monitor to my tv in another room. Or just sharing my main monitor to my tv.

#### Portfolio
- Created this homelab GitHub repository