# Arquitectura del Proyecto Khipu

## 1. Introducción

Este documento describe la arquitectura inicial propuesta para Khipu.

La arquitectura busca permitir el desarrollo progresivo de una plataforma de memoria financiera personal, considerando escalabilidad, mantenibilidad, seguridad e integración con servicios externos.

La solución será diseñada bajo principios cloud native, aplicando buenas prácticas de ingeniería de software.

---

# 2. Principios arquitectónicos

## Separación de responsabilidades

Cada componente del sistema debe tener una responsabilidad clara, evitando acoplamiento innecesario.

## Evolución incremental

La arquitectura debe permitir iniciar con un MVP simple y evolucionar hacia una plataforma más completa.

## Seguridad por diseño

La información financiera del usuario debe estar protegida desde la primera versión.

## Automatización

Los procesos repetitivos deben ser automatizados mediante servicios especializados.

## Observabilidad

El sistema debe permitir monitorear estado, rendimiento y errores.

---

# 3. Arquitectura general propuesta

Khipu estará compuesto inicialmente por los siguientes componentes:

```text
                 +----------------+
                 | Mobile App     |
                 | Flutter        |
                 +-------+--------+
                         |
                         |
                    REST API
                         |
                         |
                 +-------v--------+
                 | Backend API    |
                 | Quarkus        |
                 +-------+--------+
                         |
        +----------------+----------------+
        |                |                |
        v                v                v

 PostgreSQL       File Storage       External Services

 Database         Documents          OCR / AI / Email
```

---

# 4. Aplicación móvil

## Tecnología

Flutter

## Responsabilidad

La aplicación móvil será el principal punto de interacción del usuario.

Funciones iniciales:

- Registro de usuario.
- Inicio de sesión.
- Carga de documentos.
- Visualización de memoria financiera.
- Búsqueda de información.

---

# 5. Backend

## Tecnología

Java + Quarkus

## Responsabilidad

El backend será responsable de:

- Exponer APIs.
- Gestionar usuarios.
- Procesar documentos.
- Coordinar servicios externos.
- Aplicar reglas de negocio.

---

# 6. Estilo arquitectónico backend

## Decisión inicial

Arquitectura modular.

Khipu iniciará con una aplicación backend modular preparada para evolucionar.

Estructura propuesta:

```text
backend

├── authentication
├── users
├── documents
├── transactions
├── categories
└── search
```

---

## Justificación

Aunque Khipu podría evolucionar hacia microservicios, iniciar directamente con múltiples servicios incrementaría complejidad técnica y operativa.

El enfoque inicial será:

- Módulos independientes.
- Bajo acoplamiento.
- Límites de dominio claros.
- Separación de responsabilidades.

Esto permitirá separar servicios posteriormente si existe una necesidad real.

---

# 7. Base de datos

## Decisión inicial

PostgreSQL.

## Justificación

Khipu manejará principalmente información estructurada:

- Usuarios.
- Documentos.
- Transacciones.
- Categorías.
- Eventos financieros.

PostgreSQL ofrece:

- Modelo relacional robusto.
- Integridad de datos.
- Consultas complejas.
- Buen soporte para aplicaciones empresariales.

---

# 8. Almacenamiento de documentos

Los archivos financieros no serán almacenados directamente en la base de datos.

Arquitectura propuesta:

```text
Usuario
   |
   |
Upload documento
   |
   |
Backend
   |
   |
Object Storage
   |
   |
Metadata PostgreSQL
```

Posibles tecnologías futuras:

- Azure Blob Storage.
- AWS S3.
- Google Cloud Storage.

---

# 9. Procesamiento OCR

## Objetivo

Transformar documentos no estructurados en información financiera estructurada.

Flujo inicial:

```text
Documento
    |
    v
OCR Engine
    |
    v
Texto extraído
    |
    v
Procesamiento
    |
    v
Información financiera
```

Posibles tecnologías:

- Servicios cloud OCR.
- Modelos especializados.
- Soluciones open source.

La decisión final será evaluada durante la implementación.

---

# 10. Inteligencia Artificial

La inteligencia artificial será incorporada como una capacidad adicional del sistema.

Casos futuros:

- Consultas mediante lenguaje natural.
- Resúmenes financieros.
- Clasificación automática.
- Detección de patrones financieros.

La IA no será parte del núcleo inicial del sistema.

---

# 11. Seguridad

Consideraciones iniciales:

- Autenticación segura.
- Autorización basada en usuario.
- Comunicación cifrada mediante HTTPS.
- Protección de documentos almacenados.
- Separación de información entre usuarios.

---

# 12. CI/CD

## Herramienta

GitHub Actions.

## Objetivo

Automatizar:

- Compilación.
- Ejecución de pruebas.
- Validaciones de calidad.
- Construcción de imágenes Docker.

Flujo:

```text
Pull Request

      |
      v

GitHub Actions

      |
      +--> Build
      |
      +--> Tests
      |
      +--> Quality Checks

      |
      v

Merge main
```

---

# 13. Contenedores

## Tecnología

Docker.

## Objetivo

Garantizar ambientes reproducibles:

- Desarrollo local.
- Pruebas.
- Despliegue.

---

# 14. Evolución futura

La arquitectura podrá evolucionar hacia:

- Microservicios.
- Procesamiento asíncrono.
- Colas de mensajes.
- Servicios independientes de OCR.
- Motor de inteligencia artificial especializado.

La evolución dependerá del crecimiento del producto y necesidades reales del negocio.

---

# Estado del documento

**Versión:** 0.1.0

**Estado:** Propuesta inicial.