---
icon: material/numeric-4-box
title: Cvičení 4
---
# Pokročilé metody tematické kartografie (část 1)

## Složený kartodiagram
Pokročilý přístup ke klasickému pie chartu může vést k dělení kruhu dle množství jevů a práci se změnou poloměru těchto segmentů. V ArcGIS Pro je možné použít metodu *Proportional Symbols* a zvolit symbol půlkruhu či čtvrtkruhu, které po změně rotace formují koncentrické kruhové výseče.

Metodu je možné vyzkoušet na datech [vídeňských městských částí](https://www.data.gv.at/katalog/en/dataset/2ee6b8bf-6292-413c-bb8b-bd22dbb2ad4b){target="_blank"}.

K nim připojíme [data](https://www.data.gv.at/katalog/en/dataset/0c4279aa-e14c-4626-9b4b-882fa32551b0){target="_blank"} obsahující počty obyvatel dle místa narození za rok 2023 a predikci demografického vývoje pro rok 2043.

Nastavíme v symbologii *Proportional Symbols* a vybereme symbol čtvrtkruhu (obsažen např. v *ESRI IGL Font22*), který pro každý jev vhodně natočíme, aby dohromady pokryly celých 360°.

???+ tip "Legenda"
      Legendu lze v *Layoutu* vygenerovat obvyklým způsobem, je však nutné přidat fiktivní řádek do atributové tabulky s globálním minimem, který nám zajistí konzistentní stupnici pro všechny jevy. Najděte tedy nejnižší hodnotu mezi všemi jevy, zaokrouhlete ji vhodně směrem dolů a vyplňte do pomocného záznamu v tabulce.

## Waffle
Metoda *Waffles* zobrazuje kvantity kategorií tvořící celek. Je podobná pie chartu, ale má mřížkový vzhled. Každá ze složek kategorie je pak v mřížce zobrazena jako opakující se symbol. Symbolika se obvykle provádí pomocí různých odstínů, které reprezentují různé kategorie. Metodu lze rovněž využít pro zobrazení časových řad.

<figure markdown>
  ![](../assets/cviceni4/Waffle-grid.png "Ukázka metody z California Water Atlas (William Bowen, 1979)"){ width=500px }
</figure>

[Waffle grid toolbox for ArcGIS](https://carto.maps.arcgis.com/home/item.html?id=d749baac3ede42c3b6f011dc41627b03){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
[Mapping coronavirus waffles](https://www.esri.com/arcgis-blog/products/arcgis-pro/mapping/mapping-coronavirus-waffles/){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
[Největší emitenti ČR](https://faktaoklimatu.cz/infografiky/nejvetsi-emitenti-cr){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
[Tile grid waffle chart map in excel](https://policyviz.com/2017/09/20/tile-grid-waffle-chart-map-in-excel/){ .md-button .md-button--primary .server_name .external_link_icon_small target="_blank"}
{: .button_array}


