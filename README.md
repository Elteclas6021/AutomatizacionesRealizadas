# Automatizaciones con Power Automate

## 1. Correspondencia Word/HTML a PDF personalizado

### ¿Qué hace?
Lee una tabla de Excel con información de empleados y genera automáticamente 
un documento PDF personalizado para cada persona, enviándolo por correo electrónico.

### Flujo del proceso
1. **Trigger manual** — Se ejecuta cuando se activa manualmente
2. **List rows** — Lee los registros de la tabla Excel
3. **Apply to each** — Itera sobre cada empleado
4. **Run script** — Personaliza el documento con los datos del empleado
5. **Get file content** — Obtiene el archivo generado
6. **Create file** — Crea el archivo en SharePoint/OneDrive
7. **Convert file** — Convierte el documento a PDF
8. **Send email** — Envía el PDF al correo del empleado

### Tecnologías usadas
- Power Automate
- Microsoft Excel (fuente de datos)
- SharePoint / OneDrive
- Office Scripts
- Outlook (envío de correos)

### Captura del flujo
![Flujo Power Automate](captura_flujo.png)


## 2. Poblar Tablas de un Entorno a Otro (Dataverse)

### ¿Qué hace?
Migra datos entre entornos de Dataverse automáticamente, leyendo registros 
de un entorno origen y creándolos en el entorno destino. Útil para sincronización 
entre entornos de desarrollo, pruebas y producción.

### Flujo del proceso
1. **Trigger manual** — Se ejecuta cuando se activa manualmente
2. **List rows** — Lee los registros del entorno origen en Dataverse
3. **Apply to each** — Itera sobre cada registro encontrado
4. **List rows from selected environment** — Verifica los datos del entorno destino
5. **Add a new row to selected environment** — Inserta el registro en el entorno destino

### Caso de uso
Migración y sincronización de data maestra entre ambientes de 
Power Platform (DEV → QA → PROD).

### Tecnologías usadas
- Power Automate
- Microsoft Dataverse
- Power Platform (múltiples entornos)

### Captura del flujo
![Flujo Dataverse](captura_dataverse.png)
