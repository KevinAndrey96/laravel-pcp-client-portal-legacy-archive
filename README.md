# PCP: portal Laravel de clientes industriales (archivo histórico)

![Estado: archivo histórico](https://img.shields.io/badge/Estado-archivo%20hist%C3%B3rico-lightgrey) ![Laravel 8](https://img.shields.io/badge/Laravel%208-FF2D20) ![PHP 7.4+](https://img.shields.io/badge/PHP%207.4%2B-777BB4) ![MySQL](https://img.shields.io/badge/MySQL-4479A1)

> [!NOTE]
> Código original del portal B2B de PCP que conectaba distribuidores, ferreterías y clientes industriales (2022). Evolucionó a partir del portal de distribuidores. El producto continúa en **[pcp-industrial-wholesale-ecommerce](https://github.com/KevinAndrey96/pcp-industrial-wholesale-ecommerce)**, que reúne todos sus componentes con documentación actualizada.

## Qué contiene

- Listas de precios por cliente, asignación de lista a cada usuario y catálogo con importación y exportación a Excel.
- Pedidos con ciudad de entrega, cambio de estado, devoluciones y transferencias.
- Cotizaciones y documentos en PDF con DomPDF.
- Gestión de distribuidores y ferreterías, su asociación e importación masiva de usuarios.
- Usuarios con documento de identidad y cambio de contraseña.

## Stack original

| Componente | Tecnología |
| :--- | :--- |
| Framework | Laravel 8 |
| Lenguaje | PHP 7.4 u 8.0 |
| Base de datos | MySQL |
| Librerías | Laravel Excel, DomPDF, BBCode, Laravel Mix |

## Ejecutarlo localmente

```bash
cp .env.example .env    # completa DB_* y MAIL_* con valores locales
composer install        # vendor/ no se versiona
php artisan key:generate
php artisan migrate
php artisan serve       # http://localhost:8000
```

Requiere PHP 7.4 u 8.0, Composer 2 y MySQL. Laravel 8 dejó de recibir parches de seguridad en enero de 2023.

## Estado del repositorio

- Se conserva sin cambios funcionales como referencia del código original (2022).
- No recibe actualizaciones de dependencias; el mantenimiento ocurre en [pcp-industrial-wholesale-ecommerce](https://github.com/KevinAndrey96/pcp-industrial-wholesale-ecommerce).
- En noviembre de 2026 se depuró el historial completo: se retiraron `vendor/` y `node_modules/`, `.idea/` y el `.env` con credenciales. Todos los commits conservan su fecha original.

## Autoría

Kevin Andrey Herrera Silva ([@KevinAndrey96](https://github.com/KevinAndrey96)), con aportes de Cristian Delgado.

## Licencia

Código desarrollado para un cliente y publicado como muestra de portafolio. No incluye licencia de código abierto: todos los derechos reservados.
