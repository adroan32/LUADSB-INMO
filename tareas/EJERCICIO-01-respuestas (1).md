# Respuestas — Ejercitario Unidad 01


---

## Tema 1 · Ingeniería de software: una visión previa

**1. En tus propias palabras, define qué es la Ingeniería de Software.**

_Respuesta:_ La Ingeniería de Software es la aplicación de un enfoque sistemático, disciplinado y cuantificable al desarrollo, operación y mantenimiento del software. A diferencia de simplemente escribir código, implica utilizar principios de ingeniería, metodologías y herramientas para crear sistemas de alta calidad que cumplan con los requisitos de los usuarios, dentro de un tiempo y presupuesto definidos.


**2. Explica con un ejemplo la diferencia entre "programar" y "hacer ingeniería de software".**

_Respuesta:_ "Programar" es la acción técnica de escribir líneas de código para resolver un problema específico; por ejemplo, crear un script en Python para calcular el promedio de notas de un archivo de Excel.
"Hacer ingeniería de software" abarca todo el ciclo de vida del producto. Si se necesita un sistema de gestión académica para toda una universidad, no basta con programar: se deben realizar reuniones para levantar requisitos, diseñar la arquitectura de la base de datos, establecer protocolos de seguridad, realizar pruebas exhaustivas y crear documentación para que otros desarrolladores puedan mantener el sistema durante años.


**3. Menciona dos razones por las cuales la ingeniería de software es necesaria en el desarrollo de sistemas actuales.**

_Respuesta:_ Gestión de la complejidad: Los sistemas modernos interactúan con múltiples plataformas (web, móvil, nube) y manejan millones de datos. Sin un enfoque de ingeniería, el código se vuelve inmanejable y propenso a fallas catastróficas.

Escalabilidad y trabajo en equipo: Los proyectos hoy no los hace una sola persona. Se necesitan metodologías estandarizadas para que decenas de desarrolladores puedan colaborar simultáneamente en el mismo proyecto sin "romper" el trabajo del otro.


---

## Tema 2 · El rol de la IS en el diseño de sistemas (+ impacto de la IA)

**4. Enumera los elementos que conforman un sistema basado en computadora, además del software.**

_Respuesta:_
Hardware: Servidores, computadoras personales, sensores, etc.

Personas: Usuarios finales, administradores, soporte técnico.

Bases de Datos: La información y las estructuras donde se almacena.

Documentación: Manuales de usuario y documentación técnica del código.

Redes/Comunicaciones: La infraestructura que permite que los dispositivos se conecten.


**5. Describe brevemente la diferencia entre una visión sistémica y una visión aislada del software en el diseño de sistemas.**

_Respuesta:_ Una visión aislada considera al software como un fin en sí mismo; el enfoque está únicamente en que el programa compile y se ejecute sin errores. Una visión sistémica comprende que el software es solo un engranaje dentro de un ecosistema mucho mayor; debe interactuar fluidamente con el hardware, la topología de la red y, lo más importante, debe encajar en los procesos humanos y aportar valor real al negocio de los usuarios.


**6. Elige una herramienta de inteligencia artificial aplicada al desarrollo de software (por ejemplo, un asistente de código o de testing) e indica:**
- Qué tarea del ingeniero de software apoya o transforma.
- Un beneficio concreto que ofrece.
- Un riesgo o desafío que introduce su uso.

_Respuesta:_ Tarea que apoya: La fase de construcción (codificación). Sugiere autocompletado de funciones enteras, genera pruebas unitarias o documenta código existente.

Beneficio concreto: Aumenta exponencialmente la productividad del desarrollador al automatizar la escritura de código rutinario y estructurado ("boilerplate").

Riesgo o desafío: Puede introducir código con vulnerabilidades de seguridad sutiles o "alucinaciones". Existe el riesgo de que el ingeniero confíe ciegamente en la herramienta sin realizar una revisión crítica de la lógica insertada.


---

## Tema 3 · Historia de la ingeniería de software

**7. En tu opinión, ¿por qué la "crisis del software" de 1968 marcó un punto de inflexión para la disciplina?**

_Respuesta:_ Marcó un antes y un después porque la industria reconoció oficialmente que los métodos "artesanales" e improvisados de programación ya no escalaban frente a las nuevas capacidades del hardware. Los proyectos excedían sistemáticamente los presupuestos, se entregaban con años de retraso y fallaban en producción. Esto obligó a adoptar el rigor de la ingeniería tradicional para ganar previsibilidad, control y calidad.

**Ejercicio de relación** (completá con la letra que corresponda a cada número):

| Evento / Período | Descripción |
|---|---|
| A. Programación artesanal (1950s–60s) | 3 |
| B. Crisis del software (1968) | 1 |
| C. Modelo en cascada (1970s–80s) | 5 |
| D. Métodos iterativos (1990s) | 4 |
| E. Metodologías ágiles (2001–hoy) | 2 |

1. Se acuña el término "ingeniería de software" en una conferencia de la OTAN ante fallas y sobrecostos de proyectos.
2. Surge el Manifiesto Ágil; se popularizan Scrum, Kanban y XP.
3. El software se escribía de forma individual, sin procesos formales.
4. Ganan terreno la iteración, el prototipado y los modelos incrementales.
5. Se establecen los primeros procesos formales y estructurados de desarrollo.

---

## Tema 4 · El rol del ingeniero de software

**8. Menciona tres competencias que debe tener un ingeniero de software, además del conocimiento técnico.**

_Respuesta:_ 
Comunicación asertiva: Para negociar requisitos con clientes no técnicos y coordinar tareas con el equipo.

Pensamiento analítico y resolución de problemas: Capacidad de abstraer un problema del mundo real y dividirlo en componentes lógicos.

Adaptabilidad y aprendizaje continuo: La industria del software evoluciona rápidamente, obligando a aprender nuevos paradigmas, lenguajes y frameworks constantemente.


**9. Describe brevemente qué hace cada uno de los siguientes roles dentro de un equipo de desarrollo:**

| Rol | Descripción |
|---|---|
| Analista |Es el puente entre el cliente y el equipo. Identifica, recopila y documenta los requisitos del negocio para traducirlos en especificaciones funcionales que los programadores puedan entender. |
| Arquitecto |Diseña la estructura global del software. Toma decisiones de alto nivel sobre lenguajes, bases de datos, patrones de diseño y asegura que el sistema sea escalable y seguro. |
| Desarrollador |Se encarga de la construcción del software. Escribe, compila y depura el código fuente basándose en la arquitectura y los requisitos definidos. |
| Tester / QA |Diseña y ejecuta planes de prueba (manuales o automatizados) para encontrar defectos ("bugs") y asegurar que el producto cumple con los estándares de calidad antes del lanzamiento. |

**10. Caso breve:** Un ingeniero de software descubre, cerca de la fecha de entrega, una falla de seguridad que podría exponer datos de usuarios, pero corregirla retrasaría el proyecto una semana. ¿Qué debería hacer y por qué, considerando la ética profesional?

_Respuesta:_ El ingeniero debe reportar la falla inmediatamente a sus superiores y abogar por retrasar la entrega para aplicar la corrección. Por principios de ética profesional, el bienestar público y la protección de los datos de los usuarios tienen prioridad absoluta sobre los intereses comerciales o los plazos de entrega. Lanzar un sistema a sabiendas de que es vulnerable es una negligencia grave que no solo rompe la confianza del cliente, sino que puede acarrear severas repercusiones legales y daños de reputación irreparables para la empresa.


---

## Tema 5 · El ciclo del software

**11. Ordena y nombra las cinco fases genéricas del ciclo de vida del software vistas en clase.**

_Respuesta:_ 
Comunicación / Análisis de Requisitos: Entender qué necesita el cliente.

Diseño: Modelar la arquitectura, la base de datos y la interfaz.

Construcción (Implementación/Codificación): Escribir el código.

Pruebas (Testing): Verificar y validar que el software funcione sin errores.

Despliegue y Mantenimiento: Lanzamiento a producción y soporte continuo


**12. ¿Por qué se afirma que el mantenimiento suele ser la fase más costosa del ciclo de vida del software? Da un ejemplo hipotético.**

_Respuesta:_ Porque el software exitoso tiene una vida útil larga. Mientras el desarrollo original puede tomar 6 meses, el software puede operar durante 10 años. Durante ese tiempo, se debe invertir recursos en corregir errores tardíos, adaptar el programa a nuevos sistemas operativos y desarrollar nuevas funcionalidades.
Ejemplo: Un sistema de facturación. El desarrollo inicial se paga una vez, pero si a los 3 años cambia la ley tributaria del país (nuevos porcentajes de IVA), se debe analizar, reescribir código, volver a probar y redesplegar el sistema, incurriendo en altos costos sostenidos en el tiempo.


---

## Tema 6 · Relación con otras áreas de la ciencia de la computación

**Completen el siguiente cuadro indicando cómo cada área apoya a la ingeniería de software.**

| Área | ¿Cómo apoya a la Ingeniería de Software? |
|---|---|
| Estructuras de datos y algoritmos |Proporcionan las bases lógico-matemáticas para escribir rutinas eficientes y optimizadas, vitales cuando el software debe procesar grandes volúmenes de datos con rapidez. |
| Bases de datos |Ofrecen los modelos y lenguajes (ej. SQL) para diseñar esquemas seguros que garanticen la persistencia, integridad y recuperación veloz de la información crítica del negocio. |
| Sistemas operativos |Permiten al ingeniero comprender cómo interactúa su software con el hardware subyacente (gestión de memoria, hilos de ejecución), lo cual es crucial para diseñar aplicaciones concurrentes y estables. |
| Redes |Son esenciales para el diseño de arquitecturas modernas (cliente-servidor, microservicios). Entender protocolos y topologías permite desarrollar software que comunique datos de forma íntegra y segura a través de internet o intranets. |

---

## Tema 7 · Relación con otras disciplinas

**13. Elige dos de las siguientes disciplinas — Administración, Psicología, Economía, Derecho, Comunicación — y explica con un ejemplo concreto cómo se relacionan con el trabajo diario de un ingeniero de software.**

_Respuesta:_ 
Derecho: Un ingeniero se topa con el marco legal constantemente. Al integrar librerías de terceros, debe conocer sobre licencias de propiedad intelectual (Open Source vs Comercial) y, al diseñar bases de datos, debe garantizar el cumplimiento de las leyes de privacidad y protección de datos personales de su país.

Administración: El desarrollo de software es un negocio. La administración aporta técnicas para la gestión de proyectos (cronogramas, presupuestos, metodologías ágiles), ayudando al ingeniero a estimar los costos de su tiempo de desarrollo y asegurar que el producto sea económicamente viable.


**14. Reflexión final:** de todo lo visto en clase (definición, historia, rol del ingeniero, ciclo del software, relación con otras áreas y disciplinas, e impacto de la IA), ¿qué idea te resultó más relevante y por qué?

_Respuesta:_ La idea más relevante es comprender que el código por sí solo no resuelve problemas. La visión sistémica es transformadora: de nada sirve escribir el algoritmo más elegante del mundo si el sistema resuelve el problema equivocado o si los usuarios no pueden entender la interfaz. La ingeniería de software requiere madurez técnica, pero fundamentalmente exige empatía, ética profesional y rigor metodológico para construir soluciones que soporten el paso del tiempo y protejan a las personas que confían en ellas.

