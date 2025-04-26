# PythonMCP

Implementación de un servidor MCP (Model Context Protocol) en Python, totalmente dockerizado y listo para desarrollo y despliegue moderno.

## Descripción

Este repositorio proporciona una arquitectura base para crear y ejecutar un servidor MCP utilizando Python, con un enfoque en portabilidad y facilidad de desarrollo.  
Incluye todo lo necesario para levantar tu entorno en cuestión de minutos, sin instalaciones adicionales en tu máquina local.

Entre las características principales:

- **Desarrollo portable:** Todo el entorno se ejecuta en contenedores Docker.
- **Entorno de desarrollo integrado:** Incluye [code-server](https://github.com/coder/code-server) para utilizar Visual Studio Code directamente desde el navegador.
- **Persistencia de datos y configuración:** Separación de volúmenes para el código fuente y la configuración de VS Code.
- **Fácil de extender:** Base ideal para proyectos MCP, APIs o microservicios en Python.

## Estructura básica

La estructura de carpetas y archivos del proyecto está pensada para maximizar la portabilidad y facilitar el desarrollo con Docker y Visual Studio Code (code-server).

```plaintext
PythonMCP/
│
├── Dockerfile            # Archivo para construir la imagen personalizada del entorno (Python, code-server, etc)
├── docker-compose.yml    # Orquestador de servicios y volúmenes en Docker
├── data/                 # Aquí vivirá tu código (montado)
└── .vscode/              # Persistencia de config/extensions
```

- **Dockerfile** y **docker-compose.yml**  
  Se encuentran directamente en la raíz del proyecto. Aquí defines cómo se construye el contenedor y cómo se levantan los servicios, asegurando que cualquier persona pueda clonar el repositorio y ejecutar el entorno con un solo comando.

- **data/**  
  Es el directorio donde escribirás y almacenarás tu código fuente de Python y otros archivos del servidor MCP. Este folder se monta como un volumen en Docker, por lo que tus cambios quedan guardados incluso si eliminas o vuelves a crear los contenedores.

- **.vscode/**  
  Carpeta usada para persistir configuraciones, settings y extensiones personalizadas de Visual Studio Code (code-server). Así tu entorno de desarrollo se mantiene tal como lo dejes, entre distintos inicios y equipos.
