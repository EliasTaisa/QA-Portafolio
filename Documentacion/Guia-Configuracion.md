# ⚙️ Guía de Configuración - Ambiente de Pruebas

## Herramientas necesarias
- Postman desktop v10.18.12
- Conexión a internet estable
- Cuenta gratuita en reqres.in

## Paso 1: Instalar Postman
1. Ir a https://postman.com
2. Click en "Download the App"
3. Instalar el ejecutable
4. Crear cuenta gratuita o iniciar sesión

## Paso 2: Obtener API Key de reqres.in
1. Ir a https://reqres.in
2. Click en "Generate API Key"
3. Registrarse gratuitamente
4. Copiar la API Key generada

## Paso 3: Importar la colección
1. Abrir Postman
2. Click en "Import" en el panel izquierdo
3. Seleccionar el archivo "reqres-practica-qa.json"
4. Click en "Import"
5. Verificar que aparece la colección "reqres.in - Práctica QA"

## Paso 4: Configurar variables de entorno
1. Click en el ícono de Environments en el panel izquierdo
2. Click en "+" para crear nuevo entorno
3. Nombrar el entorno: "reqres.in - QA"
4. Agregar las siguientes variables:

| Variable | Value |
|----------|-------|
| base_url | https://reqres.in |
| api_key | tu-api-key-aquí |

5. Click en "Save"

## Paso 5: Vincular entorno a la colección
1. Click derecho en la colección "reqres.in - Práctica QA"
2. Click en "Edit"
3. Ir a la pestaña "Authorization"
4. Configurar:
   - Type: API Key
   - Key: x-api-key
   - Value: {{api_key}}
   - Add to: Header
5. Click en "Save"

## Paso 6: Verificar configuración
1. Seleccionar el entorno "reqres.in - QA" en el dropdown superior derecho
2. Abrir el request "GET - Listar usuarios página 1"
3. Click en "Send"
4. Verificar que el Status Code sea 200 OK
5. Si el resultado es correcto el ambiente está listo 

## Solución de problemas comunes
| Problema | Solución |
|----------|----------|
| Status 401 | Verificar que la API Key esté correctamente configurada |
| Status 404 | Verificar que la URL sea correcta |
| Sin respuesta | Verificar conexión a internet |
