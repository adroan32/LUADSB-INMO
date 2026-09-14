# Respuestas — Ejercitario Unidad 02

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · La naturaleza del software

**1. En tus propias palabras, explica por qué se dice que el software es un producto de "naturaleza particular" en comparación con un producto físico. Menciona al menos tres características distintivas.**

_Respuesta:_ El software difiere radicalmente de los productos físicos porque es un elemento lógico, no material. Tres características lo distinguen:

No se desgasta ni se rompe por fricción: Un puente o un motor sufren fatiga de materiales con el tiempo; el software no. Sus fallos provienen de defectos de diseño, no de deterioro físico.

Se desarrolla o se aplica ingeniería, no se fabrica: En el hardware, la fase de fabricación es la que introduce problemas de calidad y costos repetitivos. En el software, el costo principal está en el desarrollo inicial; copiarlo (fabricarlo) tiene un costo cercano a cero.

Es altamente maleable: Se espera que el software cambie constantemente (nuevos requisitos, actualizaciones) durante su vida útil, algo inviable en un producto físico ya ensamblado.


**2. ¿Por qué se afirma que la calidad del software se degrada por mal mantenimiento y no por el paso del tiempo? Da un ejemplo.**

_Respuesta:_ Porque el software en sí mismo es inmutable, pero el entorno en el que opera (sistemas operativos, bases de datos, necesidades del usuario) cambia. Cuando se realizan modificaciones para adaptar el software a estos cambios (mantenimiento), a menudo se introducen nuevos errores o se rompe la arquitectura original ("código espagueti").
Ejemplo: Un sistema de nómina funciona perfecto por 5 años. Luego, cambia la ley y se añade un nuevo impuesto parcheando el código a las apuradas. Al mes siguiente, se parchea otra regla. Tras varios parches mal diseñados, el sistema se vuelve lento, inestable y difícil de leer. El software no envejeció, su estructura se degradó por mal mantenimiento.


---

## Tema 2 · Requisitos funcionales y no funcionales

**3. Explica con tus propias palabras la diferencia entre un requisito funcional y un requisito no funcional.**

_Respuesta:_ 
Requisito funcional: Define qué debe hacer el sistema. Describe comportamientos, funciones o procesos específicos (ej. "El sistema debe calcular el IVA").

Requisito no funcional: Define cómo debe ser el sistema. Establece restricciones, estándares o atributos de calidad bajo los cuales deben operar las funciones (ej. "El cálculo del IVA debe realizarse en menos de 1 segundo").


**4. Para el siguiente caso, identifica un requisito funcional y tres requisitos no funcionales de categorías distintas: "Una aplicación de delivery de comida debe permitir a los usuarios rastrear su pedido en tiempo real."**

_Respuesta:_ 
Requisito funcional: El sistema debe capturar las coordenadas GPS del repartidor y mostrarlas actualizadas sobre un mapa en la pantalla del usuario.

Requisitos no funcionales:

Rendimiento: La posición del repartidor en el mapa debe actualizarse con una latencia máxima de 3 segundos.

Seguridad: Solo el cliente que realizó el pedido y el administrador del sistema pueden tener acceso a la ubicación del repartidor.

Usabilidad: El mapa debe integrar iconos contrastantes que permitan a los usuarios distinguir entre su casa, el restaurante y el repartidor sin necesidad de leer texto.


**5. Menciona dos razones por las cuales los requisitos no funcionales suelen entrar en conflicto entre sí. Da un ejemplo concreto de ese conflicto.**

_Respuesta:_ 
Entran en conflicto porque mejorar una cualidad suele consumir recursos (tiempo, memoria, dinero) que limitan otra.
Ejemplo: Seguridad vs. Rendimiento. Si se requiere que una base de datos encripte absolutamente toda la información con algoritmos muy complejos (alta seguridad), el tiempo que tarda el procesador en desencriptar los datos al consultarlos hará que el sistema responda más lento (bajo rendimiento).


---

## Tema 3 · Clasificación de las cualidades del software

**6. Completa el siguiente cuadro clasificando cada elemento como cualidad "de producto" o "de proceso", y justifica brevemente tu respuesta.**

| Elemento | ¿Producto o proceso? | Justificación |
| --- | --- | --- |
| Tiempo de respuesta de una aplicación móvil | PRODUCTO|Es un atributo de calidad observable en el software final mientras se ejecuta. |
| Capacidad del equipo de estimar correctamente los plazos de entrega |PROCESO |Es una cualidad de la metodología de trabajo y del equipo humano, no del código o del sistema final. |
| Facilidad de uso de una interfaz |PRODUCTO |Es una característica intrínseca del software (UI/UX) que impacta directamente al usuario. |
| Documentación interna del código fuente |PRODUCTO |Aunque no la ve el usuario final, es parte de los artefactos tangibles (producto interno) entregados por el equipo de desarrollo. |

**7. ¿Por qué se dice que una buena calidad interna favorece, pero no garantiza, una buena calidad externa? Da un ejemplo de un software con buena calidad interna pero mala calidad externa, o viceversa.**

_Respuesta:_ La calidad interna (código limpio, arquitectura modular, patrones de diseño) hace que el software sea fácil de modificar, probar y mantener. Sin embargo, no garantiza la calidad externa (lo que percibe el usuario).
Ejemplo (Buena interna / Mala externa): Un equipo desarrolla una app con un código impecable, principios SOLID y 100% de cobertura de pruebas (excelente calidad interna). Sin embargo, diseñan una interfaz tan confusa que los usuarios no saben cómo iniciar sesión, y además, la app resuelve un problema que nadie tiene. Su calidad externa (usabilidad y utilidad) es pésima, a pesar de que el código es perfecto.


---

## Tema 4 · Cualidades representativas

Relaciona cada cualidad con su definición correspondiente (completá con el número que corresponda a cada letra).

| Cualidad | N.º de definición |
| --- | --- |
| A. Corrección | 3 |
| B. Fiabilidad | 6 |
| C. Robustez | 4 |
| D. Eficiencia | 2 |
| E. Mantenibilidad | 5 |
| F. Interoperabilidad | 1 |

1. Capacidad de coexistir e intercambiar información con otros sistemas.
2. Uso adecuado de los recursos disponibles: tiempo de procesamiento, memoria, ancho de banda.
3. El software hace exactamente lo que su especificación indica, ni más ni menos.
4. Comportamiento razonable frente a situaciones no anticipadas por la especificación.
5. Facilidad para corregir errores y adaptar o mejorar el software.
6. Capacidad de funcionar sin fallar durante un período y bajo condiciones dadas.

**8. Elige dos cualidades representativas distintas a las de la actividad anterior (por ejemplo, usabilidad, portabilidad o reusabilidad) y da un ejemplo concreto —de una app, sistema o servicio real— donde esa cualidad sea especialmente crítica.**

_Respuesta:_ 
Portabilidad: Crítica en un motor gráfico como Unreal Engine. El software (juego) debe poder compilarse y ejecutarse sin grandes cambios estructurales en una PC con Windows, una PlayStation 5 o un smartphone.

Seguridad: Crítica en una pasarela de pagos como Stripe o PayPal. El sistema debe prevenir accesos no autorizados, inyecciones de código y proteger datos sensibles financieros contra vulnerabilidades.

**9. Caso breve: un equipo de desarrollo debe elegir entre optimizar la eficiencia de un sistema (tiempos de respuesta más rápidos) o su mantenibilidad (código más simple y modular), dado que el tiempo de desarrollo es limitado. ¿Qué factores debería considerar el equipo para tomar esa decisión?**

_Respuesta:_ El equipo debe evaluar el ciclo de vida esperado y la naturaleza del dominio. Si es una aplicación que requiere cálculos en tiempo real y corre en hardware limitado (ej. un dron o un dispositivo IoT), debe priorizar la eficiencia. Sin embargo, si es un sistema empresarial a largo plazo que cambiará constantemente y se ejecuta en servidores en la nube (donde el hardware es escalable y barato), debe priorizar la mantenibilidad; de lo contrario, el código complejo y poco modular los paralizará en futuras actualizaciones.


---

## Tema 5 · Calidad según el dominio de aplicación

**10. Completa el siguiente cuadro indicando qué cualidades consideras prioritarias para cada tipo de sistema, y por qué.**

| Tipo de sistema | Cualidades prioritarias | ¿Por qué? |
| --- | --- | --- |
| Sistema de control de una planta industrial |Fiabilidad, Robustez, Seguridad |Un fallo de software puede causar daños físicos a la maquinaria, detener una producción millonaria o poner en riesgo vidas humanas. No puede fallar. |
| Red social de uso masivo |Escalabilidad, Usabilidad, Rendimiento |Debe soportar picos de millones de usuarios simultáneos sin caerse, y debe ser extremadamente intuitiva para retener la atención del usuario. |
| Sistema de trading financiero de alta frecuencia |Eficiencia (Baja latencia), Corrección |Milisegundos de retraso (eficiencia) o un error de redondeo (corrección) pueden significar la pérdida de millones de dólares en la bolsa de valores. |

**11. En tu opinión, ¿es válido que un sistema de consumo masivo tolere una tasa de fallos mayor que un sistema crítico, a cambio de salir antes al mercado? Justifica tu postura.**

_Respuesta:_ Sí, en la mayoría de los casos no críticos es una estrategia de negocio válida (el modelo de Producto Mínimo Viable o MVP). En una app de consumo masivo (ej. un nuevo juego o una app de streaming), el costo de un fallo es bajo (un reinicio de la app o un usuario temporalmente frustrado). Por el contrario, el costo de oportunidad de demorar el lanzamiento puede significar que un competidor acapare el mercado. Esto jamás sería válido en sistemas críticos (aviación, medicina) donde el costo del fallo son vidas humanas.


---

## Tema 6 · Medición de la calidad del software

**12. Explica con tus propias palabras por qué se dice que una métrica es "un indicador indirecto de la cualidad, y no la cualidad en sí misma".**

_Respuesta:_ Las cualidades del software, como la "mantenibilidad" o la "usabilidad", son abstractas y subjetivas; no se pueden poner en una balanza. Para acercarnos a ellas, medimos cosas tangibles (métricas), como la "cantidad de niveles de anidamiento de un código" (complejidad ciclomática) o "el tiempo que tarda un usuario en encontrar un botón". Estas métricas son solo pistas que nos indican si vamos por buen camino, pero un código con baja complejidad no es matemáticamente garantía de que otro programador lo entienda.


**13. Menciona un riesgo concreto de que un equipo se enfoque en mejorar una métrica de calidad (por ejemplo, bajar la complejidad ciclomática) sin revisar si la cualidad real mejoró.**

_Respuesta:_ El riesgo es que el equipo comience a "engañar al sistema" para cumplir la métrica sin mejorar realmente la calidad del software. Por ejemplo, si se exige un 90% de cobertura de pruebas unitarias (métrica), los programadores podrían escribir pruebas vacías que ejecuten el código pero no verifiquen que el resultado sea correcto (sin asserts). La métrica sube al 90%, el gestor está feliz, pero la confiabilidad del sistema sigue siendo la misma o peor, habiendo desperdiciado tiempo valioso.


**14. Reflexión final: de todo lo visto en la Unidad 2 (naturaleza del software, requisitos no funcionales, clasificación de cualidades, cualidades representativas, calidad según el dominio, medición), ¿qué idea te resultó más relevante y por qué?**

_Respuesta:_ La idea más relevante de esta unidad es comprender que en ingeniería de software no existe el sistema perfecto, solo existen las concesiones ("trade-offs"). Entender las diferencias entre requerimientos funcionales y no funcionales, y cómo las cualidades como rendimiento, seguridad y mantenibilidad compiten constantemente entre sí, demuestra que el trabajo del ingeniero no es solo programar, sino tomar decisiones estratégicas e informadas para equilibrar la calidad técnica con las realidades y presupuestos del negocio.

