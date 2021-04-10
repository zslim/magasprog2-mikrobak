# Baktériumok VS vírusok

Olyan programot írunk, mellyel a bakteriális és vírusos megbetegedéseket szimuláljuk.

![microbes](https://user-images.githubusercontent.com/22755497/114267088-2e254400-99fa-11eb-8cf2-035a6087173b.jpg)

Töltsd le [ezt a félkész programot](https://elearning.uni-eszterhazy.hu/pluginfile.php/271445/mod_assign/intro/MicrobesBASE.zip) és fejleszd tovább az alábbi feladatoknak megfelelően!

## 1. feladat

Az alábbi UML ábra alapján egészítsd ki a `Microbe` absztrakt és a `Bacterium` osztályokat, illetve írd meg az interfészt!

* Mikrobáknak csak a nevét és a reprodukciós rátáját tároljuk. Az utóbbival a `Reproduce` metódus dolgozik, mely az aktuális esetszámot a reprodukciós rátával megszorozva kapja meg az új esetek számát; ezt hozzáadva az eredeti esetszámhoz kapjuk meg a frissített esetszámot.
* Baktérium esetén az aktuális esetszámot mindig a `victimCount` mezőben tároljuk, ezért a `Reproduce` metódusnak ezzel a mezővel kell dolgoznia (a kapott paramétert pedig figyelmen kívül hagynia).

![microbes_UML1](https://user-images.githubusercontent.com/22755497/114267133-63ca2d00-99fa-11eb-9d35-9ea43d724e87.png)

## 2. feladat

Az alábbi UML ábra alapján egészítsd ki a `Virus` osztályt, illetve írd meg az interfészt!

* Vírusok csak adott fajtájú gazdatestek megfertőzésével képesek reprodukálódni, ezért a `hosts` tömbben tároljuk a gazdafajtákat. Minden gazdához külön-külön tároljuk az aktuális esetszámot a `victimCounts` tömbben.
* Az `Infect` metódus a paraméterként megkapott gazdatestet fertőzi meg, ha képes.  Ha képes fertőzni, akkor átvált fertőző üzemmódba (`isInfecting`), reprodukálódik, majd visszavált nem fertőző üzemmódba. A fertőzés sikerességét a metódus logikai értékként visszaadja.
* Az `Infect` metódus a `Reproduce` metódust hívja, mely hasonlóan működik a `Bacterium` osztályban levőhöz, de most ténylegesen a megkapott paraméterrel dolgozik.

![microbes_UML2](https://user-images.githubusercontent.com/22755497/114267230-be638900-99fa-11eb-8da4-8d72b59c641d.png)

## 3. feladat

Egészítsd ki a főprogramot!

* Minden baktérium végezzen 10 reprodukciót.
* Minden vírus végezzen 10 fertőzést (random kiválasztott gazdatesten).
* Legvégül írd ki a képernyőre a listaelemek adatait! Ehhez használd az osztályok `ToString` metódusát!

*A feladat szerzője Kovásznai Gergely.*
