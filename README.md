# Vega Power Monitor

A browser app for plotting live optical power from an **Ophir Vega** power meter over its RS232 port (through a USB‑serial adapter), using the Web Serial API. It's a single HTML file with no dependencies.

**Live page:** https://nat-as.github.io/vega-power-monitor/
**Try it without hardware:** https://nat-as.github.io/vega-power-monitor/?demo

## Requirements
- Chrome or Edge on desktop. Firefox and Safari don't support Web Serial.
- An RS232 adapter connected to the Vega's DB9 port. The meter's RS232 settings are 8‑N‑1 with no flow control, at the baud rate set in the meter's setup menu.

## Features
- Choose the COM port, baud rate, framing, line terminator, timeout and DTR/RTS lines. A button can find the baud rate automatically.
- Reads instrument and sensor-head information on connect (`$II`, `$VE`, `$HI`, `$HT`, `$SU`) and shows it at the top of the page.
- Sensor settings: wavelength, range (including autorange), averaging, filter, diffuser, energy threshold, pulse length, measurement mode, zeroing and meter reset.
- Live readout, statistics, and a time plot with W, dBm and relative-to-reference display, log scale, alarm limits, and correction for an external attenuator or calibration factor.
- Exports CSV, JSON and PNG. Includes a raw command console and a built-in simulator.

## Running locally
Open `index.html` in Chrome or Edge. If the browser blocks serial access from a local file, run `python3 -m http.server` and open http://localhost:8000.
