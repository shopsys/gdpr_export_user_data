### type_company_identification
- Jedná se soupis všech informací o firmě/společnosti. 
- Jednotlivé podelementy nemusí být v definovaném pořadí. 
- Každý podelement může maximálně 1x.

#### Element: company_id
- Jedná se o datový typ: [unsignedInt](https://www.w3.org/TR/xmlschema-2/#unsignedInt) 
- Číslo je v rozsahu od **0** do **4294967295**, což odpovídá 32bitovému celému číslu.
- Jedná se o jednoznačný číselný identifikátor společnosti. 
- Tento podelement je nepovinný.

#### Element: company_name
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- **Povinný element**.
- Element musí být použit jen jednou.

#### Element: company_registration_number
- Jedná se o datový typ: [non-empty-string-max-15-length](non-empty-string-max-15-length.md)
- Tento element obsahuje identifikační číslo osoby/firmy (IČO). 
- Dle nové legislativy Česka je IČ 8-mi místné. Dle staré CZ legislativy je 7-mi místné. 
- Polsko má až 14-ti místné identifikační čísla: [Wikipedie: IČO](https://cs.wikipedia.org/wiki/Identifika%C4%8Dn%C3%AD_%C4%8D%C3%ADslo_osoby)
- Tento podlement je nepovinný a může být použit maximálně 1x.

#### Element: company_vat_registration_number
- Jedná se o datový typ: [non-empty-string-max-12-length](non-empty-string-max-12-length.md)
- Tento element obsahuje daňové identifikační číslo firmy (DIČ). 
- Některé země mají až 12-ti místné čísla: [Wikipedie: DIČ](https://cs.wikipedia.org/wiki/Da%C5%88ov%C3%A9_identifika%C4%8Dn%C3%AD_%C4%8D%C3%ADslo)
- Tento podelement je nepovinný a může být použit maximálně 1x.

#### Element: company_registration_number_for_vat_payer
- Jedná se o datový typ: [non-empty-string-max-40-length](non-empty-string-max-40-length.md)
- Tento element obsahuje daňové identifikační číslo pro daň z přidané hodnoty (IČ DPH). 
- Využívá se například na Slovensku: [Wikipedie: IČ DPH](https://sk.wikipedia.org/wiki/Identifika%C4%8Dn%C3%A9_%C4%8D%C3%ADslo_pre_da%C5%88_z_pridanej_hodnoty)
- Tento podlement je nepovinný a může být použit maximálně 1x.

#### Element: company_addresses
- Jedná se o datový typ: [type_contact_addresses](type_contact_addresses.md)
- Tento podelement obsahuje veškeré kontaktní informace společnosti, včetně emailů a telefonů.
- Tento podlement je nepovinný a může být použit maximálně 1x.

#### Element: company_other_data
- Jedná se o datový typ: [type_other_information](type_other_information.md)
- Tento element obsahuje všechny další informace, které nejsou definované výše.
- Tento podlement je nepovinný a může být použit maximálně 1x.
