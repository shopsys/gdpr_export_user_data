### type_order_item_type
- Jedná se o datový typ [string](https://www.w3.org/TR/xmlschema-2/#string)
- Jedná se vždy o povinný údaj a u jedné položky objednávky může být použit jen jednou.
- Jedná se o seznam typů položek objednávky, které mohou být použity, seznam je striktně vymezen na:

1. product - item typu produkt (lednička, ...)
2. service - item typu služba (výnos do patra, prodloužená záruka, ... )
3. shipping - item typu doprava (podočka, DPD, PPL, ... )
4. payment - item určující typ platby (hotově, bankovní převod, ... )
5. discount - item pro slevu (věrnostní sleva, slevový kupon, ... )
6. other - všechny ostatní typy

Element se používá k určení druhu položky, přesný typ (název) pak patří do item_name.
