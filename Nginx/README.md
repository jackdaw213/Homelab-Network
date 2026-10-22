## Setup

1. Enable WebSocket Support for the following services:
    - **Home Assistant**
    - **Immich**
    - **Crafty**
    - **Jellyfin**
    - **Proxmox**

2. Use HTTPS for the following services
    - **Portainer**
    - **Proxmox**
    - **Crafty WebUI** (**Crafty Server itself:** Use HTTP only (not for the web UI))

3. Create a New Access List with the following settings:
    - **Name:** `Admin`
    - **Satisfy:** `Any`
    - **Pass Auth:** `True`
    - **Allow:**
    - `<Laptop’s WireGuard IP>`
    - `<Main PC’s IP Address>`
    - **Deny Everything Else**

    > [!NOTE]
    > It's not necessary but with this Nginx only allows your machine to access critical pages (remember to change the access list of any services you don't want people to access)
