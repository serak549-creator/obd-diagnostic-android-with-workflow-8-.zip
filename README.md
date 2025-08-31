# DiagnosticApp - Full Android Starter

This project is a ready-to-open Android Studio project skeleton with:
- OBDEngine (queue, parser, flows)
- MockTransport for offline testing (no hardware required)
- Manufacturer packages in assets/manufacturer_packages/
- Testing captures in assets/testing_captures/
- Simple Compose Dashboard + ViewModel

How to run:
1. Open this folder in Android Studio.
2. Add Kotlin serialization plugin settings if needed.
3. Add the dependencies in app/build.gradle.kts (see file).
4. Build and run. The app uses MockTransport by default so you can press buttons and see sample values.

Notes:
- Replace MockTransport with BluetoothTransport and provide a paired BluetoothDevice to connect to real dongle.
- Make sure to handle runtime permissions on Android 12+.


# Transport Options Added
- WifiTransport: TCP socket to WiFi dongle (default IP 192.168.0.10:35000)
- UsbTransport: OTG USB ELM327 dongle support using usb-serial-for-android library
- BluetoothTransport and MockTransport remain available.
