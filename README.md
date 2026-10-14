# KOS — Kevin Operating System

KOS is a custom Debian-based Linux live system with a dark, futuristic XFCE desktop.
This repository is designed to be edited from an iPad browser and built into a bootable
ISO by GitHub Actions. You do **not** need a Mac.

## What is included

- Debian Linux base and XFCE desktop
- Firefox ESR browser
- Geany coding platform (syntax highlighting, projects, terminal integration)
- Thunar file manager
- XFCE settings tools
- Synaptic package manager (KOS's initial app-installation center)
- KOS-branded desktop shortcuts, wallpaper, and welcome screen
- Automated ISO build workflow

This is a first bootable foundation, not a finished commercial OS. The app store is currently
Synaptic, which installs Debian packages; a custom graphical KOS Store can be added later.

## Build the ISO from your iPad

1. Create a free GitHub repository named `KOS`.
2. Upload the contents of this project ZIP to the repository (extract the ZIP first).
3. Open the repository's **Actions** tab and enable Actions if GitHub asks.
4. Select **Build KOS ISO** and press **Run workflow**.
5. Wait for the workflow to finish. Open the completed run and download the `KOS-live-ISO` artifact.
6. The artifact contains the generated `.iso` file.

The GitHub-hosted runner does the Linux build, so your iPad does not need to run Linux compilation locally.
GitHub Actions usage limits and artifact retention may apply.

## Run KOS in a Windows virtual machine

1. Download and install VirtualBox on the Windows PC.
2. Create a new virtual machine named `KOS`.
3. Choose **Linux / Debian (64-bit)**, assign at least 4 GB RAM (2 GB may work), and create a
   virtual disk of at least 25 GB.
4. In the VM's storage settings, attach the KOS `.iso` as the optical disk.
5. Start the VM and choose the live-system boot option.
6. For best performance, enable 3D acceleration only if it works reliably with your graphics driver.

The live ISO is not automatically an installed system. To keep changes after reboot, install KOS
to the virtual disk using the included Debian installer if available, or use the live session for testing.
Back up anything important before installing an OS.

## Desktop apps

- **KOS Browser** — Firefox ESR
- **KOS Code** — Geany
- **KOS Files** — Thunar
- **KOS Software** — Synaptic Package Manager
- **KOS Settings** — XFCE Settings Manager

## Important notes

- This project builds a real Debian-based Linux live image, not a web mockup.
- It is a starting point. Branding and shortcuts are customized, but most applications are established
  Linux applications rather than newly written replacements.
- The workflow must complete successfully before an ISO artifact exists. If it fails, open the failed
  Actions run and check its logs.
- For public distribution, review Debian, application, font, and theme licenses and include any notices
  required by their respective licenses.
