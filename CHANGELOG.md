# Changelog

## 0.1.6

- Changed hose length to a numeric metre field.
- Renamed the visible short vehicle option to tank truck and changed its choices to trailer/no-trailer labels.

## 0.1.5

- Renamed the visible EasyOil switch label.
- Added the postal-code-and-amount note to the visible Heizöl24 provider switch labels.

## 0.1.4

- Changed visible delivery time options to the German ioBroker mask labels.
- Added runtime mapping from German delivery time labels to EsyOil request codes.

## 0.1.3

- Added German and English Home Assistant app configuration translations.
- Documented that provider lookups are intended for Germany and Austria only.

## 0.1.2

- Removed legacy `_enabled` provider option names from the runtime configuration path and public documentation.

## 0.1.1

- Changed visible configuration keys to match the original ioBroker adapter masks (`plz`, `amount`, `esyActive`, `deliveryTimes`, `prod`, `hoDe`, `hoAt`).
- Kept compatibility with the first `0.1.0` configuration key names.

## 0.1.0

- Initial testable Home Assistant app.
- Added MQTT Discovery sensors for Esyoil and Heizöl24 price results.
- Added attribution to the original ioBroker adapter.
