# Installation Guide: LOTL-LAN 🦀

Follow these steps to configure your environment for version **1.9.57**. This tool requires specific system-level dependencies to capture live network traffic.

## 1. System Level Dependencies (Required)

The core engine uses `PyShark`, which is a wrapper for **TShark**. You must install TShark before running the Python script.

### Linux (Debian/Ubuntu)
```bash

sudo apt-get update
sudo apt-get install tshark
# During installation, select 'Yes' when asked if non-superusers should capture packets.
sudo usermod -a -G wireshark $USER

MAC
brew install wireshark

Windows

    Download the Wireshark installer from wireshark.org.

    Run the installer and ensure TShark is checked.

    Add the Wireshark installation folder (usually C:\Program Files\Wireshark) to your System PATH.

Python Environment Setup

We recommend using a Virtual Environment (venv) to avoid library conflicts.
Create the Environment
Bash

# Navigate to the project folder
cd lotl-lan

# Create the virtual environment
python -m venv venv

Activate the Environment

    Linux/macOS:
    Bash

    source venv/bin/activate

    Windows:
    Bash

    .\venv\Scripts\activate

3. Install Python Dependencies

With your virtual environment active, install the required libraries:
Bash

pip install -r requirements.txt

4. Troubleshooting & Permissions
Permissions Error

If the HUD fails to see your network interfaces, it is likely a permissions issue.

    Linux: Ensure your user is in the wireshark group as shown in Step 1.

    Windows: Run your terminal (PowerShell or CMD) as Administrator.

Interface Selection

When the HUD launches, use the sidebar to select the correct interface (e.g., eth0 for wired, wlan0 for Wi-Fi). If you see "No packets," ensure your interface is active and connected to the LAN.
5. Execution

To launch the tactical HUD:
Bash

streamlit run lotl_lan.py
