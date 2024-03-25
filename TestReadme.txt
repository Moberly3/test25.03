
STORED XSS:

ze zacatku je vyuzit zakladni blacklist a je nebezpeci utoku treba s vyuzitim onmouseover (nejlehci fix = hodit do disallowed_attributes)
- Lze ale obejit pouzitim uppercase, je to stale nebezpecne
- Pripadne reseni metoda jenz prevadi vse do lower_case a pote prochazejici disallowed_attributes

take by bylo dobre overit allowed_tags, pres p a td lze vlozit script

-- pripadne upravy: lepsi sanitizer (treba bleach) a vyuziti jeho fragmentu


XSRF



