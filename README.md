# VintageAFKIssues
Issue Tracker Repo for https://mods.vintagestory.at/show/mod/19017

Here’s the markdown version for easy copy-pasting into GitHub:  

```markdown
# VintageAFK – Enhanced AFK System for Vintage Story

**VintageAFK** is a powerful and customizable AFK management mod for *Vintage Story*, designed for both single-player and multiplayer. It provides a range of options to improve the AFK experience, including:  

- **Skyrim-style AFK Camera Spin** – A dynamic third-person camera animation when AFK.  
- **Invincibility While AFK** – Prevents damage while idle (configurable).  
- **No Hunger Drain While AFK** – Stops food saturation from depleting.  
- **AFK Timer with Visual Indicator** – An animated GUI element showing time until AFK.  
- **Customizable AFK Behavior** – Full control via client and server-side configurations.  

---

## Configuration & Features  

VintageAFK includes both **client-side** and **server-side** configuration files, which are generated in the `modconfig` folder upon the first run.  

### Server Configuration (`serverconfig.json`)  

```json
{
  "TimeUntilAFK": 300,
  "UnAFKOnChat": true,
  "UnAFKOnMouseMove": false,
  "UnAFKOnMouseClick": true,
  "AFKDisablesHunger": true,
  "AFKDisablesHealth": true,
  "OverrideClientConfig": true,
  "UseVisualAFKSystem": true,
  "AfkCameraSpin": true,
  "VerboseLogging": true,
  "DebugMode": true,
  "AfkCommandHostileRadius": 15
}
```

- **TimeUntilAFK** (default: 300s) – Time (in seconds) before a player is marked as AFK.  
- **UnAFKOnChat / Mouse Move / Mouse Click** – Choose which actions remove AFK status.  
- **AFKDisablesHunger / Health** – Prevent hunger drain and damage while AFK.  
- **OverrideClientConfig** – Allows server admins to enforce settings on all players.  
- **UseVisualAFKSystem** – Enables the AFK timer GUI element.  
- **AfkCameraSpin** – Toggles the third-person AFK camera spin effect.  
- **AfkCommandHostileRadius** (default: 15 blocks) – Prevents AFK mode if hostile mobs are nearby.  
- **VerboseLogging / DebugMode** – Enables extra debugging details for server admins.  

### Client Configuration (`clientconfig.json`)  

```json
{
  "UseVisualAFKSystem": true,
  "AfkCameraSpin": true
}
```

- **UseVisualAFKSystem** – Enables the animated GUI timer.  
- **AfkCameraSpin** – Enables the cinematic third-person camera effect.  

---

## Commands & Permissions  

- **`/afk`** – Manually enter AFK mode (restricted by hostile radius setting).  
- **`/vafkconfig <time>`** *(Requires `VAFKAdmin` permission)* – Instantly adjust and reload the AFK timeout duration.  

### Permissions  

- **`VAFKCommand`** – Required to use `/afk`.  
- **`VAFKAdmin`** – Grants access to `/vafkconfig`.  
- **Admin Controls** – All permissions are automatically assigned to the admin group by default.  

---

## Server-Side Control & Anti-Abuse Measures  

- **Hostile Mob Radius Protection** – Players cannot activate AFK mode if a hostile mob is within **15 blocks** (prevents abuse of invincibility while in combat).  
- **Client Configuration Override** – Server admins can force client settings to maintain control over AFK mechanics.  

Whether you want a hands-free AFK system or strictly controlled multiplayer settings, **VintageAFK** gives you the tools to customize the experience exactly how you want.  
```
