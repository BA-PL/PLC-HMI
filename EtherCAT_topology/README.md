# Instrukcja 
Przygotowanie plików do wyświetlania topologii  EtherCAT na wizualizacji:
- szukamy na komputerze na którym zainstalowane jest pełne narzędzie TwinCAT, pliku EcTopology.dll (C:\TwinCAT\3.1\Components\Base)
- kopiujemy go i wklejamy do takiej samej lokalizacji na sterowniku ( jeśli na sterowniku nie ma takiej ścieżki – należy ją stworzyć)
- następnie,  na  sterowniku,  szukamy  w  lokalizacji  C:\Windows\System32  pliku  regsvr32.exe. Przeciągamy na ten plik skopiowany wcześniej EcTopology.dll. Powinien się pojawić komunikat o prawidłowej rejestracji

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/9d95ef53-449b-444b-a963-7211eb1f32c5)

- z komputera, gdzie jest narzędzie, z lokalizacji C:\TwinCAT\3.1\Config\IO\EtherCAT kopiujemy pliki xml od modułów, które występują w naszej konfiguracji, i wklejamy do tej samej lokalizacji na sterowniku (tylko pliki od modułów które rzeczywiście znajdują się w naszej konfiguracji, im więcej plików, tym dłużej wizualizacja będzie się wczytywać)
- wykonujemy restart sterownika (z poziomu systemu Windows, nie poprzez zdjęcie zasilania) Projekt PLC:
- na ekran wizualizacji wstawimy z Toolbox element ActiveX

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/173983c4-4da6-4a88-9fc1-8668389ae20a)

- we właściwości Control wybieramy opcję EcTopology.EcTopologyCtrl.1

 ![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/3e57c1d7-9a2f-449f-bf51-7c228ad0664a)

 - następnie konfigurujemy metody:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/cbca7605-449d-4f42-bddb-e8fe59d14045)

Zmienna metody TargetNetID powinna zawierać adres AmsNetID sterownika, można go odnaleźć w projekcie tutaj:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/929c0f2b-52a3-45b0-b604-737f9f77a292)

Zmienna metody DeviceID powinna zawierać ID mastera EtherCAT:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/a3f90c9f-affe-4657-b14f-1bff4208cbde)

Zmienna  metody  SlaveDescriptionPath  powinna  zawierać  ścieżkę  do  plików  xml  –  tutaj  zawsze C:\TwinCAT\3.1\Config\Io\EtherCAT

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/117d157f-0737-413b-9cac-cbab392df8ee)

Pozostała konfiguracja akcji warunkowych – jak w projekcie.
