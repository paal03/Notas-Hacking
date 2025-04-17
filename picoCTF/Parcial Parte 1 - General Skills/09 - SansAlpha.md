## **Descripción**
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.
Additional details will be available after launching your challenge instance.
## Hints
1. Where can you get some letters?
## **Solución** 
Para este reto haremos lo siguiente:
- Pare este desafio busque letras que recrearan la ruta `/usr/bin/cat`que podría usarse para ejecutar el archivo.
- Inicialice una variable para indicar "comando no encontrado: `` _1=`$ 2>&1` ``". Al ejecutarlo con esto, `` `"$_1"` ``se puede ver el siguiente resultado:
- `bash: bash: $: command not found: command not found`
- Esto proporciona muchas letras con las que trabajar y podría deletrear las letras `cat`:
- `${_1:9:1} - c`  
- `${_1:1:1} - a`  
- `${_1:19:1} - t`  
- `${_1:2:1} - s`
- Con estos caracteres `/usr/bin/cat`se pudo llegar con este comando:`/?${_1:2:1}?/???/??${_1:19:1}`
- Al ejecutar `./*/*`, `./blargh/flag.txt`se puede ver dónde se encuentra la bandera. Por lo tanto, el nombre del archivo sería `./*/????.???`.
- Al ejecutar `/???/?${_1:9:1}?${_1:10:1}`ahora actuará como el comando echo. 
- `/???/?${_1:9:1}?${_1:10:1} "$(<./*/????.???)"`
- Esto genera "return 0" y luego la bandera.

```
picoCTF{7h15_mu171v3r53_15_m4dn355_145223f1}
```

## **Notas adicionales**

## **Referencias**