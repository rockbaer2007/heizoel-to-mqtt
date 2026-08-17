# Configuration

Example:

```yaml
postal_code: "10115"
amounts: "1000,2000,3000"
interval: 60
esyoil_enabled: true
heizoel24_de_enabled: true
heizoel24_at_enabled: false
unloading_points: 1
payment_type: ec
product: normal
delivery_times: normal
hose: fortyMetre
short_vehicle: withTrailer
log_response_details: false
```

`interval` is in minutes and has a minimum of `30`.

`amounts` accepts a comma-separated list of liter amounts.

`log_response_details` writes raw provider responses to the app log. Enable it only for troubleshooting because responses may contain regional offer details.

## Attribution

This app is adapted from and inspired by the original ioBroker adapter:
[TA2k/ioBroker.heizoel](https://github.com/TA2k/ioBroker.heizoel)
