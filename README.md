# 🚀 Desafío 7 - Ansible CI/CD

## 🎯 Objetivo

El objetivo de este desafío es implementar un pipeline CI/CD utilizando Jenkins para gestionar el despliegue de los playbooks de Ansible de manera centralizada y segura, evitando el uso de credenciales locales.

## 📝 Escenario

Después de modularizar el proyecto en el Desafío 6, el equipo identificó la necesidad de automatizar el despliegue de los playbooks mediante un pipeline CI/CD. Esto garantiza la ejecución de los playbooks desde un controlador Jenkins, mejorando la seguridad y asegurando que las credenciales solo residan en el entorno controlado.

### ☀️ Beneficios del CI/CD

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

## ⚙️ Procedimiento

1. Actualizar el sistema en la máquina virtual.

![image](https://github.com/user-attachments/assets/f437ea5d-cd74-472b-80d8-8199eb110724)

![image](https://github.com/user-attachments/assets/7658456b-5004-4f2a-81c9-1fd021054ae7)

2. Instalar Git, Ansible, Java y Jenkins.

  - Git
    
![image](https://github.com/user-attachments/assets/e85986fe-69a4-4f3f-b460-349bc2397cd1)

  - Ansible

![image](https://github.com/user-attachments/assets/b953a466-f70f-40e3-adb4-9c5ee5dc6140)
 
  - Java

![image](https://github.com/user-attachments/assets/2508b333-e325-4671-86fe-10fdf3d266eb)

 - Jenkins

![image](https://github.com/user-attachments/assets/e60e4281-2d32-47e8-b466-ad2fda29ef5a)

![image](https://github.com/user-attachments/assets/4b8c9161-85ad-40e5-926e-11075858a4e8)

![image](https://github.com/user-attachments/assets/c4bc9509-e108-4ef7-b88e-826bcacf21e2)

![image](https://github.com/user-attachments/assets/1a4092ac-6703-483a-8c81-e391b1c99505)

![image](https://github.com/user-attachments/assets/6833a6ef-dbd7-4696-a5b7-235707de9c28)

  - Recuperar la contraseña

![image](https://github.com/user-attachments/assets/44fd6b28-50ae-4992-8268-2350bc69d4c9)

3. Clonar el repositorio del proyecto.

![image](https://github.com/user-attachments/assets/d198a562-0602-4d76-a200-917923dcb250)

4. Crear las ramas necesarias: DEV, STAGING, MAIN.

![image](https://github.com/user-attachments/assets/20554296-b5ad-4900-9f2c-36b16c0fdd5e)

  - Hacer un push a cada rama

![image](https://github.com/user-attachments/assets/e2588fd0-d6e0-4575-a7de-7ccea014bac2)

5. Configurar el inventario de Ansible para cada entorno.

![image](https://github.com/user-attachments/assets/79b42268-dde1-445f-8ee9-6eda6506618c)

  - DEV
    
  ![image](https://github.com/user-attachments/assets/71f8fe78-3b8e-4992-872b-c17ba2f8b23a)

  - Staging
    
  ![image](https://github.com/user-attachments/assets/9b18438d-5c72-4a47-9449-b82649079b1b)

  - Main
    
  ![image](https://github.com/user-attachments/assets/eae3e99b-9038-404f-a2ee-cad8e2be5352)

6. Configurar el pipeline en Jenkins para cada rama:

   - Crear un job por entorno.

![image](https://github.com/user-attachments/assets/ae54f5f8-9f20-4ece-8285-685913f107b7)

![image](https://github.com/user-attachments/assets/13540c38-868b-420c-8638-150ac124e78a)

![image](https://github.com/user-attachments/assets/b80511fa-c30b-4254-a872-7bdfc66f6045)

![image](https://github.com/user-attachments/assets/585e4fff-4394-49e6-b7b1-9da74d13ee37)

![image](https://github.com/user-attachments/assets/5bb6c9fd-0f5b-4047-acfb-49f8fa19a6ad)

![image](https://github.com/user-attachments/assets/29ab2ff3-e765-406b-ae61-f40b5e4cc2e3)

![image](https://github.com/user-attachments/assets/9a2d66ac-bf32-4580-a900-111c7de093e8)

   - Integrar el webhook de GitHub con Jenkins.

![image](https://github.com/user-attachments/assets/7d5acf4c-b47b-4b33-9c01-418109ffe9a2)

❗ Para completar la configuración hay que exponer la url de Jenkins a internet usando Ngrok

![image](https://github.com/user-attachments/assets/e07b3baa-7f14-4714-b0f5-518319f36e31)

- Webhook creado

![image](https://github.com/user-attachments/assets/27260c3e-257b-4506-b073-dce7a2b13ed6)

   - Probar los despliegues en cada entorno.




