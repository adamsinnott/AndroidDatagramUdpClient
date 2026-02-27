# Android Datagram UDP Client

## Overview
This repository is an Android proof-of-concept used to understand UDP datagram communication in preparation for Wake-on-LAN implementation.

It was built as a practical learning step between:
1. Java desktop/server UDP testing, and
2. A dedicated Android Wake-on-LAN application.

## Project Purpose
The goal of this project is to validate core networking behavior on Android:
- Open a UDP socket from an Android device.
- Send a datagram packet to a target IP/port.
- Receive a response packet and surface status in the UI.

This work helped de-risk protocol and device-network behavior before building productized Wake-on-LAN functionality.

## Technical Snapshot
- Language: Java
- Platform: Android
- `minSdkVersion`: 24
- `targetSdkVersion`: 29
- Permission: `android.permission.INTERNET`
- UI: simple input form for destination address and port, with connection state and received message output

## Scope and Limitations
- This is a focused prototype, not a production-ready app.
- Current implementation sends an empty UDP payload and waits for one response.
- Testing was most reliable on a physical Android device in the same network environment as the UDP server.

## How to Run
1. Start a UDP server endpoint (see companion repository below).
2. Open this project in Android Studio.
3. Run on an Android device.
4. Enter destination IP and port, then tap **Connect**.

## Companion Repositories
- Java UDP server/client used for packet testing: https://github.com/adamsinnott/JavaUdpServerClient
- Follow-on Android Wake-on-LAN implementation: https://github.com/adamsinnott/WakeOnLAN

## Notes
Initial scaffolding and approach were informed by: http://android-er.blogspot.com/2016/05/android-datagramudp-client-example.html
