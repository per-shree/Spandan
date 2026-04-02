# Inauguration Remote Video Trigger

This setup lets you press a button on one device and play the inauguration video on another device online.

It uses a public loginless MQTT broker:
- Broker: `wss://broker.hivemq.com:8884/mqtt`
- Topic format: `inauguration/<room>/control`

## Files
- `player.html` -> open this on the display/laptop/projector device
- `remote.html` -> open this on the control phone/laptop

## How to run
1. Host these files online or open them locally in browser tabs.
2. On the display device, open `player.html`.
3. On the control device, open `remote.html`.
4. Use the same room code in both pages (for example `event2026`).
5. On the player device, click **Arm Player** once before the event.
6. On remote device, click **Play Inauguration Video**.

## Important notes
- Public broker means anyone who guesses the room code could send commands.
- Use a long random room code for your event (example: `spandan-launch-2026-04-02-x9q7`).
- Internet is required on both devices.
- If autoplay with sound is blocked by browser, click Arm Player again on player device.

## Quick online sharing
If you want both devices to access these pages over internet, deploy this folder to any static host:
- GitHub Pages
- Netlify
- Vercel static deploy

Then share links like:
- `https://your-site/player.html?room=spandan-launch-2026-04-02-x9q7`
- `https://your-site/remote.html?room=spandan-launch-2026-04-02-x9q7`
