### type_price_vat_format
- Jedná se interně o datový typ [string](https://www.w3.org/TR/xmlschema-2/#string)
- V některých zemích může být DPH s desetinnými místy: [Wiki CZ - DPH](https://cs.wikipedia.org/wiki/Da%C5%88_z_p%C5%99idan%C3%A9_hodnoty) 

##### Je v povinném formátu:
- 1 až 2 čísel před desetinnou čárkou. 
- zaokrouhlení vždy na 2 desetinná místa. 
- jako oddělovač desetinných míst je preferovaná čárka, ale akceptuje i tečku.
- neobsahuje znak %. 

##### Příklady povolených zápisů: 

'21.00'

'21,00'

'6,40'

'4.80'
