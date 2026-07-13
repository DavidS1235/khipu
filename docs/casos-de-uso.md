# Casos de Uso del Proyecto Khipu

## 1. Introducción

Este documento describe las principales interacciones entre los usuarios y la plataforma Khipu.

Los casos de uso representan escenarios donde el usuario utiliza las capacidades del sistema para construir y consultar su memoria financiera personal.

---

# Actores del sistema

## Usuario

Persona que utiliza Khipu para almacenar, organizar y consultar su información financiera personal.

---

## Servicios externos (futuro)

Sistemas externos que pueden proporcionar información financiera:

- Correo electrónico.
- Bancos.
- Billeteras digitales.
- Servicios OCR.
- Servicios de inteligencia artificial.

---

# UC-001: Crear cuenta de usuario

## Descripción

El usuario crea una cuenta para acceder a su espacio financiero personal.

## Actor principal

Usuario.

## Flujo principal

1. El usuario ingresa sus datos de registro.
2. El sistema valida la información.
3. El sistema crea la cuenta.
4. El usuario obtiene acceso a Khipu.

## Resultado esperado

El usuario tiene una cuenta personal dentro de la plataforma.

---

# UC-002: Iniciar sesión

## Descripción

El usuario accede a su memoria financiera.

## Actor principal

Usuario.

## Flujo principal

1. El usuario ingresa sus credenciales.
2. El sistema valida la identidad.
3. El sistema permite el acceso.

## Resultado esperado

El usuario puede acceder a su información financiera.

---

# UC-003: Registrar documento financiero

## Descripción

El usuario agrega un documento financiero a su memoria.

## Actor principal

Usuario.

## Precondiciones

- Usuario autenticado.
- Documento disponible.

## Flujo principal

1. El usuario selecciona un documento.
2. El sistema recibe el archivo.
3. El sistema almacena el documento.
4. El sistema inicia el procesamiento.

## Resultado esperado

El documento queda registrado dentro de la memoria financiera.

---

# UC-004: Procesar documento mediante OCR

## Descripción

El sistema analiza un documento para extraer información financiera.

## Actor principal

Sistema.

## Flujo principal

1. El documento es enviado al motor OCR.
2. El texto es extraído.
3. El sistema identifica información relevante.
4. Se genera información financiera estructurada.

## Información obtenida

- Tipo de documento.
- Fecha.
- Comercio.
- Monto.
- Número de comprobante.

## Resultado esperado

El documento se convierte en información consultable.

---

# UC-005: Revisar información extraída

## Descripción

El usuario valida la información obtenida automáticamente.

## Actor principal

Usuario.

## Flujo principal

1. El usuario revisa los datos extraídos.
2. Corrige información incorrecta.
3. Confirma los datos.

## Resultado esperado

La información financiera queda validada.

---

# UC-006: Consultar memoria financiera

## Descripción

El usuario visualiza su historial financiero.

## Actor principal

Usuario.

## Flujo principal

1. El usuario accede a su historial.
2. El sistema muestra eventos financieros ordenados.
3. El usuario selecciona un evento.

## Resultado esperado

El usuario puede consultar su información financiera histórica.

---

# UC-007: Buscar información financiera

## Descripción

El usuario busca información específica dentro de su memoria financiera.

## Actor principal

Usuario.

## Ejemplos

El usuario puede buscar:

- "Compra de laptop"
- "Boleta de enero"
- "Restaurante"
- "Garantía celular"

## Flujo principal

1. El usuario ingresa una búsqueda.
2. El sistema analiza la consulta.
3. El sistema devuelve documentos relacionados.

## Resultado esperado

El usuario encuentra información financiera relevante.

---

# UC-008: Categorizar transacción

## Descripción

El usuario organiza sus movimientos financieros mediante categorías.

## Actor principal

Usuario.

## Categorías iniciales

- Alimentación.
- Transporte.
- Vivienda.
- Tecnología.
- Entretenimiento.
- Salud.
- Educación.

## Resultado esperado

La información financiera queda organizada.

---

# UC-009: Consultar información mediante IA (futuro)

## Descripción

El usuario realiza preguntas utilizando lenguaje natural.

## Actor principal

Usuario.

## Ejemplos

Usuario:

> "¿Cuánto gasté en comida este mes?"

Sistema:

> "Durante julio gastaste S/ 420 en alimentación."

Usuario:

> "Encuentra la boleta de mi laptop."

Sistema:

> "Encontré una compra realizada en enero del 2026."

## Resultado esperado

El usuario interactúa con su memoria financiera de forma natural.

---

# UC-010: Importar información automáticamente (futuro)

## Descripción

El sistema obtiene información financiera desde fuentes externas autorizadas.

## Posibles fuentes

- Gmail.
- Outlook.
- Bancos.
- Billeteras digitales.

## Resultado esperado

La memoria financiera se actualiza automáticamente.

---

# Relación entre casos de uso y versiones

| Caso de uso | Versión |
|---|---|
| Crear cuenta | MVP |
| Iniciar sesión | MVP |
| Registrar documento | MVP |
| Procesar OCR | MVP |
| Revisar información extraída | MVP |
| Consultar memoria financiera | MVP |
| Buscar información | MVP |
| Categorizar transacciones | MVP |
| Consultas IA | Futuro |
| Importación automática | Futuro |

---

# Estado del documento

Versión:

0.1.0

Estado:

En definición.