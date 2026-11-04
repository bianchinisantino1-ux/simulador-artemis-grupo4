Simulador de Reingreso Atmosférico - Misión Artemis (Problema 4)Universidad Tecnológica Nacional – Facultad Regional ResistenciaCátedra: Algoritmos y Estructuras de DatosAño: 2026Integrantes del Grupo 4Basterra, Joaquín NicolásBianchini, SantinoMañanes Amarilla, Lautaro FacundoPonce, Marcos LautaroSan Vicente, María JulianaDescripción del ProblemaEste proyecto implementa una simulación computacional modular en C para modelar la fase final de reingreso atmosférico y amerizaje de la cápsula Orión de la misión Artemis IV.El programa evalúa:Trabajo total realizado por la fuerza de rozamiento atmosférico ($W_{roz}$): Aplicando el principio de conservación de la energía entre el inicio de la reentrada ($120\text{ km}$, $11\,000\text{ m/s}$) y la apertura de paracaídas ($2{,}5\text{ km}$, $25\text{ m/s}$).Desaceleración media: Calculada durante la fase aerodinámica activa y expresada tanto en $\text{m/s}^2$ como en múltiplos de la gravedad terrestre ($g$).Fuerza media de desaceleración del agua: Dinámica del impacto final en el océano hasta el reposo tras hundirse $1{,}50\text{ m}$.Ventana de Seguridad de Reingreso: Validación del ángulo de entrada $\gamma$ ($5{,}5^\circ \le \gamma \le 7{,}0^\circ$) para evitar rebotes atmosféricos o fallos estructurales por exceso de desaceleración.Estructura del Proyectoartemis_simulador/
├── include/
│   ├── artemis.h         # Estructuras de la cápsula y prototipos físicos
│   └── validaciones.h    # Prototipos de ingreso seguro y control de buffer
├── src/
│   ├── artemis.c         # Lógica y ecuaciones físicas del reingreso
│   ├── validaciones.c    # Implementación de validaciones de entrada
│   └── main.c            # Interfaz CLI y menú principal interactivo
├── .gitignore            # Filtro de archivos binarios y temporales
├── Makefile              # Script de automatización de compilación
└── README.md             # Documentación del proyecto
Compilación y EjecuciónOpción 1: Utilizando Makefilemake
./simulador_artemis
Opción 2: Compilación directa con GCCgcc -Wall -Wextra -std=c99 -Iinclude src/main.c src/artemis.c src/validaciones.c -o simulador_artemis -lm
./simulador_artemis
Declaración Transparente del Uso de Inteligencia ArtificialEn cumplimiento con los lineamientos del trabajo práctico sobre el uso de herramientas de IA:Herramientas utilizadas: Asistencia interactiva mediante Large Language Models (LLMs).Alcance de la interacción:Estructuración inicial de la arquitectura modular de archivos (.h / .c) y confección del Makefile.Asistencia en el manejo defensivo del búfer de entrada en C (scanf y getchar) para prevenir bucles infinitos.Formateo y revisión de la documentación en sintaxis Markdown.Verificación humana: Todas las ecuaciones físicas (Trabajo-Energía, cálculo de cargas $g$), la lógica de control del menú y la depuración final de errores de compilación fueron analizadas, verificadas y probadas manualmente por el equipo de desarrollo.
