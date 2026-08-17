# Heizöl to MQTT

Home Assistant app for publishing heating-oil price data through MQTT Discovery.

Adapted from and inspired by the original ioBroker adapter:
[TA2k/ioBroker.heizoel](https://github.com/TA2k/ioBroker.heizoel)

## Entities

For every enabled source and configured amount, the app creates:

- `{source} {amount}l Preis pro 100l`
- `{source} {amount}l Gesamtpreis`
- `{source} {amount}l Händler`
- `{source} {amount}l Lieferdauer`
- `{source} {amount}l Angebote`

It also creates:

- `Heizöl Verbindung`
- `Heizöl letzte Aktualisierung`

## Sources

- Esyoil
- Heizöl24 DE
- Heizöl24 AT

## Notes

The external endpoints are public website endpoints, not official stable APIs. They may change without notice.

The configured postal code and request parameters are sent to the enabled providers.
