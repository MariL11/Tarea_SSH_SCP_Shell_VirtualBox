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

10. Hacemos click en "Aceptar" y podremos ver, en la información general de la máquina virtual, la red Nat recien aplicada.
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
1. Escribimos en la consola ip a, pulsamos Enter y obtendremos la IP de Servidor.
![Servidor: Comando ip a](/img/Imagen_35.PNG)

    IP: 10.0.2.10/24    
![Servidor: Ver IP](/img/Imagen_36.PNG)


* Casa
1. Seleccionamos el icono de Menú de la barra de tareas.
![Casa: Click Menú Barra de tareas](/img/Imagen_37.PNG)

2. Pasamos el ratón por encima de "Herramientas del sistema" y hacemos click en "QTerminal".
![Casa: Click QTerminal](/img/Imagen_38.PNG)

3. Se abrirá la consola y escribimos el comando ip a para obtener la IP de Casa.
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

1. Escribimos "Símbolo del sistema" en el buscador de la barra de tareas y hacemos click sobre la aplicación.
![Escribir Símbolo del sistema en Buscador](/img/Imagen_67.png)
![Click Símbolo del sistema](/img/Imagen_68.png)

2. Escribimos el siguiente comando y le damos a "Enter":
```bash
nombre_del_usuario_servidor@127.0.0.1 -p puerto_anfitrión
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
1. Escribimos "exit" en el terminal del equipo anfitrión.
![Comando exit Equipo Anfitrión](/img/Imagen_74.PNG)
![Confirmación Desconexión Servidor](/img/Imagen_75.PNG)

> Conéctate desde el **equipo anfitrión** a **Casa**.

1. Escribimos el siguiente comando y le damos a "Enter":
```bash
nombre_del_usuario_casa@127.0.0.1 -p puerto_anfitrión
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
1. Escribimos "exit" en el terminal del equipo anfitrión.
![Comando exit Equipo Anfitrión](/img/Imagen_81.PNG)
![Confirmación Desconexión Casa](/img/Imagen_82.PNG)

#### Equipo **Casa**:
> Conéctate desde **Casa** a **Servidor**

1. Abrimos el terminal en Casa,  escribimos el siguiente comando y le damos a "Enter":
```bash
nombre_del_usuario_servidor@IP_invitado -p puerto_anfitrión
```
![Comando conexión Casa - Servidor](/img/Imagen_83.PNG)

2. Autorizadamos la conexión escribiendo "yes".
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
1. Escribimos "exit" en el terminal de Casa.
![Comando exit Casa](/img/Imagen_88.PNG)
![Confirmación Desconexión Servidor](/img/Imagen_89.PNG)

### Conexión mediante claves asimétricas.
#### Equipo **Casa**:
> Crea un par de claves con el protocolo <span style="color:navajowhite">ed25519</span> y con el nombre <span style="color:navajowhite">claves_trabajo</span>.
