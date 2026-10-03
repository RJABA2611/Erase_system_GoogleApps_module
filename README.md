# Erase System Gapps

**Erase System Gapps** is a systemless Magisk module that removes the Google Apps (GApps) bundled in the system partition of your ROM or GSI, without modifying the partition itself.

## What does it do?

The module uses Magisk's `.replace` mechanism to hide these system components:

- **Google Play Services** (`GmsCore`)
- **Google Play Store** (`Phonesky`)
- **Google Services Framework** (`GoogleServicesFramework`)

It also includes an empty `default-permissions-google.xml`, so no permissions are granted automatically to Google apps.

Since everything is done systemlessly, **your system partition is never touched**. Disabling or removing the module restores everything to its original state.

## Who is it for?

It was created for custom ROMs and GSIs that ship with GApps preinstalled, for people who want a cleaner system with fewer Google services running in the background. Apps installed by the user in the data partition are not affected.

## Requirements

- A device with root through **Magisk v20.4 or newer**
- A ROM or GSI that includes GApps in the system partition

## Installation

1. Download the latest `.zip` from the **Releases** section.
2. Open Magisk and go to **Modules → Install from storage**.
3. Select the zip file.
4. Reboot your device.

## Uninstallation

Open Magisk, go to **Modules**, remove the module and reboot.

## Tested on

- Samsung Galaxy Tab A7 Lite (SM-T220) running a GSI

## Important notice

Without Google Play Services and the Play Store, apps that depend on them (push notifications, Google sign-in, in-app purchases, maps) may stop working. Make a backup before installing. Use it at your own risk.

## Author

Created by RJABA26, as my first Magisk module.
