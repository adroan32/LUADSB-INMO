# Respuestas — Ejercitario Unidad 03


---

## Tema 1 · Rigor y formalidad

**1. Explica con tus propias palabras la diferencia entre "rigor" y "formalidad" en el desarrollo de software. Da un ejemplo de cada uno.**

_Respuesta:_ 
Rigor: Es la aplicación sistemática, cuidadosa y disciplinada de métodos y herramientas. Implica seguir un proceso metódico y documentado, sin dejar las cosas al azar. Ejemplo: Utilizar una lista de verificación estricta (checklist) para revisar el código de otro desarrollador y asegurar que cumple con las convenciones del equipo antes de integrarlo.

Formalidad: Es el nivel más alto de rigor, donde se utilizan lenguajes matemáticos y lógicos para especificar, diseñar o verificar un sistema, permitiendo demostrar que es correcto mediante pruebas matemáticas. Ejemplo: Utilizar notación Z o cálculos matemáticos precisos para demostrar que un algoritmo de cifrado no tiene vulnerabilidades teóricas.


**2. ¿Por qué no conviene formalizar por completo todos los aspectos de un proyecto de software? Menciona un caso donde sí valga la pena hacerlo.**

_Respuesta:_ No conviene porque la formalización extrema es sumamente costosa, lenta y requiere personal altamente especializado. Para la gran mayoría del software (ej. una tienda online o un blog), el costo de la formalidad supera ampliamente los beneficios.
Caso donde sí vale la pena: En sistemas críticos para la vida o la seguridad (Life-Critical Systems), como el software de vuelo de un avión comercial, los sistemas de control de reactores nucleares o los marcapasos médicos. En estos casos, un fallo es catastrófico, por lo que demostrar matemáticamente la corrección del código justifica el costo.


---

## Tema 2 · Separación de intereses

**3. En tus propias palabras, ¿qué significa "separar intereses" en el diseño de un sistema? Da un ejemplo distinto al visto en clase.**

_Respuesta:_ Significa dividir el software en partes distintas de manera que cada parte aborde un propósito, responsabilidad o "interés" (concern) único, solapándose lo menos posible con las demás. Esto permite que los desarrolladores se concentren en resolver un problema a la vez sin que los cambios en un área rompan otra.
Ejemplo: En un reproductor de música, separar la lógica que decodifica el archivo MP3 (audio) de la lógica que dibuja la barra de progreso en la pantalla (interfaz de usuario).


**4. Para una aplicación de reservas de vuelos, identifica al menos tres "intereses" o aspectos distintos que deberían mantenerse separados, y explica brevemente por qué.**

_Respuesta:_ 
Autenticación y Seguridad: Encargada del registro, inicio de sesión y validación de sesiones de los usuarios. Por qué: Las reglas de seguridad y contraseñas deben ser independientes de cómo se buscan los vuelos.

Motor de Búsqueda de Vuelos: Encargada de consultar la base de datos de aerolíneas, filtrar por fechas y destinos, y ordenar por precio. Por qué: Es una lógica pesada de lectura de datos que puede escalar de forma distinta al resto.

Procesamiento de Pagos: Encargada de conectar con tarjetas de crédito y pasarelas de pago. Por qué: Si la empresa decide cambiar de proveedor de pagos (ej. pasar de PayPal a Stripe), no debería ser necesario alterar en absoluto el motor de búsqueda.

---

## Tema 3 · Modularidad

**5. Explica con tus propias palabras la relación entre modularidad, acoplamiento y cohesión.**

_Respuesta:_ La modularidad es la práctica de dividir el sistema en módulos más pequeños. Para que esta división sea efectiva y de calidad, se deben buscar dos objetivos: alta cohesión y bajo acoplamiento. La cohesión mide qué tan relacionadas están las tareas dentro de un mismo módulo (queremos que estén muy enfocadas en un solo propósito). El acoplamiento mide la dependencia entre distintos módulos (queremos que sean lo más independientes posible).


**6. Completa el siguiente cuadro indicando si cada situación es un ejemplo de "alto acoplamiento" o de "baja cohesión", y justifica tu respuesta.**

| Situación | ¿Acoplamiento o cohesión? | Justificación |
| --- | --- | --- |
| Un módulo de "utilidades" que mezcla validaciones, envío de emails y cálculos financieros |Baja cohesión |El módulo no tiene un propósito claro o único; agrupa tareas completamente desconectadas entre sí. |
| Dos módulos que se llaman constantemente entre sí y comparten variables globales |Alto acoplamiento |Tienen una dependencia excesiva. Un cambio en la estructura interna de uno inevitablemente romperá el otro. |
| Un módulo de "reportes" que además valida los permisos del usuario |Baja cohesión |Mezcla la lógica de autorización (seguridad) con la lógica de presentación de datos (reportes), violando el principio de responsabilidad única. |
| Un módulo de autenticación que solo se encarga de validar credenciales |Alta cohesión (y bajo acoplamiento si está bien diseñado) |Es la situación ideal. Todas las operaciones internas del módulo contribuyen a un solo objetivo bien definido: validar identidades. |

**7. ¿Por qué una interfaz bien definida entre módulos reduce el impacto de los cambios internos de cada uno?**

_Respuesta:_ Porque la interfaz actúa como un "contrato" entre módulos. Mientras el módulo respete el contrato (es decir, siga recibiendo los mismos parámetros de entrada y devolviendo el mismo tipo de salida), su código interno (el "cómo" lo hace) puede ser reescrito, optimizado o cambiado por completo sin que los demás módulos que lo utilizan se enteren o dejen de funcionar.


---

## Tema 4 · Abstracción

Relaciona cada nivel de abstracción con su descripción correspondiente (completá con el número que corresponda a cada letra).

**8. Relaciona cada nivel con su descripción:**

| Nivel | N.º de descripción |
| --- | --- |
| A. Negocio / Requisitos | 2 |
| B. Diseño / Arquitectura | 3 |
| C. Implementación / Código | 1 |

1. Instrucciones concretas, escritas en un lenguaje de programación.
2. Qué problema resuelve el sistema para el usuario, sin detalles técnicos.
3. Cómo se organizan los componentes del sistema y cómo interactúan entre sí.

**9. Da un ejemplo de una situación cotidiana (no necesariamente de software) donde se apliquen distintos niveles de abstracción.**

_Respuesta:_ 
Alto nivel: "Tengo que ir al trabajo girando el volante y pisando los pedales".

Bajo nivel (oculto por la abstracción): La bomba inyecta gasolina en los cilindros, las bujías generan una chispa que causa la combustión, y los pistones giran el cigüeñal.
El conductor no necesita entender la termodinámica del motor (bajo nivel) para poder conducir (alto nivel). La abstracción oculta la complejidad innecesaria.


---

## Tema 5 · Anticipación al cambio

**10. ¿Qué significa "anticipar el cambio" en el diseño de software? ¿Implica predecir exactamente qué va a cambiar en el futuro?**

_Respuesta:_ No, es imposible predecir exactamente qué va a cambiar. "Anticipar el cambio" significa asumir como un hecho que los requisitos, las tecnologías y las leyes van a cambiar. Por lo tanto, implica diseñar el sistema de manera flexible, encapsulando las decisiones de diseño para que, cuando ocurra el cambio, el esfuerzo y el riesgo de modificar el software sean mínimos.


**11. Para un sistema de pagos en línea, identifica una parte que probablemente cambie en el futuro y propone cómo aislarla del resto del sistema.**

_Respuesta:_ 
Parte que cambiará: La pasarela de pago externa (ej. hoy usan el Banco Nacional, mañana quieren integrar procesadores de criptomonedas).

Cómo aislarla: Usando el patrón de diseño Adapter (o inyección de dependencias). Se crea una interfaz genérica llamada ProcesadorDePago con un método procesarCobro(monto). El sistema principal solo "habla" con esa interfaz. Luego, se crean clases específicas para cada banco que implementen esa interfaz. Si hay que agregar un banco nuevo, se añade una clase nueva sin tocar el código central del sistema.


---

## Tema 6 · Generalidad

**12. ¿Cuál es el riesgo de generalizar demasiado una solución? Da un ejemplo concreto de una solución "sobre-generalizada".**

_Respuesta:_ El riesgo es crear un sistema extremadamente complejo, costoso de mantener y difícil de entender para resolver problemas que probablemente nunca ocurran ("sobre-ingeniería").
Ejemplo concreto: Para una pizzería local de barrio que solo quiere mostrar un menú y un número de teléfono en su web, el ingeniero decide crear un sistema generalizado multi-idioma, con soporte para múltiples monedas, cálculo de impuestos internacionales y un CMS complejo. Gastó semanas de trabajo y presupuesto en funcionalidades (generalidad) que la pizzería jamás utilizará.


---

## Tema 7 · Incrementalidad

**13. Explica la diferencia entre construir un sistema de forma incremental y construirlo todo de una vez ("big bang").**

_Respuesta:_ 
Big Bang: Se intentan definir todos los requisitos al principio, se codifica durante meses o años a puerta cerrada, y se lanza todo el sistema de una sola vez al final. Tiene un alto riesgo de fracaso si lo que se construyó no era lo que el usuario realmente necesitaba.

Incremental: El sistema se construye en partes pequeñas y funcionales. Se lanza una primera versión básica (pero que funciona), y luego se le van agregando módulos (incrementos) en ciclos cortos. Permite obtener retroalimentación temprana del cliente y corregir el rumbo antes de gastar todo el presupuesto.


**14. Reflexión final: de los siete principios vistos en la Unidad 3, ¿cuál te parece más difícil de aplicar en la práctica, y por qué?**

_Respuesta:_ El principio más difícil de aplicar en la práctica suele ser la Anticipación al cambio (junto con la Generalidad). La dificultad radica en encontrar el punto de equilibrio exacto: si diseñas un sistema muy rígido, los cambios futuros requerirán reescribir todo el código; pero si diseñas intentando anticipar cada posible variante futura, caes en la sobre-generalización, creando una arquitectura innecesariamente compleja y difícil de entender. Ese balance ("diseñar para el cambio sin diseñar para cosas que no necesitamos") requiere mucha experiencia técnica y madurez analítica.

