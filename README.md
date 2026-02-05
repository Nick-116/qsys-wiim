# qsys-wiim

Q-Sys Plugin for WiiM Audio Players using the HTTP API with local polling.

<img width="880" height="621" alt="qsys-wiim-example" src="https://github.com/user-attachments/assets/de2272e2-7322-43d1-8bb6-a4ef54259c4c" />

## Features

- HTTPS control of WiiM players via HTTP API
- Auto device name fetch on startup and IP change
- Now Playing: album art, title, artist, album
- Transport controls: prev, play/pause, play, pause, next, stop
- Player mode detection and labeling
- Playlist browser with art thumbnails and one-click start
- Manual playlist refresh button
- Status polling interval control
- Playlist/song icons you can drag right into a UCI

## Quick Start

1. Import `WiiM_Player.qplug` into Q-SYS Designer.
2. Drag **WiiM Player** into your design.
3. Open the control panel and set the device IP address.
4. Click **Update Playlists** (or let it auto-refresh on startup/IP change).

## Notes

- Album art is fetched and encoded on the Core, so the Core needs network access to the artwork URL.
- Playlist art loads sequentially to avoid CPU spikes.
- The "Stop" button actually just switches the input to optical in. This is becuase I couldnt find a way for the API to set the input to "none". If the API updates at any point I will change this.

## Requirements

- Q-SYS Designer 10.1+
- WiiM device on the same network

