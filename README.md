# Architektura systemów komputerowych-Zadanie semestralne 2
# Opis projektu
Projekt jest prostym alarmem wykorzystuje mikrokontroler ATMega328P (Arduino), mały wyświetlacz 7 pinowy oraz PIRy. Można ustawić każdego PIRa z osobna aby rejestrował wykrycie ruchu o którym informuje wyświetlacz, za informacje czy PIR zarejestruje wykryty ruch i przekaże go do wyświtlacza odpowiedzialna jest dioda, dioda świeci PIR rejestruje i przekazuje, dioda wyłączona PIR nie przekazuje.Każdą diode można włączyć i wyłączyć co jest jednoznacze z tym, że PIR wysyła bądź nie informacji do wyświetlenia
# Funkcje
-Sterownik całego obwodu mikrokontroler ATMega328P (Arduino) 

-Obsługa 5 czujników ruchu PIR

-Możliwość wyłączenie i włączenia każdego czujnika

-Każdy PIR posiada swjoą diode LED która informuje o włączeniu bądź wyłączeniu PIRa

-Panel LED pokazuje informacje na temat aktywności alarmu (dolna kreska-nieaktywny, górna kreska aktywny)

-Licznik aktywnych PIRów (Licznik wykrytych ruchów od 1-5)
# Zastosowany sprzęt
•Mikrokontroler ATMega328P (Arduino)

•Czujnik ruch PIR x5

•Rezystor 1kΩ x10

•Rezystor 250Ω x1

•Panel LED 7 pinowy

•Dioda LED (czerwona) x5

•Przycisk x5

•8-bitowy rejestr przesuwny (74HC595)

•Przewody (różowy, fioletowy, czarny)
# Link do projektu w TinkerCad
https://www.tinkercad.com/things/kTcxIvqyMKj-ask?sharecode=7MFY-UlmYapReJWqLh_6AfLYa9pHraKVC2Dxa0aHRac
