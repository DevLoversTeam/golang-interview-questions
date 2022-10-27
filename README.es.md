**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

<h1>
  Go <img src="./assets/go.svg" width="40" height="40" />
</h1>

<h2>Most Popular Go Interview Questions and Answers</h2>


<details>
<summary>1. ¿Qué es Go y para qué tareas fue creado?</summary>

#### Go

Go (o Golang) es un lenguaje de programación compilado de tipo estático creado
en Google por Robert Griesemer, Rob Pike y Ken Thompson. Está diseñado poniendo
énfasis en la simplicidad, la previsibilidad, la compilación rápida y el alto
rendimiento en los sistemas de producción.

#### Para qué tareas se creó Go:

1. **Sistemas de red y servidor:** Servicios HTTP/API, proxies, puertas de
   enlace, backend para aplicaciones de alta carga.

2. **Infraestructura en la nube:** herramientas de orquestación, CI/CD,
   observabilidad, utilidades DevOps (razón por la cual muchos proyectos nativos
   de la nube se escriben en Go).

3. **Computación concurrente:** tareas donde el procesamiento de datos en
   paralelo, el control de latencia y el uso eficiente de los recursos son
   importantes.

4. **Programación del sistema a nivel de aplicación:** herramientas CLI,
   demonios, trabajadores en segundo plano, servicios de integración.

#### Por qué Go:

- Sintaxis concisa y baja complejidad cognitiva del código.

- Modelo de concurrencia incorporado (`goroutine`, `channel`).

- Compilación rápida y ciclo de desarrollo sencillo.

- Conjunto de herramientas estándar conveniente (`go test`, `go vet`, `pprof`,
  módulos).

Por lo tanto, Go se creó como un lenguaje de ingeniería práctico para servicios
escalables, mantenibles y de alto rendimiento donde la confiabilidad, la
velocidad de desarrollo y la simplicidad operativa son importantes.

</details>


<details>
<summary>2. ¿Cuáles son los principales principios de diseño del lenguaje Go?</summary>

#### Go

El diseño de Go no se basa en la máxima "expresividad" a cualquier costo, sino
en la viabilidad de la ingeniería: el código debe ser fácil de leer, fácil de
mantener y confiable durante el largo ciclo de vida del sistema.

#### Principios básicos del diseño de Go:

1. **Simplicidad sobre complejidad:** El lenguaje evita deliberadamente
   construcciones demasiado complejas para reducir la cantidad de errores y el
   umbral de entrada al código base.

2. **Legibilidad y falta de ambigüedad:** Se prefiere un código claro que
   cualquier ingeniero del equipo, no solo el autor, pueda entender rápidamente.

3. **Compilación rápida y desarrollo productivo:** El ciclo "escrito →
   construido → probado" debe ser corto, lo que acelera las iteraciones en
   proyectos reales.

4. **Simultaneidad incorporada:** `goroutine` y `channel` son una parte orgánica
   del lenguaje, no un parche externo, por lo que la computación paralela es
   compatible de forma nativa.

5. **Composición sobre jerarquía pesada:** Go favorece el enfoque de "componer
   el comportamiento a partir de partes simples" en lugar de construir cadenas
   de herencia profundas.

6. **Minimalismo en características, maximización en practicidad:** menos
   "magia", comportamiento más predecible durante la ejecución y depuración.

7. **Estándar de herramientas único:** `go fmt`, `go test`, `go mod`, `go vet`
   forman una cultura de desarrollo común sin fragmentación de herramientas.

#### Generalización:

Go está diseñado como un lenguaje para el desarrollo de equipos y la
programación industrial: disciplina el estilo, fomenta la claridad de
pensamiento en el código y proporciona un buen equilibrio entre simplicidad y
eficiencia.

</details>


<details>
<summary>3. ¿Cuáles son las características clave de Go en comparación con otros idiomas?</summary>

#### Go

Go se destaca porque combina una sintaxis concisa con un modelo de ejecución de
ingeniería muy práctico: el lenguaje no sobrecarga al desarrollador con una
complejidad innecesaria, pero proporciona herramientas para construir sistemas
rápidos y confiables.

#### Características clave de Go:

1. **Sintaxis simple y estricta:** el código es fácil de leer y la uniformidad
   estilística se mantiene automáticamente a través de `go fmt`.

2. **Compilar en un binario nativo:** una aplicación generalmente se compila en
   un único ejecutable sin grandes dependencias externas al inicio.

3. **Tipo estático con alta previsibilidad:** se detecta una gran cantidad de
   errores en la etapa de compilación, lo que aumenta la confiabilidad en la
   producción.

4. **Simultaneidad incorporada:** `goroutine` y `channel` hacen de la
   programación paralela un mecanismo natural en lugar de auxiliar.

5. **Ciclo de desarrollo rápido:** la compilación relativamente rápida y las
   herramientas estándar aceleran las pruebas y la entrega de cambios.

6. **Biblioteca estándar sólida:** redes, HTTP, criptografía, manipulación de
   archivos, creación de perfiles y pruebas disponibles listas para usar.

7. **Modelo de error explícito:** En Go, los errores se manejan explícitamente a
   través de `error`, lo que hace que el control de estado sea transparente y
   controlable.

8. **GC y memoria administrada:** El lenguaje simplifica el desarrollo backend
   del sistema sin obligarlo a administrar manualmente el ciclo de vida de la
   mayoría de los objetos.

9. **Un enfoque modular práctico:** `go mod` estandariza la gestión de
   dependencias y crea reproducibilidad.

#### Conclusión:

A diferencia de muchos lenguajes que gravitan hacia la máxima abstracción o la
controlabilidad de bajo nivel, Go mantiene intencionadamente un equilibrio de
ingeniería: simplicidad, rendimiento, escalabilidad y conveniencia para el
desarrollo en equipo.

</details>


<details>
<summary>4. ¿Cuál es la diferencia entre el paradigma de programación imperativo y declarativo? Dar ejemplos de idiomas.</summary>

#### Go

Los paradigmas imperativo y declarativo difieren principalmente en el enfoque de
la descripción: el primero explica **cómo** realizar la tarea paso a paso, el
segundo — **qué exactamente** se debe obtener como resultado.

#### Paradigma imperativo:

1. **Esencia:** El programador especifica explícitamente la secuencia de
   instrucciones, transiciones de estado, bucles, bifurcaciones y orden de
   ejecución.

2. **Enfoque:** control de algoritmos y control de flujo de ejecución.

3. **Rasgos típicos:** variables, asignaciones, `for`, `if`, mutación de datos.

4. **Ejemplos de lenguajes:** Go, C, C++, Rust (en la mayoría de las prácticas),
   Java.

#### Paradigma declarativo:

1. **Esencia:** describe el resultado deseado o las propiedades del sistema sin
   detallar los pasos de implementación.

2. **Enfoque:** modelo de datos, reglas y restricciones, no mecánica
   algorítmica.

3. **Características típicas:** expresiones de nivel superior, minimización de
   mutaciones explícitas, abstracción del orden de ejecución.

4. **Ejemplos de lenguajes/enfoques:** SQL, HCL (Terraform), HTML/CSS, estilos
   funcionales en Haskell y parcialmente en Elixir.

#### Conclusión práctica:

- En sistemas reales, los paradigmas a menudo se combinan.

- Go es principalmente de naturaleza imperativa, pero algunos elementos de
  declaratividad aparecen en configuraciones, descripciones de esquemas, DSL y
  consultas de datos.

- Para la entrevista, es importante enfatizar que la elección del paradigma no
  es una cuestión de "mejor o peor", sino de hacer coincidir la tarea, el equipo
  y los requisitos de soporte del código.

</details>


<details>
<summary>5. ¿Por qué Go es bueno para escribir servicios nativos en la nube?</summary>

#### Go

No es casualidad que Go sea considerado uno de los lenguajes más naturales para
Cloud Native: sus propiedades arquitectónicas coinciden bien con los requisitos
de los sistemas distribuidos modernos: escalabilidad, observabilidad,
confiabilidad y simplicidad operativa.

#### Por qué Go es eficaz en un entorno nativo de la nube:

1. **Computación concurrente liviana:** `goroutine` y `channel` simplifican la
   construcción de servicios que manejan una gran cantidad de solicitudes
   simultáneamente.

2. **Alto rendimiento y tiempo de ejecución predecible:** El compilador Go y el
   programador optimizado funcionan bien en escenarios de red ocupada.

3. **Inicio e implementación rápidos:** normalmente el resultado de una
   compilación es un binario único que es fácil de contener e implementar en
   Kubernetes u otros orquestadores.

4. **Baja sobrecarga operativa:** Imágenes de Docker simples, compilación
   rápida, menos problemas de dependencia de inicio.

5. **Potente biblioteca estándar:** `net/http`, `context`, `crypto`, `encoding`
   y otros paquetes le permiten crear soluciones de producción sin una
   dependencia excesiva de marcos de terceros.

6. **Conveniencia para los profesionales de la observabilidad:** En Go, es fácil
   integrar métricas, seguimiento y creación de perfiles, lo cual es fundamental
   para la explotación de la nube.

7. **Ecosistema resistente de herramientas de infraestructura:** Gran parte de
   la pila nativa de la nube está escrita específicamente en Go (por ejemplo,
   Kubernetes, Prometheus, Helm, Terraform), lo que simplifica las integraciones
   y el contexto de comando.

8. **Claridad de código en el desarrollo de equipos:** Go fomenta soluciones
   sencillas, lo que reduce la carga cognitiva que supone admitir una
   arquitectura de microservicios.

#### Resumen:

Go es muy adecuado para los servicios Cloud Native porque combina previsibilidad
de ingeniería con rendimiento y conveniencia práctica: desde escribir código
hasta su implementación, monitoreo y soporte a largo plazo.

</details>


<details>
<summary>6. ¿Qué son las variables `shadowing` y cómo pueden provocar errores en la lógica empresarial?</summary>

#### Go

`Shadowing` (sombreado) es cuando se declara una nueva variable en el ámbito
interno con el mismo nombre que la externa. Como resultado, el código no
funciona con la variable "esperada", sino con su copia local por nombre.

#### Cómo ocurre con mayor frecuencia:

1. **Declaración breve `:=` en un bloque anidado:** el desarrollador espera una
   asignación y, de hecho, se crea una nueva variable.

2. **El manejo de errores (`err`) en `if`/`for`/`switch`:** local `err` eclipsa
   al externo, lo que provoca que las comprobaciones de estado posteriores
   fallen.

3. **Trabajar con estado en funciones largas:** el sombreado de variables
   intermedias dificulta la lectura y aumenta el riesgo de defectos lógicos.

#### Por qué esto es peligroso para la lógica empresarial:

1. **Verificaciones de condición falsa:** el sistema puede saltar a la rama de
   ejecución incorrecta porque se está verificando la variable "incorrecta".

2. **Estado perdido o incorrecto:** por ejemplo, el resultado del cálculo
   permaneció en el bloque local y el estado externo no se actualizó.

3. **Depuración compleja:** visualmente el nombre es el mismo, pero
   semánticamente son objetos diferentes; el error se manifiesta de forma
   discreta y a menudo sólo en casos de combate.

4. **Defectos silenciosos sin pánico:** un programa puede compilarse y
   ejecutarse, pero devolver un resultado comercial incorrecto.

#### Cómo prevenir `shadowing`:

- Distingue deliberadamente entre `=` y `:=` en todos los bloques anidados.

- Mantenga breve la visibilidad de las variables y evite funciones excesivamente
  largas.

- Utilice nombres claros y semánticamente precisos, especialmente para estados y
  errores.

- Conecte el análisis estático (`go vet`, `golangci-lint`) con reglas de
  detección de sombreado.

- En lugares críticos de la lógica, agregue pruebas para escenarios negativos y
  condiciones de contorno.

#### Conclusión:

`Shadowing` no es una peculiaridad sintáctica, sino una fuente de errores
lógicos insidiosos. En el código Go de producción, la disciplina de la
declaración de variables afecta directamente la corrección del comportamiento
comercial del sistema.

</details>
