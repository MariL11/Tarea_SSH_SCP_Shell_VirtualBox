# Tarea SSH - SCP -Shell - VirtualBox

> Crea un repositorio PRIVADO en Github con la documentación de esta práctica. Redacta la práctica usando Markdown, aporta trozos de código con los comandos  <span style="color:navajowhite">shell</span> y capturas de pantalla.

## VirtualBox
> Crea una **red NAT**.
1. Abrimos la aplicación Oracle VM VirtualBox y hacemos click sobre el siguiente icono:
![Click a icono](/img/Imagen_01.PNG)

2. Seleccionamos la opción "Red" y pulsamos sobre "Redes Nat".
![Click opción Red](/img/Imagen_02.png)
![Click Redes Nat](/img/Imagen_03.PNG)

3. Le damos a "Crear" y editamos la información que queremos que tenga nuestra red Nat.
![Click opción Crear](/img/Imagen_04.PNG)
![Rellenar información red Nat](/img/Imagen_05.PNG)

4. Una vez rellenada la información, le damos al botón "Aplicar" para crear la red Nat.
![Click Aplicar](/img/Imagen_06.PNG)


> Crea dos máquinas virtuales (MV) en la red anterior:

> Recuerda asignar la interfraz de red  **red NAT** antes de iniciar las MV para realizar la instalación de los
sistemas operativos.

> * **Servidor**: con un Ubuntu server sin entorno gráfico. Usuario: <span style="color:navajowhite">sergio</span>, contraseña: <span style="color:navajowhite">sergio</span>.
> * **Casa**: con un LUbuntu con el entorno gráfico por defecto (LXQt). Usuario: <span style="color:navajowhite">carmen</span>, contraseña: <span style="color:navajowhite">carmen</span>.

> Ten en cuenta que en los siguientes apartados tendrás que ir actualizando el redireccionamiento de puertos (post forward) según los servicios a los que quieras acceder desde el **equipo anfitrión**.

> Desde cada MV muestra la configuración de las interfaces.

1. Abrimos la aplicación Oracle VM VirtualBox y seleccionamos "Nueva".
![Click opción Nueva](/img/Imagen_07.PNG)

2. Rellenamos la siguiente información para crear la máquina virutal "Servidor":
![Servidor: Panel con información a rellenar ](/img/Imagen_08.PNG)
![Servidor: Panel rellenado](/img/Imagen_09.PNG)

3. Le damos a "Siguiente" y seguimos seleccionando las opciones que deseamos para nuestra máquina virtual.

4. Para terminar la creación de la máquina virtual, saldrá el siguiente panel con las propiedades de nuestra máquina y le daremos a "Terminar":
![Servidor: Panel propiedades máquina virtual](/img/Imagen_10.PNG)

5. Aparecerá nuestra máquina virtual creada en el menú principal.
![Servidor: Máquina virtual creada](/img/Imagen_11.PNG)

6. Volvemos a realizar los pasos anteriores para crear la máquina virtual "Casa".
![Casa: Panel de información rellenado](/img/Imagen_12.PNG)
![Casa: Panel propiedades máquina virtual](/img/Imagen_13.PNG)
![Casa: Máquina virtual creada](/img/Imagen_14.PNG)

7. Pulsamos click derecho sobre una máquina virtual y seleccionamos "configuración".
![Click configuración](/img/Imagen_15.png)

8. Seleccionamos "Red".
![Click Red](/img/Imagen_16.PNG)

9. Seleccionamos el desplegable "Conectado a" y elegimos la red que creamos con anterioridad (Red Nat - RedNat_Despliegue).
![Click desplegable "Conectado a"](/img/Imagen_17.PNG)
![Click Red Nat](/img/Imagen_18.png)

10. Hacemos click en "Aceptar" y podremos ver, en la información general de la máquina virtual, la red Nat recién aplicada.
![Click Aceptar Red Nat](/img/Imagen_19.PNG)
![Casa: Información general Red](/img/Imagen_20.PNG)

11. Volvemos a repetir los pasos anteriores con la otra máquina virtual desde el número 7.
![Servidor: Información general Red](/img/Imagen_21.PNG)

12. Iniciamos las máquinas virtuales dandole al botón de "Iniciar", teniendo seleccionado antes una máquina, y comenzamos a instalar los sistemas operativos.
![Click Iniciar](/img/Imagen_22.PNG)

13. Nos saldrá la siguiente pantalla en ambas máquinas y seleccionamos "Try or Install Ubuntu Server" en Servidor y "Try or Install LUbuntu" en Casa.

* Servidor

![Seleccionar Try or Install Ubuntu Server](/img/Imagen_23.png)


* Casa

![Seleccionar Try or Install LUbuntu](/img/Imagen_24.png)

14. Vamos realizando las instalaciones con las configuraciones que deseemos, y una vez que nos aparezca insertar los datos de los usuarios y contraseñas, tendremos que poner lo siguiente:

* Servidor -> Usuario: sergio, Contraseña: sergio

![Servidor:Configuración de perfil](/img/Imagen_25.png)
![Servidor:Rellenado información perfil](/img/Imagen_26.png)


* Casa -> Usuario: carmen, Contraseña: carmen

![Casa:Configuración de perfil](/img/Imagen_27.PNG)
![Casa:Rellenado información perfil](/img/Imagen_28.PNG)

15. Seguimos avanzando con las instalaciones, y una vez finalizadas, les daremos a "Reiniciar   ahora" y a "Hecho".

* Servidor

![Servidor: Seleccionar Reiniciar ahora](/img/Imagen_29.png)

* Casa

![Casa: Seleccionar Hecho](/img/Imagen_30.PNG)

16. Las máquinas virtuales se reiniciarán y mostrarán por pantalla que iniciemos sesión.

* Servidor

![Servidor: Iniciar sesión](/img/Imagen_31.png)

* Casa

![Casa: Inicias sesión](/img/Imagen_32.PNG)

17. Introduccimos los usuarios y las contraseñas correspondientes, y entramos al servidor de Servidor y al escritorio de Casa.

* Servidor

![Servidor: Entrada servidor](/img/Imagen_33.PNG)

* Casa

![Casa: Entrada al escritorio](/img/Imagen_34.PNG)


> Usa el comando <span style="color:navajowhite">ip a</span> para ver las IP asignadas a cada MV.

* Servidor

1. Escribimos en la consola "ip a", pulsamos "Enter" y obtendremos la IP de Servidor.
![Servidor: Comando ip a](/img/Imagen_35.PNG)

    IP: 10.0.2.10/24    
![Servidor: Ver IP](/img/Imagen_36.PNG)


* Casa

1. Seleccionamos el icono de Menú de la barra de tareas.
![Casa: Click Menú Barra de tareas](/img/Imagen_37.PNG)

2. Pasamos el ratón por encima de "Herramientas del sistema" y hacemos click en "QTerminal".
![Casa: Click QTerminal](/img/Imagen_38.PNG)

3. Se abrirá la consola y escribimos el comando "ip a" para obtener la IP de Casa.
![Casa: Comando ip a](/img/Imagen_39.PNG)

    IP: 10.0.2.9/24
![Casa: Ver IP](/img/Imagen_40.PNG)


## Linux Shell
> Instala o comprueba que ya estén instalados los servicios: <span style="color:navajowhite">openssh-server</span> y <span style="color:navajowhite">ufw</span>.


1. Instalamos el openssh-server con el comando "sudo apt install openssh-server".

* Servidor

![Servidor: Instalar OpenSSH-Server](/img/Imagen_41.PNG)

* Casa

![Casa: Instalar OpenSSH-Server](/img/Imagen_42.PNG)

2. En mitad de la instalación, nos mostrarán si deseamos continuar y escribiremos "S" y "Y".

* Servidor

![Servidor: Confirmar continuidad instalación](/img/Imagen_43.PNG)

* Casa

![Casa: Confirmar continuidad instalación](/img/Imagen_44.PNG)

3. Y ya tendremos el openssh-server instalado en ambas máquinas.

* Servidor

![Servidor: Instalación terminada](/img/Imagen_45.PNG)

* Casa

![Casa: Instalación terminada](/img/Imagen_46.PNG)


4. Instalamos el ufw con el comando "sudo apt install ufw".

* Servidor

![Servidor: Instalar ufw](/img/Imagen_47.PNG) 

* Casa

![Casa: Instalar ufw](/img/Imagen_48.PNG) 

5. En esta ocasión, se nos muestran en ambas máquinas virtuales que el ufw ya está instalado. En caso contrario, debemos de confirmar la continuidad de la instalación como lo hicimos con el openssh-server y obtenemos el ufw instalado.

* Servidor

![Servidor: ufw instalado](/img/Imagen_49.PNG) 

* Casa

![Casa: ufw instalado](/img/Imagen_50.PNG) 


> Comprueba que el servicio <span style="color:navajowhite">ufw</span> está activo y en funcionamiento.

> Comprueba que el servicio <span style="color:navajowhite">ssh</span> está activo y en funcionamiento.

> Recuerda usar <span style="color:navajowhite">systemctl</span>.

1. Comprobamos que el servicio ufw está activo a través del comando "sudo systemctl status ufw".

* Servidor

![Servidor: comprobar estado ufw](/img/Imagen_51.PNG) 

* Casa

![Casa: comprobar estado ufw](/img/Imagen_52.PNG) 

2. Vemos el ufw activo en ambas máquinas.

* Servidor

![Servidor: ufw activo](/img/Imagen_53.PNG) 

* Casa

![Casa: ufw activo](/img/Imagen_54.PNG) 

3. Comprobamos que el servicio ssh está activo a través del comando "sudo systemctl status ssh".

* Servidor

![Servidor: comprobar estado ssh](/img/Imagen_55.PNG) 

* Casa

![Casa: comprobar estado ssh](/img/Imagen_56.PNG) 

4. Vemos el ssh activo en ambas máquinas.

* Servidor

![Servidor: ssh activo](/img/Imagen_57.PNG) 

* Casa

![Casa: ssh activo](/img/Imagen_58.PNG) 


> Añade la regla en el cortafuegos para <span style="color:navajowhite">ssh</span>.

1. Añadimos la regla en el cortafuegos a través del comando "sudo ufw allow OpenSSH" o "sudo ufw allow ssh".

* Servidor

![Servidor: comando añadir regla cortafuegos](/img/Imagen_59.PNG) 
![Servidor: regla cortafuegos añadida](/img/Imagen_60.PNG)

* Casa

![Casa: comando añadir regla cortafuegos](/img/Imagen_61.PNG) 
![Casa: regla cortafuegos añadida](/img/Imagen_62.PNG)

> Añade en VirtualBox el redireccionamiento de puertos para poder acceder desde el **equipo anfitrión** a **Servidor** y **Casa** con el servicio <span style="color:navajowhite">ssh</span>.

1. Abrimos la aplicación Oracle VM VirtualBox y hacemos click sobre el siguiente icono:
![Click a icono](/img/Imagen_01.PNG)

2. Seleccionamos la opción "Red" y pulsamos sobre "Redes Nat".
![Click opción Red](/img/Imagen_02.png)
![Click Redes Nat](/img/Imagen_03.PNG)

3. Pulsamos sobre "Reenvío de puertos".
![Click Reenvío de puertos](/img/Imagen_63.PNG)

4. Hacemos click sobre el icono verde y añadimos dos puertos.
![Click Icono Verde](/img/Imagen_64.PNG)
![Añadir puertos](/img/Imagen_65.PNG)

5. Modificamos los puertos con las características que poseen cada máquina virtual y le damos a "Aceptar".
![Modificar puertos](/img/Imagen_65.PNG)
![Click Aceptar](/img/Imagen_66.PNG)

## SSH
### Conexión mediante usuario y contraseña

#### Equipo **Anfitrión**:

> Conéctate desde el **equipo anfitrión** a **Servidor**.

1. Escribimos "Símbolo del sistema" en el buscador de la Barra de tareas y hacemos click sobre la aplicación.
![Escribir Símbolo del sistema en Buscador](/img/Imagen_67.png)
![Click Símbolo del sistema](/img/Imagen_68.png)

2. Escribimos el siguiente comando y le damos a "Enter":
```bash
ssh nombre_del_usuario_servidor@127.0.0.1 -p puerto_anfitrión
```
![Comando conexión Servidor](/img/Imagen_69.PNG)

3. Autorizadamos la conexión escribiendo "yes".
![Autorizar conexión Servidor](/img/Imagen_70.PNG)

4. Una vez conseguida la conexión, nos saldrá en la terminal el usuario de Servidor en color verde.
![Usuario Servidor en Equipo Anfitrión](/img/Imagen_71.PNG)

> Para comprobar que estás en el servidor, crea un archivo de texto llamando <span style="color:navajowhite">servidor.txt</span>.

1. Escribimos el comando 
"touch nombre_archivo" y le damos a "Enter".
![Crear archivo servidor.txt](/img/Imagen_72.PNG)

2. Nos dirigimos a la máquina virtual Servidor y escribimos el comando "ls -la" para ver si se ha creado el archivo servidor.txt.
![Ver archivo en Servidor](/img/Imagen_73.PNG)


> Desconéctacte del servidor.
1. Escribimos "exit" en la terminal del equipo anfitrión.
![Comando exit Equipo Anfitrión](/img/Imagen_74.PNG)
![Confirmación Desconexión Servidor](/img/Imagen_75.PNG)

> Conéctate desde el **equipo anfitrión** a **Casa**.

1. Escribimos el siguiente comando y le damos a "Enter":
```bash
ssh nombre_del_usuario_casa@127.0.0.1 -p puerto_anfitrión
```
![Comando conexión Casa](/img/Imagen_76.PNG)

2. Autorizadamos la conexión escribiendo "yes".
![Autorizar conexión Casa](/img/Imagen_77.PNG)

3. Una vez conseguida la conexión, nos saldrá en la terminal el usuario de Casa en color verde.
![Usuario Casa en Equipo Anfitrión](/img/Imagen_78.PNG)

> Para comprobar que estás en el servidor, crea un archivo de texto llamado <span style="color:navajowhite">casa.txt</span>.

1. Escribimos el comando 
"touch nombre_archivo" y le damos a "Enter".
![Crear archivo casa.txt Casa](/img/Imagen_79.PNG)

2. Nos dirigimos a la máquina virtual Casa y escribimos el comando "ls -la" para ver si se ha creado el archivo casa.txt.
![Ver archivo en Casa](/img/Imagen_80.PNG)

> Desconéctate del servidor.
1. Escribimos "exit" en la terminal del equipo anfitrión.
![Comando exit Equipo Anfitrión](/img/Imagen_81.PNG)
![Confirmación Desconexión Casa](/img/Imagen_82.PNG)

#### Equipo **Casa**:
> Conéctate desde **Casa** a **Servidor**

1. Abrimos el terminal en Casa,  escribimos el siguiente comando y le damos a "Enter":
```bash
ssh nombre_del_usuario_servidor@IP_invitado -p puerto_anfitrión
```
![Comando conexión Casa - Servidor](/img/Imagen_83.PNG)

2. Autorizamos la conexión escribiendo "yes".
![Autorizar conexión Casa - Servidor](/img/Imagen_84.PNG)

3. Una vez conseguida la conexión, nos saldrá en la terminal el usuario de Servidor en color verde.
![Usuario Servidor en Casa](/img/Imagen_85.PNG)

> Para comprobar que estás en el servidor, crea un archivo de texto llamado <span style="color:navajowhite">casa.txt</span>.
1. Escribimos el comando 
"touch nombre_archivo" y le damos a "Enter".
![Crear archivo casa.txt Servidor](/img/Imagen_86.PNG)

2. Nos dirigimos a la máquina virtual Servidor y escribimos el comando "ls -la" para ver si se ha creado el archivo casa.txt.
![Ver archivo en Servidor](/img/Imagen_87.PNG)

> Desconéctate del servidor.
1. Escribimos "exit" en la terminal de Casa.
![Comando exit Casa](/img/Imagen_88.PNG)
![Confirmación Desconexión Servidor](/img/Imagen_89.PNG)

### Conexión mediante claves asimétricas.
#### Equipo **Casa**:
> Crea un par de claves con el protocolo <span style="color:navajowhite">ed25519</span> y con el nombre <span style="color:navajowhite">claves_trabajo</span>.
> Recuerda usar <span style="color:navajowhite">ssh-keygen</span>.

1. Escribimos en la terminal el comando "ssh-keygen -t ed25519".
![Comando ssh-keygen](/img/Imagen_90.PNG)

2. Escribimos el nombre "claves_trabajo" para las claves.
![Escribir nombre claves](/img/Imagen_91.PNG)

3. Nos saldrá el siguiente mensajes y le daremos a "Enter":
![Passphrases](/img/Imagen_92.PNG)

4. Obtendremos un par de claves.
![Par de claves hechas](/img/Imagen_93.PNG)
![Ver Par de claves](/img/Imagen_94.PNG)

> Exporta la clave al **Servidor**. Recuerda usar <span style="color:navajowhite">ssh-copy-id</span>.
1. Escribimos el siguiente comando en Casa y le damos a "Enter":
```bash
ssh-copy-id -p puerto_anfitrión -i claves_trabajo.pub nombre_del_usuario_servidor@IP_invitado
```
![Comando exporta clave](/img/Imagen_95.PNG)

2. Introduccimos la contraseña del usuario sergio.
![Introduccir contraseña Servidor](/img/Imagen_96.PNG)

3. Se nos mostrará por pantalla que la clave pública ha sido exportada con éxito. La clave privada nunca se deberá de compartir.
![Clave exportada](/img/Imagen_97.png)

> Conéctate desde **Casa** a **Servidor** mediante la <span style="color:navajowhite">clave claves_trabajo</span>.
1. Escribimos el siguiente comando y le damos a "Enter":
```bash
ssh -i ./nombre_clave nombre_del_usuario_servidor@IP_invitado
```
![Clave conexión Casa - Servidor](/img/Imagen_125.PNG)

2. Una vez conseguida la conexión, nos saldrá en la terminal el usuario de Servidor en color verde.
![Usuario Servidor en Casa](/img/Imagen_98.PNG)

> Para comprobar que estás en el servidor, crea un archivo de texto llamado <span style="color:navajowhite">claves.txt</span>.
1. Escribimos el comando 
"touch nombre_archivo" y le damos a "Enter".

2. Nos dirigimos a la máquina virtual Servidor y escribimos el comando "ls -la" para ver si se ha creado el archivo claves.txt.
![Ver archivo en Servidor](/img/Imagen_99.PNG)

> Desconéctate del servidor.
1. Escribimos "exit" en la terminal de Casa.
![Comando exit Casa](/img/Imagen_88.PNG)
![Confirmación Desconexión Servidor](/img/Imagen_89.PNG)

### Apache
#### Equipo **Casa**:
> Conéctacte desde **Casa** a **Servidor** mediante la clave  <span style="color:navajowhite">claves_trabajo</span>.
1. Escribimos el siguiente comando y le damos a "Enter":
```bash
ssh -i ./nombre_clave nombre_del_usuario_servidor@IP_invitado
```
![Clave conexión Casa - Servidor](/img/Imagen_125.PNG)

2. Una vez conseguida la conexión, nos saldrá en la terminal el usuario de Servidor en color verde.
![Usuario Servidor en Casa](/img/Imagen_98.PNG)

> Instala en el equipo **Servidor** el servicio <span style="color:navajowhite">apache2</span>.
1. Escribimos en la terminal el comando "sudo apt install apache2".
![Comando sudo apt install apache2](/img/Imagen_100.PNG)

2. Introducimos la contraseña del usuario sergio.
![Escribir contraseña sergio](/img/Imagen_101.PNG)

3. Autorizamos la instalación escribiendo "S".
![Autorizar instalación apache2](/img/Imagen_102.PNG)

4. Tendremos instalado el apache2.
![Instalado apache2](/img/Imagen_103.PNG)

> Comprueba que el servicio <span style="color:navajowhite">apache2</span> está activo y en funcionamiento.
1. Comprobamos que el servicio apache2 está activo a través del comando "sudo systemctl status apache2".
![Comprobar estado apache2](/img/Imagen_104.PNG) 

2. Veremos el apache2 activo.
![Apache2 activo](/img/Imagen_105.PNG) 

> Añade la regla en el cortafuegos para <span style="color:navajowhite">apache2</span>.
1. Añadimos la regla en el cortafuegos a través del comando "sudo ufw allow Apache".
![Comando añadir regla cortafuegos](/img/Imagen_106.PNG) 
![Regla cortafuegos añadida](/img/Imagen_107.PNG) 

> Añade en VirtualBox el redireccionamiento de puertos para poder acceder desde el **equipo anfitrión Servidor** con el servidor <span style="color:navajowhite">apache2</span>.
1. Abrimos la aplicación Oracle VM VirtualBox y hacemos click sobre el siguiente icono:
![Click a icono](/img/Imagen_01.PNG)

2. Seleccionamos la opción "Red" y pulsamos sobre "Redes Nat".
![Click opción Red](/img/Imagen_02.png)
![Click Redes Nat](/img/Imagen_03.PNG)

3. Pulsamos sobre "Reenvío de puertos".
![Click Reenvío de puertos](/img/Imagen_63.PNG)

4. Hacemos click sobre el icono verde y añadimos un nuevo puerto.
Modificamos el puerto con las características que posee la máquina virtual y le damos a "Aceptar".
![Click Aceptar](/img/Imagen_108.PNG)
![Puerto apache creado](/img/Imagen_109.PNG)

### SCP
#### Equipo **Casa**:
> Crea en el equipo **Casa** una página web <span style="color:navajowhite">index.html</span> como la siguiente con **tu nombre y apellidos**.

``` html
<!DOCTYPE html>
<html lang="es">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Mi primer Servidor Apache</title>
</head>
<body>
 <h1>Mi primer Servidor Apache</h1>
 <h2>NOMBRE Y APELLIDOS</h2>
 <h2>Despliegue de aplicaciones web</h2>
</body>
</html>
```

1. Escribimos el comando "nano nombre_archivo" y pulsamos "Enter".
![Comando nano index.html](/img/Imagen_110.PNG)

2. Se creará y se abrirá el archivo recién creado, y escribiremos el html con nuestro nombre y apellidos.
![Abierto archivo index.html](/img/Imagen_111.PNG)
![Escribir información html](/img/Imagen_112.PNG)

3. Guardamos el archivo con el nombre index.html y utilizamos el comando "ls -la" para ver el archivo.
![Ver archivo index.html](/img/Imagen_113.PNG)

> Copia el archivo anterior en **Servidor**, en la carpeta <span style="color:navajowhite">/var/www/html</span>.

> Recuerda usar <span style="color:navajowhite">scp</span>.

1. Copiamos el archivo y lo enviamos a Servidor a través del siguiente comando:
```bash
scp -i ./nombre_clave ./nombre_archivo nombre_del_usuario_servidor@IP_invitado:~/
```
![Copiar index.html y enviar a Servidor](/img/Imagen_114.PNG)
![Index.html enviado](/img/Imagen_115.PNG)

No podemos enviar el archivo directamente al /var/www/html debido a que no tenemos los permisos necesarios.

2. Entramos desde Casa a Servidor a través de la clave claves_trabajo.
![Entrar Servidor desde Casa](/img/Imagen_116.PNG)

3. Utilizamos el comando "sudo mv index.html /var/www/html" para mover el archivo al directorio /var/www/html, y le damos a "Enter".
![Mover index.html](/img/Imagen_117.PNG)

4. Escribimos la contraseña del usuario sergio y pulsamos "Enter".
![Escribir contraseña Servidor](/img/Imagen_118.PNG)

5. Nos dirigimos al directorio /var/www/html a través del comando "cd" y usamos "ls -la" para ver el archivo index.html.
![Comando cd y ver index.html](/img/Imagen_119.PNG)

> Desde <span style="color:navajowhite">Casa</span> abre un navegador web y prueba que puedes acceder a la web.

1. Seleccionamos el icono de Menú de la Barra de tareas.
![Click Menú Barra de tareas](/img/Imagen_37.PNG)

2. Pasamos el ratón por encima de "Internet" y hacemos click en "Navegador web Firefox".
![Click Firefox](/img/Imagen_120.PNG)

3. Escribimos IP anfitrión : Puerto anfitrión (127.0.0.1 : 8080) y le damos a "Enter".
![Dirección web](/img/Imagen_121.PNG)

4. Obtenemos la información guardada en el index.html.
![Visualización index.html](/img/Imagen_122.PNG)

#### Equipo **Anfitrión**:
> Desde el <span style="color:navajowhite">equipo</span> anfitrión abre un navegador web y prueba que puedes acceder a la web.

1. Abrimos un navegador web, escribimos la IP de Servidor (10.0.2.10) y pulsamos "Enter".
![Dirección web](/img/Imagen_123.png)

2. Obtenemos la información guardada del archivo index.html.
![Visualización index.html](/img/Imagen_124.PNG)

