### type_price_format
- Jedná se interně o datový typ [string](https://www.w3.org/TR/xmlschema-2/#string)

##### Je v povinném formátu:
- 1 až 14 čísel před desetinnou čárkou. 
- zaokrouhlení vždy na 8 desetinných míst. 
- oddělovač desetinných míst je preferovaná čárka, ale akceptuje i tečku.
- oddělovač tisíců se nepoužívá.
- neobsahuje žádné dodatečné informace o měně. 

##### Příklady povolených zápisů: 

'1202.00000000'

'1202.25487500'

'+1202,25487500'

'-1202.25487500'

'+125468286302.25487500'