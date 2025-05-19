# 🚀 Desafío 7 - Ansible CI/CD

## 🎯 Objetivo

El objetivo de este desafío es implementar un pipeline CI/CD utilizando Jenkins para gestionar el despliegue de los playbooks de Ansible de manera centralizada y segura, evitando el uso de credenciales locales.

## 📝 Escenario

Después de modularizar el proyecto en el Desafío 6, el equipo identificó la necesidad de automatizar el despliegue de los playbooks mediante un pipeline CI/CD. Esto garantiza la ejecución de los playbooks desde un controlador Jenkins, mejorando la seguridad y asegurando que las credenciales solo residan en el entorno controlado.

### 🪧 Beneficios del CI/CD

- 🔒 **Seguridad mejorada:** Las credenciales permanecen exclusivamente en el controlador Jenkins.
- 🌐 **Despliegues automatizados:** El pipeline garantiza que todos los cambios sean gestionados desde el repositorio.
- 📂 **Estrategia de Branches:**
  - **DEV:** Entorno de desarrollo, cambios frecuentes y libertad para probar.
  - **STAGING:** Entorno de pruebas de integración, cambios aplicados solo mediante PR.
  - **MAIN:** Entorno productivo, despliegues aprobados desde STAGING.

## 🚀 Tecnologías Utilizadas

- 🐧 **Linux (VM)** - Entorno de despliegue
- 🛠️ **Ansible** - Configuración como código
- 💻 **Jenkins** - Pipeline CI/CD
- 🌐 **Git** - Control de versiones
- 📂 **GitHub** - Repositorio del proyecto
- ☁️ **Ngrok** - Exposición de Jenkins a internet
