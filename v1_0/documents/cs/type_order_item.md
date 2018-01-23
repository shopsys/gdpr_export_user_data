### type_order_item
- Jedná se o data jedné položky objednávky. 
- Na pořadí podelementů nezáleží. 

#### Element: item_type
- Jedná se o datový typ: [type_order_item_type](type_order_item_type.md)
- Určuje o jakou položku se jedná. Jestli produkt, dopravu, platbu, ....
- **Tento podelement je povinný**.
- Element musí být použit jen jednou.

#### Element: item_name
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o jméno/popis položky. Pro dopravu může být název dopravy a u produktu může být název produktu. 
- **Tento podelement je povinný**.
- Element může být použit jen jednou.

#### Element: item_variant
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Pokud se jedná o produkt s variantami, zde múže být určení konkrétní varianty. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_catalog_number
- Jedná se o datový typ: [non-empty-string-max-40-length](non-empty-string-max-40-length.md)
- Mělo by být použito pro katalogové číslo produktu, ale lze využít i například u zásilkovny pro určení odběrného místa.
- U plateb typu GoPay lze využít pro určení podtypu platby (bankovní převod, kartou online, ... )
- Kód by měl být neměnný
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_ean
- Jedná se o datový typ: [non-empty-string-max-40-length](non-empty-string-max-40-length.md)
- Jedná se o EAN produktu.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_serial_number
- Jedná se o datový typ: [non-empty-string-max-40-length](non-empty-string-max-40-length.md)
- Jedná se o seriové číslo/part number produktu.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_unit
- Jedná se o datový typ: [non-empty-string-max-15-length](non-empty-string-max-15-length.md)
- Jedná se o jednotku množství, například Ks, Balení, m2, m3, palety, ...
- **Tento podelement je povinný**.
- Element musí být použit jen jednou.

#### Element: item_quantity
- Jedná se o datový typ [decimal](https://www.w3.org/TR/xmlschema-2/#decimal)
- Jedná se o množství objednaných položek. Pokud se jedná o Ks, očekává se integer.
- Pro položky zakoupitelné jinak než v kusech (napříkad metry čtvereční, litry atd.).
- **Tento podelement je povinný**.
- Element musí být použit jen jednou.

#### Element: item_currency
- Jedná se o datový typ: [country_code](country_code.md)
- Jedná se o mezinárodní kód měny.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_unit_price_without_vat
- Jedná se o datový typ: [type_price_format](type_price_format.md)
- Jedná se o cenu za jeden kus/balení bez DPH.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_unit_price_with_vat
- Jedná se o datový typ: [type_price_format](type_price_format.md)
- Jedná se o cenu za jeden kus/balení s DPH.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_total_price_without_vat
- Jedná se o datový typ: [type_price_format](type_price_format.md)
- Jedná se o cenu za celou položku bez DPH. Tedy item_unit_price_without_vat * item_quantity. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_total_price_with_vat
- Jedná se o datový typ: [type_price_format](type_price_format.md)
- Jedná se o cenu za celou položku s DPH. Tedy item_unit_price_with_vat * item_quantity. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_price_vat
- Jedná se o datový typ: [type_price_vat_format](type_price_vat_format.md)
- Jedná se o sazbu DPH. Pokud je 21% uvádíme '21,00', '5,50'. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: item_other_data
- Jedná se o datový typ: [type_other_information](type_other_information.md)
- Obsahuje veškerá další data, které souvisí s položkou objednávky a nebylo je možné přiřadit k jiným elementům.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.