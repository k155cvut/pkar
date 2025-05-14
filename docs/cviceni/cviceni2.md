---
icon: material/numeric-2-box
title: Cvičení 2
---

# Zpracování dat, geokódování

## Geocoding
1.  Klikněte pravým tlačítkem myši na tabulku importovanou do ArcGIS Pro a vyberte možnost *Geocode addresses*.
Tím se načte průvodce geokódováním, který je velmi intuitivní. V několika krocích nastavte parametry geokódování,
nezapomeňte odhadnout kredity a spustit operaci.
2.  U geokódovaných adres může být několik výsledků: Matched, Tied a Unmatched. Nyní můžete geokódované adresy znovu porovnat
    
    ???+ tip "Evaluace výsledků geocodingu"
        Po geokódování tabulky adres můžete zjistit, že ne všechny adresy nebo místa v tabulce byly napojeny na očekávané výsledky.
        Kontrola vaší tabulky může odhalit důvod neočekávané shody; například na vašem vstupu mohlo chybět pole, mohlo dojít ke shodě
        názvů nebo mohl být název lokace napsán chybně. V takových případech můžete zkontrolovat výsledky, provést opravy v tabulce a
        aktualizovat výsledky geokódování. Pomocí interaktivního nástroje pro opětovné přiřazení v aplikaci ArcGIS Pro můžete ručně
        zkontrolovat adresy a provést opravy původního vstupu a znovu geokódovat, změnit polohu adresy nebo vybrat jiného kandidáta.
        Můžete také upravit nastavení lokátoru a geokódovat adresy, které byly přiřazeny k neočekávaným výsledkům. Tento proces se
        nazývá *Rematching*.

3.  Prakticky si lze geocoding vyzkoušet např. na tabulce [Tour dates Eltona Johna](https://en.wikipedia.org/wiki/Farewell_Yellow_Brick_Road#Tour_dates){target="_blank"} z Wikipedie.
Tu je nejprve nutné načíst do Excelu pomocí nástroje *Načíst data z webu* a zadání URL. Výběrem správné tabulky v dialogovém okně proběhne import dat, které je vhodné
doplnit a opravit (např. odfiltrovat řádky s názvy kontinentů či doplnění názvu států do prázdných kolonek). Pro potřeby geocodingu využijeme sloupce *City* a *Country*.





