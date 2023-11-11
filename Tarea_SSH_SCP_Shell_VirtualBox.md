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

> Comprueba que el servicio <span style="color:navajowhite">ufw</span> está activo y en funcionamiento.

> Comprueba que el servicio <span style="color:navajowhite">ssh</span> está activo y en funcionamiento.

> Recuerda usar <span style="color:navajowhite">systemctl</span>.