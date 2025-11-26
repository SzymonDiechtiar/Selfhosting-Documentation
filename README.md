# Selfhosting-Guide

<h1>UNDER CONSTRUCTION ! ! !</h1>

<h2>Step 0: Introduction</h2>

This repository will contain a guide documenting my setup of selfhosted services on a 10 years old PC that i got from a friend. My configuration may not be perfect so feel free to suggest changes.

List of things i will explain how to set up:
- Proxmox VE (to virtualise all below)
- pfSense (router)
- Ubuntu Server (running Docker with: Traefik, Jellyfin, Servarr, Navidrome, Nextcloud...)
- TrueNAS

<h2>Step 1: Downloading Proxmox and Preparing a Bootable USB Drive</h2>

<h3>1.1 Download Proxmox VE</h3>

  1. Open your web browser and visit <a url="https://www.proxmox.com/en/downloads/proxmox-virtual-environment/iso/proxmox-ve-9-1-iso-installer">Proxmox Download site</a>

<h3>1.2 Create a Bootable USB Drive</h3>

  1. Insert a USB flash drive (at least 4GB in size) into your computer. Use one of the following methods to write the Proxmox image to the USB drive:

  Windows:
  
  1. Download and install <a href="https://rufus.ie/en/#download">Rufus</a>.
  2. Open Rufus and select your USB drive.
  3. Click the “SELECT” button and choose the unzipped .img file you downloaded.
  4. Click “Start” and let Rufus create the bootable USB.

  Linux (Debian and Ubuntu):

  1. Download package .deb <a href="https://github.com/balena-io/etcher/releases/">balenaEtcher</a>.
  2. Change directory into Downloads: 

         cd ~/Downloads
     
  3. Install using apt:

         sudo apt install ./balena-etcher_******_amd6.deb
     
  4. Open program:
     
         balena-etcher
     
  5. Click "Flash from file" -> chose your ISO -> Click "Select target" -> chose your USB flash drive -> Click "Flash!"

<h2>Step 2: Install Proxmox</h2>

<b>Boot from the USB Flash Drive</b>

  1.1 Boot the installer
  
  - Plug the USB flash drive and power on your PC.
  - Press F10 (or the relevant boot menu key) to select the USB drive as the boot device.
    
  1.2 Select the USB Drive in Boot Menu

  - In the boot menu, you’ll see a list of available boot devices. Select the USB flash drive that contains the Proxmox installer.
  - Press Enter to boot from the USB drive.


    
        
      
      
  
