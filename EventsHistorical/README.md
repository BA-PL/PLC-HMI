# Instrukcja

Przykład  pokazuje,  jak  stworzyć  własną  tabelę  zdarzeń  z  historią  (100  ostatnich  zdarzeń).  Aby dostosować go do swoich potrzeb należy:
- w akcji ACT_1045_PL lub ACT_1033_US zdefiniować treść eventów

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/4fa210f2-456e-4a3c-a0bd-63a1b8238a0a)

- w akcji ACT_Active zdefiniować warunki wystąpienia zdarzenia 
- w akcji ACT_ClassDefinition przypisać klasy zdarzeniom (np. klasa o ID 0 to alarmy, ID 1 to ostrzeżenia, ID 2 to wiadomości)
  
Historia zdarzeń jest realizowana poprzez zapis tablicy ze zdarzeniami jako dane PERSISTENT.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/b0a13aee-fe6a-4066-8b74-7107a6b63aca)

Do projektu jest dołączona również przykładowa wizualizacja.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/96f1da85-f11b-4104-9b38-83e1f5aeb2ea)
