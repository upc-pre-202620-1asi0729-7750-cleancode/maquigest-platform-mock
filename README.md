# MaquiGest Platform Mock

API REST simulada desarrollada para el proyecto académico **MaquiGest**, correspondiente al curso de Aplicaciones Open Source de la Universidad Peruana de Ciencias Aplicadas (UPC).

## 1. Descripción del proyecto

**MaquiGest Platform Mock** es una API REST simulada que permite realizar pruebas, integrar funcionalidades y demostrar el funcionamiento de la aplicación web MaquiGest durante sus primeras etapas de desarrollo.

Esta API proporciona información ficticia relacionada con la gestión de equipos de maquinaria, alquileres, suscripciones, mantenimientos e incidencias.

Su propósito principal es facilitar la integración del frontend con servicios REST sin depender inicialmente de un backend real.

**Importante:** este repositorio no corresponde al backend definitivo. La implementación real se desarrolla de manera independiente en `maquigest-platform`, utilizando Java, Spring Boot, MySQL, Domain-Driven Design (DDD), CQRS y arquitectura hexagonal.

## 2. Tecnologías utilizadas

- **Node.js:** entorno de ejecución de JavaScript.
- **JavaScript:** lenguaje utilizado para implementar el servidor.
- **JSON Server:** herramienta para simular servicios REST.
- **JSON:** formato utilizado para almacenar los datos ficticios.
- **Git y GitHub:** herramientas de control de versiones y colaboración.

## 3. Estructura del proyecto

```text
maquigest-platform-mock/
├── .gitignore
├── package.json
├── README.md
├── seed.json
└── server.js
```

### Descripción de los archivos

| Archivo | Descripción |
|---|---|
| `server.js` | Implementa el servidor y los endpoints de la API simulada. |
| `seed.json` | Contiene los datos iniciales utilizados en las demostraciones. |
| `package.json` | Define las dependencias y los scripts de ejecución. |
| `.gitignore` | Excluye dependencias y archivos que no deben versionarse. |
| `README.md` | Contiene la documentación del proyecto. |

## 4. Instalación y ejecución

### 4.1. Requisitos previos

Para ejecutar el proyecto localmente, es necesario contar con:

- Node.js.
- npm.
- Git.

### 4.2. Clonar el repositorio

```bash
git clone https://github.com/upc-pre-202620-1asi0729-7750-cleancode/maquigest-platform-mock.git
```

Ingresar al directorio:

```bash
cd maquigest-platform-mock
```

### 4.3. Instalar dependencias

```bash
npm install
```

### 4.4. Ejecutar la API

```bash
npm start
```

El servidor utiliza el puerto definido mediante la variable de entorno `PORT`. Si no se especifica uno, utiliza el puerto predeterminado configurado en el proyecto.

Para ejecutar localmente en un puerto específico, desde PowerShell:

```powershell
$env:PORT = "3101"
npm start
```

## 5. Endpoints de la API

Los principales recursos se encuentran disponibles bajo el prefijo:

`/api/v1`

### 5.1. Verificación del servicio

| Método | Endpoint | Descripción |
|---|---|---|
| GET | `/health` | Verifica el estado de funcionamiento del servidor. |

### 5.2. Autenticación simulada

| Método | Endpoint | Descripción |
|---|---|---|
| POST | `/api/v1/authentication/sign-in` | Simula el inicio de sesión de un usuario. |
| POST | `/api/v1/authentication/sign-up` | Simula el registro de una nueva cuenta. |

Los mecanismos de autenticación implementados son únicamente demostrativos y no deben utilizarse como un sistema de seguridad productivo.

### 5.3. Recursos REST

La API simulada contempla los siguientes recursos:

| Recurso | Descripción |
|---|---|
| `profiles` | Información de perfiles de usuario. |
| `equipment-categories` | Categorías de equipos de maquinaria. |
| `equipment` | Información de equipos registrados. |
| `rental-requests` | Solicitudes de alquiler. |
| `rentals` | Operaciones y registros de alquiler. |
| `deliveries` | Entregas de equipos. |
| `equipment-returns` | Devoluciones de equipos. |
| `subscription-plans` | Planes de suscripción disponibles. |
| `user-subscriptions` | Suscripciones de los usuarios. |
| `maintenances` | Registros de mantenimiento. |
| `incidents` | Incidencias relacionadas con los equipos. |

Las operaciones disponibles para cada recurso dependen de su configuración en el servidor simulado.

## 6. Gestión de datos

El archivo `seed.json` contiene los registros ficticios utilizados para inicializar la API.

Durante la ejecución, el servidor utiliza almacenamiento temporal para gestionar las operaciones solicitadas por el frontend.

Por esta razón, los cambios realizados durante las pruebas pueden perderse cuando el servicio se reinicia o vuelve a desplegarse.

Las cuentas creadas mediante el registro simulado también son temporales.

## 7. Limitaciones de la API simulada

Esta implementación presenta las siguientes limitaciones:

- No utiliza una base de datos MySQL persistente.
- No implementa un sistema real de autenticación y autorización mediante JWT.
- No representa la arquitectura definitiva del backend.
- No garantiza la conservación permanente de los registros.
- No está diseñada para entornos productivos.
- Debe utilizarse únicamente con información ficticia de demostración.

Estas limitaciones serán abordadas mediante el desarrollo del backend real de MaquiGest.

## 8. Estrategia de control de versiones

El repositorio utiliza **GitFlow** para organizar el desarrollo y controlar la publicación de versiones estables.

| Rama | Propósito |
|---|---|
| `main` | Contiene las versiones estables del proyecto. |
| `develop` | Integra las funcionalidades desarrolladas. |
| `feature/*` | Permite implementar funcionalidades o mejoras individuales. |
| `release/*` | Se utiliza para preparar las versiones estables. |

### Versión inicial

**v1.0.0:** primera versión estable de la API simulada, con los recursos principales, autenticación demostrativa y documentación inicial.

## 9. Repositorios relacionados

El proyecto MaquiGest está organizado en repositorios independientes:

- **maquigest-webapp:** aplicación web desarrollada con Angular.
- **maquigest-platform:** backend real desarrollado con Spring Boot.
- **maquigest-platform-mock:** API REST simulada.
- **maquigest-website:** página de presentación del proyecto.
- **maquigest-report:** documentación académica y evidencias del desarrollo.

Esta separación permite organizar los componentes del sistema y mantener independientes sus responsabilidades.

## 10. Propósito académico

MaquiGest Platform Mock forma parte de las evidencias de desarrollo del proyecto MaquiGest.

Su repositorio conserva el historial de implementación, la organización mediante GitFlow y la primera versión estable de los servicios simulados.

El desarrollo posterior de la plataforma real permitirá incorporar la persistencia de datos, seguridad, reglas de negocio y patrones arquitectónicos requeridos por el proyecto académico.