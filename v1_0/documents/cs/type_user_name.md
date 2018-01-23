### type_user_name
- Jedná se o datový typ skládájící se z několika podelemntů.
- **Podelementy musí být v definovaném pořadí!**

1. salutation
2. prefix
3. firstname
4. middlename
5. lastname
6. suffix
7. fullname

#### Element: salutation 
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o oslovení.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: prefix
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se akademické tituly, oslovení, ....
- Tento podelement je nepovinný.
- Element může být použit maximálně 20x.

#### Element: firstname
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Křesní jméno uživatele. 
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: middlename
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o prostřední jméno, pokud jich má uživatel více jsou odděleny mezerou.
- Tento podelement je nepovinný.
- Element může být použit jen jednou.

#### Element: lastname
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Jedná se o přijmení. 
- **Tento podelement je povinný**.
- Element může být použit jen jednou.

#### Element: suffix
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Suffix jsou tituly za jménem např PhDr, MBA, ... a například generační tituly st., ml., III. 
- Tento podelement je nepovinný.
- Element může být použit maximálně 20x.

#### Element: fullname
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Mělo by se jednat o sloučeninu předchozích elementů prefix, firstname, lastname, suffix v pořadí dle regionálního tvaru.
- **Tento podelement je povinný**.
- Element může být použit jen jednou.
