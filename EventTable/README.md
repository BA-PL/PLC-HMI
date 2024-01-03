# Instrukcja

Jeżeli chcemy wykorzystać element EventTable (tabela alarmów w wizualizacji), to należy opcję tę uaktywnić. Robi się to poprzez kliknięcie PPM na projekt PLC i wybranie właściwości:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/631303ce-b4d9-40a5-a4d1-631e6d4b6281)

Następnie w zakładce Visualization Profile uaktywniamy element EventTable. Od tej pory będzie on dostępny w Toolbox wizualizacji w kategorii SpecialControls.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/cb775f88-8ef9-4d2a-8bac-c24e7509f8db)

Przykładowy projekt pozwala na logowanie zdarzeń na podstawie trzech tablic zmiennych globalnych typu BOOL, oddzielnych dla alarmów, ostrzeżeń i komunikatów. Zdarzenia zapisywane są w pamięci sterownika w zmiennych globalnych (GVL_EventsSimple) tylko w czasie, w którym są aktywne i są automatycznie usuwane po wyzerowaniu zmiennej wywołującej dane zdarzenie.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/0f570d50-bc0b-480b-a9ec-a045e2f70c4f)

To co należy zrobić w PLC, to zdefiniować, kiedy dany alarm ma wystąpić. Przykładowo, jeżeli ma wystąpić alarm o ID =1 to przypisujemy warunek do pierwszego indeksu tablicy MSG_Alarm_List etc.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/e866d747-07ee-4d1c-aad1-51c847501a55)

Samą treść alarmów definiuje się w plikach xml.
W załączniku znajdują się dwa pliki – TcEventsSourceLocation oraz UserEvents. Oba te pliki powinny znajdować się na sterowniku w lokalizacji \TwinCAT\3.1\Target\Resource. Jeżeli takie pliki już istnieją w tej lokalizacji, należy je nadpisać tymi z załącznika. Treść zdarzeń definiujemy właśnie w pliku UserEvents. Zdarzenia są podzielone na 3 grupy: alarmy, ostrzeżenia i wiadomości. Każde z grup ma przypisane swoje źródło i pod tym źródłem definiujemy dane zdarzenia w danej podgrupie. Jeżeli pliki będą już gotowe, należy wykonać miękki restart systemu Windows na sterowniku.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/227a4b9e-2f5e-4acd-96ec-6e4a58f20789)
