| Error kód | Popis |
| ----------- | ----------- |
| **400**| neplatná hodnota parametra požiadavky — konkrétne validácie sú uvedené pri parametroch danej požiadavky vyššie. Text odpovede vždy obsahuje dôvod zamietnutia. |
| **402**| v tejto skupine požiadaviek znamená **402 aj nedostatok kreditu**, nie len prekročený denný alebo mesačný limit API volaní (odpoveď ```Not enough credit```) |
| **502**| register CRE (Centrálny register exekúcií) je momentálne nedostupný alebo dopyt do neho zlyhal. **Kredit sa v tomto prípade nestrhne**, požiadavku je možné neskôr zopakovať. Týka sa požiadaviek, ktoré sa dopytujú priamo do CRE — *DistraintSearch* a *DistraintDetail*. |
