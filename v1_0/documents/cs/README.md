# Export uživatelských dat v1.0

## Popis bloků a značek

#### Hlavička dokumentu: 
`<?xml version="1.0" encoding="UTF-8" ?>`

Celý XML export je ve kódování UTF-8. 

#### Element: customers
- Jedná se o hlavní obalovací elemtent. Obsahuje více záznamů zákazníků, případně instancí jednoho zákazníka.

#### Element: customer
- Jedná se o podelement `customers`.
- Element obsahuje data vždy jednoho zákazníka, kterého lze jednoznačně identifikovat, například pomocí registrace. 
- Například pokud bude chtít jeden zákazník export všech svých dat na základě svého emailu novakovi@seznam.cz, může se stát, že tento email je navázán na více účtů, třeba paní Nováková a pan Novák a tedy pro každý záznam (Novák i Nováková) bude existovat právě jeden element customer
- Pokud se jedná o data od neregistovaných uživatelů, pak se očekává, že pro každý jeden záznam z objednávky bude jeden element customer. Pokud by tedy v našem přípádě Nováku udělal pan Novák dvě objednávky před registrací, pak by existovaly záznamy:
- - `<customer><customer_id>0</customer_id>...<lastname>Novák</lastname>...</customer>`
- - `<customer><customer_id>0</customer_id>...<lastname>Novák</lastname>...</customer>`
- - `<customer><customer_id>1</customer_id>...<lastname>Novák</lastname>...</customer>`
- - `<customer><customer_id>2</customer_id>...<lastname>Nováková</lastname>...</customer>`
- Element obsahuje další podelementy, přičemž nezáleží na jejich pořadí. Povinnost uvádět podelement je definována u každého elementu.

#### Element: customer_id
- Jedná se o datový typ: [unsignedInt](https://www.w3.org/TR/xmlschema-2/#unsignedInt) 
- Číslo je v rozsahu od **0** do **4294967295**, což odpovídá 32bitovému celému číslu.
- Jedná se o jednoznačný číselný identifikátor zákazníka, například pro opakovaný export/import. 
- Pokud je 0 a nebo není vyplněn, bere se jako neregistrovaný.
- Tento podelement je nepovinný.

#### Element: customer_name
- Jedná se o datový typ: [type_user_name](type_user_name.md)
- **Povinný element**.
- Element musí být použit jen jednou.

#### Element: customer_login_name
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o přihlašovací jméno, například "novak123", "novak@email.cz", ...
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_languages
- Jedná se o datový typ: [type_languages](type_languages.md)
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_addresses
- Jedná se o datový typ: [type_contact_addresses](type_contact_addresses.md)
- Obsahuje adresy uživatele rozdělené vnitřně podle typu.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_phones 
- Jedná se o datový typ: [type_contact_phones](type_contact_phones.md)
- Obsahuje všechna telefonní čísla, které uživatel zadal. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_emails
- Jedná se o datový typ: [type_contact_emails](type_contact_emails.md)
- Obsahuje všechny emailové adresy, které má uživatel vyplněné v profilu. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_emails_in_newsletter
- Jedná se o datový typ: [type_contact_emails](type_contact_emails.md)
- Obsahuje všechny emailové adresy, které jsou pro daného uživatele přihlášeny k newsletteru.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_registration
- Jedná se o datový typ: [dateTime](https://www.w3.org/TR/xmlschema-2/#dateTime)
- Obsahuje datum registrace uživatele. 
- Tento podelement je nepovinný, ovšem v rámci GDPR je doporučenný.
- Element může být použit jen jednou.

#### Element: customer_last_login
- Jedná se o datový typ: [dateTime](https://www.w3.org/TR/xmlschema-2/#dateTime)
- Obsahuje datum registrace uživatele. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_profile_images 
- Jedná se o datový typ: [type_link_images](type_link_images.md)
- Obsahuje všechny profilové obrázky, které má uživatel nahrané u svého profilu (pokud aplikace umožňuje).
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_company 
- Jedná se o datový typ: [type_company_identification](type_company_identification.md)
- Obsahuje informace o firmě, jedná-li se o firemního klienta.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_other_data 
- Jedná se o datový typ: [type_other_information](type_other_information.md)
- Obsahuje veškerá data, které souvisí s uživatelským profilem a nebylo je možné přiřadit k jiným elementům.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: customer_orders
- Jedná se o datový typ: [type_customer_orders](type_customer_orders.md)
- Obsahuje veškerá data, související s objednávkami uživatele.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.
