# Instrukcja

PopUp (okienko dialogowe) – istnieje możliwość, aby dany ekran wizualizacji pełnił rolę okienka popup (ze zmiennymi parametrami) oraz możliwością reakcji na sposób jego zamknięcia (OK lub Cancel). 

W przykładzie stworzono ekran Dialog Test z parametrem sText (wyświetlany na środku okienka).

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/521a825a-cfe8-4c63-9d6e-8371d715ffa1)

Dla tego ekranu, w jego właściwościach, należy ustawić opcję Use visualization as Dialog:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/d1b6892f-1221-4bb8-ac52-bc45404e69b5)

Nazwa  ekranu  zawierającego  Popup  powinna  znaleźć  się  w  funkcjach  CloseMessageDialog  oraz OpenMessageDialog w kodzie PLC:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/50742e13-2ae1-4b18-941f-334431005284)

W przykładzie otwarcie dialogu odbywa się zmienną bOpen w programie P_Dialog, zmienna sMessage jest wyświetlanym parametrem.

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/8fe7cdc0-c2c3-4c3f-a993-c667d713101e)

W dalszej części kodu można dopisać reakcję na konkretny sposób zamknięcia okienka:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/4b7b8086-08cf-4c32-912c-6ade89f97ff4)

Pod przycisku na wizualizacji należy podpiąć odpowiednie akcje:

![image](https://github.com/BA-PL/PLC-HMI/assets/155453679/0b512733-024d-4774-b9c1-423aa678a127)
