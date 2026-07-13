# Requisitos del Proyecto Khipu

## 1. Introducción

Este documento define los requisitos funcionales y no funcionales de Khipu.

Los requisitos representan las capacidades esperadas del sistema y servirán como base para el diseño de arquitectura, desarrollo y validación del producto.

---

# 2. Requisitos funcionales

Los requisitos funcionales describen las acciones que el sistema debe permitir realizar a los usuarios.

---

## RF-001: Registro de usuario

### Descripción

El sistema debe permitir que un usuario cree una cuenta personal para gestionar su memoria financiera.

### Criterios de aceptación

- El usuario puede registrarse utilizando correo electrónico.
- El sistema valida la información ingresada.
- Cada usuario posee un espacio financiero independiente.

---

## RF-002: Autenticación de usuario

### Descripción

El sistema debe permitir que usuarios registrados puedan acceder de forma segura a su información.

### Criterios de aceptación

- El usuario puede iniciar sesión.
- El sistema valida las credenciales.
- La información financiera solo es visible para el propietario.

---

## RF-003: Gestión de documentos financieros

### Descripción

El sistema debe permitir almacenar documentos relacionados con actividades financieras personales.

### Tipos de documentos iniciales:

- Boletas electrónicas.
- Facturas.
- Recibos.
- Estados de cuenta.
- Comprobantes de pago.

### Criterios de aceptación

- El usuario puede cargar un documento.
- El sistema almacena la información asociada.
- El usuario puede consultar documentos previamente registrados.

---

## RF-004: Procesamiento OCR de documentos

### Descripción

El sistema debe extraer información relevante desde documentos utilizando tecnología OCR.

### Información esperada:

- Fecha.
- Comercio.
- Monto.
- Número de documento.
- Tipo de comprobante.

### Criterios de aceptación

- El sistema procesa documentos digitales o imágenes.
- La información extraída puede ser revisada.
- El usuario puede corregir información incorrecta.

---

## RF-005: Clasificación financiera

### Descripción

El sistema debe permitir categorizar información financiera.

### Ejemplos:

- Alimentación.
- Transporte.
- Tecnología.
- Entretenimiento.
- Salud.
- Educación.

### Criterios de aceptación

- Los documentos pueden asociarse a categorías.
- El usuario puede modificar categorías.

---

## RF-006: Línea de tiempo financiera

### Descripción

El sistema debe construir una vista cronológica de eventos financieros del usuario.

### Criterios de aceptación

- El usuario puede visualizar eventos ordenados por fecha.
- Cada evento contiene información relevante.
- El usuario puede acceder al documento original.

---

## RF-007: Búsqueda de información financiera

### Descripción

El sistema debe permitir encontrar información almacenada.

### Ejemplos:

Buscar:

- "Laptop Lenovo"
- "Compra en Plaza Vea"
- "Boleta de enero"
- "Garantía del celular"

### Criterios de aceptación

- La búsqueda retorna documentos relacionados.
- El usuario puede acceder al detalle.

---

# 3. Requisitos no funcionales

Los requisitos no funcionales definen atributos de calidad del sistema.

---

## RNF-001: Seguridad

El sistema debe proteger la información financiera personal del usuario.

Consideraciones:

- Autenticación segura.
- Autorización basada en usuario.
- Protección de información sensible.
- Comunicación cifrada.

---

## RNF-002: Disponibilidad

El sistema debe estar diseñado para mantener disponibilidad adecuada para sus usuarios.

Objetivo inicial:

- Disponibilidad mínima esperada: 99%.

---

## RNF-003: Rendimiento

El sistema debe responder adecuadamente ante operaciones frecuentes.

Consideraciones:

- Consulta de documentos.
- Búsquedas.
- Procesamiento de información.

---

## RNF-004: Escalabilidad

La arquitectura debe permitir crecimiento progresivo.

Debe soportar:

- Mayor cantidad de usuarios.
- Mayor volumen de documentos.
- Nuevas fuentes de información.

---

## RNF-005: Mantenibilidad

El sistema debe seguir buenas prácticas de ingeniería.

Consideraciones:

- Código organizado.
- Pruebas automatizadas.
- Documentación técnica.
- Integración continua.

---

## RNF-006: Privacidad

La información financiera pertenece exclusivamente al usuario.

El sistema debe garantizar:

- Separación de datos entre usuarios.
- Control de acceso.
- Protección de documentos almacenados.

---

# 4. Restricciones iniciales

## Tecnológicas

- Backend desarrollado con Java y Quarkus.
- Aplicación móvil desarrollada con Flutter.
- Base de datos definida durante el diseño arquitectónico.
- Uso de contenedores Docker.
- Integración continua mediante GitHub Actions.

---

## Alcance geográfico inicial

El producto será diseñado inicialmente para usuarios en Perú.

Consideraciones:

- Comprobantes electrónicos peruanos.
- Bancos y billeteras digitales locales.
- Formatos utilizados en el mercado peruano.

---

# 5. Supuestos

- Los usuarios proporcionarán autorización para procesar sus documentos.
- Los documentos pueden contener información incompleta.
- Los modelos OCR pueden requerir validación humana.
- Las integraciones externas dependerán de disponibilidad de APIs.

---

# 6. Estado del documento

Versión:

0.1.0

Estado:

En definición.