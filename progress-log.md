# Progress Log

## July 2026

### Week 1

#### Initial Decisions
- Chose to add 1TB HDD for ubuntu server VM instead of sharing an SSD and HDD between the Arch install and VM using a LV (logical volume).
- I chose arch as it forces the most hands-on and complex understanding of linux.
- I chose a VM instead of a old laptop for a server so it can have access to more power, and be easily managed from the Arch host. Also it lets me learn virtulization, and network passthrough.
- Arch PC will also be used for Wii and other game emulation.
- Chose to use VS Code due to Azure support.

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
> [!WARNING]
> UFW and libvirt had an issue when setting up the ubuntu server VM that caused automatic DHCP configuratiion to fail.
- Investigated firewall settings and dnsmasq logs to check for misconfigurations or errors. This revealed nothing.
- Claude found the issue. **"Default: deny (routed) — this is very likely our culprit. UFW's default policy is denying routed (forwarded) traffic between network interfaces, which includes traffic passing through the bridge (virbr0) — this is a well-known interaction issue between UFW and libvirt's virtual networking."**


- Tailscale mesh architecture for remote access
  - Pi 5 as exit node
  - iPhone as client (will probably add laptop too)
  - Allows remote access to use SSH and Navidrome streaming
  > [!WARNING]
  > SSH passkey still enabled even after disabling in configs. "PasskeyAuthentication no". Found a second instance of this variable in another config (Cloud-Init) that was overriding this.

#### Self-Hosting (Raspberry Pi 5)
- Navidrome music streaming server
- Tailscale exit node configuration

> [!WARNING]
> Had an issue where audio on Arch was quite low.
- Fix was to change amixer settings to fix ALSA hardware volume control for audio out to DAC. Decibal settings were at 72/127dB changed to 110/127dB


#### Other Tasks
- Installed Yay (AUR manager). Used Yay to install claude.ai desktop app, discord, vs code.
- Added the following extensions to VS Code: Python, SVG Preview, Claude, Continue.dev

#### Portfolio
- Created this homelab GitHub repository