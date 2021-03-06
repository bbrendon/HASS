# UPB platform for Home Assistant


## Getting Started

1. Install upb-cli -- https://github.com/DaAwesomeP/upb-cli
1. Make sure upb-cli is in the system path
1. Update your configuration.yaml with the platform setting such as the example below.
1. Make sure the user running HASS has access to the serial port.

## Limitations

1. No access to links
1. Not two-way. i.e. You can control the lights from HASS but changes in the physical world don't appear in HASS.
1. Not fully python native - requires upb-cli node application.

## Example configuration.yaml

```
light:
  - platform: upb
    serial_port: /dev/ttyS1
    network_id: 82
    devices:
      - id: 13
        name: Bathroom Fan
      - id: 12
        name: Bathroom Vanity
```        
