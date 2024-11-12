# Explicació del DTD y XML per al meu projecte "PHASMOPHOBIA"

## **Objectiu:**
El objectiu del projecte es presentar uns fantasmes y uns mapes del joc "Phasmophobia". A més es mostraran caracteristiques d'aquestos dos elements per a raonar que mapes afavorixen a uns certs tipus de fantasmes sobre la base de les seues habilitats i característiques. També he buscat crear una estructura fàcilment ampliable perquè en futures actualitzacions es puguen afegir dades sense massa problemàtica

### **DTD Explicat:**
Per a començar creem el primer element principal del DTD "PHASMOPHOBIA" i dins d'este els dos elements a definir: "fantasma" i "mapa". Li afegim "+" per a indicar que com a mínim hi haurà un element de cada però poden haver-hi més. Després creem "fantasma" i declarem els elements que li pertanyen, en este cas "proba1", "proba2", "proba3" "descripcio_f" i "foto_f". El motiu pel qual creem 3 proves diferents i no un sol element "prova" amb un "+" és perquè sempre hauran 3 proves, ni una mes ni una menys. Després li afegim els atributs obligatoris amb #REQUIRED: id, nom, data d'introducció, velocitat i cordura a la qual caça. Tant la velocitat com la cordura  a la qual caça el fantasma han de pertànyer a uns valors específics pel que introduïm estos valors entre | per a que soles es puguen elegir aquestos.
Per a finalitzar amb "fantasma" declarem tots els seus elements com #PCDATA ja que tots estos s'emplenaran amb text en el XML, incloent-hi les rutes de les imatges.

Repetim este procés amb "mapa" però canviant els seus elements a: "descripcio_m", "fusible", "posesio_maleïda" i "foto_m". Cal recalcar que la possessió maleïda no sempre estarà en tots els mapes pel que afegim un "?" per a demostrar la seua opcionalitat.
Afegim els seus atributs ,també obligatoris amb #REQUIRED, que en este cas seran: "id", "nom", "tamany", "data_introduccio" i "obert". 
En aquest cas només existixen 4 tipus de grandària diferents especificats en l'atribut, cas paregut al de la velocitat o la cordura a la que caça el fantasma. D'altra banda el mapa pot o no ser obert, però com en la majoria de cas este serà tancat el valor de "obert" per defecte serà "no"
Finalitzem tant la part de "mapa" com el DTD declarant tots els elements anteriorment esmentats com #PCDATA pels mateixos motius que en "fantasma"
