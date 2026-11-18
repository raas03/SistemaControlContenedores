# Sistema de Control de Contenedores y Ubicación en Almacén

Proyecto de la asignatura **Ingeniería de Software I** (UAPA), Grupo AE.
Tablero del proyecto: [GitHub Project](https://github.com/users/raas03/projects/3)

## 1. Sistema digital

Una empresa de carga necesita un sistema para controlar los contenedores que llegan al puerto y su ubicación en los almacenes.

- Al arribar, cada contenedor recibe una ubicación en uno de los almacenes, **en el orden en que fue descargado** del barco.
- Cada almacén tiene **áreas por rango de tamaño** de contenedor y cada área tiene una **capacidad máxima**.
- Se registra la **fecha de arribo**. Si a los **90 días** ningún cliente lo ha reclamado, el contenedor pasa al **almacén de donaciones**, donde los que más tiempo llevan en el puerto se colocan más cerca de la puerta.

El sistema debe permitir consultar:

- La ubicación de un contenedor dado su tamaño y número.
- La cantidad de contenedores en cada almacén, en orden ascendente.
- La cantidad de contenedores de un tamaño específico.
- La información de las áreas.
- La información de los clientes (país, nombre, estatal o privado).

## 2. Enfoque de desarrollo: Kanban

Usamos **Kanban** sobre GitHub Projects porque:

- El trabajo de esta etapa (análisis, modelado, documentación) llega de forma continua y no en sprints de duración fija.
- El tablero hace visible en qué estado está cada tarea y quién la tiene.
- Permite limitar el trabajo en progreso y cambiar prioridades sin esperar el cierre de un sprint.
- Es un equipo pequeño, y Kanban no exige ceremonias ni roles formales como Scrum.

**Columnas del tablero:** Backlog → Por hacer → En progreso → En revisión → Finalizado

## 3. Tarjetas iniciales

| # | Tarjeta | Prioridad | Estado | Rol | Asignado |
|---|---------|-----------|--------|-----|----------|
| 1 | Análisis de requisitos del sistema | Alta | En progreso | Analista | @ismaira-l |
| 2 | Configuración del tablero y documentación inicial | Media | En revisión | Líder de proyecto | @raas03 |
| 3 | Modelado de datos: contenedores, almacenes, áreas y clientes | Alta | Por hacer | Arquitecto / Modelado | @100095020-gif |
| 4 | Módulo de registro de arribo y asignación de ubicación | Alta | Por hacer | Desarrollador | @100095020-gif |
| 5 | Módulo de consultas y reportes | Media | Backlog | Desarrollador | @josevalentinet304-spec |
| 6 | Control de 90 días y almacén de donaciones | Media | Backlog | Desarrollador | @josevalentinet304-spec |

## 4. Roles del equipo

| Rol | Responsabilidad | Integrante |
|-----|-----------------|------------|
| Líder de proyecto (responsable del tablero) | Planifica, prioriza el backlog, mantiene el tablero Kanban al día y coordina al equipo. | @raas03 |
| Analista | Levanta y documenta los requisitos funcionales y no funcionales y las reglas de negocio. | @ismaira-l |
| Arquitecto / Responsable de modelado | Diseña el modelo de datos, los diagramas y la arquitectura del sistema. | @100095020-gif |
| Desarrollador | Implementa los módulos del sistema (registro, asignación de ubicación, consultas y donaciones). | @100095020-gif, @josevalentinet304-spec |
| QA (control de calidad) | Define los casos de prueba, verifica que cada tarjeta cumpla sus criterios de aceptación y la mueve de *En revisión* a *Finalizado*. | @ismaira-l |
| Responsable de documentación | Redacta y organiza la documentación del proyecto y el README. | @raas03 |

Cada integrante cubre dos roles por el tamaño del equipo. QA lo lleva una persona que no desarrolla, para que nadie apruebe su propio trabajo.
