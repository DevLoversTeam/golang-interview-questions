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
