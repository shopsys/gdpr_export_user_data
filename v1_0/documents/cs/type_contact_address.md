### type_contact_address
- Jedná se o seznam elementů pro adresy různých typů.
- Pořadí subelementů je libovolné.

#### Element: company
- Jedná se o datový typ: [type_company_identification](type_company_identification.md)
- Tento podelement obsahuje další elementy s údaji o firmě.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: contact_name 
- Jedná se o datový typ: [type_user_name](type_user_name.md)
- Tento podelement je nepovinný, lze jej využít třeba u doručovací adresy.
- Element může být použit jen jednou.

#### Element: contact_phone 
- Jedná se o datový typ: [type_phone](type_phone.md)
- Tento podelement je nepovinný, lze jej využít třeba u doručovací adresy.
- Element může být použit jen jednou.

#### Element: contact_email 
- Jedná se o datový typ: [type_contact_email](type_contact_email.md)
- Tento podelement je nepovinný, lze jej využít třeba u fakturační adresy.
- Element může být použit jen jednou.

#### Element: address_type 
- Jedná se o datový typ: [address_type](address_type.md)
- Jedná se o seznam předdefinovaných hodnot.
- **Tento podelement je povinný**.
- Element může být použit jen jednou.

#### Element: street
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o ulici i s číslem popisným a nebo číslem orientačním.
- Pokud se jedná o adresu, kde není ulice (stává se v menších obcích), tak zde se vyplní jen číslo popisné. 
- **Tento podelement je povinný**.
- Element může být použit jen jednou.

#### Element: city
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o město, obec, nebo vesnici.
- **Tento podelement je povinný**.
- Element může být použit jen jednou.

#### Element: region_or_state
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- U větších států se jedná o identifikaci území adresy (vojvodství, stát v případě federace, kraj, ... ).
- Tento podelement je nepovinný. 
- Element může být použit jen jednou.

#### Element: country_code 
- Jedná se o datový typ: [country_code](country_code.md)
- Jedná se o seznam předdefinovaných hodnot.
- **Tento podelement je povinný**.
- Element může být použit jen jednou.

#### Element: postal_code
- Jedná se o datový typ: [non-empty-string-max-10-length](non-empty-string-max-10-length.md)
- Jedná se o poštovní směrovací číslo. V různých zemích se používají různé délky a různé formáty.
- **Tento podelement je povinný**.
- Element může být použit jen jednou.
