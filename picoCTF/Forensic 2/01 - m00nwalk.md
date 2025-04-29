## **Descripción**
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
## Hints
1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option
## **Solución** 
Para este reto haremos lo siguiente:
- Para este reto hicimos uso de un decodificador de sstv, descargamos lo siguiente 
	- git clone https://github.com/colaclanth/sstv.git
- Esto nos ayudara a decodificar el audio .wav, dándonos la imagen.
- Este reto hace uso del método de transmisión de imágenes estáticas por radio SSTV.


```
cGljb0NURntiZWVwX2Jvb3BfaW1faW5fc3BhY2V9
picoCTF{beep_boop_im_in_space}
```

## **Notas adicionales**
La Televisión de Barrido Lento (SSTV) ==es un método para transmitir imágenes estáticas mediante ondas de radio==. En este proceso, los detalles de la imagen (píxeles y colores) se codifican como cambios en las frecuencias de audio y se transmiten como señales de radio, permitiendo que en el receptor se reconstruya la imagen original.
## **Referencias**
https://www.qsl.net/ce4uyp/QUE%20ES%20EL%20SSTV.pdf