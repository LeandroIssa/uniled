[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge)](https://github.com/hacs/integration)
[![BuyMeCoffee][buymecoffeebadge]][buymecoffee]
[![GitHub Release][releases-shield]][releases]
[![GitHub Activity][commits-shield]][commits]
[![License][license-shield]][license]

# ![HA][ha-logo] UniLED - The Universal Light Controller


UniLED Currently supports the following range of cheap BLE addressable LED controllers:

- [SP107E][SP107E] 
- [SP110E][SP110E]
- [SP601E][SP601E] 
- [SP611E][SP61xE]
- [SP617E][SP61xE]

---

## Installation

### HACS Automated Installation

You can install this component through [HACS](https://hacs.xyz/) to easily receive updates.

After installing HACS, visit the HACS _Integrations_ pane and add `https://github.com/monty68/uniled` as an `Integration` by following [these instructions](https://hacs.xyz/docs/faq/custom_repositories/). You'll then be able to install it through the _Integrations_ pane.

### Manual Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `uniled`.
4. Download _all_ the files from the `custom_components/uniled/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant
7. In the HA UI go to "Settings" -> "Devices & Services" -> "Integrations" click "+" and search for "Universal Light Controller"

### Adding Devices and Model Identification Issues

UniLED does it's best to identify the exact model through a number of different mechanisms, however
if you are having difficulty adding a device, especially where it fails to identify the model. Then,
first try using the applicable Android/IOS app and ensure the device name is set to match the devices
model then attempt adding the device into Home Assistant. If it still fails, enable debugging (see below) in Home Assistant, re-attempt adding the device, then open an issue attaching the debug log 
output to assist with further invetigation.

## Debugging

To debug the integration, add the following to your `configuration.yaml`

```yaml
logger:
  default: warning
  logs:
    custom_components.uniled: debug
```


## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)

***

[uniled]: https://github.com/monty68/uniled
[ha-logo]: docs/img/ha-logo-32x32.png
[SP107E]: docs/sp107e.md
[SP110E]: docs/sp110e.md
[SP601E]: docs/sp601e.md
[SP61xE]: docs/sp61Xe.md
[Info]: info.md
[user_profile]: https://github.com/monty68
[maintenance-shield]: https://img.shields.io/badge/maintainer-Monty-blue.svg?style=for-the-badge
[buymecoffee]: https://www.buymeacoffee.com/monty68
[buymecoffeebadge]: https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg?style=for-the-badge
[hacsbadge]: https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/v/release/monty68/uniled?display_name=release&include_prereleases&style=for-the-badge
[releases]: https://github.com/monty68/uniled/releases
[commits-shield]: https://img.shields.io/github/last-commit/monty68/uniled?style=for-the-badge
[commits]: https://github.com/monty68/uniled/commits/main
[license]: https://github.com/monty68/uniled/blob/main/LICENSE
[license-shield]: https://img.shields.io/github/license/monty68/uniled.svg?style=for-the-badge
