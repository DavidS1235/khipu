# ADR-003: Arquitectura modular inicial

## Estado

Aceptada.

## Contexto

Khipu podría requerir múltiples servicios independientes en el futuro:

- Usuarios.
- Documentos.
- OCR.
- IA.
- Búsqueda.

Sin embargo, separar desde el inicio en microservicios aumenta la complejidad operacional.

---

## Alternativas consideradas

### Microservicios desde el inicio

Ventajas:

- Separación completa.
- Escalabilidad independiente.

Desventajas:

- Mayor complejidad.
- Más infraestructura.
- Mayor esfuerzo inicial.

---

### Monolito modular

Ventajas:

- Desarrollo más rápido.
- Menor complejidad.
- Límites de dominio claros.
- Fácil evolución hacia microservicios.

---

## Decisión

Khipu iniciará con una arquitectura modular dentro de una aplicación backend única.

---

## Consecuencias

La aplicación podrá evolucionar hacia servicios independientes cuando exista una necesidad real.