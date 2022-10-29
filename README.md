# Logdatenkonverter
Konverter von Simrad Diagnosedaten in das Actisence EBL Format

Simrad, Lowrance und B&G Plottern mit einer Firmware ab 18.x haben nun eine Diagnosefunktion für das NMEA2000 Netzwerk.
Unter Menü -> Einstellungen -> Netzwerk -> Diagnose findet man eine Schaltfläche Log für die letzten x Minuten speichern.

Diese Funktion speichert ein Linuxtypisches Logfile als .tar ab, in dem mehrere Einzeldateien mit je einer Minute langen Logfiles im .pcap Format befinden.
Über die Software Logdatenkonverter kann nun dieses binäre Logfile in ein Actisence .ebl (Electronic Binary Log) konvertiert werden.

Das konvertierte File kann mit dem Actisence EBL-Reader betrachtet werden.
https://actisense.com/wp-content/uploads/2020/02/Actisense-EBL-Reader-v2.027-x86-Setup.exe_.zip

Implementiert sind zur Zeit über 160 Singleframes, sowie die FastPaket mit den PGN: 
126996 (Productinformation), 
126998 (ConfigurationIformation), 
127489 (Engine Dynamic), 
129285 (Navigation Route/WP Information) und 
129540 (GNSS Sat in View)
