## **Descripción**
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Hints
1. How can you be sure of the redaction?
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de un archivo pdf. 
- Al abrirlo solo nos muestra unas líneas de texto, en este caso al parecer hay algunas que están tapadas en negro.
- En este caso solo seleccionamos todo el texto en el pdf, y con ello pudimos ver sin problema aquellas cadenas en negro.

```
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.
Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.

picoCTF{C4n_Y0u_S33_m3_fully}

```

## **Notas adicionales**

## **Referencias**