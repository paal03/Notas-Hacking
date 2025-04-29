## **Descripción**
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Primero, intenté abrir este archivo con Wireshark
- Tras revisar todos los flujos UDP, no se detectó ninguna bandera. No se encontró ninguna.
- Depues de analizar un momento me di cuenta de que se encontraba lo siguiente
- Lo que me interesó de estos paquetes es que en el puerto de origen UDP ( `udp.srcport`) había `5000`lo que parecía ser algún valor ASCII.
- Exporté estos paquetes como dump.pcap, ahora se hizo uso de un script para tomar todos los puertos de origen UDP de estos paquetes, restar 5000 y decodificar ASCII:


```
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```

## **Notas adicionales**

## **Referencias**