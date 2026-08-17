# Configuration

Example:

```yaml
plz: "10115"
amount: "1000,2000,3000"
interval: 60
esyActive: true
deliveryTimes: normal
payment_type: ec
prod: normal
unloading_points: 1
hose: fortyMetre
short_vehicle: withTrailer
hoDe: true
hoAt: false
log_response_details: false
```

`interval` is in minutes and has a minimum of `30`.

`amount` accepts a comma-separated list of liter amounts.

The visible configuration keys follow the original ioBroker adapter masks. Older `0.1.0` names for postal code, amount, product and delivery time are still accepted as fallback, but provider toggles use `esyActive`, `hoDe` and `hoAt`.

Heizöl24 uses postal code and amount like the original adapter note says. The detailed delivery, payment, product, hose and vehicle options are used for Esyoil.

`log_response_details` writes raw provider responses to the app log. Enable it only for troubleshooting because responses may contain regional offer details.

## Attribution

This app is adapted from and inspired by the original ioBroker adapter:
[TA2k/ioBroker.heizoel](https://github.com/TA2k/ioBroker.heizoel)
