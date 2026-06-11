## Estructura de carpetas

- [ ] `src/app`: rutas, layout y bootstrap.
- [ ] `src/components`: componentes reutilizables.
- [ ] `src/features`: módulos por dominio.
- [ ] `src/hooks`: hooks compartidos.
- [ ] `src/services`: clientes API y adaptadores.
- [ ] `src/store`: estado global.
- [ ] `src/types`: tipos compartidos.
- [ ] `src/utils`: utilidades puras.
- [ ] `src/assets`: recursos estáticos.
- [ ] `tests`: pruebas y fixtures.

## Convenciones de nombres

- [ ] Componentes en `PascalCase`.
- [ ] Hooks con prefijo `use`.
- [ ] Archivos de componentes en `PascalCase`.
- [ ] Utilidades en `camelCase`.
- [ ] Constantes en `UPPER_SNAKE_CASE`.
- [ ] Tipos e interfaces en `PascalCase`.
- [ ] Carpetas de dominio en `kebab-case`.
- [ ] Tests con sufijo `.test`.
- [ ] Estilos junto al componente.
- [ ] Nombres orientados al negocio.

## Organización de componentes con sus responsabilidades

- [ ] Presentacionales: solo UI.
- [ ] Contenedores: datos y acciones.
- [ ] Formularios: validación local.
- [ ] Listas: render y paginación.
- [ ] Modales: foco y cierre.
- [ ] Layouts: estructura visual.
- [ ] Pages: composición de vistas.
- [ ] Componentes base: sin negocio.
- [ ] Componentes de dominio: reglas del caso.
- [ ] Evitar componentes con responsabilidades mixtas.

## Uso de hooks

- [ ] Extraer lógica reutilizable.
- [ ] Mantener hooks pequeños.
- [ ] No renderizar JSX en hooks.
- [ ] Devolver datos y acciones.
- [ ] Aislar efectos externos.
- [ ] Declarar dependencias completas.
- [ ] Evitar estado duplicado.
- [ ] Encapsular suscripciones.
- [ ] Tipar entradas y salidas.
- [ ] Probar hooks críticos.

## Gestión del estado

- [ ] Estado local por defecto.
- [ ] Estado global solo compartido.
- [ ] Separar UI y dominio.
- [ ] Normalizar colecciones grandes.
- [ ] Derivar datos al leer.
- [ ] Evitar duplicar servidor.
- [ ] Persistir solo lo necesario.
- [ ] Resetear estado al cerrar sesión.
- [ ] Mantener acciones explícitas.
- [ ] Documentar estados complejos.

## Gestión de llamadas API

- [ ] Centralizar clientes HTTP.
- [ ] Usar funciones por endpoint.
- [ ] Tipar request y response.
- [ ] Validar datos externos.
- [ ] Manejar abortos.
- [ ] Evitar llamadas en componentes base.
- [ ] Cachear lecturas repetidas.
- [ ] Reintentar solo idempotentes.
- [ ] No exponer secretos.
- [ ] Mapear DTO a dominio.

## Manejo de errores y cargas

- [ ] Mostrar carga inmediata.
- [ ] Usar estados vacíos claros.
- [ ] Mostrar errores recuperables.
- [ ] Registrar errores inesperados.
- [ ] Evitar pantallas bloqueadas.
- [ ] Permitir reintento.
- [ ] Deshabilitar acciones en progreso.
- [ ] Preservar datos previos útiles.
- [ ] Validar formularios antes de enviar.
- [ ] No ocultar fallos silenciosamente.

## Librerías aprobadas

- [ ] React para UI.
- [ ] TypeScript para tipos.
- [ ] Vite para build.
- [ ] React Router para rutas.
- [ ] TanStack Query para servidor.
- [ ] Zustand para estado global.
- [ ] React Hook Form para formularios.
- [ ] Zod para validación.
- [ ] Vitest para pruebas.
- [ ] Testing Library para UI.
