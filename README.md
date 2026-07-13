# Proyecto Universitario: Control de Versiones y Trabajo Colaborativo

## Información de los Integrantes
* **Nombres:** Ismael Hurtado y Cesar Martinez
* **Asignatura:** Programación I
* **Semestre:** Primer Semestre

---

## Parte 1 — Investigación Teórica

### 1. ¿Qué es un sistema de control de versiones y por qué es útil?
Un sistema de control de versiones (VCS) es un software diseñado para registrar y administrar los cambios realizados en los archivos de un proyecto a lo largo del tiempo. Funciona como una "máquina del tiempo" del código. 

En proyectos colaborativos es indispensable porque:
* Permite que varias personas trabajen en el mismo archivo simultáneamente sin borrarse el trabajo mutuamente.
* Mantiene un historial transparente de quién hizo qué cambio, cuándo y por qué.
* Facilita la recuperación de versiones anteriores del proyecto en caso de errores graves.

### 2. Conceptos Clave de Git
* **Repositorio:** Es la carpeta virtual o contenedor digital donde se guardan todos los archivos de un proyecto, junto con el historial completo de sus modificaciones.
* **Branch (Rama):** Es una línea de tiempo paralela e independiente dentro del repositorio. Permite desarrollar funciones nuevas o corregir errores sin alterar la versión del proyecto que ya funciona (rama principal).
* **Merge (Fusión):** Es el proceso de unir los cambios de una rama secundaria dentro de otra rama (generalmente hacia la rama principal) una vez que el trabajo ha sido revisado y aprobado.
* **Conflicto de código:** Ocurre cuando dos personas modifican exactamente la misma línea de un archivo con textos diferentes en ramas distintas, y el sistema no puede decidir automáticamente cuál cambio conservar, requiriendo intervención humana.

### 3. Diferencias: SVN (Centralizado) vs. Git (Distribuido)
| Característica | SVN (Centralizado) | Git (Distribuido) |
| :--- | :--- | :--- |
| **Arquitectura** | Existe un único servidor central donde se guarda el historial. | Cada desarrollador tiene una copia local completa del historial en su computadora. |
| **Conectividad** | Requiere conexión a internet constante para hacer commits o ver el historial. | Se puede trabajar, ver el historial y hacer commits sin internet. Solo requiere conexión para sincronizar. |
| **Velocidad** | Más lento, ya que cada acción debe comunicarse con el servidor central. | Extremadamente rápido, porque la mayoría de las operaciones ocurren localmente. |

### 4. Flujo de Trabajo Típico en Git
1. **Creación de ramas:** Se genera una rama secundaria a partir de la principal (`main`) para trabajar en un cambio específico de forma aislada.
2. **Commits:** Se realizan modificaciones en los archivos y se guardan localmente como "puntos de control" acompañados de un mensaje explicativo.
3. **Pull Requests (PR):** Se suben los cambios al servidor remoto y se abre una solicitud formal para que el resto del equipo revise el código antes de integrarlo.
4. **Merge:** Tras la aprobación de la revisión y la resolución de posibles conflictos, los cambios se fusionan definitivamente en la rama principal.

---

## Parte 2 — Práctica Colaborativa: Bitácora del Flujo

### Objetivo del Proyecto Técnico
Simular y ejecutar un flujo de trabajo colaborativo profesional empleando la interfaz de GitHub, aplicando metodologías de ramificación, registro de cambios y resolución de conflictos de código.

### Flujo Seguido y Ramas Creadas
El proyecto se estructuró a partir de la rama raíz `main`. Posteriormente, se generó la rama secundaria `desarrollo-companero` para simular las tareas aisladas de desarrollo.

### Commits Realizados
* **En rama `main`:** 1. `docs: agregar lista de integrantes`
  2. `docs: agregar descripcion del objetivo`
* **En rama `desarrollo-companero`:** 1. `docs: registrar equipo en rama secundaria`
  2. `docs: agregar proposito alternativo`

### Conflicto Presentado y Resolución
* **El Conflicto:** Al intentar realizar el *Pull Request* para fusionar `desarrollo-companero` dentro de `main`, GitHub bloqueó la fusión automática debido a que ambas ramas modificaron las mismas líneas del archivo `README.md` con información contradictoria.
* **La Resolución:** Se utilizó la herramienta interactiva **Resolve Conflicts** de GitHub de manera directa en la web. Se eliminaron manualmente las etiquetas de colisión (`<<<<<<<`, `=======`, `>>>>>>>`) y se unificaron los textos en una versión limpia y definitiva, concluyendo con éxito el *Merge* final del repositorio.
