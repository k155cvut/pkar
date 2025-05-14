---
icon: material/numeric-5-box
title: Cvičení 5
---
## Složený kartodiagram
Pokročilý přístup ke klasickému pie chartu může vést k dělení kruhu dle množství jevů a práci se změnou poloměru těchto segmentů. V ArcGIS Pro je možné použít metodu *Proportional Symbols* a zvolit symbol půlkruhu či čtvrtkruhu, které po změně rotace formují koncentrické kruhové výseče.

Metodu je možné vyzkoušet na datech [vídeňských městských částí](https://www.data.gv.at/katalog/en/dataset/2ee6b8bf-6292-413c-bb8b-bd22dbb2ad4b){target="_blank"}.

K nim připojíme [data](https://www.data.gv.at/katalog/en/dataset/0c4279aa-e14c-4626-9b4b-882fa32551b0){target="_blank"} obsahující počty obyvatel dle místa narození za rok 2023 a predikci demografického vývoje pro rok 2043.

Nastavíme v symbologii *Proportional Symbols* a vybereme symbol čtvrtkruhu (obsažen např. v *ESRI IGL Font22*), který pro každý jev vhodně natočíme, aby dohromady pokryly celých 360°.

???+ tip "Legenda"
      Legendu lze v *Layoutu* vygenerovat obvyklým způsobem, je však nutné přidat fiktivní řádek do atributové tabulky s globálním minimem, který nám zajistí konzistentní stupnici pro všechny jevy. Najděte tedy nejnižší hodnotu mezi všemi jevy, zaokrouhlete ji vhodně směrem dolů a vyplňte do pomocného záznamu v tabulce.

## Coxcomb
Jedná se o varianta na pie chart, která vzniká dělením kruhu do rovnoměrných segmentů (např. dle počtu časových úseků), s poloměrem (výseče) lišícím se podle kvantity jevu. Výsledkem jsou segmenty, které se liší rozsahem od středu grafu. Obvykle se používá k zobrazení časových jevů v souladu s původním použitím Florence Nightingale v jejím klasickém diagramu úmrtnosti východních armád z roku 1858.

<figure markdown>
  ![](../assets/Nightingale-mortality.jpg "Diagram úmrtnosti (F. Nightingale, 1858)"){ width=500px }
</figure>

[Coxcomb toolbox for ArcGIS](https://carto.maps.arcgis.com/home/item.html?id=ebdf8024e9714c7dbfa4f5342634fcdb){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
[Mapping coronavirus coxcombs](https://www.esri.com/arcgis-blog/products/arcgis-pro/mapping/mapping-coronavirus-coxcombs/){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
{: .button_array}

???+ tip "Legenda"
      V případě metody **coxcombs** toolbox sice vytvoří kartodiagramy, ale nadstavba pro tvorbu legendy v layoutu neexistuje. Proto
      je nutné si připravit data způsobem, který zajistí tvorbu legendy již v samotném průběhu vizualizace. Doporučení pro strukturu
      coxcombs tedy zní takto:

      - do tabulky dat přidejte fiktivní záznamy, které budou obsahovat globální minimum a globální maximum (stejné napříč všemi kategoriemi)

      - další (tedy třetí) fiktivní záznam bude obsahovat takové hodnoty, které se objeví v legendě (tzn. vhodně zaokrouhlené a rostoucí po směru hodin)
      
      - pokud záznamy pouze vkládáte jako *Add Row* v atributové tabulce, umístí se do počátku souřadnicového systému; vy však můžete přemístit bod
      reprezentující legendu (třetí fiktivní záznam) do blízkosti mapového obsahu, aby se zobrazil v mapovém okně layoutu.

[Data](../assets/data/Coxcomb_Mzdy_DRI.xlsx) k testování metody zahrnují vývoj mezd v Česku a za stejné období vývoj cen nemovitostí (ceny za metr čtvereční) pro jednotlivé kraje.