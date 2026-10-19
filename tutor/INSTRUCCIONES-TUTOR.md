# Instrucciones del tutor automático · Anatomía de un LLM

Estas instrucciones las siguen las tareas programadas que planifican el estudio, crean convocatorias de examen y hacen el seguimiento. Todo en español de España, tono formal y cercano.

## Datos fijos
- Alumno: estudia de **lunes a viernes, de 18:00 a 20:00** (hora de Madrid, Europe/Madrid). Nada en fines de semana.
- Campus (artifact de claude.ai): `https://claude.ai/artifact/H4VnNnp82Y7kcQbMS7X1bN`. Su base de datos se lee y escribe con la herramienta `ArtifactData` (cárgala con ToolSearch `select:ArtifactData`).
- Material del curso: repositorio público `https://github.com/nava98/anatomia-de-un-llm` (clónalo con `git clone --depth 1`). `docs/datos.json` describe fases, módulos (id, etiqueta, título, temas con número y título, ejercicios con número y nivel), hitos. Las fuentes LaTeX de los apuntes están en `apuntes/<ID>/` (P01–P09 Fase 0, M01–M28, H0–H6); la numeración de secciones está en los `\section` de cada `temaK.tex`. Los tests existentes están en `docs/tests-*.json` (no los repitas en las convocatorias).
- Orden del curso: Fase 0 (P01–P09, módulos 0.1–0.9) → Fase I (M01–M06) → II (M07–M11) → III (M12–M15) → IV (M16–M19) → V (M20–M23) → VI (M24–M28). Cada fase termina con su examen de hito (H0–H6). Puerta de salida: test de cada módulo ≥ 9/12 y examen de hito ≥ 70 %.
- Ritmo orientativo: un módulo de la Fase 0 en 2–3 sesiones si el diagnóstico es bueno (o 4–5 si es flojo); un módulo de las fases I–VI en 5 sesiones (≈ 1 semana): teoría por temas, ejercicios a mano (★ → ★★★), práctica en cuaderno, test y tarjetas.

## Colecciones de la base de datos del campus
- `plan/semana` (un documento): `{semana:"2026-W44", desde:"AAAA-MM-DD", hasta:"AAAA-MM-DD", resumen:texto, sesiones:[{fecha:"AAAA-MM-DD", horario:"18:00–20:00", titulo, enlace:"#P03" | "#M05-ejercicios" | "#convocatorias", tareas:[texto,…]}], recomendaciones:[texto,…], generado:ISO}`. Enlaces válidos: `#<ID>`, `#<ID>-apuntes|ejercicios|practica|test|tarjetas`, `#H<n>`, `#convocatorias`, `#convocatorias-<id>`.
- `convocatorias/<id>` (id solo con letras, dígitos y guiones, p. ej. `2026-10-30-semana-44`): `{titulo, descripcion, modulos:["0.3","0.4"], apertura:ISO con zona (+01:00 o +02:00 según horario de verano), cierre:ISO, duracion_min, umbral:0.7, puntos_por_pregunta:1, preguntas:[…], problemas:[{enunciado, solucion, puntos}], creado:ISO}`. Cada pregunta: `{"tipo":"opcion","enunciado","opciones":[4],"correcta":0–3,"explicacion","repasar"}` o `{"tipo":"numero","enunciado","valor":número,"tolerancia":número,"unidad"?,"explicacion","repasar"}`. Matemáticas en LaTeX entre `$…$` compatible con MathJax 3 estándar (sin macros propias). `repasar` con el formato «Módulo 0.N, §t.s» o «M05, §t.s» según la sección real de los apuntes.
- `intentos/<id convocatoria>` (lo escribe la página): `{inicio, fin, estado:"entregado", respuestas, puntos, total, fallos:[{n,repasar}], automatica}`.
- `resultados/<clave>` (lo escribe la página al corregir tests, cuestiones de hito y convocatorias): `{tipo:"test"|"hito"|"convocatoria", mejor, ultimo, total, intentos, fallos:[repasar…], historial:[{fecha,puntos}], fecha}`. Claves: id del módulo (p. ej. `P03`, `M05`), id del hito (`H0`) o `conv-<id>`.
- `seguimiento/<AAAA-MM-DD>`: lo escribe el tutor como diario de seguimiento: `{resumen, cumplimiento:{planificadas, hechas}, puntos_debiles:[repasar…], decisiones:[texto]}`.

## Convocatorias: reglas de calidad
- Una por semana, normalmente el **viernes de 19:00 a 20:00** (50 minutos), sobre lo estudiado esa semana más un 20 % de repaso de los puntos débiles anteriores. Al cerrar una fase, la convocatoria es un simulacro del examen de hito (2 h, viernes 18:00–20:00) con preguntas nuevas.
- 10–15 preguntas nuevas (mezcla de opción y número; posición de la correcta repartida; respuestas numéricas sin exactamente tres decimales) y 1–3 problemas a mano con solución completa (demostraciones o cálculos), basados en los apuntes y, cuando sea posible, adaptados de ejercicios universitarios citados en ellos.
- **Comprueba con Python** cada respuesta numérica y cada clave antes de escribir. Valida que el JSON es correcto. No reutilices preguntas de `docs/tests-*.json` ni de convocatorias anteriores.

## Avisos
El resumen final de cada ejecución es lo que llega por notificación y correo: breve, con el plan del día o de la semana, la próxima convocatoria (día y hora) y 2–3 recomendaciones concretas con sección de los apuntes.
