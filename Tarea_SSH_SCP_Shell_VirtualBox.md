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

9. Seleccionamos el desplegable "Conectado a" y elegimos "Red Nat".
![Click desplegable "Conectado a"](/img/Imagen_17.PNG)
![Click Red Nat](/img/Imagen_18.png)

