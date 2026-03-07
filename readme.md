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
Da nur eine **Unterstützung** der Anlage auf dem Dach realisiert werden soll, wird nur von Sonnenuntergang bis Sonnenaufgang eingespeist.
## Vorgabe 0, wenn keine Unterstützung
In der Zeit von Sonnenaufgang bis Sonnenuntergang soll nicht eingespeist werden, deshalb Vorgabe fix 0.
Damit sichergestellt ist, dass die Vorgabe auch in Ausnahmefällen gemacht wird, wird über einen Injector alle 10 Minuten die Vorgabe 0 aktiviert  
  
  
# Update Fronius Werte für Dashboard
<img width="1223" height="234" alt="{16F2F52C-EFBF-4113-BFCC-B43C8D853C9D}" src="https://github.com/user-attachments/assets/a15cf03e-bfd8-4563-91a1-23464427ce3a" />  

Die Werte werden von der Fronius API im Standard nur alle 30 Sekunden abgefragt.  
Das ist eine nicht veränderbare Standardeinstellung.  
Nachdem die Werte von den Shelly Messgeräten aber subscribed werden und somit on change nicht vorhersebar kommen, entsteht oft ein etwas seltsames Bild mit inkosistenent Werten.  

  
# Licht Keller Gang
<img width="1124" height="357" alt="{FE550D5B-EE04-425E-BF4C-03B3FFFD152A}" src="https://github.com/user-attachments/assets/0e875b31-29fc-4c11-8df3-6c64721cbed3" />  



# Lüftung Vorratskeller
<img width="1030" height="261" alt="{E37022EE-433D-4B68-A52C-4AC7E5654740}" src="https://github.com/user-attachments/assets/ab3e1ef5-a456-44ed-9498-8bbe749d31c5" />  



