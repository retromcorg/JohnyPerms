# JohnyPerms
JPerms is a minimal permissions plugin for Project Poseidon that supports UUID-based player permissions. 

## ⚠️ Notice
> JohnyPerms is actively used by RetroMC and a number of other legacy servers, however it **should not be considered a feature-rich permissions plugin** like PermissionsEx or GroupManager.
> It is **minimal**, providing only basic user-management commands. Group management must currently be handled manually through the configuration files at the moment.

> There are no immediate plans to add additional features to the JPerms 1 branch.

## Current capabilities
- **Group and user management:** JSON-backed storage for groups and individual users, including prefixes/suffixes and a configurable default group.
- **Inheritance-aware permissions:** Groups can inherit from other groups, and wildcard permissions are expanded against the server’s registered permissions to keep effective nodes accurate.
- **UUID based:** Player data is stored by UUID allowing persistant permisisons when players change usernames.
- **Command control:** `/jperms` subcommands cover listing and editing user permissions, assigning groups, viewing inheritance, and saving/reloading storage.
- **Optional SuperPerms override:** A configuration toggle injects a custom `PermissibleBase` for servers that need deeper SuperPerms overrides.

## What’s still missing
JPerms is currently a minimum viable product. Some commonly requested niceties are not implemented yet:
- A number of JPerms commands such as adding permissions to groups haven't been added.
- Built-in chat formatting.

## Usage overview
1. Install the plugin and start the server once to generate configuration and language files. The plugin will unload on first run so you can adjust settings.
2. Define groups and set a default group in `permissions.json`, or use the defaults generated.
3. Run `/jperms plugin save` or `/jperms plugin reload` to save or reload data without a restart. You can make changes by saving, modfying `permissions.json`, and then reloading.

## Notes
- If `import.permissionsex` is enabled and PermissionsEx is installed, JPerms will automatically import data and then disable the import flag.
