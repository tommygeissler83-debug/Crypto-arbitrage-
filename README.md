# Krypto Arbitrage Android

Android-WebView-App mit EUR-Spot-Ticker-Scanner für Kraken, Coinbase Exchange, Bitstamp und Bitvavo.

## Was derzeit integriert ist
- Live Bid/Ask/Last für BTC, ETH und SOL in EUR, soweit das jeweilige EUR-Markt-Paar verfügbar ist
- Öffentliche Ticker-APIs; für diese Kursabfragen ist kein Börsen-API-Schlüssel erforderlich
- Börsenvergleich und grobe Netto-Arbitrage-Schätzung mit einstellbarem Einsatz und geschätzter Gebühr
- manuelle Aktualisierung

## Abgrenzung zur vollständigen Deutschland-Liste
MiCA-/CASP-Zulassungen umfassen auch Verwahrer, Broker, Banken und andere Dienstleister, die nicht selbst eine öffentlich handelbare EUR-Spotbörse mit Orderbuch und API anbieten. Deshalb sind nicht alle im Register aufgeführten CASPs als Arbitrage-Handelsplätze vergleichbar. Der offizielle ESMA-MiCA-Registerstand ist dynamisch und sollte vor jeder Erweiterung geprüft werden.

Diese Version verbindet vier Anbieter mit öffentlich zugänglichen EUR-Ticker-Endpunkten: Kraken, Coinbase Exchange, Bitstamp und Bitvavo. Weitere in Deutschland zugelassene bzw. passportierte Anbieter können ergänzt werden, sobald ein nutzbares EUR-Spot-Paar und ein stabiler API-Endpunkt verifiziert sind. Die App behauptet nicht, bereits alle in Deutschland zugelassenen Anbieter abzudecken.

## Wichtige Einschränkungen
- Es werden Ticker-Bid/Ask-Werte verwendet, keine vollständige Prüfung der Orderbuch-Tiefe. Angezeigte Chancen sind indikativ und keine garantierte Arbitrage.
- Transferkosten, Slippage, Liquidität, Handelslimits, Ausführungszeit und steuerliche Auswirkungen sind nicht vollständig berücksichtigt.
- Echter automatischer Echtgeld-Handel ist NICHT implementiert. Dafür müssen Anbieter, sichere API-Anbindung, Orderbuch-/Balance-Prüfung, Risikogrenzen, Not-Aus und Nutzerfreigabe ergänzt werden. API-Schlüssel niemals mit Auszahlungsrechten verwenden.
- Die App benötigt Internetzugriff.

## APK über GitHub Actions bauen
1. Projektinhalt in ein GitHub-Repository laden.
2. Actions öffnen und `Build Android APK` ausführen.
3. Das Artifact `krypto-arbitrage-debug-apk` herunterladen und entpacken.
4. `app-debug.apk` auf Android installieren.
