##### Spoločné návratové HTTP error kódy:
| Error kód | Popis |
| ----------- | ----------- |
| **402**| prekročený denný, alebo mesačný limit api volaní |
| **403**| neoprávnený prístup<br />*Možné dôvody*:<ul><li>nesprávna hodnota API kľúča (viď konštruktor triedy a parameter  apiKey, privateKey)</li><li>prístup k metóde, na ktorú nemáte oprávnenie</li><li>nesprávny verifikačný hash (zlý výpočet alebo chybne zadaný jeden z parametrov výpočtu)</li><li>zakázaný prístup k API</li><li>vypršanie FinStat Licencie</li></ul> |
