# QRP-Labs QMX+ Professional Communications Interface
USB Interface for the QMX+

## Screenshots

![Main Interface](screenshot1.png)
![Settings Panel](screenshot2.png)

---

## Live Demo

Coming soon via GitHub Pages!

---

## Local Installation

1. Clone or download this repository.
2. Open `index.html` in your browser.


A modern, web-based control interface for the QRP-Labs QMX+ transceiver, providing comprehensive radio control, logging, and monitoring capabilities through your browser.

![QMX Interface](https://img.shields.io/badge/Version-1.0-blue) ![License](https://img.shields.io/badge/License-MIT-green) ![Platform](https://img.shields.io/badge/Platform-Web-orange)

## 🚀 Features

### 📡 Radio Control
- **Serial Connection**: Direct USB/Serial communication with QMX+ transceiver
- **Frequency Control**: Intuitive knob-style tuning interface with multiple step sizes
- **Mode Selection**: USB, LSB, CW, and Digital modes
- **Band Selection**: Quick access to all amateur bands (160m - 6m)
- **VFO Management**: A/B VFO control with swap and copy functions
- **TX/RX Control**: Push-to-talk functionality

### 🎛️ Advanced Controls
- **Volume Control**: Real-time AF gain adjustment with visual feedback
- **Keyer Speed**: CW speed control (5-50 WPM)
- **Memory Channels**: 10 programmable memory locations with custom labels

### 📊 Monitoring & Meters
- **S-Meter**: Real-time signal strength indication
- **SWR Meter**: Standing wave ratio monitoring
- **LCD Display**: Mimics the radio's built-in display
- **CAT Monitor**: Live command/response logging

### 📝 Logging System
- **QSO Logger**: Built-in contact logging with real-time frequency/mode capture
- **ADIF Support**: Import/export industry-standard ADIF files
- **Search & Filter**: Quick callsign search functionality
- **Time Synchronization**: Automatic UTC time sync for accurate logging

### 🎨 User Interface
- **Draggable Panels**: Customizable layout - rearrange panels to your preference
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Professional Styling**: Modern glass-morphism design with smooth animations
- **Keyboard Shortcuts**: Arrow keys for frequency tuning, Enter for quick logging

## 🛠️ Installation

### Requirements
- Modern web browser with WebSerial API support (Chrome 89+, Edge 89+)
- QRP-Labs QMX+ transceiver
- USB cable for radio connection
- [Sortable.js](https://sortablejs.github.io/Sortable/) library (included or CDN)

### Setup
1. **Download the files**:
   ```bash
   git clone https://github.com/sparks72/qmx-interface.git
   cd qmx-interface
   ```

2. **Download Sortable.js** (optional - for offline use):
   - Download `Sortable.min.js` from [SortableJS releases](https://github.com/SortableJS/Sortable/releases)
   - Place it in the same directory as `index.html`
   - Uncomment line 8 and comment line 10 in the HTML file

3. **Open in browser**:
   - Simply open `index.html` in a compatible web browser
   - Or serve through a local web server for enhanced security

## 🖥️ Usage

### Initial Setup
1. **Connect your QMX+** to your computer via USB
2. **Open the interface** in your web browser
3. **Select baud rate** (typically 115200)
4. **Click "Connect Serial"** and select your QMX+ port
5. **Wait for connection** - you should see "CONNECTED" status

### Basic Operation

#### Frequency Tuning
- **Mouse/Touch**: Click and drag the main tuning knob
- **Scroll Wheel**: Use mouse wheel over the knob for fine tuning
- **Keyboard**: Use arrow keys when knob is focused
- **Step Size**: Adjust from 1 Hz to 10 kHz increments

#### Band Changes
- Click any **band button** (160m-6m) for quick band changes
- Interface remembers your last frequency on each band
- Automatic frequency restoration when switching bands

#### Memory Channels
- **Store**: Select "Store" mode, then click any M1-M10 button
- **Recall**: Select "Recall" mode, then click a stored memory
- **Edit**: Right-click any memory or use "Edit" mode for advanced editing
- **Quick Store**: Double-click any memory in Recall mode

#### QSO Logging
1. Enter callsign (automatically converts to uppercase)
2. Adjust RST reports as needed
3. Add name, QTH, and comments (optional)
4. Click "LOG QSO" or press Enter in callsign field
5. Export logs in ADIF format for other logging programs

### Advanced Features

#### Panel Customization
- **Drag panels** by their headers between left, center, and right columns
- **Custom layouts** are automatically saved
- **Reset layout** by clearing browser storage if needed

#### CAT Monitoring
- View real-time CAT commands in the monitor panel
- Useful for troubleshooting communication issues
- Color-coded: Green (TX), Blue (RX), Red (Errors)

#### Time Synchronization
- Automatic UTC time sync from internet time servers
- Ensures accurate QSO timestamps
- Falls back to local time if sync fails

## 🔧 Configuration

### Baud Rate Settings
The interface supports multiple baud rates:
- 9600 (legacy)
- 19200
- 38400
- 57600
- **115200** (recommended)

### Memory Export/Import
- **Export**: Save all memory channels as JSON file
- **Import**: Load previously saved memory configurations
- **Backup**: Regular exports recommended for configuration backup

## 🐛 Troubleshooting

### Connection Issues
- **Port not found**: Ensure QMX+ drivers are installed
- **Permission denied**: Try closing other applications using the serial port
- **Connection drops**: Check USB cable and port reliability

### Performance Issues
- **Slow response**: Reduce polling frequency or check serial connection
- **Browser compatibility**: Use Chrome or Edge for best WebSerial support
- **Memory usage**: Clear CAT log periodically (automatically limited to 200 entries)

### Common Solutions
- **Refresh page** to reset connection state
- **Check console** (F12) for detailed error messages
- **Verify QMX+ firmware** compatibility with CAT commands

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit your changes**: `git commit -m 'Add amazing feature'`
4. **Push to branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**

### Development Guidelines
- Maintain backward compatibility with QMX+ firmware
- Follow existing code style and structure
- Test thoroughly with actual hardware
- Update documentation for new features

## 📋 Supported CAT Commands

The interface implements the following Kenwood-compatible CAT commands:

| Command | Function | Description |
|---------|----------|-------------|
| `FA` | Set/Get VFO A Frequency | 11-digit frequency in Hz |
| `IF` | Get Transceiver Status | Complete radio status |
| `MD` | Set/Get Mode | 1=LSB, 2=USB, 3=CW, 6=DIGI |
| `AG` | Set/Get AF Gain | Audio volume control |
| `PC` | Set/Get Power | RF power in tenths of watts |
| `KS` | Set/Get Keyer Speed | CW speed in WPM |
| `LC` | Get LCD Display | 32-character LCD content |
| `SM` | Get S-Meter | Signal strength reading |
| `SW` | Get SWR | Standing wave ratio |
| `TX/RX` | PTT Control | Transmit/Receive switching |

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **QRP-Labs** for the excellent QMX+ transceiver
- **SortableJS** team for the drag-and-drop functionality
- **Amateur Radio Community** for continued support and feedback
- **Web Serial API** developers for enabling browser-hardware communication

## 📞 Support

- **Issues**: Report bugs via [GitHub Issues](https://github.com/yourusername/qmx-interface/issues)
- **Discussions**: Join conversations in [GitHub Discussions](https://github.com/yourusername/qmx-interface/discussions)
- **Email**: dj0cu@darc.de (replace with your contact)

## 🔄 Version History

### v1.0.0 (Current)
- Initial release
- Full QMX+ CAT control implementation
- Memory management system
- QSO logging with ADIF support
- Time synchronization
- Responsive UI with draggable panels

---

**73 and happy QRP DXing!** 📻

*If you find this interface useful, please give it a ⭐ on GitHub and share it with your fellow QRP enthusiasts!*
