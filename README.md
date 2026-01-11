# Architektura systemów komputerowych – Zadanie semestralne 2

## Opis projektu
Projekt jest prostym alarmem wykorzystującym mikrokontroler ATMega328P (Arduino), jednocyfrowy wyświetlacz 7-segmentowy oraz czujniki ruchu PIR. Każdy czujnik PIR może być konfigurowany niezależnie w celu rejestrowania wykrycia ruchu, o czym informuje wyświetlacz.

Za informację o tym, czy dany czujnik PIR rejestruje wykryty ruch i przekazuje go do wyświetlacza, odpowiada dioda LED. Gdy dioda świeci, czujnik PIR jest aktywny i przekazuje informacje o wykryciu ruchu. Gdy dioda jest wyłączona, czujnik nie przekazuje żadnych danych. Każdy czujnik PIR można niezależnie włączać i wyłączać, co jednoznacznie określa jego stan aktywności.

---

## Funkcje
- Sterowanie całym obwodem za pomocą mikrokontrolera ATMega328P (Arduino)
- Obsługa pięciu czujników ruchu PIR
- Możliwość niezależnego włączania i wyłączania każdego czujnika
- Każdy czujnik PIR posiada własną diodę LED informującą o jego stanie
- Panel LED wyświetlający informacje o stanie alarmu:
  - dolna kreska – alarm nieaktywny
  - górna kreska – alarm aktywny
- Licznik aktywnych czujników PIR (liczba wykrytych ruchów od 1 do 5)

---

## Zastosowany sprzęt
- Mikrokontroler ATMega328P (Arduino)
- Czujnik ruchu PIR ×5
- Rezystor 1 kΩ ×10
- Rezystor 250 Ω ×1
- Wyświetlacz LED 7-segmentowy
- Dioda LED (czerwona) ×5
- Przycisk ×5
- 8-bitowy rejestr przesuwny 74HC595
- Przewody połączeniowe (różowy, fioletowy, czarny)

---

## Schematy
<img width="725" height="453" alt="image" src="https://github.com/user-attachments/assets/ba234c07-a49d-4b45-990b-6c2f2c71db23" />
<img width="1098" height="845" alt="image" src="https://github.com/user-attachments/assets/c70e900b-0f14-4a98-bebb-3dd8951ed3cc" />
<img width="1092" height="846" alt="image" src="https://github.com/user-attachments/assets/414e005c-7c9d-4d4e-803e-1e4b42482d57" />


---

## Link do projektu w Tinkercad
https://www.tinkercad.com/things/kTcxIvqyMKj-ask?sharecode=7MFY-UlmYapReJWqLh_6AfLYa9pHraKVC2Dxa0aHRac

---

## Opis działania alarmu
Po włączeniu alarmu żaden czujnik PIR nie jest aktywny, co sygnalizowane jest dolną kreską wyświetlaną na panelu LED. Aby włączyć czujnik PIR, należy nacisnąć przycisk znajdujący się obok danego czujnika.

Każdy czujnik PIR posiada osobną diodę LED informującą o jego stanie:
- zgaszona dioda – czujnik PIR wyłączony
- zapalona dioda – czujnik PIR włączony

Po włączeniu dowolnego czujnika PIR (zapalona dioda LED) na panelu LED pojawia się górna kreska, informująca o aktywnym alarmie. Gdy aktywny czujnik PIR wykryje ruch, informacja ta zostaje wyświetlona na panelu LED.

Jeżeli ruch zostanie wykryty przez:
- jeden czujnik – wyświetlana jest liczba **1**
- dwa czujniki – wyświetlana jest liczba **2**
- analogicznie aż do **5** czujników

Aby wyłączyć czujnik PIR, należy ponownie nacisnąć odpowiadający mu przycisk.

---

## Opis działania programu
Program obsługuje pięć czujników ruchu PIR, które mogą być niezależnie włączane i wyłączane za pomocą przycisków. Dla każdego czujnika zapamiętywany jest jego stan aktywności oraz informacja o tym, czy wykrył on już ruch.

Po uruchomieniu programu wszystkie czujniki są wyłączone, a licznik wykryć ustawiony jest na zero. Naciśnięcie przycisku powoduje zmianę stanu odpowiadającego mu czujnika. Włączenie czujnika zeruje licznik oraz informacje o wcześniejszych wykryciach, natomiast jego wyłączenie usuwa ewentualne wykrycie z licznika.

Dla aktywnych czujników program cyklicznie sprawdza sygnał z wejścia PIR. Wykrycie ruchu powoduje zwiększenie licznika tylko jeden raz dla danego czujnika, co zapobiega wielokrotnemu zliczaniu tego samego zdarzenia.

Stan czujników sygnalizowany jest diodami LED. Na wyświetlaczu 7-segmentowym sterowanym przez rejestr przesuwny 74HC595 prezentowany jest znak „–” przy braku aktywnych czujników, „0” gdy nie wykryto ruchu lub liczba odpowiadająca ilości wykrytych ruchów.

---

## Autor
Daniel Pajewski  
Nr albumu: 21525

