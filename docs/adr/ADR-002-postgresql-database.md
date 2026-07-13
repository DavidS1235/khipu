# ADR-002: Uso de PostgreSQL como base de datos principal

## Estado

Aceptada.

## Contexto

Khipu requiere almacenar información estructurada relacionada con:

- Usuarios.
- Documentos.
- Transacciones.
- Categorías.
- Eventos financieros.

La información financiera requiere consistencia e integridad.

---

## Alternativas consideradas

### PostgreSQL

Ventajas:

- Base de datos relacional madura.
- Integridad referencial.
- Consultas complejas.
- Excelente soporte para datos transaccionales.

---

### Cosmos DB

Ventajas:

- Escalabilidad horizontal.
- Modelo NoSQL flexible.
- Integración con ecosistemas cloud.

Desventajas:

- Mayor complejidad para relaciones entre entidades.
- Menor orientación hacia datos altamente relacionados.

---

## Decisión

Se utilizará PostgreSQL como base de datos principal de Khipu.

---

## Consecuencias

### Positivas

- Modelo adecuado para información financiera.
- Mayor control sobre relaciones y consistencia.
- Amplio soporte en herramientas Java.

### Negativas

- Escalamiento horizontal requiere planificación futura.

---

## Referencias

Documentación oficial de PostgreSQL.