# No Body Is An Island

**Un juego multijugador para realidad virtual que combina una aplicación móvil desarrollada en Flutter con un entorno VR en Unity.**

---

## Descripción y justificación del proyecto
*No Body Is An Island* es un juego experimental que explora la interacción social en entornos de virtuales.  

El objetivo es combatir la individualización y el aislamiento social propios de las experiencias de realidad virtual, derivados de las características de los visores, que normalmente solo permiten a una persona acceder al mundo virtual mientras los demás quedan fuera. 

En este prototipo:  
- Un jugador usa las **gafas de realidad virtual** y se encuentra inmerso en un mundo digital.  
- El otro jugador interactúa desde el exterior mediante una aplicación desarrollada en **Flutter**, que envía mensajes OSC a Unity.  

Ambos deben **comunicarse y cooperar** para superar los niveles, aportando así una nueva forma de juego colaborativo en este campo.  

La idea de fondo es que **nadie es una isla**: toda persona necesita compañía e interacción, incluso dentro de los mundos virtuales.

---

## Objetivos
1. Desarrollar una aplicación en **Flutter** que envíe mensajes OSC a Unity.  
2. Crear una **beta jugable** en Unity con plataformas controladas desde la app móvil.  

---

## Especificaciones de la aplicación (Flutter)
- **Pantallas:**  
  - Pantalla de introducción con un vídeo animado del título del juego y un botón para acceder a la pantalla principal.  
  - Pantalla principal dedicada al control de plataformas.  

- **Estética:**  
  - Fondo gris y tipografía *CascadiaCode* definida en el archivo `pubspec.yaml`.  
  - Efecto *glow* en textos y elementos visuales, implementado con el paquete [`flutter_glow`](https://pub.dev/packages/flutter_glow).  

- **Control de plataformas:**  
  - Tres plataformas (rojo, verde, azul).  
  - Cada bloque de control incluye:  
    - Nombre de la plataforma.  
    - Cuadrado de color que se desplaza visualmente según el valor de posición.  
    - Dos botones (`increase` y `decrease`) implementados con `GestureDetector` para modificar la variable de posición.  

- **Comunicación OSC:**  
  - Envío de valores al mundo VR en Unity mediante el paquete [`osc`](https://pub.dev/packages/osc).  

- **Icono:**  
  - Generado con [`flutter_launcher_icons`](https://pub.dev/packages/flutter_launcher_icons).  
  - Basado en la composición química de la **noradrenalina**, un elemento que será relevante en la narrativa del videojuego.  

---

## Especificaciones del videojuego (Unity)
- Desarrollo en **Unity con soporte VR**.  
- Recepción de mensajes OSC desde la app Flutter.  
- Mundo de prueba con **plataformas de tres colores** controladas externamente.  
- Script personalizado que sincroniza el movimiento del jugador con el de las plataformas (evitando que caiga al vacío cuando estas se mueven).  

---

## Estado y perspectivas
Este trabajo es un **prototipo inicial**, con una primera implementación jugable en Unity y una aplicación móvil funcional.  

En el futuro se plantea:  
- Desarrollar la **narrativa** completa del videojuego.  
- Ampliar la jugabilidad con más sensores del móvil.  
- Implementar control de parámetros de sintetizadores en tiempo real (a través de OSC).  
- Convertir el móvil en un **instrumento lúdico-musical** que complemente la experiencia VR.  

---

![NoBodyIsAnIsland](https://www.instagram.com/p/C38S6ttijD6/?img_index=1)
