# Heizöl to MQTT

Home Assistant app repository for publishing heating-oil price data through MQTT Discovery.

The app polls public price calculator endpoints from Esyoil and Heizöl24 and creates Home Assistant MQTT sensors for configured postal codes and amounts. It is intended for Germany and Austria only.

Adapted from and inspired by the original ioBroker adapter:
[TA2k/ioBroker.heizoel](https://github.com/TA2k/ioBroker.heizoel)

## Installation

[![Open your Home Assistant instance and add the Heizöl to MQTT app repository](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Frockbaer2007%2Fheizoel-to-mqtt)

1. Open Home Assistant.
2. Go to **Settings > Apps > App-Store**.
3. Open the three-dot menu and choose **Repositories**.
4. Add this repository URL:

   ```text
   https://github.com/rockbaer2007/heizoel-to-mqtt
   ```

5. Install **Heizöl to MQTT**.
6. Configure `plz`, `amount` and sources.
7. Start the app.

## Features

- Esyoil price lookup.
- Heizöl24 Germany price lookup.
- Heizöl24 Austria price lookup.
- Valid for German and Austrian postal codes only.
- Multiple liter amounts, for example `1000,2000,3000`.
- Configuration keys aligned with the original ioBroker masks, for example `plz`, `amount`, `esyActive`, `deliveryTimes`, `payment_type`, `prod`, `unloading_points`, `hose`, `short_vehicle`, `hoDe` and `hoAt`.
- German and English Home Assistant configuration translations.
- MQTT Discovery sensors for price per 100 liters, total price, dealer, delivery days and offer count.
- MQTT Discovery sensors for the first 6 offers per source and amount: provider name, total price, price per liter and price per 100 liters.
- Attributes with the best offer and selected request parameters.

Heizöl24 uses postal code and amount like the original adapter note says. The detailed delivery, payment, product, hose and vehicle options are used for Esyoil.

Only use German or Austrian postal codes that match the selected providers.

## Privacy

The configured postal code, amount and delivery options are sent to the selected external price providers. Do not enable sources you do not want to query.

## Status

This is an early testable MVP. The external endpoints are not officially documented APIs and can change.

## License

MIT
