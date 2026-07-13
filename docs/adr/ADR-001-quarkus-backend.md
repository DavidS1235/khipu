# ADR-001: Uso de Quarkus como framework backend

## Estado

Aceptada.

## Contexto

Khipu requiere una plataforma backend capaz de gestionar usuarios, documentos financieros, procesamiento de información e integraciones con servicios externos.

El backend debe permitir:

- Desarrollo eficiente.
- Buen rendimiento.
- Bajo consumo de recursos.
- Preparación para ambientes cloud.
- Desarrollo basado en Java.

El equipo cuenta con experiencia previa en Java y Spring Boot, por lo que se evaluaron diferentes alternativas dentro del ecosistema Java.

---

## Alternativas consideradas

### Spring Boot

Ventajas:

- Ecosistema maduro.
- Amplia comunidad.
- Gran cantidad de librerías.
- Amplio uso empresarial.

Desventajas:

- Mayor consumo de recursos comparado con frameworks cloud native.
- Algunas capacidades modernas requieren configuración adicional.

---

### Quarkus

Ventajas:

- Diseñado para aplicaciones cloud native.
- Bajo consumo de memoria.
- Excelente integración con contenedores.
- Buen soporte para compilación nativa.
- Compatible con estándares Java.

Desventajas:

- Ecosistema menor comparado con Spring Boot.
- Menor cantidad de ejemplos disponibles.

---

## Decisión

Se utilizará **Quarkus como framework principal para el backend de Khipu**.

La elección se basa en:

- Oportunidad de aprendizaje tecnológico.
- Enfoque cloud native.
- Buen rendimiento.
- Compatibilidad con Java.
- Preparación para futuras arquitecturas distribuidas.

---

## Consecuencias

### Positivas

- Aplicación moderna basada en Java.
- Buen rendimiento en ambientes contenerizados.
- Preparación para despliegues cloud.

### Negativas

- Curva inicial de aprendizaje.
- Menor comunidad comparado con Spring Boot.

---

## Referencias

- Documentación oficial de Quarkus.