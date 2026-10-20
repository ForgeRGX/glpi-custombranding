# GLPI Custom Branding

A community-maintained fork of [i-Vertix/glpi-modifications](https://github.com/i-Vertix/glpi-modifications), a GLPI plugin for customizing branding elements such as logos, the browser tab title, and the login-page background.

This fork is maintained by [ForgeRGX](https://github.com/ForgeRGX) in the repository [ForgeRGX/glpi-custombranding](https://github.com/ForgeRGX/glpi-custombranding).

## Features

- Customize the branding logos used by GLPI.
- Customize the page title shown in the browser tab.
- Add a background image to the login page.

## Compatibility

- Intended targets: GLPI 11.x and GLPI 12.x.
- PHP requirements depend on the GLPI version in use. Check the official [GLPI requirements](https://glpi-install.readthedocs.io/en/latest/prerequisites.html) before installing.
- The plugin does not use GLPI's external REST API for its core branding functionality. Migrating to the GLPI High-Level API v3 is therefore not, by itself, required for this plugin.
- Compatibility declarations in the plugin metadata are not proof of runtime compatibility. Test installation, activation, branding changes, login-page background delivery, deactivation, and uninstall/backup restoration on the exact GLPI and PHP versions you run.

> **Status:** GLPI 12 compatibility is a target and requires validation against a real GLPI 12 instance. Do not treat a successful PHP syntax check or a version declaration as a complete integration test.

## Installation

1. Back up your GLPI installation and any existing branding assets.
2. Download or clone this repository.
3. Copy the plugin directory into GLPI's `plugins` directory, or into `marketplace` if that is how you manage local plugins.
4. The plugin directory must be named `mod` for GLPI to recognize it with the current plugin identifier.
5. Ensure the web-server account has the permissions required to read the plugin files and write to the locations used by the plugin. Adapt ownership and paths to your operating system and installation; do not blindly copy example paths from another server.
6. Sign in to GLPI with an account that can manage plugins, install the plugin, and activate it.
7. Open the plugin's **Configure** page to manage branding settings.

Refer to the upstream project documentation for additional details and deployment-specific permission examples: [i-Vertix/glpi-modifications](https://github.com/i-Vertix/glpi-modifications).

## Updating and uninstalling

- Back up your GLPI installation and branding assets before updating.
- Follow the plugin's documented deactivation/uninstallation procedure before deleting its files, so that any backed-up original assets can be restored where supported.
- Verify the restoration behavior in a test environment before using it on a production instance.

## Differences from upstream

This fork's goal is to maintain the plugin for GLPI 11 and investigate/adapt compatibility with GLPI 12. Changes should be documented in commits and tested against the supported GLPI versions. Until the GLPI 12 runtime tests are complete, compatibility with every GLPI 12 minor release is not guaranteed.

## Upstream project and attribution

- Upstream repository: [i-Vertix/glpi-modifications](https://github.com/i-Vertix/glpi-modifications)
- Original project credits, notices, and license are retained in the repository.
- This fork is independent and is not affiliated with or endorsed by the GLPI project or i-Vertix.

## License

This project retains the upstream license. See [`LICENSE`](LICENSE) for the full license text. The upstream project identifies its license as GNU GPL v3 or later; review the included license file before redistributing modified versions.
