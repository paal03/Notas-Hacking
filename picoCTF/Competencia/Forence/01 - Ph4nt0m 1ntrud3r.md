## **Descripción**
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.
## Hints
1. Filter your packets to narrow down your search.
2. Attacks were done in timely manner.
3. Time is essential
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo con wget, este se trata de un pcap, procedemos a abrirlo con wireshark y comenzamos a analizar.
- Después de ver los paquetes nos damos cuenta de que existen cadenas en formato base64
- Además de ello los filtramos en el tiempo que fueron llegando
- Extraemos las cadenas y las colocamos en un decodificador en este caso utlizamos la pagina de cyberchef.
- Con esto obtenemos la siguiente bandera
```
cGljb0NURg==
ezF0X3c0cw==
bnRfdGg0dA==
XzM0c3lfdA==
YmhfNHJfOQ==
NTlmNTBkMw==
fQ==

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}

```

## **Notas adicionales**
Podemos hacer uso de un string en la terminal para extraer todas la cadenas, aqui se mostraran las que estan en base64 y los ordenamos conforme fueron llegando.

## **Referencias**
- https://gchq.github.io/CyberChef