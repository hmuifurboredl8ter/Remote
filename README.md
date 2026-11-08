# Remote Button Tester

A small Android app that displays the hardware input events delivered to it, useful for identifying buttons on an unfamiliar Bluetooth remote.

## Run it

1. Open this repository in Android Studio and let Gradle sync.
2. Build and install the `app` on your Moto G 5G (2025).
3. Pair the remote in the phone's **Settings → Bluetooth**. Many remotes present as a keyboard or gamepad and need no special app permission.
4. Open **Remote Button Tester** and press each remote button. The app logs Android key-down/key-up events, key and scan codes, device name, input source, repeats, and gamepad/joystick motion events.

`KEYCODE_*` values are Android's interpretation of the button; `scanCode` is the lower-level device-specific code. Write down which physical button produces each event. This app identifies events—it cannot determine a button's intended function or change how the remote behaves in other apps.

## Notes

- Keep the tester in the foreground while pressing buttons.
- Android may reserve or intercept some buttons (for example, power or volume), so those may not appear in the app.
- If a button produces no event, the remote may use a proprietary Bluetooth profile, require its companion app, or not send input while this app is open.
- No Bluetooth permission is requested: pairing and connection are managed by Android Settings.
