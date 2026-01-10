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
# Schematy
<img width="725" height="453" alt="image" src="https://github.com/user-attachments/assets/948c8be2-9c0f-4eee-8311-c14340274488" />

<img width="876" height="677" alt="image" src="https://github.com/user-attachments/assets/43eb12a8-cbbb-4320-a599-78053584ba9d" />

<img width="876" height="676" alt="image" src="https://github.com/user-attachments/assets/646b88c8-299a-4164-9208-9b56a03fd5e2" />

# Link do projektu w TinkerCad
https://www.tinkercad.com/things/kTcxIvqyMKj-ask?sharecode=7MFY-UlmYapReJWqLh_6AfLYa9pHraKVC2Dxa0aHRac

# Opis działa alramu/Instrukcja obsługi
Po włączeniu alarmu żaden czujnik nie jest aktywny o czym świadczy kreska wyświtlana na dole panelu LED, aby włączyć czujnik PIR należy wcisnąć przycisk znajdujący się po prawo od każdego czujnika. Każdy czujnik PIR posiada osobną dioda informującą o aktywności alarmu (dioda nieświeci-PIR wyłączony, dioda świeci-PIR włączony).Po włączeniu dowlonego PIRa (dioda świeci) kreska będzie świeci na górze panelu LED informując o tym, że alaram jest aktywny 
