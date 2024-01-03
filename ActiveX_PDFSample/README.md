# Instrukcja

Przykład  pokazuje  obsługę  kontrolki  ActiveX  –  w  tym  przypadku  do  obsługi  plików  PDF.  Kroki konfiguracji:

- wstawiamy z Toolbox kontrolkę ActiveX

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/9ffcf71a-841b-4718-8881-af08c4c9defc)

- we właściwościach kontrolki ustawiamy właściwość Control na AcroPDF.PDF.1

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/254beb71-b533-4789-aa0d-54e156c7ac91)

UWAGA! Na urządzeniu, na którym będzie uruchamiana wizualizacja z obsługą PDF, w systemie musi być zainstalowana aplikacja do obsługi takich plików. 

Następnie konfigurujemy wywołanie warunkowe, używając metody LoadFile:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/05823c62-801b-4e6e-9b32-c5c53b06daf9)

W parametrze Call Condition należy podpiąć zmienną typu BOOL, która będzie wywoływać metodę, a jako kolejny parametr zmienną, która będzie przechowywać ścieżkę do pliku wraz z jego nazwą i rozszerzeniem, np.:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/0bafd7c4-5144-4636-afb9-8089db3ddcf2)



