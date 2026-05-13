# Episode 02 · Network Design and Proxmox Bridges

Commands and configuration for the bridges we create in this episode.

## What we build

Four Linux Bridges in Proxmox, one per network segment. No IPs on the host. No physical NICs attached. Pure internal switches.

| Bridge | Network | Purpose |
|---|---|---|
| vmbr10 | 10.10.10.0/24 | Corporate |
| vmbr20 | 10.10.20.0/24 | DMZ |
| vmbr30 | 10.10.30.0/24 | SOC |
| vmbr40 | 10.10.40.0/24 | Attacker |

## Creating the bridges in the web GUI

1. Log in to Proxmox at `https://[your-proxmox-ip]:8006`
2. Click on your node name in the left tree
3. Click **Network** in the left menu
4. For each bridge:
   - Click **Create** > **Linux Bridge**
   - Name: `vmbr10` (then `vmbr20`, `vmbr30`, `vmbr40`)
   - IPv4: leave empty
   - Bridge Ports: leave empty
   - VLAN aware: unchecked
   - Comment: `Corporate Network 10.10.10.0/24` (adjust per bridge)
   - Click **Create**
5. After all four exist, click **Apply Configuration** at the top
6. Confirm the warning to reload networking

## Verifying from the shell

\`\`\`bash
ip link show | grep vmbr
\`\`\`

All bridges must show `state UP`.

## If a bridge shows DOWN

Most common causes:
1. Apply Configuration was not clicked
2. A typo in the bridge name (Proxmox requires names start with `vmbr`)
3. Networking failed to restart cleanly

Recovery:

\`\`\`bash
systemctl restart networking
ip link show | grep vmbr
\`\`\`

## What we did NOT do (yet)

- We did not assign IPs to any bridge
- We did not connect any bridge to a physical network card
- We did not enable VLANs

These happen later via the firewall (pfSense) or per-VM.

## Reference

- Architecture diagram: [`../docs/architecture-diagram.png`](../docs/architecture-diagram.png)
- Watch the episode: [coming soon]
- Next episode: [Episode 03 — Installing pfSense](../episode-03-pfsense/)
