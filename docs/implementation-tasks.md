# Tareas de implementacion

## 1. Preparar base del proyecto

**Objetivo:** Crear la base React + TypeScript sobre la que se construira el Gestor de Tareas ICE.

**Alcance incluido:**
- Configuracion inicial con Vite, React y TypeScript.
- Instalacion y configuracion de Material UI.
- Tema base Material Design.
- Estructura de carpetas segun la guia tecnica.
- Configuracion inicial de rutas, tests y linting si aplica.

**Archivos o carpetas previsibles a modificar:**
- `package.json`
- `vite.config.ts`
- `tsconfig.json`
- `src/app`
- `src/components`
- `src/features`
- `src/types`
- `src/utils`
- `tests`

**Criterios de aceptacion:**
- La app arranca en local sin errores.
- TypeScript compila correctamente.
- Material UI esta disponible y tematizado.
- La estructura de carpetas queda creada.
- Existe una prueba minima de renderizado.

**Dependencias:** Ninguna.

## 2. Implementar navegacion y layout principal

**Objetivo:** Construir la estructura navegable de la aplicacion con rutas y layout Material UI.

**Alcance incluido:**
- `MainLayout` con `AppBar`, `NavigationDrawer` y `MainContent`.
- Rutas principales: `/`, `/tasks`, `/tasks/new`, `/tasks/:taskId`, `/tasks/:taskId/edit`, `/tasks/:taskId/confirmed`.
- Redireccion de `/` a `/tasks`.
- Pantalla `NotFoundPage`.
- Estados placeholder para pantallas aun no implementadas.

**Archivos o carpetas previsibles a modificar:**
- `src/app`
- `src/components/layout`
- `src/features/tasks/pages`
- `src/components/navigation`

**Criterios de aceptacion:**
- El usuario entra en `/` y llega a `/tasks`.
- La navegacion lateral muestra las secciones definidas.
- Todas las rutas principales renderizan una pantalla.
- El layout mantiene coherencia visual con Material Design.
- Las rutas inexistentes muestran `NotFoundPage`.

**Dependencias:** Tarea 1.

## 3. Implementar listado y detalle de tareas

**Objetivo:** Permitir visualizar tareas existentes, estados vacios y acceso a creacion, detalle y edicion.

**Alcance incluido:**
- `TasksListPage` con `TaskListSection`.
- Filtros y orden basicos segun la jerarquia definida.
- `EmptyTasksState` cuando no haya tareas.
- Tarjetas o filas Material UI con titulo, objetivo, plazo y score ICE.
- `TaskDetailPage` con resumen, ICE y acciones.

**Archivos o carpetas previsibles a modificar:**
- `src/features/tasks/pages`
- `src/features/tasks/components`
- `src/features/tasks/types`
- `src/store` o estado local inicial
- `src/utils`

**Criterios de aceptacion:**
- El listado muestra tareas mock o estado vacio.
- El boton `Crear tarea` navega a `/tasks/new`.
- Cada tarea permite navegar a su detalle.
- El detalle muestra datos funcionales de la tarea.
- Los estados vacio y carga son visibles y claros.

**Dependencias:** Tarea 2.

## 4. Implementar formulario de tarea y sugerencia ICE por IA

**Objetivo:** Crear el flujo de alta/edicion de tarea con solicitud y revision de sugerencia ICE.

**Alcance incluido:**
- `TaskCreatePage` y `TaskEditPage`.
- `TaskForm` con titulo, descripcion, objetivo y plazo.
- Validacion con mensajes en campos Material UI.
- Accion `Sugerir ICE con IA`.
- `AiIceSuggestionPanel` con impacto, confianza, esfuerzo, score y justificacion.
- Manejo de carga, error, reintento y edicion manual.

**Archivos o carpetas previsibles a modificar:**
- `src/features/tasks/pages`
- `src/features/tasks/components`
- `src/features/tasks/hooks`
- `src/services`
- `src/types`
- `src/utils`

**Criterios de aceptacion:**
- El formulario impide solicitar ICE si faltan campos minimos.
- La solicitud muestra estado de carga.
- La respuesta IA se presenta para revision.
- El error permite reintentar o editar manualmente.
- El usuario puede aceptar o modificar valores ICE.

**Dependencias:** Tareas 2 y 3.

## 5. Completar confirmacion y flujo principal end to end

**Objetivo:** Cerrar el flujo principal desde listado hasta tarea confirmada y revisable.

**Alcance incluido:**
- `ReviewTaskSummary` antes de guardar.
- Creacion de tarea con ICE final.
- `TaskConfirmedPage` con resumen de tarea, ICE final y origen IA/manual.
- Navegacion desde confirmacion a listado, detalle o nueva tarea.
- Persistencia inicial del estado dentro del alcance del MVP.
- Pruebas del flujo principal.

**Archivos o carpetas previsibles a modificar:**
- `src/features/tasks/pages`
- `src/features/tasks/components`
- `src/features/tasks/hooks`
- `src/store`
- `src/services`
- `tests`

**Criterios de aceptacion:**
- El usuario crea una tarea desde el listado.
- El usuario revisa la sugerencia ICE y puede editarla.
- La tarea se confirma y aparece en el listado.
- La pantalla de confirmacion muestra el resumen correcto.
- El flujo principal queda cubierto por una prueba verificable.

**Dependencias:** Tareas 3 y 4.
