# Anatomía de un LLM

Curso de fundamentos matemáticos y computacionales de los grandes modelos de lenguaje, en español. Parte del nivel de primer curso de ingeniería, con una Fase 0 que repasa todas las matemáticas previas (demostraciones, conjuntos y funciones, álgebra, trigonometría, cálculo, probabilidad y estadística), y llega hasta el preentrenamiento a escala, el ajuste a preferencias, los agentes y la interpretabilidad. La Fase VI aplica todo lo anterior al diseño y la construcción de optimizadores con IA para procesos industriales, logística, energía y software 3D, con casos concretos y cuadernos ejecutables.

**Campus web:** https://nava98.github.io/anatomia-de-un-llm/

## Contenido

- **Apuntes** de 37 módulos (2194 páginas): una Fase 0 de repaso con 9 módulos, 23 módulos en 5 fases y una Fase VI aplicada con 5 módulos, organizados en temas con definiciones, teoremas, demostraciones y ejercicios graduados: ★ comprensión, ★★ cálculo a mano, ★★★ demostración. Son 1874 ejercicios con solución completa paso a paso en el apéndice de cada documento; una parte está adaptada de cursos y libros universitarios, con la fuente indicada.
- **Siete exámenes de hito**, el último con el proyecto final del curso,, uno por fase, con test, problemas, proyecto de fase, solucionario y tabla de autoevaluación.
- **Resúmenes** de cada módulo (NM1): todo el texto, las definiciones, los resultados y las tablas, sin demostraciones, ejemplos ni ejercicios, con la misma numeración que los apuntes.
- **Prácticas** en cuadernos de Python (NumPy, Matplotlib y PyTorch).
- **Campus web** (carpeta `docs/`): visor de los PDF, índice de ejercicios con acceso al enunciado y a la solución, prácticas ejecutables en el navegador con Pyodide, tests con corrección automática, tarjetas de repaso y un resumen por módulo.

## Plan del curso


### Fase 0. Preliminares matemáticos (repaso previo)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 0.1 | Lógica y técnicas de demostración | 73 | 89 | [PDF](docs/pdf/010-F0-P01-apuntes-demostraciones.pdf) | [PDF](docs/pdf/011-F0-P01-resumen.pdf) · 19 p. | [LaTeX](apuntes/P01/) | — |
| 0.2 | Conjuntos, funciones y relaciones | 67 | 88 | [PDF](docs/pdf/020-F0-P02-apuntes-conjuntos-funciones.pdf) | [PDF](docs/pdf/021-F0-P02-resumen.pdf) · 17 p. | [LaTeX](apuntes/P02/) | — |
| 0.3 | Números, álgebra y sumatorios | 67 | 91 | [PDF](docs/pdf/030-F0-P03-apuntes-algebra.pdf) | [PDF](docs/pdf/031-F0-P03-resumen.pdf) · 20 p. | [LaTeX](apuntes/P03/) | — |
| 0.4 | Trigonometría y números complejos | 68 | 91 | [PDF](docs/pdf/040-F0-P04-apuntes-trigonometria-complejos.pdf) | [PDF](docs/pdf/041-F0-P04-resumen.pdf) · 19 p. | [LaTeX](apuntes/P04/) | — |
| 0.5 | Cálculo diferencial de una variable | 84 | 91 | [PDF](docs/pdf/050-F0-P05-apuntes-calculo-diferencial.pdf) | [PDF](docs/pdf/051-F0-P05-resumen.pdf) · 21 p. | [LaTeX](apuntes/P05/) | — |
| 0.6 | Cálculo integral y series | 78 | 90 | [PDF](docs/pdf/060-F0-P06-apuntes-calculo-integral.pdf) | [PDF](docs/pdf/061-F0-P06-resumen.pdf) · 23 p. | [LaTeX](apuntes/P06/) | — |
| 0.7 | Vectores y funciones de varias variables | 75 | 90 | [PDF](docs/pdf/070-F0-P07-apuntes-varias-variables.pdf) | [PDF](docs/pdf/071-F0-P07-resumen.pdf) · 21 p. | [LaTeX](apuntes/P07/) | — |
| 0.8 | Combinatoria y probabilidad | 75 | 91 | [PDF](docs/pdf/080-F0-P08-apuntes-probabilidad.pdf) | [PDF](docs/pdf/081-F0-P08-resumen.pdf) · 20 p. | [LaTeX](apuntes/P08/) | — |
| 0.9 | Estadística | 86 | 92 | [PDF](docs/pdf/090-F0-P09-apuntes-estadistica.pdf) | [PDF](docs/pdf/091-F0-P09-resumen.pdf) · 25 p. | [LaTeX](apuntes/P09/) | — |
| H0 | *Examen de hito 0* | 30 | 9 | [PDF](docs/pdf/099-F0-H0-examen.pdf) | — | [LaTeX](apuntes/H0/) | — |

### Fase I. Fundamentos matemáticos (semanas 1–8)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 1 | Modelos de lenguaje probabilísticos | 32 | 24 | [PDF](docs/pdf/110-F1-M01-apuntes-modelos-de-lenguaje.pdf) | [PDF](docs/pdf/111-F1-M01-resumen.pdf) · 15 p. | [LaTeX](apuntes/M01/) | [Cuaderno](practicas/112-F1-M01-practica.ipynb) |
| 2 | Álgebra lineal I | 43 | 32 | [PDF](docs/pdf/120-F1-M02-apuntes-algebra-lineal-1.pdf) | [PDF](docs/pdf/121-F1-M02-resumen.pdf) · 21 p. | [LaTeX](apuntes/M02/) | [Cuaderno](practicas/122-F1-M02-practica.ipynb) |
| 3 | Álgebra lineal II | 52 | 38 | [PDF](docs/pdf/130-F1-M03-apuntes-algebra-lineal-2.pdf) | [PDF](docs/pdf/131-F1-M03-resumen.pdf) · 21 p. | [LaTeX](apuntes/M03/) | [Cuaderno](practicas/132-F1-M03-practica.ipynb) |
| 4 | Cálculo para el aprendizaje automático | 50 | 35 | [PDF](docs/pdf/140-F1-M04-apuntes-calculo.pdf) | [PDF](docs/pdf/141-F1-M04-resumen.pdf) · 20 p. | [LaTeX](apuntes/M04/) | [Cuaderno](practicas/142-F1-M04-practica.ipynb) |
| 5 | Probabilidad y estadística | 44 | 31 | [PDF](docs/pdf/150-F1-M05-apuntes-probabilidad.pdf) | [PDF](docs/pdf/151-F1-M05-resumen.pdf) · 20 p. | [LaTeX](apuntes/M05/) | [Cuaderno](practicas/152-F1-M05-practica.ipynb) |
| 6 | Teoría de la información | 50 | 33 | [PDF](docs/pdf/160-F1-M06-apuntes-informacion.pdf) | [PDF](docs/pdf/161-F1-M06-resumen.pdf) · 20 p. | [LaTeX](apuntes/M06/) | [Cuaderno](practicas/162-F1-M06-practica.ipynb) |
| H1 | *Examen de hito 1* | 31 | 6 | [PDF](docs/pdf/190-F1-H1-examen.pdf) | — | [LaTeX](apuntes/H1/) | — |

### Fase II. Aprendizaje automático y redes neuronales (semanas 9–16)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 7 | Optimización | 54 | 38 | [PDF](docs/pdf/210-F2-M07-apuntes-optimizacion.pdf) | [PDF](docs/pdf/211-F2-M07-resumen.pdf) · 24 p. | [LaTeX](apuntes/M07/) | [Cuaderno](practicas/212-F2-M07-practica.ipynb) |
| 8 | Aprendizaje supervisado | 49 | 35 | [PDF](docs/pdf/220-F2-M08-apuntes-supervisado.pdf) | [PDF](docs/pdf/221-F2-M08-resumen.pdf) · 23 p. | [LaTeX](apuntes/M08/) | [Cuaderno](practicas/222-F2-M08-practica.ipynb) |
| 9 | Redes neuronales | 50 | 37 | [PDF](docs/pdf/230-F2-M09-apuntes-redes-neuronales.pdf) | [PDF](docs/pdf/231-F2-M09-resumen.pdf) · 23 p. | [LaTeX](apuntes/M09/) | [Cuaderno](practicas/232-F2-M09-practica.ipynb) |
| 10 | Diferenciación automática | 51 | 36 | [PDF](docs/pdf/240-F2-M10-apuntes-autograd.pdf) | [PDF](docs/pdf/241-F2-M10-resumen.pdf) · 21 p. | [LaTeX](apuntes/M10/) | [Cuaderno](practicas/242-F2-M10-practica.ipynb) |
| 11 | Entrenar redes profundas | 50 | 38 | [PDF](docs/pdf/250-F2-M11-apuntes-redes-profundas.pdf) | [PDF](docs/pdf/251-F2-M11-resumen.pdf) · 22 p. | [LaTeX](apuntes/M11/) | [Cuaderno](practicas/252-F2-M11-practica.ipynb) |
| H2 | *Examen de hito 2* | 30 | 6 | [PDF](docs/pdf/290-F2-H2-examen.pdf) | — | [LaTeX](apuntes/H2/) | — |

### Fase III. Secuencias y Transformer (semanas 17–22)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 12 | Representar el lenguaje | 48 | 32 | [PDF](docs/pdf/310-F3-M12-apuntes-tokenizacion.pdf) | [PDF](docs/pdf/311-F3-M12-resumen.pdf) · 22 p. | [LaTeX](apuntes/M12/) | [Cuaderno](practicas/312-F3-M12-practica.ipynb) |
| 13 | Atención | 41 | 29 | [PDF](docs/pdf/320-F3-M13-apuntes-atencion.pdf) | [PDF](docs/pdf/321-F3-M13-resumen.pdf) · 19 p. | [LaTeX](apuntes/M13/) | [Cuaderno](practicas/322-F3-M13-practica.ipynb) |
| 14 | El Transformer completo | 51 | 37 | [PDF](docs/pdf/330-F3-M14-apuntes-transformer.pdf) | [PDF](docs/pdf/331-F3-M14-resumen.pdf) · 21 p. | [LaTeX](apuntes/M14/) | [Cuaderno](practicas/332-F3-M14-practica.ipynb) |
| 15 | Construye tu GPT | 49 | 31 | [PDF](docs/pdf/340-F3-M15-apuntes-mini-gpt.pdf) | [PDF](docs/pdf/341-F3-M15-resumen.pdf) · 21 p. | [LaTeX](apuntes/M15/) | [Cuaderno](practicas/342-F3-M15-practica.ipynb) |
| H3 | *Examen de hito 3* | 31 | 6 | [PDF](docs/pdf/390-F3-H3-examen.pdf) | — | [LaTeX](apuntes/H3/) | — |

### Fase IV. Escala, sistemas y arquitecturas modernas (semanas 23–28)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 16 | Preentrenamiento a escala | 54 | 38 | [PDF](docs/pdf/410-F4-M16-apuntes-escala.pdf) | [PDF](docs/pdf/411-F4-M16-resumen.pdf) · 24 p. | [LaTeX](apuntes/M16/) | [Cuaderno](practicas/412-F4-M16-practica.ipynb) |
| 17 | Hardware y sistemas distribuidos | 53 | 36 | [PDF](docs/pdf/420-F4-M17-apuntes-hardware.pdf) | [PDF](docs/pdf/421-F4-M17-resumen.pdf) · 24 p. | [LaTeX](apuntes/M17/) | [Cuaderno](practicas/422-F4-M17-practica.ipynb) |
| 18 | Arquitecturas modernas | 57 | 40 | [PDF](docs/pdf/430-F4-M18-apuntes-arquitecturas.pdf) | [PDF](docs/pdf/431-F4-M18-resumen.pdf) · 26 p. | [LaTeX](apuntes/M18/) | [Cuaderno](practicas/432-F4-M18-practica.ipynb) |
| 19 | Inferencia y generación | 59 | 40 | [PDF](docs/pdf/440-F4-M19-apuntes-inferencia.pdf) | [PDF](docs/pdf/441-F4-M19-resumen.pdf) · 24 p. | [LaTeX](apuntes/M19/) | [Cuaderno](practicas/442-F4-M19-practica.ipynb) |
| H4 | *Examen de hito 4* | 27 | 6 | [PDF](docs/pdf/490-F4-H4-examen.pdf) | — | [LaTeX](apuntes/H4/) | — |

### Fase V. Alineamiento, RL, agentes e interpretabilidad (semanas 29–36)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 20 | Ajuste fino e instrucciones | 54 | 36 | [PDF](docs/pdf/510-F5-M20-apuntes-ajuste-fino.pdf) | [PDF](docs/pdf/511-F5-M20-resumen.pdf) · 25 p. | [LaTeX](apuntes/M20/) | [Cuaderno](practicas/512-F5-M20-practica.ipynb) |
| 21 | Aprendizaje por refuerzo y preferencias | 53 | 38 | [PDF](docs/pdf/520-F5-M21-apuntes-preferencias.pdf) | [PDF](docs/pdf/521-F5-M21-resumen.pdf) · 25 p. | [LaTeX](apuntes/M21/) | [Cuaderno](practicas/522-F5-M21-practica.ipynb) |
| 22 | Agentes, herramientas y RAG | 62 | 42 | [PDF](docs/pdf/530-F5-M22-apuntes-agentes-rag.pdf) | [PDF](docs/pdf/531-F5-M22-resumen.pdf) · 29 p. | [LaTeX](apuntes/M22/) | [Cuaderno](practicas/532-F5-M22-practica.ipynb) |
| 23 | Interpretabilidad y seguridad | 61 | 39 | [PDF](docs/pdf/540-F5-M23-apuntes-interpretabilidad.pdf) | [PDF](docs/pdf/541-F5-M23-resumen.pdf) · 29 p. | [LaTeX](apuntes/M23/) | [Cuaderno](practicas/542-F5-M23-practica.ipynb) |
| H5 | *Examen de hito 5* | 34 | 7 | [PDF](docs/pdf/590-F5-H5-examen.pdf) | — | [LaTeX](apuntes/H5/) | — |

### Fase VI. Diseño y construcción de optimizadores con IA (semanas 37–44)

| Módulo | Título | Páginas | Ejercicios | Apuntes | Resumen | Fuentes | Práctica |
|---|---|--:|--:|---|---|---|---|
| 24 | Formular y resolver problemas de optimización | 66 | 46 | [PDF](docs/pdf/610-F6-M24-apuntes-formulacion.pdf) | [PDF](docs/pdf/611-F6-M24-resumen.pdf) · 26 p. | [LaTeX](apuntes/M24/) | [Cuaderno](practicas/612-F6-M24-practica.ipynb) |
| 25 | Modelos sustitutos, diseño de experimentos y optimización bayesiana | 72 | 50 | [PDF](docs/pdf/620-F6-M25-apuntes-optimizacion-bayesiana.pdf) | [PDF](docs/pdf/621-F6-M25-resumen.pdf) · 30 p. | [LaTeX](apuntes/M25/) | [Cuaderno](practicas/622-F6-M25-practica.ipynb) |
| 26 | Control óptimo, gemelos digitales y aprendizaje por refuerzo para procesos | 70 | 48 | [PDF](docs/pdf/630-F6-M26-apuntes-control-rl.pdf) | [PDF](docs/pdf/631-F6-M26-resumen.pdf) · 32 p. | [LaTeX](apuntes/M26/) | [Cuaderno](practicas/632-F6-M26-practica.ipynb) |
| 27 | Optimización geométrica y software 3D | 70 | 53 | [PDF](docs/pdf/640-F6-M27-apuntes-geometria-3d.pdf) | [PDF](docs/pdf/641-F6-M27-resumen.pdf) · 29 p. | [LaTeX](apuntes/M27/) | [Cuaderno](practicas/642-F6-M27-practica.ipynb) |
| 28 | LLM como optimizadores y del prototipo a la producción | 76 | 49 | [PDF](docs/pdf/650-F6-M28-apuntes-llm-produccion.pdf) | [PDF](docs/pdf/651-F6-M28-resumen.pdf) · 33 p. | [LaTeX](apuntes/M28/) | [Cuaderno](practicas/652-F6-M28-practica.ipynb) |
| H6 | *Examen de hito 6* | 50 | 5 | [PDF](docs/pdf/690-F6-H6-examen.pdf) | — | [LaTeX](apuntes/H6/) | — |

## Estructura del repositorio

```
apuntes/          fuentes LaTeX: estilo-apuntes.sty, latexmkrc y una carpeta por módulo (P01–P09 de la Fase 0 y M01–M28) y por examen (H0–H6)
docs/             campus web (GitHub Pages) y PDF compilados en docs/pdf/
practicas/        cuadernos de Jupyter de cada módulo
```

## Compilar los apuntes

Se necesita XeLaTeX con TeX Live completo (o Overleaf con el compilador XeLaTeX). Desde la carpeta de un módulo:

```
cd apuntes/M13
latexmk -r ../latexmkrc M13-atencion.tex
```

Cada documento principal incluye sus temas con `\input` y usa la plantilla común `../estilo-apuntes`, con tipografía Latin Modern.

## Criterio de superación de una fase

Test de cada módulo con al menos 9 aciertos sobre 12, autoevaluación del laboratorio igual o superior al 70 % y examen de hito igual o superior al 70 %.

## Fuentes

Los apuntes son de redacción propia. Siguen la estructura y la notación de cursos y libros de referencia (MIT, Stanford, Berkeley, CMU, Cambridge; Strang, Bishop, Goodfellow–Bengio–Courville, Jurafsky–Martin, Cover–Thomas, Sutton–Barto, entre otros) y de los artículos originales de cada método, citados en la bibliografía de cada módulo. Los ejercicios adaptados indican su procedencia. Sobre modelos comerciales (Claude, Gemini, Grok) solo se usa información pública.
