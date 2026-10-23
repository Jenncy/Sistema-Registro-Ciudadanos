# Sistema de Registro de Ciudadanos

Aplicación web desarrollada con **CodeIgniter 4** para administrar información de ciudadanos y catálogos territoriales/académicos relacionados.

## Funcionalidades principales

El sistema incluye operaciones **CRUD** para los siguientes módulos:

- Ciudadanos
- Niveles académicos
- Municipios
- Departamentos
- Regiones

## Tecnologías y requisitos previos

| Componente | Requisito |
| --- | --- |
| Lenguaje | PHP **8.1+** |
| Framework | CodeIgniter 4 |
| Gestor de dependencias | Composer |
| Base de datos recomendada | MySQL/MariaDB |
| Extensiones PHP obligatorias | `intl`, `mbstring` |
| Servidor | Apache/Nginx o servidor de desarrollo de CodeIgniter |

## Instalación desde cero

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/Jenncy/Sistema-Registro-Ciudadanos.git
   ```
2. Entrar al directorio del proyecto:
   ```bash
   cd Sistema-Registro-Ciudadanos
   ```
3. Instalar dependencias:
   ```bash
   composer install
   ```
4. Crear el archivo de entorno a partir del ejemplo:
   ```bash
   cp "env copy" .env
   ```
5. Editar `.env` y configurar:
   - `app.baseURL` (por ejemplo: `http://localhost:8080/`)
   - Credenciales de base de datos (`database.default.*`)
6. Crear/configurar la base de datos usando los recursos disponibles en `app/Database` (migraciones o scripts que se incorporen al proyecto).
7. Levantar el servidor de desarrollo:
   ```bash
   php spark serve
   ```
8. Abrir la aplicación en:
   - `http://localhost:8080`

## Estructura relevante del proyecto

```text
Sistema-Registro-Ciudadanos/
├── app/                 # Lógica de aplicación (controladores, modelos, vistas, config)
│   └── Database/        # Migrations y Seeds
├── public/              # Punto de entrada web (document root)
├── system/              # Núcleo de CodeIgniter 4
├── tests/               # Pruebas automatizadas
├── writable/            # Cache, logs, sesiones y archivos temporales
├── spark                # CLI de CodeIgniter
├── composer.json        # Dependencias y scripts
└── phpunit.xml.dist     # Configuración base de PHPUnit
```

## Rutas y módulos disponibles

Rutas definidas actualmente en `app/Config/Routes.php`:

### Consulta/listado

- `GET /ver_niveles`
- `GET /ver_ciudadanos`
- `GET /ver_municipios`
- `GET /ver_departamentos`
- `GET /ver_regiones`

### Niveles académicos

- `GET /insertar_nivel`
- `GET /actualizar_nivel/{id}`
- `GET /eliminar_nivel/{id}`
- `POST /guardar_nivel`
- `POST /modificar_nivel`

### Ciudadanos

- `GET /insertar_ciudadano`
- `GET /actualizar_ciudadano/{id}`
- `GET /eliminar_ciudadano/{id}`
- `POST /guardar_ciudadano`
- `POST /modificar_ciudadano`

### Municipios

- `GET /insertar_municipio`
- `GET /actualizar_municipio/{id}`
- `GET /eliminar_municipio/{id}`
- `POST /guardar_municipio`
- `POST /modificar_municipio`

### Departamentos

- `GET /insertar_departamento`
- `GET /actualizar_departamento/{id}`
- `GET /eliminar_departamento/{id}`
- `POST /guardar_departamento`
- `POST /modificar_departamento`

### Regiones

- `GET /insertar_region`
- `GET /actualizar_region/{id}`
- `GET /eliminar_region/{id}`
- `POST /guardar_region`
- `POST /modificar_region`

## Pruebas

Puedes ejecutar las pruebas con cualquiera de estos comandos:

```bash
composer test
# o
vendor/bin/phpunit
```

## Seguridad

- No subas el archivo `.env` al repositorio.
- Configura el servidor web para exponer únicamente `public/` como document root.
- Cambia credenciales por defecto antes de desplegar en ambientes compartidos o productivos.

## Licencia

Este proyecto se distribuye bajo licencia **MIT**.
