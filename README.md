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

```plaintext
PythonMCP/
│
├── Dockerfile
├── docker-compose.yml
├── data/        # Aquí vivirá tu código (montado)
└── .vscode/     # Persistencia de config/extensions

