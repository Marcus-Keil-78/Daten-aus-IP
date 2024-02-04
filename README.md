# Daten-aus-IP
Mit dem Modul "ipinfo" daten auslesen und mit Tkinter ausgeben und auch als .txt speichern können

Es wird für das Paket "ipinfo2 ein Token benötigt. Diesen habe ich in der Kostenlosen Variante. Da ich mehere Token habe, habe ich diese in einerJson-Datei abgespeichert und hole mir diese aus der Json in die Variable "tkoen_daten". Diese muß duch eueren Token ersetzt werden. Diesen könnt ihr unter https://ipinfo.io/ erhalten.

Das Dictinonary "sprachen_dict" ist erweiterbar. Dies wird für die Übersetzung der erhaltenen Werte benötigt, da diese in Englisch sind. Da ich die Deutschen Wörter gerne hätte, muß dies noch übersetzt werden. Es ist zwar nicht nötig gewesen, das auch die Quell-Sprache angegeben wird, aber bei meinen Versuchen konnte ich die Rückgabewerte für beide Comboboxen erreichen, so das anhand des Dictinonarys "sprachen_dict" die Values für beide Comboboxen zurückerhalte.

Die Daten werden entweder für eine IPv4 oder für eine IPv6 Adresse angezeigt, sofern die vorhanden ist.
Die Funktion "get_wan_ips" holt mithilfe von https://api.ipify.org (für IPv4) bzw. https://api6.ipify.org (für IPv6) die IP-Adresse des Gateways/Routers und gibt diese zurück. Falls keine Vorhanden ist, wird None zurückgegeben.

Das Speichern der angezeigten Daten ist nur als Textdatei möglich.
Damit beim Speichern keine Fehler auftreten, ist die Variabel "abfrage_daten_holen" eingesetzt. erst wenn diese True ist, kann gespeichert werden. Die ist dann True, wenn die Daten geholt wurden. Beim Zurücksetzten der Ausgaben, wird die auf False gesetzt.
Wenn der Speicherpfad einen leeren Sting zurück gibt, würde eine Fehler auftauchen, damit das nicht passiert wird mit IF abgefragt, der Pfad ungleich einen Leeren Sting ist.

Die Positionierung der Buttons, Label, etc. erfolgt über Frames, so das in dem Fenster hauptsächlich die Hauptframes zu sehen sind. Die Überschrift ist ein einfaches Label.
