Temat: Propozycja na projekt indywidualny
Opublikowane przez: dr inż. Maciej Stodolski
Data publikacji: 20.11.2015 19:47

Moja propozycja to rozwiązywanie układów równań z macierzami rzadkimi
Skoro już umiemy je wczytywać, dodawać, mnożyć to wystarczy wykonać kilka funkcji

Dowolną macierz kwadratową (NIEOSOBLIWĄ) można zdekomponować na iloczyn dwu macierzy L*U
L to macierz,dolna trójkątna, która na diagonali ma jedynki (nie trzeba ich przechowywać), ma elementy poniżej diagonali i SAME ZERA powyżej diagonali.

U to górna trójkątna, która powyżej diagonali ma elementy a poniżej nie.
Nazywa się to dekompozycją Gaussa Newtona.

Układ równan jest postaci A * x = b, gdzie znamy A i b (wektor prawych stron) i szukay nieznanego wektora x. 

Jeżeli A = L * U to L * U * x = b

Iloczyn macierzy i wektora daje wektor, wiec możemy przyjać że U * x = y

Czyli otrzymamy L * y = b

Pomnózmy pierwszy wiersz macierzy przez y otrzymamy y1 = b1 => OK, mamy już Y1 :)
Teraz drugi wiersz: l21 * y1 + 1 * y2 = b2 => stąd y2 = b2 - l21 * b1
I tak dalej. Rozwiązanie układu równań z macierzą dolną trójkątną to dwie proste pętel

jak wyliczymy wszystkie y to mamy U * x = y

Macierz trójkątną górną rozwiazujemy od końca. 
Ostatni wiersz pomnozony przez x da nam:

Unn * xn = yn => xn = yn/Unn 

Czyli rozwiazanywanie z macierzą L robimy od pirwszego wiersza a z macierzą U od ostatniego do pierwszego.

1. Jezeli macierz A jest rzadka to macierz odwrotna do niej jest gęsta => nie nalezy NIGDY wyliczać maciery odwrotnej 
2. Jezeli macierz A jest rzadka to L i U będą rzadkie. Bardziej zaawansowane algorytmy dekompozycji Gaussa zmieniają kolejność kolumn w macierzy (tak zwany wybór elementu głownego) aby zapewnić dobre uwarunkowanie macierzy L i U oraz ich "rzadkość"
3. Program będzie wczytywał macierz A i wektor b a zapisywał do drugiego pliku L, U, x

To jest moja propozycja jako rozwinięcie macierzy rzadkich. 
Bardziej dociekliwi mogą poczytać o wyborze elementu głownego i permutacji kolmn podczas dekompozycji. Trzeba pamietac, ze jeżeli tego nie zrobimy to macierz A MUSI mieć na diagonali najwieksze wartosci elementow (nie moze być ZER na diagonali)

Pozdrawiam

Maciej
