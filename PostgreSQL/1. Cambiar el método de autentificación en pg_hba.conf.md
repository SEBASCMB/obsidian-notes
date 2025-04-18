## 📝 **¿Qué es `pg_hba.conf`?**

define **cómo** **se** _El archivo `pg_hba.conf`define **cómo se autentican los usuarios** al conectarse a PostgreSQL . Aquí te explico_al conectarse a PostgreSQL. Aquí te explico cómo **ubicarlo, editarlo, cambiar el método de autenticación** y reiniciar el servicio para aplicar los cambios.

📍 1. Localizar el archivopg_hba.conf

🔎 Ubicaciones comunes:

Linux :

- `/etc/postgresql/<versión>/main/pg_hba.conf`

- `/var/lib/pgsql/data/pg_hba.conf`

WIndows :

`C:\Program Files\PostgreSQL\<versión>\data\pg_hba.conf`

## 🧰 Buscar el archivo en Linux:

```linux
find / -name pg_hba.conf 2>/dev/null
```

## ✏️ 2. Abrir el archivo para edición

🐧 Linux:

```linux
sudo nano /ruta/a/pg_hba.conf
```

 🪟 windows:
- Usa **Notepad++** o **Bloc de notas** con permisos de **Administrador** .

## 🧬 3. Estructura del archivo

```linux
# TYPE  DATABASE  USER  ADDRESS      METHOD
local   all       all               peer
host    all       all   0.0.0.0/0   md5
```

### 🧩Campos:

- TIPO : Tipo de conexión ( `local`, `host`, etc.).

- DATABASE : Base de datos a la que aplica la regla ( `all` para todas).

- USUARIO : Usuario afectado ( `all` para todos).

- DIRECCIÓN : IP permitida (solo en `host`).

- MÉTODO : Método de autenticación ( `md5`, `peer`, `trust`, etc.).

## 🔄 4. Cambiar el método de autenticación

### Métodos comunes:

- 🔐 `md5`: Requiere contraseña (recomendado).
    
- 🤝 `peer`: El usuario del SO debe coincidir con el de PostgreSQL.
    
- 🚨 `trust`: Sin contraseña ( **no recomendado** ).

🔁 Ejemplo de uso `md5`:

```linux
local   all   all               md5
host    all   all   0.0.0.0/0   md5
```

## 💾 5. Guardar y reiniciar PostgreSQL

### 🧷 Guardar el archivo:

- En `nano`: `Ctrl + O`→ `Enter`→`Ctrl + X`
    
- En otros editores: simplemente **guardar** .
    
### 🔁 Reiniciar el servicio PostgreSQL:

#### 🔧 Linux (systemd):

```linux
sudo systemctl restart postgresql
```

#### 🪟 Windows:

- Desde el panel de **Servicios**
    
- El uso de la herramienta **pgAdmin** o **Stack Builder** .

## ✅ 6. Verificar la conexión

### 🌐 Conectarse desde la terminal:

```linux
	psql -U <usuario> -d <base_de_datos>

```

### 🔑 Cambiar la contraseña de un usuario (si usas `md5`):

```linux
ALTER USER nombre_usuario WITH PASSWORD 'tu_clave_segura';

```
