# J7-C_UC96_BLE_Logger
Bluetooth Low Energy Data logging for J7-C/UC96 USB Digital Power Testers

## Installation

Requires [gattlib](https://github.com/labapart/gattlib).

## Usage

Just start the script to show the measurements of the first found J7-C on screen.

```
usage: j7c-gat.py [-h] [-v | -q] [-d DEVICE] [-w] [-r] [-H HCI]
                  [-T SCANTIME] [-m {Text,CSV,JSON,RAW,InfluxDB}]
                  [-O OUTPUT] [-a] [--csv-delimiter CSV_DELIMITER]
                  [--csv-no-header] [--json-pretty] [--raw-header]
                  [--raw-pretty]

Receive measurement values from a J7-C USB power monitor using BLE

options:
  -h, --help            show this help message and exit
  -v, --verbose         increase output verbosity. Repeat for higher
                        verbosity (max. 5)
  -q, --quiet           suppress non-data output messages

Device control:
  -d DEVICE, --device DEVICE
                        target device MAC address. If no address is given
                        the first compatible device found will be used
  -w, --wait            wait for device to appear
  -r, --reconnect       wait and reconnect when loosing connection
  -H HCI, --hci HCI     HCI used for communication. Defaults to hci0
  -T SCANTIME, --scantime SCANTIME
                        Time in seconds to scan for devices. Defaults to 2
                        Seconds

Output options:
  -m {Text,CSV,JSON,RAW,InfluxDB}, --mode {Text,CSV,JSON,RAW,InfluxDB}
                        output type
  -O OUTPUT, --output OUTPUT
                        output file, device or network address
                        ([tcp|udp]://[host_or_ip]:port)
  -a, --append          append output if it is a file

Output options for CSV:
  --csv-delimiter CSV_DELIMITER
                        CSV delimiter. Default: ';'
  --csv-no-header       Omit CSV header

Output options for JSON:
  --json-pretty         Use pretty-print for JSON Output

Output options for RAW:
  --raw-header          Add address header
  --raw-pretty          Use pretty-print for RAW Output
```
