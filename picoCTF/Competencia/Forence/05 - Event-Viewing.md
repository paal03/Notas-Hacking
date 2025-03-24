## **Descripción**
One of the employees at your company has their computer infected by malware! Turns out every time they try to switch on the computer, it shuts down right after they log in. The story given by the employee is as follows:

1. They installed software using an installer they downloaded online
2. They ran the installed software but it seemed to do nothing
3. Now every time they bootup and login to their computer, a black command prompt screen quickly opens and closes and their computer shuts down instantly.

See if you can find evidence for the each of these events and retrieve the flag (split into 3 pieces) from the correct logs!Download the Windows Log file [here](https://challenge-files.picoctf.net/c_verbal_sleep/123d9b79cadb6b44ab6ae912f25bf9cc18498e8addee851e7d349416c7ffc1e1/Windows_Logs.evtx)

## Hints
1. Try to filter the logs with the right event ID
2. What could the software have done when it was ran that causes the shutdowns every time the system starts up?
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo en una maquina windows para poderlo abrir con el visor de eventos.
- El reto nos dice que la flag esta dividida en 3 partes.
  1. Para encontrar la primera:
	 - Use la opcion de "FIND" y como argumento coloque "installer", esto lo hice asi ya que nos dice que lo primero que hiceron fue instalar el software.
	- Al hacer esta buscada la nos aparece como primera buscada el evento con ID - 1033, el revisarlo encontramos una cadena que al paracer esta en base64
	- Solo queda hacer la decodificacion y obtenemos la primera parte de la banera
2. Para la segunda parte:
	- Ahora sabemos que el evento tiene el "ID - 1033" y además encontramos en este mismo que el nombre de lo que se esta ejecutando es "Totally_Legit_Software".
	- Usamos FIND y como criterio de busqueda "Totally_Legit_Software", buscamos entre los registros devueltos y en uno de ellos se encunetra la otra parte de la bandera.
3. Para la tercera parte: 
		- Puro ultimo usaremos nuevamente FIND y esta vez usaremos el criterio de busqueda "shutdown.exe" , esto ya que el equipo se apaga depues de inciar sesion igual nos guiamos usando las pistas.

```
cGljb0NURntFdjNudF92aTN3djNyXw==
dDAwbF84MWJhM2ZlOX0=
MXNfYV9wcjN0dHlfdXMzZnVsXw==

picoCTF{Ev3nt_vi3wv3r_1s_a_pr3tty_us3ful_t00l_81ba3fe9}

```

## **Notas adicionales**

## **Referencias**
- https://gchq.github.io/CyberChef