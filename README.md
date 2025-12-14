# Sistema de Gestión de Productos y Categorías - TECLAB

Este proyecto es una aplicación web desarrollada en **PHP** implementando el paradigma de **Programación Orientada a Objetos (POO)** y el patrón de diseño MVC (Modelo-Vista-Controlador) simplificado. Permite la gestión administrativa (CRUD) de productos y categorías, incluyendo la carga de imágenes.

## 📋 Características

* **Gestión de Productos:** Listado, alta, baja y modificación de productos.
* **Gestión de Categorías:** Administración de las categorías a las que pertenecen los productos.
* **Carga de Imágenes:** Funcionalidad para subir y asociar imágenes a cada producto.
* **Base de Datos Relacional:** Uso de MySQL con claves foráneas para vincular productos y categorías.
* **Arquitectura POO:** Código modularizado utilizando Clases, Herencia y Autoload.

## 🚀 Tecnologías Utilizadas

* **Lenguaje:** PHP 8.2 (Backend)
* **Base de Datos:** MySQL / MariaDB
* **Frontend:** HTML5, CSS3
* **Servidor Web:** Apache (vía XAMPP, WAMP o similar)

## 📂 Estructura del Proyecto

El proyecto está organizado de la siguiente manera para mantener el código limpio y mantenible:

* **`/assets`**: Contiene los recursos estáticos.
    * `/css`: Hojas de estilo (estilos.css).
    * `/img`: Imágenes de los productos y recursos gráficos.
* **`/backend`**: Controladores y Vistas del panel de administración.
    * Archivos `.php` que manejan la lógica de recepción de formularios (`productos.php`, `categorias.php`) y los listados visuales.
* **`/class`**: Núcleo de la lógica de negocio (Modelos).
    * `database.php`: Clase para la conexión (PDO) y consultas genéricas (Select, Insert, Update, Delete).
    * `productos.php`: Clase que gestiona la entidad Producto.
    * `categorias.php`: Clase que gestiona la entidad Categoría.
    * `autoload.php`: Script para la carga automática de clases.
* **`/database`**: Scripts SQL.
    * `database.sql`: Archivo necesario para crear la estructura de la base de datos inicial.

## 🛠️ Instalación y Configuración

Sigue estos pasos para ejecutar el proyecto en tu entorno local:

1.  **Clonar el repositorio** o descargar los archivos en la carpeta pública de tu servidor web (por ejemplo, `C:\xampp\htdocs\MiProyecto`).

2.  **Base de Datos:**
    * Abre tu gestor de base de datos (phpMyAdmin, MySQL Workbench, etc.).
    * Crea una base de datos nueva o ejecuta directamente el archivo que se encuentra en:
        `database/database.sql`
    * *Nota:* El script intenta crear la base de datos llamada `MIPROYECTOCOPIA`.

3.  **Configuración de Conexión:**
    * Verifica las credenciales de conexión en los archivos `class/productos.php` y `class/categorias.php`. Por defecto están configuradas así:
    ```php
    define("HOST", '127.0.0.1');
    define("USER", 'root');
    define("PASS", '');
    define("DB", 'miproyectoCOPIA'); // Asegúrate que coincida con tu BD
    ```

4.  **Ejecución:**
    * Abre tu navegador y ve a: `http://localhost/MiProyecto/`
    * El archivo `index.php` te redirigirá automáticamente al listado de productos.

## 📸 Capturas del Sistema

La estructura de la base de datos relacional es la siguiente:
![Estructura DB](./assets/img/estruct-database.JPG)

Listado de productos funcionando:
![Listado Productos](./assets/img/productos%20list.JPG)

## ✒️ Autores

* **Facundo Coria** - Desarrollo

---
*Proyecto realizado para la práctica universitaria de TECLAB.*
