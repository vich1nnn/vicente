# Vicente
# 🌌 Orion SaaS — Sistema de Gestión Comercial & POS de Alta Eficiencia

> **Orion** es una plataforma web y ecosistema móvil de vanguardia diseñado para modernizar, automatizar y escalar las operaciones de retail y venta comercial. Desarrollado originalmente para optimizar la operación de la cadena de tiendas de calzado **Cmoran**, Orion evoluciona desde un MVP de Proyecto de Título hacia un software multi-empresa (SaaS) con proyección nacional e internacional.

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Python](https://img.shields.io/badge/Python-3.12-blue.svg?logo=python&logoColor=white)](https://python.org)
[![React](https://img.shields.io/badge/React-18-blue.svg?logo=react&logoColor=white)](https://react.dev)

---

## 🚀 El Dolor Operativo vs. La Solución Orion

En el retail tradicional (y bajo sistemas como Bsale), procesos clave como la **Auditoría de Inventarios** y el **Control de Cambios** se ejecutan de manera arcaica: anotando a lápiz y papel para luego transcribir manualmente a hojas de cálculo de Excel.

* **El Problema:** El flujo tradicional de toma de inventario consume hasta **2 días de trabajo continuo**, generando un alto nivel de errores humanos, estrés operativo, duplicación de tareas y descuadraturas ciegas. El control de cambios se gestiona en cuadernos físicos de forma propensa a fraudes.
* **La Solución Orion:** Digitalización instantánea a través de una interfaz web responsive adaptada a dispositivos móviles. El personal escanea el calzado directo en bodega usando la cámara del smartphone o lectores bluetooth, reduciendo un proceso crítico de **2 días a solo 2-3 horas**.

### 📊 Comparativa de Eficiencia

| Proceso | Flujo Tradicional (Papel/Excel) | Ecosistema Orion |
| :--- | :--- | :--- |
| **Conteo de Inventario** | 2 días (48 horas aproximadas) | **2 - 3 Horas** |
| **Registro de Datos** | Manual con lápiz y transcripción posterior | **Automático (Escaneo de código de barras)** |
| **Margen de Error** | Alto (Inconsistencias de lectura manual) | **Mínimo (Validación digital directa)** |
| **Consolidación** | Tablas de Excel propensas a corrupción | **Base de Datos Relacional en Tiempo Real** |
| **Verificación** | Lenta y posterior al cierre del conteo | **Instantánea (Pre-cuadratura en vivo)** |

---

## ✨ Características Principales

### 📦 1. Módulo de Auditoría de Inventario Express
* **Modo Conteo Móvil:** Escaneo directo mediante el celular en las sucursales.
* **Pre-cuadratura Automática:** El sistema compara el stock físico real contra el stock teórico reportado por el backend o la API de origen.
* **Alertas de Descuadratura:** Panel limpio (UI estilo Linear/Stripe) que expone variaciones exactas de tallas y modelos para aprobación gerencial.

### 💳 2. Punto de Venta (POS) & Facturación Electrónica (SII)
* **Emisión de DTE Directa:** Generación instantánea de boletas y facturas electrónicas integradas con las normativas fiscales vigentes (SII en Chile).
* **Diseño Marca Blanca:** Inyección dinámica del logotipo personalizado de cada empresa o sucursal en el encabezado de los comprobantes y archivos PDF generados.

### 🔄 3. Control Automatizado de Cambios (Anti-Fraude)
* **Digitalización del Cuaderno:** Registro automatizado de productos entrantes, salientes y diferencias de dinero.
* **Validación Rigurosa de Políticas:** Bloqueo automatizado del sistema si un cliente supera el límite de **2 cambios dentro de un periodo de 30 días**.
* **Ticket de Cambio Inteligente:** Generación de tickets estilizados con códigos QR únicos legibles en cualquier sucursal interconectada.

### 🔗 4. Arquitectura de Sincronización (Migración Híbrida)
* Conectividad robusta via API REST para interactuar de forma transparente con el sistema heredado (Bsale), permitiendo operar paralelamente en tiendas piloto sin interrumpir la contabilidad de la empresa madre.

---

## 🛠️ Arquitectura y Stack Tecnológico

Orion se construye sobre una infraestructura moderna, desacoplada y altamente escalable:

* **Frontend:** React + Next.js (Interfaces ultra-rápidas, minimalistas, modo oscuro nativo, estilizado con **Tailwind CSS** y componentes de alto nivel).
* **Backend:** API REST robusta implementada en Python utilizando **Django** (o alternativas de alto rendimiento como FastAPI).
* **Base de Datos:** PostgreSQL (Modelado relacional estricto optimizado para el control transaccional de múltiples sucursales, productos y stock por tallas/SKU) junto a Redis para caché.
* **Infraestructura Cloud:** Compatible con Supabase (Auth, Base de Datos administrada y Storage) o despliegues dedicados en Amazon Web Services (AWS RDS & EC2).

---

## 📐 Diseño del Modelo Relacional (Esquema BD)

El núcleo de datos está optimizado para el manejo de variantes de productos (Tallas/SKUs) y el control histórico de transacciones comerciales:
