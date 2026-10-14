# Build troubleshooting

## Workflow says `lb: command not found`
The workflow installs `live-build`; rerun the workflow after checking the Install live-build step.

## Workflow fails while downloading packages
Rerun it. Debian mirrors or GitHub-hosted networking can occasionally fail. If it repeats, inspect the first
package/repository error in the Actions log.

## ISO builds but VM shows a black screen
Try disabling 3D acceleration, increase RAM to 4 GB, and use the VM's default graphics controller.
The ISO targets x86_64/amd64 PCs, not ARM-only devices.

## Apps do not appear
Use the Applications menu. Some desktop launchers can be hidden by the desktop environment; the installed
apps are also available from the menu and can be started by their command names.

## Note about the first build
The initial workflow builds a Debian live ISO with stock XFCE defaults plus KOS launchers and welcome page.
A later release can add a fully custom dock/window shell, KOS Store UI, installer branding, and a custom boot theme.
