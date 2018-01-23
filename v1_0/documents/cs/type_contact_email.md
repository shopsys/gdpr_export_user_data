### type_contact_email
- Jedná se o datový typ [string](https://www.w3.org/TR/xmlschema-2/#string)
- Pro účely tohoto exportu se očekává emailová adresa v základním tvaru, tedy ve formátu '`jmeno@domena.TLD`'.
- Jméno je jméno uživatele v poštovním systému, neznamená to jeho skutečné jméno.
- Doména a TLD koncovka znamená, že doména musí být .com, .cz, ... tedy email *root@localhost* neprojde validací.
- **Pole očekává vždy jen jeden email**, není tedy možné vložit do pole více emailů pomocí oddělovačů. 
- **Pole očekává tečku jako oddělovat domény a TLD koncovky**.
