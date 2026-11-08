# Remote Button Tester

A small Android app that displays the hardware input events delivered to it, useful for identifying buttons on an unfamiliar Bluetooth remote.

## Run it

1. Open this repository in Android Studio and let Gradle sync.
2. Build and install the app on your Moto G 5G (2025).
3. Pair the remote in the phone's Settings → Bluetooth.
4. Open Remote Button Tester and press each remote button.

The app logs Android key-down/key-up events, key codes, scan codes, device names, and motion events. This identifies the button event; it does not discover a remote's intended function.

## Notes

- Keep the tester in the foreground while pressing buttons.
- Some buttons (power, volume, etc.) may be intercepted by Android and not appear.
- If no event appears, the remote may use a proprietary Bluetooth profile or require its companion app.
