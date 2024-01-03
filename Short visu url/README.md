# Skracane adresu wizualizacji web

Wpis do rejestrów służy do skracania domyślnego adresu wizualizacji webowej na sterownikach z systemem operacyjnym Windows Embedded Compact.

Domyślny adres: http://adres_IP_sterownika/Tc3PlcHmiWeb/Port_851/Visu/nazwa_pliku.htm Adres można skrócić do formy: http://adres_IP_sterownika/nazwa_pliku.htm

Gdzie  nazwa_pliku  to  nazwa  skonfigurowana  w  projekcie  TwinCAT  w  ustawianiach  elementu WebVisualization:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/e8e36796-8732-4875-a3d0-f6b0f57f4517)

Plik WEB_visu.reg należy skopiować na sterownik (np. za pomocą folderu Public) i uruchomić, a następnie wykonać miękki restart sterownika.
