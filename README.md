# sistema-di-navigazione
sistema di navigazione a bordo di Polaris


Nuovo sistema di navigazione composto da :

Dell Latitude E7250, openCPN, (SignalK server non attivo) + tablet Oukitel RT1 rugged con Android 11 (installati Remote Desktop Microsoft da Google Play, NKE Display, opencpn)

RaspberryZeroW con IMU 9255, software pypilot (tinycore), AP con SSID pypilot

Nano-baro : Arduino nano con sensore BMP180 per pressione e temperatura collegato via USB al RaspberryZeroW. Genera stringhe NMEA XDR con temperatura e pressione (nanobaro)

    il laptop e il tablet si collegano all’AP pypilot (192.168.14.1) senza password
    openCPN legge da USB dati Seatalk (GPS, wind, depth) e AIS (da dAISy)
    openCPN legge da tcp 192.168.14.1:20220 dati NMEA roll, pitch, heading + pressione e temperatura da nanobaro
    sul tablet
    NKE display (android) legge dati da tcp 192.168.14.1:20220

DATI

source PYPILOT: Roll, Pitch, Heading

source NANOBARO: Air temperature, Barometer

source SEATALK: Wind speed, Wind dir (apparent/true), GPS (Latitude, Longitude, Speed, Course, Time), Depth

source DAISY: AIS

WINDOWS:
attivare Remode Desktop (da settings, system)
su tablet Android attivare Remote Desktop
collegarsi al PC

