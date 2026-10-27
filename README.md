# reuel.cz

Zdroj webu [reuel.cz](https://reuel.cz): čisté HTML a CSS, nic se nesestavuje.
Hostuje GitHub Pages z větve `main`, z kořene repozitáře.

| Co | Soubory |
|---|---|
| úvodní stránka — prezentace AI služeb pro firmy | `index.html`, `reuel.css`, `img/`, `fonts/` |
| projekty — skrytá stránka, vede na ni jen logo na úvodní stránce | `projekty/index.html` |
| stránky Watsona (viz níž) | `watson/`, `styl.css` |
| chybová stránka | `404.html` |

Vzhled úvodní stránky jde z firemního designu JAY STUDIO: vínová, písma Jost
a Literata. Znak loga (`img/logo.svg`) je zjednodušené schéma z hlavičky;
stránky ho vkládají přes `<use href="/img/logo.svg#znak">`. Ikona v záložce
prohlížeče je jiný soubor, `img/ikona.svg` (písmeno „j“). Písma jsou uložená tady ve `fonts/` (licence SIL Open Font License,
texty licencí vedle nich), nic se nenačítá odjinud.

## Náhled u sebe

```bash
python3 -m http.server 8000
```

Pak otevřít http://localhost:8000. Dvojklik na soubor nestačí: odkazy začínají
lomítkem (`/reuel.css`) a počítají s kořenem webu.

## Nasazení

`git push` do `main`. Za minutu dvě je změna venku.

## Co se nesmí rozbít

Stránky ve `watson/` jsou zapsané v Google Cloud Console jako domovská stránka,
zásady ochrany soukromí a podmínky užití OAuth aplikace Watson:

- https://reuel.cz/watson/
- https://reuel.cz/watson/soukromi.html
- https://reuel.cz/watson/podminky.html

Adresy neměnit a text držet pravdivý vůči tomu, co Watson skutečně dělá —
Google se na něj odvolává. Watson ani `styl.css` se při úpravách úvodní stránky
neupravují.

`CNAME` drží vlastní doménu. Bez něj web spadne zpátky na adresu github.io.
