# reuel.cz

Zdroj webu [reuel.cz](https://reuel.cz): čisté HTML a jeden `styl.css`, nic se
nesestavuje. Hostuje GitHub Pages z větve `main`, z kořene repozitáře.

## Náhled u sebe

```bash
python3 -m http.server 8000
```

Pak otevřít http://localhost:8000. Dvojklik na soubor nestačí: odkazy začínají
lomítkem (`/styl.css`) a počítají s kořenem webu.

## Nasazení

`git push` do `main`. Za minutu dvě je změna venku.

## Co se nesmí rozbít

Stránky ve `watson/` jsou zapsané v Google Cloud Console jako domovská stránka,
zásady ochrany soukromí a podmínky užití OAuth aplikace Watson:

- https://reuel.cz/watson/
- https://reuel.cz/watson/soukromi.html
- https://reuel.cz/watson/podminky.html

Adresy neměnit a text držet pravdivý vůči tomu, co Watson skutečně dělá —
Google se na něj odvolává. Zbytek webu je cvičiště.

`CNAME` drží vlastní doménu. Bez něj web spadne zpátky na adresu github.io.
