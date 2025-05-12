## **Descripción**
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.
## Hints
1. Filter your packets to narrow down your search.
2. Attacks were done in timely manner.
3. Time is essential.
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Se trata de un archivo pcap, el cual podemos abrir, con wireshark.
- Después de analizar un poco el archivo nos damos cuenta de que hay segmentos de cadenas en base64.
- Ahora para unirlas tendremos que mirar los tiempos en que se envían.
- Primero iremos uniendo las partes desde el primer paquete que se envió, y así consecutivamente.
- Lo otra forma de extraer estos paquetes en ese orden, es hacer uso del siguiente comando con los siguientes opciones.
- Esto nos imprimirá la bandera.

```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Ph4nt0m 1ntrud3r]
└─$ tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r | base64 -d

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3} 
```

## **Notas adicionales**

## **Referencias**