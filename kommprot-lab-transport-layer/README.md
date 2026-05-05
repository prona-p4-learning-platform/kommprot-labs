# Cheat Sheet: TShark and Tmux

## Aufgabe 2

1. iperf3 muss in dem Container "Server" als Server gestartet werden. Nutzen Sie die Help-Flag "-h", um herauszufinden, welche Parameter Sie übergeben müssen
2. Nun müssen Sie in dem Container "Client" ebenfalls iperf3 starten. Sie benötigen die Parameter, dass das Programm als Client gestartet werden soll und die IP-Adresse + Port des Servers, zu dem Sie sich verbinden möchten
3. Um iperf3 mit UDP zu starten benötigen Sie zwei weitere Parameter: Sie müssen den Parameter für UDP selbst und den Parameter für die gewünschte Bitrate übergeben

## Aufgabe 3

1. Um zwei Terminals zu öffnen benötigen Sie "tmux". Installieren und öffnen Sie dieses Programm
2. Um nun ein zweites Terminalfenster zu öffnen, drücken Sie "CTRL + B", lassen Sie es wieder los und drücken nun die Taste "%"
3. Um zwischen den Fenstern zu wechseln, drücken Sie "CTRL + B", lassen Sie es erneut los und drücken Sie nun die Pfeiltasten links und rechts um jeweils in das linke und rechte Terminal zu kommen
4. Um eine Terminalsession zu schließen, schreiben Sie "exit"
5. Nutzen Sie Tshark mit den folgenden Argumenten, damit Sie ausschließlich HTTP und HTTPs Pakete mitschneiden und anzeigen: "tshark -i eth0 -f "tcp port 80" -Y "http" -O http"
6. Um eine Webseite aufzurufen, nutzen Sie den Befehl "curl". Wenn Sie einen Statuscode "301" erhalten, versuchen Sie es erneut mit "curl -L"
