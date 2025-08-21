# XML Configuration Exporter

A lightweight web-based tool for generating customized XML configuration files based on user input and predefined templates.

## Overview

This tool allows users to:
- Select a configuration template from a dropdown menu.
- Input custom values (e.g., appliance name, WiFi SSID).
- Export a modified XML file tailored to their selections.

## How It Works

1. Templates are mapped in `machine_templates.json`.
2. When a machine is selected, the corresponding XML template is loaded.
3. User inputs are injected into specific `<string>` elements in the XML.
4. The updated XML is downloaded as `SITEMANAGER.CFG`.
5. Copy `SITEMANAGER.CFG` to USB and insert into unconfigured SiteManager.

## Setup

1. Ensure `index.html` is served via a local or remote web server.
2. Include:
   - `machine_templates.json` (maps machine names to XML template file paths)
   - XML template files referenced in the JSON

## Usage

1. Open the tool in a browser.
2. Select a machine.
3. Enter required values.
4. Click **Export** to download the customized XML file.

## Notes

- All fields must be filled before exporting.
- XML templates must contain `<string label="...">` elements for replacement.

