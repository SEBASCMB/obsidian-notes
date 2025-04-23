📦 Información del sistema

Este comando devuelve la versión exacta de PostgreSQL que estás utilizando, junto con información del compilador y arquitectura. Es útil para validar compatibilidad con ciertos comandos o extensiones, y cuando reportas errores o trabajas en entornos colaborativos.

```sql
SELECT VERSION();
```
***Muestra la versión actual de PostgreSQL.***

🆘 Ayuda

```sql

\h             -- Muestra ayuda general
\h comando     -- Muestra ayuda sobre un comando específico (ej: \h SELECT)

```

`\h`  es tu primer aliado cuando estás aprendiendo SQL. Te da acceso directo a la documentación integrada de PostgreSQL, sin necesidad de salir de la consola. Si olvidas cómo usar `INSERT`, por ejemplo, simplemente haces `\h INSERT.

🗃 Bases de datos

```sql
\l             -- Lista todas las bases de datos
\c nombre_db   -- Conectarse a una base de datos específica

```

Estos comandos te permiten visualizar todas las bases de datos disponibles y cambiar de contexto dentro del servidor. Es útil cuando gestionas múltiples entornos o deseas moverte entre bases en desarrollo, pruebas o producción.

📂 Esquemas y objetos

```sql
\dn            -- Lista los esquemas
\dt            -- Lista las tablas del esquema actual
\dv            -- Lista las vistas
\df            -- Lista las funciones
\du            -- Lista los roles/usuarios

```

Estos comandos son esenciales para explorar la estructura interna de tu base de datos. Si acabas de conectarte a una base que no creaste tú, esto te ayuda a entender su arquitectura rápidamente.

💾 Editor y archivos

```sql
\e             -- Abre el editor de texto por defecto
\ef            -- Abre el editor para funciones
\i archivo.sql -- Ejecuta comandos desde un archivo
\o archivo.log -- Guarda la salida en un archivo
\q             -- Cierra la consola psql

```

Con estos comandos puedes trabajar más cómodamente: editar funciones complejas, ejecutar scripts que ya tienes guardados o guardar la salida para compartir resultados o debuggear más adelante. Perfecto si trabajas con varios scripts o haces respaldo de tus consultas.


⏱ Ejecución y monitoreo

```sql 
\g             -- Ejecuta el último comando
\s             -- Muestra el historial de comandos
\timing        -- Activa/desactiva el tiempo de ejecución de comandos

```

Aquí tienes herramientas para trabajar más eficientemente: puedes re-ejecutar un comando sin volver a escribirlo, revisar qué has hecho y medir cuánto tiempo toma una consulta (muy útil al optimizar).

### 🛠 SQL Básico

🏗 Crear base de datos y tablas

```sql
CREATE DATABASE nombre_db;

CREATE TABLE nombre_tabla (
    columna1 tipo,
    columna2 tipo,
    ...
);

```

➕ Insertar datos

```sql

INSERT INTO nombre_tabla (columna1, columna2)
VALUES ('dato1', 'dato2');

```

Usado para cargar datos en tu tabla. Puedes hacer inserciones únicas o múltiples (con varias líneas `VALUES`). Ideal cuando estás haciendo pruebas o registrando nuevos elementos.

🔍 Consultar datos

```sql
SELECT * FROM nombre_tabla;

-- Ejemplo con condiciones
SELECT columna FROM nombre_tabla WHERE condicion;

```

Este comando es el más usado del lenguaje SQL. Te permite consultar datos, aplicar filtros (WHERE), ordenar resultados `(ORDER BY)`, y más. Aquí es donde realmente empieza el análisis de la información.

🔁 Actualizar datos
```sql

UPDATE nombre_tabla
SET columna = 'nuevo_valor'
WHERE condicion;

```

Ideal para corregir errores o cambiar el estado de un registro. Es muy importante siempre usar una `condicion` para evitar modificar todos los registros de la tabla por accidente

❌ Eliminar datos

```sql
DELETE FROM nombre_tabla
WHERE condicion;

```

Permite eliminar registros específicos. Igual que con `UPDATE`, es fundamental usar` WHERE`, o podrías borrar toda tu tabla. También se puede usar `TRUNCATE` si quieres eliminar todos los registros sin condición.


