
| Used Board | ESP32-S3 |
| ---------- | -------- |

# TinyUSB MIDI Device Example

This example shows how to set up ESP chip to work as a USB MIDI Device.
It outputs a MIDI note sequence via the native USB port.
As a USB stack, a TinyUSB component is used.
### Build and Flash

Build the project and flash it to the board, then run monitor tool to view serial output:

```bash
idf.py -p PORT flash monitor
```
## MIDI output

You can monitor midi output with [Protokol by hexler](https://hexler.net/protokol#get)
## Example Output

After the flashing you should see the output at idf monitor:

```
I (285) example: USB initialization
I (285) tusb_desc:
┌─────────────────────────────────┐
│  USB Device Descriptor Summary  │
├───────────────────┬─────────────┤
│bDeviceClass       │ 0           │
├───────────────────┼─────────────┤
│bDeviceSubClass    │ 0           │
├───────────────────┼─────────────┤
│bDeviceProtocol    │ 0           │
├───────────────────┼─────────────┤
│bMaxPacketSize0    │ 64          │
├───────────────────┼─────────────┤
│idVendor           │ 0x303a      │
├───────────────────┼─────────────┤
│idProduct          │ 0x4008      │
├───────────────────┼─────────────┤
│bcdDevice          │ 0x100       │
├───────────────────┼─────────────┤
│iManufacturer      │ 0x1         │
├───────────────────┼─────────────┤
│iProduct           │ 0x2         │
├───────────────────┼─────────────┤
│iSerialNumber      │ 0x3         │
├───────────────────┼─────────────┤
│bNumConfigurations │ 0x1         │
└───────────────────┴─────────────┘
I (455) TinyUSB: TinyUSB Driver installed
I (465) example: USB initialization DONE
```

Disconnect UART-to-USB port and connect the native USB port to a computer then the device should show up as a USB MIDI Device while outputting notes.
