# ☄️ HexMeteorites.sk

HexMeteorites is a feature-rich Skript plugin that drops meteors filled with loot into random locations across multiple worlds. Includes tier-based rewards, timed spawns, player teleportation, and a full GUI editor for loot customization.

---

## ✨ Features

- ⏱ Auto-scheduled meteor drops
- 🌍 Multi-world random impact location
- 💥 Explosion and lightning effects
- 💰 Loot chest with tiered rewards
- 🟢 Common, 🟡 Rare, 🔴 Legendary loot tiers
- 🧠 Weighted tier roll logic
- 🧱 GUI setup: `/meteortiersetup`
- 📢 Broadcast meteor announcements
- ✅ Auto-clear crater after delay
- 🧭 `/meteortp` command for instant teleport

---

🔧 Requirements

- Skript (2.6+ recommended)
- SkQuery
- Vault
- EssentialsX or another Vault-compatible economy plugin

---

📁 Installation

1. Download and install the required plugins.
2. Place `HexMeteorites.sk` in:
   `/plugins/Skript/scripts/`
3. Reload Skript with:
   `/skript reload HexMeteorites`

---

## 🚧 Roadmap

### 🔨 In Progress
- [x] Tier-based loot system (Common, Rare, Legendary)
- [x] GUI loot editor for each tier
- [x] Multi-world random impact support
- [x] Weighted tier selection logic
- [x] Broadcasts and teleport command
- [x] Auto-clear crater after time

### 📝 Planned Features
- [ ] Custom meteor mob defenders
- [ ] Live event scoreboard (first to loot, most meteors visited)
- [ ] `/meteorstatus` command with countdown
- [ ] Configurable loot effects (particles, sounds)
- [ ] YML-based persistent storage for loot
- [ ] Admin command to spawn meteor manually
- [ ] MythicMobs support for rare spawns

### 💡 Ideas Under Review
- Meteor drop zones (only specific biome/world)
- Faction territory meteor boosts
- Voting or bidding to "call" meteors

---

## 🔧 Configuration

### Options

```skript
options:
    meteor-interval: 30 minutes
    world-names: world, world_nether, world_the_end
    radius: 2000
    chest-lifetime: 5 minutes
    display-prefix: <gradient:#f7941d:#e74c3c>[HexMeteorites]</gradient> &7> 
```

- **meteor-interval**: Time between drops
- **world-names**: Worlds to choose from
- **radius**: Max X/Z coordinate range
- **chest-lifetime**: Time before loot disappears
- **display-prefix**: Prefix for all chat messages

---

## 🧪 Loot Tier System

```skript
{meteorloot::common::*}
{meteorloot::rare::*}
{meteorloot::legendary::*}
```

```skript
{meteortier::weights::common} = 60
{meteortier::weights::rare} = 30
{meteortier::weights::legendary} = 10
```

The plugin randomly selects a tier based on weights and chooses a random item from that tier to place in the meteor chest.

---

## 🖼 GUI Command: `/meteortiersetup`

- Row 1: Common items
- Row 2: Rare items
- Row 3: Legendary items
- Use barrier items to clear each tier
- Closing GUI auto-saves items

---

## 📜 Commands

| Command | Description |
|--------|-------------|
| `/meteortp` | Teleport to the latest meteor drop |
| `/meteortiersetup` | Open GUI to edit loot for all tiers |

---

## 📂 File Structure

```plaintext
HexMeteorites/
├── HexMeteorites.sk
├── LICENSE
└── README.md
```

---

## 📝 License

This project is licensed under the **MIT License (Modified - No Resale)**.  
See the `LICENSE` file for details.

---

## 💖 Support Development

[☕ Donate on Ko-fi](https://ko-fi.com/aponder)
[💸 Donate via PayPal](https://www.paypal.com/donate/?business=6TUCF33LPY9K2&no_recurring=0&item_name=Development+and+Coding+Features&currency_code=USD)

---

## 📬 Contact

Questions or feedback? Reach out via [aponder.dev](mailto:aponder.dev)

---

Thank you for using HexMeteorites! ☄️
