# Excelátor – česko-anglický generátor Excel vzorců

Jednoduchý, responzivní generátor Excel vzorců s českým a anglickým rozhraním a světlým/tmavým režimem. Stačí otevřít `index.html` a aplikace funguje. **Bez instalace, bez registrace, bez backendu a bez externích knihoven.**

## Co umí

- Vybrat **počet, součet, minimum, maximum nebo průměr**.
- Přidávat kombinace podmínek: prodejce, produkt, město, částka nebo vlastní sloupec.
- Filtrovat **jednotlivé měsíce, rozsah měsíců nebo konkrétní data**.
- Pracovat s číselnými podmínkami (`<`, `>`, `=`, `≤`, `≥`, „mezi“) a textovými podmínkami („obsahuje“, „začíná na“…).
- Nastavit písmena sloupců i počáteční/koncový řádek.
- Přepnout jazyk **celého webu (Čeština / English)** přímo v horní liště.
- Zapnout **Dark mode / Light mode** viditelným tlačítkem v horní liště, i na mobilu.
- Zapamatovat jazyk webu a vzhled do `localStorage` v prohlížeči.
- Nezávisle přepnout jazyk **excelových vzorců** a oddělovač argumentů (`;` / `,`).
- Vyzkoušet hotové příklady podle školních úloh.
- Zkopírovat vzorec jedním kliknutím, bez odesílání dat na server.

**Důležité:** Aplikace vytváří **vzorec**, nikoliv finální výsledek. Ten se vypočítá až po vložení vzorce do tabulky v Excelu.

## Ovládání / How to use

Vpravo nahoře vyber **Čeština / English** a tlačítkem se symbolem měsíce/slunce přepni **tmavý / světlý režim**. Přepnutí jazyka webu nezmění jazyk vzorců v Excelu; ten najdeš v rozbalovacím **Nastavení sloupců a Excelu / Columns and Excel settings**.

At the top right, select **Čeština / English** and use the moon/sun button to switch **dark / light mode**. The website language is independent from the Excel formula language, which you can configure under **Columns and Excel settings**.

## Jak web spustit na GitHub Pages

1. Na [github.com/new](https://github.com/new) založ nový repozitář. Třeba `excelator` a dej **Public**.
2. Nahraj soubory `index.html`, `README.md` a `.nojekyll` přímo **do kořenové složky** repozitáře (`Add file` → `Upload files` → `Commit changes`).
3. Otevři **Settings → Pages**.
4. V sekci **Build and deployment** nastav **Source: Deploy from a branch**.
5. Vyber **Branch: main**, složku **/(root)** a klikni na **Save**.
6. Po zveřejnění bude web dostupný na adrese `https://TVUJ-UCET.github.io/excelator/` (pokud repo nazveš `excelator`).

> Neuploaduj ZIP jako jeden soubor. **Rozbal ho** a nahraj jeho obsah: `index.html` musí být v rootu repozitáře.

## Úpravy

Celá aplikace je v souboru `index.html` (HTML, CSS a JavaScript). Můžeš jej upravovat přímo přes GitHub, nebo třeba ve VS Code. Není nutný žádný build ani Node.js.

## Omezení

- Datum se porovnává jako skutečné datum v Excelu; pokud jsou data uložená jako text, před použitím je převeď na datum.
- Podmínky se kombinují logikou **A ZÁROVEŇ (AND)**, nikoliv „nebo“.
- Pro desetinná čísla použij odpovídající jazykové nastavení Excelu.
- Moderní Excel rozpoznává `SUMIFS`, `COUNTIFS`, `MINIFS`, `MAXIFS`, `AVERAGEIFS`; některé velmi staré verze Excelu nemusí podporovat `MINIFS`/`MAXIFS`.

Vytvořeno jako jednoduchý samostatný projekt pro sdílení přes GitHub Pages.