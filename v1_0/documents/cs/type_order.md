### type_order
- Jedná se o data jedné objednávky. 
- Na pořadí podelementů nezáleží. 

#### Element: order_id
- Jedná se o datový typ: [unsignedInt](https://www.w3.org/TR/xmlschema-2/#unsignedInt) 
- Číslo je v rozsahu od **0** do **4294967295**, což odpovídá 32bitovému celému číslu.
- Jedná se o jednoznačný číselný identifikátor objednávky, například pro opakovaný export/import. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: variable_symbol
- Jedná se o datový typ: [non-empty-string-max-10-length](non-empty-string-max-10-length.md)
- Jedná se o variabilní symbol objednávky, jeho maximální délka je 10 znaků.  
- [Wiki: Variabilní symbol](https://cs.wikipedia.org/wiki/Variabiln%C3%AD_symbol)
- **Tento podelement je povinný**.
- Element musí být použit jen jednou.

#### Element: constant_symbol
- Jedná se o datový typ: [non-empty-string-max-4-length](non-empty-string-max-4-length.md)
- Jedná se jednoznačný identifikátor typu převodu 
- [Wiki: Variabilní symbol](https://cs.wikipedia.org/wiki/Konstantn%C3%AD_symbol_%28bankovn%C3%AD_identifik%C3%A1tor%29)
- Vždy obsahuje 1 až 4 znaky. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: specific_symbol
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Tento element určuje specifický symbol objednávky.
- [Wiki: Specifický symbol](https://cs.wikipedia.org/wiki/Specifick%C3%BD_symbol)
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: order_create_date
- Jedná se o datový typ: [dateTime](https://www.w3.org/TR/xmlschema-2/#dateTime)
- Obsahuje čas založení objednávky v systému. 
- **Tento podelement je povinný**.
- Element musí být použit jen jednou.

#### Element: order_paid
- Jedná se o datový typ [boolean](https://www.w3.org/TR/xmlschema-2/#boolean)
- Jedná se o informaci zda bylo zaplaceno. 1 pro zaplaceno. 0 pro ještě nezaplaceno.
- Tento podelement je nepovinný.

#### Element: order_canceled
- Jedná se o datový typ [boolean](https://www.w3.org/TR/xmlschema-2/#boolean)
- Jedná se o informaci zda bylo stornování. 1 pro stornováno. 0 pro běžnou objednávku.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: order_addresses
- Jedná se o datový typ: [type_contact_addresses](type_contact_addresses.md)
- Obsahuje různé adresy vázané k objednávce rozdělené vnitřně podle typu.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: order_items
- Jedná se o datový typ: [type_order_items](type_order_items.md)
- Obsahuje různé položky objednávky, které jsou rozdělené vnitřně podle typu.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: order_other_data 
- Jedná se o datový typ: [type_other_information](type_other_information.md)
- Obsahuje veškerá další data, které souvisí s objednávkou a nebylo je možné přiřadit k jiným elementům.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.