
STORED XSS:

ze zacatku je vyuzit zakladni blacklist a je nebezpeci utoku treba s vyuzitim onmouseover (nejlehci fix = hodit do disallowed_attributes)
- Lze ale obejit pouzitim uppercase, je to stale nebezpecne
- Pripadne reseni metoda jenz prevadi vse do lower_case a pote prochazejici disallowed_attributes

take by bylo dobre overit allowed_tags, pres p a td lze vlozit script

-- pripadne upravy: lepsi sanitizer (treba bleach) a vyuziti jeho fragmentu


XSRF
V kodu udelame upravenou metodu _DoDelete v souboru "gruyere.py", ktera by mela vyuzivat overeni pomoci CSRF tokenu, tak bychom meli ten token stale menit a tim predejit problemu.

Tato funkce musi byt implementovana a pote spustena s kodem, coz by melo slouzit jako mozna ochrana proti utokum typu XSRF, alespon v tomto pripade.

Pripadne zmeny:
Overeni vstupu: pridana zakladni kontrola, ktera ma zajistit, jestli je parametr index retezcem. Mozna bude potreba dalsi overovani (napriklad overit, zda se jedna o platne cislo v urcitem rozsahu nebo vyuziti potrebneho souctu cisel)



