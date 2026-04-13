# Laboratorio-1


## Descripción del laboratorio
Este laboratorio tiene como objetivo comprender el comportamiento cinemático de un robot móvil de tracción diferencial utilizando el simulador Webots. 
Mediante el control de los actuadores (motores de las ruedas izquierda y derecha), exploramos cómo las distintas velocidades afectan el movimiento del robot, 
pasando de líneas rectas a curvas y rotaciones sobre su propio eje.

## Cómo ejecutar la simulación en Webots
1. Instalar y abrir el software **Webots**.
2. Cargar un mundo que contenga un robot diferencial compatible (como el **e-puck**).
3. Asegurarse de que los nombres de los dispositivos en el código coincidan con los del robot simulado (`'left wheel motor'` y `'right wheel motor'`).
4. Cargar los scripts de Python (.py) desarrollados en la sección de controladores del robot.
5. Reproducir la simulación utilizando los botones de control de tiempo en la interfaz de Webots.

## Resultados obtenidos
Durante el experimento, se programaron diversos comportamientos controlando la velocidad de la rueda derecha y la velocidad de la rueda izquierda. Se obtuvieron los siguientes trazados:

* **Línea Recta:** Se logró asignando velocidades iguales a ambos motores. El robot avanzó sin desviación.
* **Curva:** Se asignaron velocidades asimétricas, demostrando un giro fluido hacia el lado más lento.
* **Círculo:** Se mantuvo una relación asimétrica constante durante el tiempo suficiente para cerrar el trazado perimetral de los 360 grados.
* **Figura en 8:** Se concatenaron movimientos curvos invirtiendo temporalmente los valores de los motores. Primero un giro a la derecha, seguido de un giro a la izquierda por el doble de tiempo  y cerrando el ciclo nuevamente hacia la derecha.


¿Qué ocurre cuando ambas ruedas tienen la misma velocidad?
El robot describe un movimiento en línea recta. Al no haber diferencia de velocidad entre la rueda izquierda y la derecha, no se genera velocidad angular (giro), por lo que el robot simplemente avanza o retrocede de forma lineal sin desviarse.

¿Cómo cambia la trayectoria cuando las velocidades son diferentes?
La trayectoria deja de ser recta y se convierte en una trayectoria curva. El robot tenderá a girar hacia el lado de la rueda que se mueve a menor velocidad. Por ejemplo, si la rueda izquierda gira más rápido que la derecha, el robot trazará una curva hacia la derecha.

¿Qué ocurre cuando una rueda gira en sentido opuesto a la otra?
El robot experimentará una rotación en el lugar (o giro sobre su propio eje central). Al tener velocidades opuestas con la misma magnitud (una avanza y la otra retrocede), el desplazamiento lineal se anula, dejando únicamente una rotación en el mismo sitio.

¿Qué tipo de movimiento permite dibujar un círculo?
Se requiere un movimiento curvo constante y sostenido. Para lograrlo, debes asignar velocidades diferentes a cada rueda (ambas en el mismo sentido) y mantener esos mismos valores fijos durante el tiempo necesario para completar los 360 grados. La diferencia entre las velocidades de ambas ruedas es lo que determinará el radio del círculo trazado.
