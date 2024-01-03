# Instrukcja

Poniższy  przykład  pokazuje,  jak  edytować  domyślne  elementy  z  biblioteki  VisuDialogs  –  w  tym konkretnym przypadku domyślne klawiatury. 

W  pierwszym  kroku,  należy  w  bibliotece  VisuDialogs  (powinna  się  ona  dodać  przy  tworzeniu wizualizacja, bądź można ją dodać do projektu ręcznie) odnaleźć elementy np. Keypad lub Numpad:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/4bd60dfe-8b5b-4820-a143-346633f6a80d)

Element można dwuklikiem otworzyć, a następnie zaznaczyć wszystkie elementy (grafikę) i skopiować do swojego, wcześniej przygotowanego ekranu wizualizacji. To samo należy zrobić ze zmiennymi przypisanymi do tego elementu:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/342cfc05-6466-4d5b-8770-462c950c3d27)

W przykładzie jest to ekran wizualizacji CustomKeypad, do którego elementy zostały skopiowane:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/3f46ed2a-94cf-4c6c-b5ee-28e1752eb062)

Po  skopiowaniu,  można  dowolnie  (pod  kątem  graficznym)  edytować  element.  W  opisywanym przykładzie jako  dodatkowa  opcja,  skonfigurowano Hotkeys  – pozwala  to  wprowadzać  znaki jednocześnie za pomocą klawiatury ekranowej wizualizacji jak i klawiatury fizycznej podłączonej do urządzenia.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/a216557b-1281-44e3-a8f0-c34b043dfa33)

Aby korzystać z wyedytowanych klawiatur, należy wykonać te kroki:
- we właściwościach ekranu, który zawiera klawiaturę, należy ustawić właściwość Use visualization as na NumKeypad:
 
![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/5053051c-c47c-4a7f-af41-950ca7a70072)

- następnie należy zapisać i przebudować projekt
-  następnie w VisualizationManagerze
  ![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/eb01ed20-b02d-4885-814c-507183636900)

W zakładce Dialog settings dokonujemy odpowiednich ustawień dla elementu Keypad

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/740343e3-1d5c-4758-bd23-7b123cf6ed9c)

Następnie zapisujemy, przebudowujemy i wgrywamy projekt. Od tej pory jako metoda wprowadzania znaków na wizualizacji, powinna pojawiać się nasza edytowana klawiatura. 
UWAGA! Należy zwrócić uwagę na wybraną metodę nadpisywania zmiennej z poziomu wizualizacji. Klawiatura Custom będzie działać przy wybranej opcji Default, lub przy konkretnym wskazaniu tej klawiatury. 

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/43db2f0c-edba-4601-97c5-0237dac47bb8)
