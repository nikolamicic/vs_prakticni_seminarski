# 2023_Analysis_Widgetci

# Verifikacija Softvera - samostalni praktični seminarski
U okviru ovog repozitorijuma će biti predstavljen praktični seminarski rad na kursu Verifikacija Softvera.

Seminarski rad je samostalnog tipa i svodi se na primenu alata za verifikaciju softvera na već postojeći projekat otvorenog koda.

Projekat nad kojim će biti primenjeni alati se nalazi na github adresi: https://github.com/eminfedar/widgetci

Autor ovog projekta je Emin Fedar (github username: eminfedar).

Primena alata će biti izvršena na master grani, nad komitom čiji je hash code sledeći: 05588c036cd4c6d6eddd5b595d027968ac484140

# Spisak korišćenih alata:
  1. Clang-tidy i Clazy
  2. Cppcheck
  3. GCov
  4. QML-profiler


# Spisak pronađenih bagova:
  1. Clang-tidy i Clazy su kreirali upozorenje da postoji neinicijalizovano polje na kraju poziva konstruktora, detaljnije objašnjenje se može pronaći u fajlu output.txt u okviru foldera clang_tidy_clazy.
  2. Cppcheck alat je otkrio grešku u fajlu widgetci/wqml- system.cpp na liniji 78 i predstavlja pronadenu funkciju koja je non-void tipa, a ipak ne sadrži povratnu vrednost.
  3. GCov alat je otkrio fajlove čija je pokrivenost veoma mala, gde na primer imamo fajlove wqmlsystem.cpp koji ima pokrivenost 21.2% i wqmlsystem.h sa pokrivenošću 0.0%.