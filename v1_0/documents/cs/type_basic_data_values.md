### type_basic_data_values
- Jedná se podelement obsahující všechny ostatní data, které nejsou vyjmenovaná v nadřazeném elementu.
- Může být použit například pro různé poznámky, dodatky apod.
- Tento element se skládá z podelementů:

1. data_name
2. data_values

#### Element: data_name
- Jedná se o datový typ: [non-empty-string-max-150-length](non-empty-string-max-150-length.md)
- Element obsahuje identifikátor hodnot. Jako hodnota by měl být použit jednoznačný název, např: "order_user_note".
- **Povinný element**.
- Element musí být použit jen jednou.
 
#### Element: data_values
- Jedná se o datový typ [string](https://www.w3.org/TR/xmlschema-2/#string)
- Element musí být minimálně jednou použit. 
- Maximální počet opakování není stanoven, lze jej tedy použít pro export polí.
- U složitějších hodnot je doporučeno použít CDATA atribut pro obalení textu.
