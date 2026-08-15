# Laboratorio de skills

## Propósito
Este proyecto es el hogar permanente de skills chicas e independientes entre sí — herramientas útiles para el día a día que no forman parte de un flujo de trabajo mayor (a diferencia de otros proyectos como el sistema de estudio de Moodle o el de Tupperware, donde varias skills colaboran entre sí). Una skill puede quedarse acá indefinidamente; no hay obligación de que "se independice" a su propio proyecto.

## Cómo trabajar en este proyecto
- Cuando Alesio pida algo sin nombrar una skill explícitamente, **inferir** cuál skill del índice corresponde al pedido, según su descripción. Ante la duda entre dos o más skills, o si ninguna encaja con claridad, preguntar antes de actuar en lugar de asumir.
- Idioma por defecto para toda salida generada por las skills de este laboratorio: **español**.
- Cada skill vive en su propia subcarpeta, con su propio archivo de prompt y (si corresponde) su propia carpeta de outputs.

## Estructura de carpetas
```
Laboratorio-de-skills/
├── CLAUDE.md                  (este archivo)
├── <nombre-skill>/
│   ├── skill.md                (prompt completo de la skill)
│   └── outputs/                 (archivos que la skill genera, si aplica)
└── <nombre-skill-2>/
    ├── skill.md
    └── outputs/
```

## Convención de nombres (propuesta — ajustable)
- Carpetas y archivos: `kebab-case`, sin tildes ni espacios. Ej.: `planificador-rutina/`, `idea-regalo/`.
- El prompt/spec de cada skill siempre se llama `skill.md` dentro de su propia carpeta.
- Los outputs van dentro de `outputs/`, con nombre descriptivo en `kebab-case` (ej. `planificacion.md`, `exportable.ics`).
- Si una skill no genera archivos (por ejemplo, una que solo imprime resultados en pantalla), no necesita carpeta `outputs/`.

## Cómo sumar una skill nueva
1. Alesio envía el prompt de creación de la skill (estructura: Nombre / Cuándo usarla / Contexto-Rol / Instrucciones / Reglas-Límites / Accionar en casos no ideales / Formato de salida / Ejemplos).
2. Crear la subcarpeta `<nombre-skill>/` con el archivo `skill.md` conteniendo ese prompt completo.
3. Agregar una fila a la tabla de "Skills disponibles" de este archivo, con el nombre y una descripción de una línea lo bastante clara como para poder inferir cuándo corresponde usarla.

## Skills disponibles

| Skill | Descripción breve | Cuándo usarla |
|---|---|---|
| idea-regalo | Genera ideas de regalo reales (producto, precio, link) para una persona según su perfil, presupuesto y fecha de entrega, con justificación psicológica de por qué puede gustarle | Cuando Alesio pida ideas de regalo, sugerencias de qué regalarle a alguien, o invoque "idea-regalo" explícitamente |
| planificador-rutina | Organiza y actualiza la agenda/rutina de Alesio (facultad, entrenamiento, formación, tareas, varios) respetando reglas de sueño, entrenamiento y bloques de estudio; genera planificación legible y versión exportable tipo iCalendar. | Cuando Alesio pida planificar, organizar, agendar o actualizar su rutina/horario, o invoque explícitamente "planificador-rutina". |
| english-mining | Extrae del episodio/video que Alesio indique las expresiones de inglés (idioms, phrasal verbs, vocabulario) más útiles para su Work and Travel en un ski resort de California; mantiene un banco de expresiones confirmadas, avanza automáticamente por la serie y arma repaso de speaking con repetición espaciada. Todo el contenido de esta skill (prompt, banco y respuestas) es en inglés, no en español. | Cuando Alesio pida minar expresiones de un episodio/video, mencione "english-mining" explícitamente, o se trate de la corrida automática diaria (7:00 AM GMT-3). |
