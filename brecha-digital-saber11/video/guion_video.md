# Guion del video (≈ 4 minutos)

> El video debe durar **entre 2 y 5 minutos**. Este guion apunta a ~4:00 para tener margen.
> Graben con pantalla compartida (presentación + cuaderno de Colab). Reemplacen [Integrante X] por sus nombres.
> Enlace al video: pegarlo en el `README.md` (YouTube "no listado" o Google Drive con acceso público).

| Tiempo | Quién | Pantalla | Qué decir |
|---|---|---|---|
| 0:00 – 0:25 | [Integrante 1] | Diapositiva 1 → 2 | "Hola, somos [nombres], estudiantes de Ingeniería de Sistemas. Nos preguntamos si la **brecha digital** en Colombia se convierte en una **brecha de aprendizaje**: ¿los estudiantes sin internet ni computador en casa obtienen menores puntajes en el Saber 11? Usamos datos abiertos del ICFES: 1.584 estudiantes del periodo 2022-2." |
| 0:25 – 1:05 | [Integrante 1] | Diapositiva 3 + Colab: celdas de duplicados y bitácora de limpieza | "**Etapa 1.** Los datos públicos vienen sucios: la mitad de las filas estaban duplicadas, los puntajes llegaban como texto, había respuestas como 'No sabe' que en realidad son datos faltantes, puntajes de inglés en cero y edades de hasta 64 años. Eliminamos duplicados, convertimos tipos, calculamos la edad y creamos variables nuevas, como el índice de acceso digital de 0 a 2." |
| 1:05 – 1:50 | [Integrante 2] | Diapositiva 4 → 5 | "**Etapa 2.** El puntaje global promedio es 249 sobre 500, con mediana y moda de 245 y una desviación estándar de 51 puntos: hay bastante variación. Al comparar grupos, quienes tienen internet y computador promedian 42 puntos más que quienes no tienen ninguno. La prueba t confirma que la diferencia por internet no es azar (p < 0,001) y la d de Cohen de 0,68 indica un efecto mediano-grande." |
| 1:50 – 2:30 | [Integrante 2] | Diapositivas 6 → 7 | "**Etapa 3: la historia.** El acceso cae en los estratos bajos: en estrato 1 solo la mitad tiene internet. Pero no es solo el estrato: **dentro de cada estrato**, tener internet suma entre 17 y 31 puntos. Y hay un patrón territorial: en el Caribe y la Amazonía la mitad de los estudiantes no tiene conexión y tienen los puntajes más bajos." |
| 2:30 – 3:20 | [Integrante 3] | Diapositivas 8 → 9 (y celda de métricas en Colab) | "Construimos dos modelos de regresión lineal. El simple dice que cada recurso digital suma unos 21 puntos. El múltiple controla estrato, colegio, zona, región y educación de la madre: en datos que no vio predice con un error medio de 37 puntos, mejor que el modelo base, y es estable en validación cruzada. Aun así, internet suma 10 puntos y computador 8, ambos significativos. Un hallazgo curioso: el estrato pierde peso; lo que importa es lo que el estrato permite tener." |
| 3:20 – 3:50 | [Integrante 3] | Diapositiva 11 | "**¿Cómo lo aplicaríamos?** Como ingenieros de sistemas propondríamos un sistema de alerta temprana: un pipeline que descarga los datos abiertos, un modelo que estima el puntaje esperado por municipio y un dashboard que muestra dónde priorizar wifi, equipos y aulas digitales, midiendo después el impacto." |
| 3:50 – 4:10 | Todos | Diapositiva 12 | "Aprendimos que limpiar datos es la mitad del trabajo, que la estadística convierte intuiciones en evidencia y que un modelo sencillo bien explicado comunica mucho. Asociación no es causalidad, pero los datos son consistentes. ¡Gracias!" |

## Consejos de grabación
- Usen Zoom, Teams o OBS para grabar pantalla + cámara; ensayen una vez con cronómetro.
- Hablen sobre lo que se ve en pantalla; resalten con el cursor el número del que hablan.
- Exporten en MP4. Si pesa más de 100 MB, súbanlo a YouTube (no listado) o Drive y pongan solo el enlace en el README.
