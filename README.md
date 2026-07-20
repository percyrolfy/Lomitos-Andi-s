# Lomitos-Andi-s
Sistema de venta para comida Rápida
# 🍔 Lomitos Andy's - Sistema de Ventas y Catálogo

¡Bienvenido a **Lomitos Andy's**! Este es un sistema web moderno, fluido y completamente interactivo diseñado para la gestión de pedidos de comida rápida. La aplicación permite a los usuarios navegar por un catálogo dinámico de combos, personalizar sus pedidos con notas específicas y procesar la compra en tiempo real.

Desarrollado sobre la tecnología **Blazor WebAssembly / Server** utilizando **C#** y estilizado con **Bootstrap 5**.

---

## 🚀 Características Principales

* **Catálogo Interactivo**: Visualización limpia de los combos disponibles en formato Grid con tarjetas dinámicas.
* **Carrito con Multi-Contador**: Al agregar el mismo combo varias veces, el sistema incrementa automáticamente la cantidad en una sola línea del carrito, permitiendo sumar (`+`) o restar (`-`) unidades con botones ágiles.
* **Notas de Personalización**: Campo dedicado para añadir especificaciones especiales a la orden (ej. *"Sin cebolla"*, *"Extra salsa"*), las cuales se unifican de forma transparente en la facturación del pedido.
* **Gestión de Fecha y Hora**: Selector flexible que permite alternar entre capturar la hora del sistema en tiempo real o definir una fecha/hora personalizada de forma manual.
* **Diseño 100% Responsive**: Interfaz adaptativa optimizada mediante Bootstrap 5 para lucir perfecta y ser fácil de operar tanto en computadoras de escritorio como en teléfonos móviles.
* **Persistencia de Estado**: Consumo centralizado de datos a través de un servicio inyectado (`ServicioVentas`) que comparte el estado de la orden actual de forma consistente entre múltiples vistas de la aplicación.

---

## 🛠️ Tecnologías Utilizadas

* **Framework**: .NET / Blazor
* **Lenguaje**: C#
* **Maquetación y Estilos**: HTML5, CSS3, Bootstrap 5 (Clases fluidas y flexbox)
* **Iconos**: Emojis Nativos (Compatibilidad cross-platform sin dependencias externas pesadas)

---

## 📂 Componentes Clave del Sistema

El flujo del pedido está dividido estratégicamente en componentes reutilizables de Blazor:

1. **`ServicioVentas.cs` (Servicios)**: Actúa como el motor del estado global de la aplicación. Almacena temporalmente los datos del `PedidoActual`, la lista de combos en el menú (`MenuComida`) y la colección de pedidos procesados.
2. **`Counter.razor` (Catálogo y Datos)**: Es la interfaz principal. Contiene el formulario del cliente (Nombre, Fecha, Notas, Método de Pago) y la cuadrícula de productos disponibles. Implementa una clase interna `ItemCarrito` para procesar matemáticamente las sumas y cantidades con casteo seguro a `double`.
3. **`Weather.razor` (Detalle de Facturación)**: Componente que actúa como pasarela de confirmación. Lee el estado finalizado desde el servicio inyectado, muestra el resumen en formato de factura limpia y procesa la confirmación del pedido.

---

## 💻 Instrucciones de Ejecución

Para levantar y probar este sistema en tu entorno local, asegúrate de tener instalado el SDK de .NET correspondiente y sigue estos pasos:

1. **Clonar el repositorio**:
   ```bash
   git clone git@github.com:percyrolfy/tw2-FormularioCRUD.git
   cd tw2-FormularioCRUD
