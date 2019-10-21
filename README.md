# BSB Lan sensor 

This custom component handles the communication to a BSB-Lan Module and create the entities for Home Assistant.
I've extended the script created by liudger (https://github.com/liudger/BSB-LAN-Component-for-Home-Assistant)
to control 2 parallel heating systems (4 heating circuits) Systems via LPB Bus.

info for the BSB-LAN Module
https://github.com/fredlcore/bsb_lan

dicussion about this component
https://community.home-assistant.io/t/bsb-lan-component/113501/1




### Installation

download the bsb_lan folder and
copy this folder to `<config_dir>/custom_components/`.

<B> Sensor component install </B>

Add the following entry for your sensor in your `configuration.yaml`:

```yaml
sensor:
  - platform: bsb_lan
    host: <<HOST_HERE>>
    bus_number: <<BUS_NUMBER (default=0)>>
    payload: 
      - '8700'
      - '8830'
      - '8740'
      - '8006'
      - '8003'
      - '1600'



