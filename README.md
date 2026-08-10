# Advanced Checkpoint Editor

**Advanced Checkpoint scenario and Mutator configuration builder for Insurgency: Sandstorm.**

Advanced Checkpoint Editor is a browser-based configuration tool for creating, editing, and generating advanced **Checkpoint Co-op Mutator** configurations for *Insurgency: Sandstorm*.

It provides a structured interface for configuring AI forces, checkpoint-specific deployments, counter attacks, fire support, objective supplies, traps, and other advanced gameplay systems without manually editing large and complex `.ini` configuration files.

---

## Features

### AI Soldier Classes

* Register custom `AISoldierClasses`
* Automatic index assignment
* Built-in custom class presets
* Manual class path input
* Class removal rules by index
* Class removal rules by keyword
* `EnemyForceTips` configuration
* Rich Text support for enemy force messages

### Checkpoint / Bot Soldier Configuration

Configure individual checkpoints using:

* Default configuration
* Counter Attack configuration
* A–Z checkpoint configurations
* Custom AI soldier classes
* Class removal rule sets
* Enemy Force Tips
* Revenge Fire Support sets

This allows different checkpoints to use completely different enemy compositions and behaviors.

### Retaliatory Counter Attack

Configure enemy counter attacks when players remain at a captured or defended objective for too long.

Options include:

* Activation range
* Trigger probability
* Minimum / maximum trigger interval
* Counter Attack intensity
* Assault reinforcement count
* Map exclusions
* Center-screen messages
* Chat messages
* Counter Attack duration
* Post-counter-attack behavior
* Player respawn behavior
* Revenge Fire Support groups
* Revenge Fire Support timing and frequency

### Custom Fire Support

Register custom fire support resources and automatically assign indexes.

Custom fire support definitions can be shared by:

* Threat Fire Supports
* HQ Fire Supports
* Revenge Fire Support

The editor supports both built-in presets and manually entered resource paths.

### Objective Spawn Armaments

Configure equipment spawned around destructible objectives, including:

* Ammunition
* Weapon-related supplies
* Spawn quantities
* Spawn distance
* Applicable objectives

### Objective Door Traps

Configure traps around objectives with options for:

* Trap type
* Applicable checkpoints
* Spawn probability
* Spawn radius
* Closed / intact door requirements
* AI avoidance probability

> Avoid using this feature together with mods that continuously scan doors, as excessive scanning may negatively affect client FPS.

### Threat Fire Supports

Configure enemy fire support triggered by player concentration or surviving classes.

Options include:

* Minimum surviving player count
* Trigger interval
* Individual fire support probabilities
* Number of calls
* Warning messages
* Priority target classes
* Cluster detection
* Detection radius

### HQ Fire Supports

Configure player-requested HQ fire support through chat commands.

Features include:

* Unlock checkpoints
* Notification delay
* Request timeout
* Custom chat commands
* Available fire support
* Warning messages
* Call limits
* Authorized classes
* Request / approval / timeout messages
* Landing location prompts and validation

---

## Configuration Workflow

The intended workflow is:

```text
Select Mutator Instance
        ↓
Configure AI Classes
        ↓
Configure Checkpoint Forces
        ↓
Configure Counter Attacks
        ↓
Configure Fire Support
        ↓
Configure Objectives
        ↓
Generate .ini
        ↓
Copy / Download
        ↓
Add to Mutators.ini
        ↓
Test In-Game
```

The editor is designed to replace repetitive manual editing of complex configuration blocks with a structured configuration interface.

---

## Import & Export

Configurations can be saved and transferred using JSON.

Supported operations:

* Export configuration to JSON
* Import configuration from JSON
* Reset the current configuration
* Generate the final `.ini` configuration

This makes it possible to maintain different scenario configurations and share them between users.

---

## Multi-Instance Support

Multiple **AdvancedCheckpoint** Mutator instances can be configured independently.

This allows a server to maintain multiple configuration blocks and combine different AdvancedCheckpoint configurations when required.

---

## Built for Mod Developers

Advanced Checkpoint Editor is primarily intended for:

* Insurgency: Sandstorm mod developers
* Server administrators
* Custom Co-op scenario creators
* Mutator developers
* Advanced server configuration

The tool is particularly useful for large configurations where manually maintaining indexes, checkpoint mappings, class lists, fire support groups, and message definitions becomes error-prone.

---

## Client-Side & Offline

The editor runs entirely in the user's browser.

It does **not** require:

* A backend server
* An API
* A database
* An account
* External CDN resources
* Server-side processing

Configuration data is processed locally in the browser and is not uploaded by the application.

The tool can therefore be used as a standalone local web application as well as through GitHub Pages.

---

## Technology

Built using standard web technologies:

* HTML
* CSS
* JavaScript

No build system or backend service is required for the application itself.

---

## Important Notes

`CustomAISoldierClasses` and `CustomFireSupport` are resource path references.

The referenced mod must still be installed on the target server for the configuration to function.

Elements within the same collection must not contain duplicate entries.

Generated configuration should always be tested against the target game version and installed mod versions.

---

## Project Status

**Active Development**

The editor is continuously expanded as additional AdvancedCheckpoint configuration options and practical modding use cases are identified.

---

## Disclaimer

This is an independent community-made tool.

It is **not an official tool** and is not affiliated with, sponsored by, or endorsed by New World Interactive or Focus Entertainment.

*Insurgency: Sandstorm* and all related trademarks and intellectual property belong to their respective owners.

---

## Links

* **Web Application:** https://leimuu.github.io/AdvancedCheckpointEditor/
* **Repository:** https://github.com/LeiMuu/AdvancedCheckpointEditor

---

## License

See the repository for licensing information.
