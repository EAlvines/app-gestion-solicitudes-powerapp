# 🚀 Portal de Gestión de Solicitudes - Power Platform

Solución low-code para automatizar la gestión de solicitudes, eliminando el uso de emails y centralizando la comunicación.

## 🏗️ Arquitectura de la Solución

[Usuario Final] 
       |
       | (Registra solicitud / Consulta estado)
       v
+--------------------------------+
|      Power Apps (Frontend)     |
|                                |
| - Formulario de solicitudes    |
| - Galería de vistas            |
| - Roles: Usuario & Admin       |
+--------------------------------+
       |  [Conectores]
       |  (Leer/Escribir datos)
       v
+--------------------------------+
|   SharePoint List (Backend)    |
|                                |
| - Lista "Solicitudes"          |
| - Campos: Titulo, Estado,      |
|   Asignado, Fecha, etc.        |
+--------------------------------+
       |  [Trigger]
       |  (Cuando se modifica un ítem)
       v
+--------------------------------+
|    Power Automate (Flujos)     |
|                                |
| 1. Flujo 1:                    |
|    - Email confirmación        |
|      al usuario                |
|                                |
| 2. Flujo 2:                    |
|    - Email notificación        |
|      al asignado               |
+--------------------------------+
       |
       | (Envía correos)
       v
  [Office 365 Outlook]

## ⚙️ Componentes Utilizados
- **Frontend:** Power Apps (Con roles de Usuario y Administrador)
- **Backend/Database:** SharePoint List
- **Automation:** Power Automate (Flujos para notificaciones por email)
- **Security:** Permisos granularizados a nivel de app y de lista de SharePoint.

## 🎯 Funcionalidades
- Registro de solicitudes por parte de usuarios.
- Panel de administración para asignar responsables y actualizar estados.
- Notificaciones automáticas por email (Confirmación y actualizaciones).

## 📸 Vistas de la Aplicación

<img width="1881" height="1009" alt="image" src="https://github.com/user-attachments/assets/eacee8a5-13ef-4a0b-a90d-fc57ae642e29" />

<img width="1263" height="712" alt="image" src="https://github.com/user-attachments/assets/02e23350-8240-4c4f-bbf5-9bc6790752d3" />

<img width="1259" height="713" alt="image" src="https://github.com/user-attachments/assets/f629ad52-7759-40c9-8859-69a455229ca6" />

<img width="1250" height="703" alt="image" src="https://github.com/user-attachments/assets/e7d1d5dd-fc51-42b6-85e5-66dc3016a340" />
