# 🚀 INFRASTRUCTURE_DOCKER_SHARED

[![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Aplicación** para crear servicios que permitan la administración de diferentes bases de datos. Para que las bases de datos puedan ser accedidas por este servicio de administración, se debe conectar a la misma red especificada en cada gestor de administración. 

---
<br>

## <a id="inicio-rapido"></a>⚡ Inicio Rápido (5 minutos)

### 1️⃣ Clonar Repositorio

#### Clonar repositorio de GitHub:
```bash
git clone https://github.com/gustavo-0426/infrastructure-docker-compose-shared.git
```

### 2️⃣ Configurar Variables de Entorno

#### Crear o modificar archivo docker-compose\\.env con sus respectivos valores:
```bash
# Configuración de pgAdmin
PGADMIN_EMAIL=admin@admin.com
PGADMIN_PASSWORD=admin123
```

### 3️⃣ Ejecutar Aplicación con Docker Compose

#### Construir y ejecutar:
```bash
docker-compose -f docker-compose/compose.yml up -d
```

#### Verificar contenedores activos:
```bash
docker-compose -f docker-compose/compose.yml ps
```

#### Ver logs en tiempo real:
```bash
docker-compose -f docker-compose/compose.yml logs -f
```

#### Ver logs de un servicio específico:
```bash
docker-compose -f docker-compose/compose.yml logs -f pgadmin
```

#### Acceder a pgAdmin:
- URL: `http://localhost:8080`
- Email: El configurado en `PGADMIN_EMAIL`
- Password: El configurado en `PGADMIN_PASSWORD`

---

## 📝 Agregar Otros Servicios de Administración

Si deseas agregar otros servicios de administración de bases de datos (como **Workbench**, **phpMyAdmin** etc.), simplemente:

1. Agrega el nuevo servicio en `.\docker-compose\compose.yml` siguiendo el ejemplo del servicio pgAdmin
2. Configura las variables de entorno necesarias en el archivo `.env`
3. Sigue los mismos pasos del [Inicio Rápido](#inicio-rapido)

---