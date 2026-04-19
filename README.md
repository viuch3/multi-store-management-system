# Multi Store Management System 

## Descripción

Multi-store-magement-system es una plataforma de gestión diseñada para permitir a un Area Manager supervisar y administrar múltiples tiendas de forma remota. El sistema centraliza información clave como ventas, inventario, desempeño de tiendas y gestión de personal, facilitando la toma de decisiones basada en datos.

El proyecto está orientado al sector retail y busca resolver los problemas de visibilidad, control y coordinación en entornos con múltiples puntos de venta.

---

## Problema

En operaciones retail con múltiples tiendas, los Area Managers enfrentan desafíos como:

* Falta de visibilidad en tiempo real del rendimiento de cada tienda
* Dependencia de reportes manuales y descentralizados
* Dificultad para comparar métricas entre tiendas
* Control limitado del inventario
* Comunicación poco estructurada entre niveles operativos

Este sistema propone una solución centralizada para mejorar la eficiencia operativa.

---

## Objetivos

* Centralizar la gestión de múltiples tiendas en una sola plataforma
* Permitir el monitoreo remoto del rendimiento
* Facilitar el análisis de ventas e indicadores clave (KPIs)
* Mejorar la gestión de inventario
* Optimizar la comunicación entre Area Managers y Store Managers
* Proveer una base escalable para futuras integraciones

---

## Usuarios del sistema

### Area Manager

* Supervisa múltiples tiendas
* Analiza métricas y reportes
* Define objetivos de rendimiento
* Gestiona Store Managers

### Store Manager

* Administra una tienda específica
* Supervisa al equipo de ventas
* Gestiona inventario local
* Reporta al Area Manager

### Vendedor

* Registra ventas
* Interactúa con el sistema de forma limitada

---

## Funcionalidades principales

* Dashboard de rendimiento por tienda
* Registro de ventas con detalle por producto
* Gestión de inventario y movimientos
* Administración de usuarios y roles
* Definición y seguimiento de objetivos (KPIs)
* Sistema de mensajería interna
* Notificaciones
* Auditoría de acciones del sistema

---

## Modelo del sistema

El sistema está basado en un modelo orientado a objetos que incluye:

* Usuario (con roles: Area Manager, Store Manager, Vendedor)
* Tienda
* Venta y Detalle de Venta
* Producto y Categoría
* Inventario y movimientos
* Objetivos y resultados
* Mensajes y notificaciones
* Auditoría

Diagrama completo disponible en:

[Ver diagrama de clases](docs/diagrama-clases.md)

---

## Arquitectura

El sistema sigue una arquitectura por capas:

* Capa de presentación (Frontend)
* Capa de aplicación (Backend API)
* Capa de datos (Base de datos)

---

## Backend

El backend está desarrollado en Python utilizando:

* Django
* Django REST Framework

Organización del backend:

```plaintext
backend/
│
├── config/        → Configuración principal
├── apps/
│   ├── usuarios/  → Gestión de usuarios y roles
│   ├── tiendas/   → Gestión de tiendas
│   ├── ventas/    → Ventas y transacciones
│   ├── inventario/→ Productos e inventario
```

---

## Estructura del proyecto

```plaintext
docs/        → Documentación del sistema
backend/     → API y lógica de negocio
frontend/    → Interfaz de usuario
database/    → Modelo y scripts de base de datos
```

---

## Tecnologías

* Python
* Django
* Django REST Framework
* PostgreSQL 
* Git y GitHub

---

## Estado del proyecto

El proyecto se encuentra en fase de desarrollo inicial. Actualmente se está implementando el backend y el modelo de datos basado en el diagrama de clases.

---

## Escalabilidad futura

El sistema está diseñado para soportar:

* Integración con sistemas de punto de venta (POS)
* Aplicación móvil
* Reportes avanzados y analítica
* Notificaciones en tiempo real
* Gestión avanzada de empleados

---

## Instalación (backend)

```bash
git clone https://github.com/viuch3/multi-store-management-system
cd backend

python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate

pip install -r requirements.txt

python manage.py migrate
python manage.py runserver
```

---

