# Configuration

Example:

```yaml
plz: "10115"
amount: "1000,2000,3000"
interval: 60
esyActive: true
deliveryTimes: ohne
payment_type: ec
prod: Normal Schwefelarm
unloading_points: 1
hose: 40
short_vehicle: mit Anhänger möglich
hoDe: true
hoAt: false
log_response_details: false
```

`interval` is in minutes and has a minimum of `30`.

`amount` accepts a comma-separated list of liter amounts.

The app is intended for Germany and Austria only. Use German or Austrian postal codes that match the selected providers.

`deliveryTimes` uses the same visible values as the ioBroker mask: `ohne`, `7:00 - 12:00 Uhr`, `12:00 - 17:00 Uhr`, `2 Wochentage (Express)`, `3 - 5 Wochentage (Mo.-Fr.)` and `6 - 10 Wochentage (Mo.-Fr.)`.

`prod` uses the visible oil product names from the ioBroker mask: `Normal Schwefelarm`, `Premium Schwefelarm`, `Klimaneutral Premium`, `Klimaneutral Normal`, `Bio 10`, `Bio 15` and `Bio 10 Premium`.

`hose` is entered as a number in metres. It is mapped to the nearest supported EasyOil hose class internally. `short_vehicle` is shown as `Tankwagen` and accepts `mit Anhänger möglich` or `ohne Anhänger`.

In the German Home Assistant UI, `esyActive` is shown as `EasyOil aktivieren`. `hoDe` and `hoAt` are shown as `Heizöl24 Deutschland aktivieren (Nur PLZ und Menge wird übernommen)` and `Heizöl24 Österreich aktivieren (Nur PLZ und Menge wird übernommen)`.

The visible configuration keys follow the original ioBroker adapter masks. Older `0.1.0` names for postal code, amount, product and delivery time are still accepted as fallback, but provider toggles use `esyActive`, `hoDe` and `hoAt`.

Heizöl24 uses postal code and amount like the original adapter note says. The detailed delivery, payment, product, hose and vehicle options are used for Esyoil.

`log_response_details` writes raw provider responses to the app log. Enable it only for troubleshooting because responses may contain regional offer details.

## Attribution

This app is adapted from and inspired by the original ioBroker adapter:
[TA2k/ioBroker.heizoel](https://github.com/TA2k/ioBroker.heizoel)
