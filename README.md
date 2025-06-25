# IDEA-Store
Este repositorio contiene la propuesta y el codigo correspondiente a la solución web de la tienda IDEA Aviation Corp

# 📄 Propuesta Técnica de Solución

## 1. 🧹 Resumen Ejecutivo

Esta propuesta plantea el desarrollo de una nueva tienda e-commerce para la escuela de aviación **IDEA Aviation Corp**, con el objetivo de reemplazar la actual solución basada en WooCommerce. La necesidad de este cambio surge a raíz de múltiples desafíos técnicos y operativos que afectan directamente el rendimiento, la escalabilidad y la seguridad del sistema actual. La nueva solución estará construida utilizando el framework PHP CodeIgniter, que ofrece un enfoque más limpio, modular y orientado al rendimiento, y se alojará en el servidor dedicado ya existente. Con esta implementación, se busca modernizar la plataforma de comercio electrónico, mejorar la integridad de los datos y establecer una base sólida para futuras integraciones con sistemas internos y externos.

## 2. 🕵️‍♂️ Identificación del Problema

- La tienda actual en WooCommerce depende de una gran cantidad de plugins, muchos de los cuales generan conflictos entre sí, afectan negativamente la performance general y amplían la superficie de ataque frente a amenazas externas.
- La estructura de la base de datos de WordPress no está optimizada para operaciones de e-commerce a gran escala, resultando en lentitud en las consultas, errores intermitentes y pérdida de eficiencia en procesos críticos como el checkout o la carga de catálogos.
- El sitio actual ha sido objeto de ataques de spam y malware, lo que ha derivado en bloqueos por parte de servicios externos y en una pérdida de confianza por parte de los usuarios.
- Existe una dificultad creciente para integrar la plataforma actual con sistemas administrativos, financieros y legacy de la institución.

## 3. 🧠 Análisis de la Situación Actual

- La plataforma WooCommerce funciona sobre WordPress, un CMS generalista no diseñado originalmente para manejar operaciones de e-commerce complejas.
- El almacenamiento de datos se encuentra desorganizado y redundante debido al uso excesivo de plugins, lo que complica tanto la escalabilidad como las tareas de mantenimiento.
- El servidor dedicado actual aloja múltiples servicios, lo cual incrementa la posibilidad de conflictos y limita la capacidad de aislamiento de fallos.
- No existen procesos estandarizados de integración con sistemas externos ni mecanismos robustos de respaldo o recuperación ante incidentes.

## 4. 🌟 Objetivos de la Solución

- El objetivo principal es construir una nueva plataforma de comercio electrónico que sea ligera, segura, personalizable y alineada con los estándares de desarrollo moderno.
- Se mantendrán funcionalidades clave como productos variables (con tallas, colores u otras características), pagos en cuotas (con integración a pasarelas compatibles), y la posibilidad de administrar catálogos dinámicos desde una interfaz intuitiva.
- Toda la información será almacenada en una base de datos relacional (MySQL) estructurada de forma eficiente para garantizar consultas rápidas y seguras, y estará disponible para ser consultada de manera externa mediante interfaces seguras.
- La solución será construida de forma modular, permitiendo futuras extensiones y una integración fluida con sistemas cloud y legacy como sistemas académicos, CRMs y ERPs propios de IDEA Aviation Corp.

## 5. 🛠️ Propuesta Técnica

- El desarrollo se realizará utilizando **CodeIgniter**, un framework PHP que promueve el desarrollo estructurado siguiendo el patrón MVC. Esto permitirá separar claramente las capas de lógica de negocio, presentación y acceso a datos.
- Se diseñarán módulos independientes para productos, carrito de compras, gestión de usuarios, pagos y consultas externas. Cada módulo será documentado y versionado, facilitando el mantenimiento y futuras mejoras.
- Se empleará **MySQL** como motor de base de datos, aprovechando su capacidad para manejar transacciones, integridad referencial, y consultas complejas mediante índices bien diseñados.
- La aplicación se desplegará en el servidor dedicado de IDEA Aviation Corp, asegurando un entorno controlado. Se aplicarán buenas prácticas de seguridad como validación de entrada, control de sesiones, cifrado de contraseñas y protección contra inyecciones SQL.
- La arquitectura técnica será preparada para facilitar integraciones RESTful con sistemas internos y externos, permitiendo una interoperabilidad eficiente en un entorno heterogéneo.

## 6. 🔀 Plan de Implementación

El proceso de desarrollo contempla varias etapas planificadas para asegurar una implementación robusta y alineada con las necesidades del cliente:

- **Semana 1 – Discovery y preparación:** Se realizará un relevamiento detallado de requerimientos funcionales y técnicos, análisis de datos existentes, definición de arquitectura y diseño preliminar de interfaz de usuario. Se establecerán los criterios de aceptación, casos de uso clave y la planificación detallada del proyecto.

- **Semanas 2 a 5 – Desarrollo:** Se implementarán los módulos centrales: catálogo de productos, gestión de stock, carrito de compras, sistema de pagos y gestión de usuarios. Cada módulo será probado individualmente antes de su integración. También se desarrollarán las API necesarias para exposición y consumo de datos.

- **Semana 6 – Pruebas y validación:** Se realizarán pruebas de integración, pruebas funcionales, validación con usuarios clave y pruebas de rendimiento. Se verificarán flujos críticos como el proceso de compra, carga de productos y seguridad en la autenticación.

- **Semanas 7 y 8 – Migración de datos:**
  - Se realizará la migración de todos los datos del último año desde la instalación WooCommerce existente.
  - Los datos más antiguos se almacenarán en un sistema de tipo **datawarehouse** sobre MySQL, optimizado para consultas históricas y reporting.
  - Se implementarán scripts de validación y limpieza de datos para asegurar la integridad y consistencia de la información migrada.

## 7. 📈 Impacto Esperado

- Se espera una **reducción significativa en los tiempos de carga** del sitio y una mejora general en la experiencia del usuario final.
- La eliminación de plugins innecesarios y del entorno WordPress reducirá drásticamente la superficie de ataque, disminuyendo el riesgo de infecciones por malware y spam.
- La estructura modular facilitará la evolución del sistema y su integración con herramientas de gestión internas como sistemas académicos o financieros.
- La exposición de datos mediante interfaces seguras permitirá implementar nuevos procesos automatizados y conectar la tienda con plataformas de análisis y monitoreo.

## 8. 💰 Estimación de Costos

- **Costo de desarrollo:** Basado en una estimación de tiempo y recursos necesarios para cada fase del proyecto, incluyendo diseño, desarrollo, documentación y pruebas.
- **Costo de migración:** Incluye el análisis de la estructura de datos actual, desarrollo de scripts de extracción y transformación, y ejecución controlada de la migración.
- **Mantenimiento y soporte:** Puede ser ofrecido bajo modalidad mensual, por paquete de horas o soporte on-demand, cubriendo actualizaciones, resolución de incidencias y mejoras evolutivas.

## 9. 👨‍💼 Recomendaciones Organizacionales

- Se recomienda la capacitación del personal encargado del soporte técnico y la operación diaria de la tienda, incluyendo sesiones prácticas y manuales de uso.
- Es importante establecer un proceso de despliegue controlado, que incluya ambientes de prueba y políticas de control de versiones.
- Se sugiere adoptar una metodología ágil o iterativa para futuras mejoras, permitiendo una evolución constante de la plataforma.

## 10. ⚠️ Riesgos y Plan de Contingencia

- **Riesgo de pérdida de datos durante la migración:** Se mitigará mediante respaldos completos, pruebas piloto de migración, y verificación de datos post-migración.
- **Riesgo de incompatibilidades con integraciones:** Se reducirá utilizando pruebas automatizadas de API y una arquitectura desacoplada.
- **Riesgo de resistencia al cambio por parte de usuarios internos:** Se abordará con documentación clara, formación práctica y acompañamiento post-implementación.

## 11. 📌 Anexos Técnicos

- Diagrama de arquitectura de la nueva solución.
- Modelo entidad-relación de la base de datos operativa y del datawarehouse.
- Ejemplos de endpoints de API RESTful para integraciones externas.
- Cronograma detallado de ejecución por semana.
