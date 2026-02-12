# Balkonkraftwerk Vorgabe Einspeiseleistung
<img width="1082" height="563" alt="{27F1B325-1D34-47FB-8143-8D39A2E5C15A}" src="https://github.com/user-attachments/assets/9a92d394-d1ad-4176-8703-f767f5dcbc34" />

## Werte
Es werden gemessene Werte addiert.
Weil das Balkonkraftwerk nur 800W ausgeben kann und damit die Auswirkungen nicht so groß sind, wird die Summe danach durch 4 dividiert.
Die maximale Summe der gemessenen Werte (bei Gleichzeitigkeit 1) ist 2000 + 2000 + 2000 + 250 + 3600 = 9850 W.
Es macht also keinen Sinn, mit so einem Wert weiter zu arbeiten
## Glättung
Danach eine Glättung mit Tiefpass um Ausreisser und große Sprünge abzufedern (z.B. die Dampfbügelstation in WZ  EZ)
## Limiter
Limiter zwischen 100 und 800W damit ist sichergestellt, dass der Minimalverbrauch im Haus geliefert wird, aber niemals mehr als 800W, weil ansonsten die Anker API die Vorgabe ablehnt.
## Zeitbegrenzung
Da nur eine Unterstützung der Anlage auf dem Dach realisiert werden soll, wird nur von Sonnenuntergang bis Sonnenaufgang eingespeist.
## Vorgabe 0, wenn keine Unterstützung
In der Zeit von Sonnenaufgang bis Sonnenuntergang soll nicht eingespeist werden, deshalb Vorgabe fix 0.
Damit sichergestellt ist, dass die Vorgabe auch in Ausnahmefällen gemacht wird, wird über einen Injector alle 10 Minuten die Vorgabe 0 aktiviert
