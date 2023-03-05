# Mikrotik-antimining
Scripts antiminería para Mikrotik

Esta instrucción creada para que ROS bloquee la minería en los navegadores de los usuarios. Ayuda a ahorrar recursos de PC u otros dispositivos y no
tensa los nervios.

Encontré un par de instrucciones, pero son para uso local, para software como Ublock, Adblock o el archivo host del sistema. yo decidí
implementarlos para todas mis redes y crear scripts e instrucciones para la implementación de Mikrotik.

La idea principal es obtener listas de otros repositorios:

https://raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/hosts.txt

https://raw.githubusercontent.com/greatis/Anti-WebMiner/master/hosts

y convertirlos a scripts ROS.
Necesitas:
- Máquina Linux con servidor WEB
- Enrutador Mikrotik (podría ser ROS en su VM)

Pasos para reproducir:
- Al principio, debe colocar ad_stop.sh en algún lugar de su servidor y otorgar permiso de ejecución.
- El segundo paso es crear un directorio, al que se podrá acceder a través de http. (Se necesita la configuración del servidor web) Podría ser un servidor en su red local o incluso su PC en funcionamiento.
- El tercer paso es agregar el script (ad_stop.sh) al programador (crontab) y verificar su oportunidad de funcionar. Simplemente ingrese a su navegador http://yourserverip/ y verá el archivo antimining_dns.rsc.
- El último paso es configurar Mikrotik y agregar scripts para descargar y aplicar antimining_dns.rsc. Además, debe configurar el programador.

