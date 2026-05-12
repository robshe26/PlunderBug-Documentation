# Plunder Bug - Tool Overview 

- This document holds a description of the tool `Plunder Bug`, and its uses

## Overview 

The Plunder Bug is an advanced LAN Tap that lets you bug Ethernet connections, functioning as a man in the middle for wired networks. This allows penetration testers and system administrators to intercept network traffic. This tool operates at the hardware layer and can silently duplicate network packets without interrupting the target's workflow. 

## How it Works: The Hardware

The Plunder Bug physically bridges a wired network connection while siphoning a copy of the data via USB-C.
- Physical Setup: You unplug an existing Ethernet cable from a target device, plug it into one of the Plunder Bug's RJ45 ports, and run a second Ethernet cable from the other RJ45 port back to the target. The USB-C port then connects to your computer to provide power.
- Passthrough: To the network, it looks like a continuous wired connection. It auto-negotiates 10/100 Base-t Fast Ethernet to maintain a stable link.
- The Data Collection: Data flowing between the two Ethernet ports is mirrored to the USB-C connection, allowing the user to read and capture raw packets using standard network analysis software like Wireshark.

## Capabilities 

The Plunder Bug offers both stealth and active engagement features. 

A. Passive Monitoring Mode 
  - In this mode, the device acts as a traditional "listen only" tap. This means that it silently duplicates the network traffic passing through it without altering the data or injecting any of its own MAC addresses, making it incredibly difficult for network defenders to detect.

B. Active Engagement Mode 
  - when configured for active mode, the Plunder bug transforms into an mini-switch. This "injects' your connected machine directly into the target network segment, allowing you to perform active network scans, interact with local services, or launch network based attacks.

C. Cross-Platform Operations 
  - It features cross-platform connection scripts for Windows, Mac, Linux. Most notably, integrates with a dedicated Android App, allowing an operator to plug the tap directly into their smartphone and perform full packet captures from their pocket.

## Primary Use Cases

- Penetration Testing:
  -  Physical red-teaming where an attacker gains brief access to a server room, printer, or office desk, tapping an Ethernet line to capture cleartext credentials, VoIP traffic, or sensitive file transfers.
- System Administration:
   - Diagnosing deep-level network issues, analyzing application traffic, or auditing hardware installing a software-based packet sniffer is impossible
- Emergency Connectivity:
  - The tool can also function as a standard USB-C to Ethernet adapter for a laptop when you simpily need a reliable hardwired connection. 
