# Natural Scroll Switcher

A lightweight macOS menu bar app that automatically switches between natural and traditional scrolling based on your input device.

## Features

- 🖱️ **Automatic Detection**: Detects whether you're using a trackpad or mouse
- ⚡ **Real-time Switching**: Instantly adjusts scroll direction without system preference changes
- 🎯 **Smart**: Trackpad uses natural scrolling, mouse uses traditional scrolling
- 🪶 **Lightweight**: Minimal system resource usage
- 🚀 **Launch at Login**: Optional auto-start on system boot

## How It Works

The app monitors scroll events to detect device type:
- **Trackpad**: Continuous/momentum scrolling → Natural scrolling
- **Mouse**: Discrete scrolling → Traditional scrolling (inverted in real-time)

No system preference changes needed - scroll direction is modified on-the-fly through event interception.

## Requirements

- macOS 11.0 (Big Sur) or later
- Accessibility permissions (required for scroll event monitoring)

## Installation

### From Release (Recommended)

1. Download `NaturalScrollSwitcher-v1.0.0.dmg` from [Releases](../../releases/latest)
2. Open the DMG file
3. Drag **Natural Scroll Switcher.app** to your **Applications** folder
4. Eject the DMG
5. Open Applications folder and right-click **Natural Scroll Switcher** → **Open** (first time only)
6. Click **Open** in the security dialog
7. Grant **Accessibility** permissions when prompted

### Build from Source

1. Clone this repository
2. Open `NaturalScrollSwitcher.xcodeproj` in Xcode
3. Build and run (⌘R)

### Note for First-Time Users

Since this app is not notarized, macOS will show a security warning on first launch. This is normal for unsigned apps. Simply:
- Right-click → **Open** (don't double-click)
- Click **"Open"** in the dialog

Once opened the first time, you can launch normally afterward.

## Usage

1. **Launch the app** - Look for the mouse icon (🖱️) in your menu bar
2. **Grant permissions** - Allow Accessibility access when prompted
3. **Just scroll!** - The app automatically detects your device and adjusts scrolling

### Menu Options

- **Status Display**: Shows current active device (Trackpad/Mouse) and scroll type
- **Open Accessibility Settings**: Quick access to system preferences
- **Launch at Login**: Toggle automatic startup
- **Quit**: Exit the application

## Privacy

This app:
- ✅ Runs entirely locally on your Mac
- ✅ Does not collect any data
- ✅ Does not require internet connection
- ✅ Does not send any information anywhere
- ✅ Only monitors scroll events for device detection

## How It's Different

Unlike other solutions that toggle system preferences, Natural Scroll Switcher:
- Works instantly without system daemon restarts
- Doesn't require administrator privileges
- Has zero latency when switching devices
- Never modifies your system settings
- Uses minimal CPU (event-based, not polling)

## Troubleshooting

### App doesn't detect device switching
- Ensure Accessibility permissions are granted
- Go to **System Settings** → **Privacy & Security** → **Accessibility**
- Make sure **Natural Scroll Switcher** is enabled

### Scrolling doesn't change
- Try scrolling more distinctly (trackpad with momentum, mouse with clicks)
- Check that the app is running (menu bar icon visible)

### App won't open
- Right-click the app and select **Open** (don't double-click)
- Check **System Settings** → **Privacy & Security** for a blocked app message

## Technical Details

- **Language**: Swift
- **Minimum macOS**: 11.0 (Big Sur)
- **Architecture**: Event tap-based scroll interception
- **Permissions**: Accessibility (for monitoring scroll events)

## License

MIT License - See [LICENSE](LICENSE) for details

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Support

If you encounter any issues, please open an issue on GitHub.

### Acknowledgments

Built with native macOS frameworks:
• CoreGraphics for event monitoring
• IOKit for device detection
• Cocoa for menu bar interface

⸻

Made with ❤️ for macOS users who switch between trackpad and mouse