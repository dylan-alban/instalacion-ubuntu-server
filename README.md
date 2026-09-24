# instalacion-ubuntu-server

## 1.Primer paso: montar la ISO
instalar la iso del ubuntu server para instalarla en virtual box y seguir los pasos que nos da el programa (instalarla con "proced whit unattended installation" desactivado)
- nos puede salir un error como este, que intentaremos solucionar: <img width="787" height="447" alt="Captura de 2026-09-15 16-28-49" src="https://github.com/user-attachments/assets/dd6e220f-eddb-47e8-ae86-1ac918433490" />

## 2.Segundo paso: Instalar ubuntu server
una vez podamos iniciar la iso de ubuntu en la virtual box nos saldra una pantalla con tres opciones, *Try or install ubuntu server, Ubuntu server whit the HWE kernel y test memory* seleccionaremos la primera opcion

<img width="712" height="403" alt="Captura de 2026-09-17 17-43-20" src="https://github.com/user-attachments/assets/eb9a2a5f-0f7b-456b-bb91-4065b4614166" />

### Elegir idioma 
Despues elegiremos el idioma tanto del sistema operativo como del teclado, y nos saldran una configuracion de red con este nombre enp0s3 o enp0s8 y con un DHCP esto lo dejaremos en blanco y continuaremos dandole a "done";
### Configurar proxy y mirror
Tambien nos saldra una configuracion para el Proxy y otra para el "mirror", las dejaremos en blanco para configurarlas mas adelante.
### Almacenamiento
Tendremos que elegir el tamaño de almacenimiento eligiremos la opcion de usar el dico entero que normalmente sera la que ya venga seleccionada
<img width="954" height="416" alt="Captura de 2026-09-17 18-01-26" src="https://github.com/user-attachments/assets/793090f0-5ff0-4d32-a19a-c654db51c99f" />
### Configuracion del perfil
Tendremos que elegir los nombres y contraseña
<img width="955" height="436" alt="Captura de 2026-09-17 18-15-41" src="https://github.com/user-attachments/assets/a8053242-59b9-4434-80c0-7bde15a6dc5e" />
### Servidor ssh y snap
En el servidor ssh es muy importante que eligamos la opcion de "install openssh server"
### Fin
Cuando termine de instalarse el sistema operativo le daremos a reiniciar ahora y se te da error abria que cerrar la maquina apagandola y quitar el  dvd en virtual box y volveremos a iniciar la maquina y ya estara listo

## 3. Tercer paso: configurar la ip del Host-only y la interfaz
Una vez el Sistema bien instalado tendriamos que configurar el SSH fijandola con netplan en el gestor de red, esto para que no cambiemos de ip cada vez que iniciemos la maquina

### Encontrar el fichero
Haora mismo al ejecutar "ls /etc/netplan" solo saldra un unico fichero llamado ".ymal" 
<img width="277" height="21" alt="Captura de 2026-09-22 16-35-19" src="https://github.com/user-attachments/assets/1653df1a-b2b9-4fd2-8cdb-75bc2597369a" />
### Editar el fichero
Para poder editar este fichero usaremos este comando "sudo nano /etc/netplan/50-cloud-init.yaml" 
<img width="894" height="476" alt="Captura de 2026-09-22 16-19-28" src="https://github.com/user-attachments/assets/772fe4de-2e62-41e0-8c8f-10773eefed19" />
pondremos lo que pone en la captura y terminariamos.
