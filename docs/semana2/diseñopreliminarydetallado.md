## **Diseño Preliminar y Diseño Detallado en la Ingeniería de Software**
El diseño de software es una fase crítica del ciclo de vida del desarrollo, en la que se transforman los requisitos del sistema (obtenidos en el análisis) en una estructura técnica que guiará la implementación. Este proceso se divide en dos etapas principales: diseño preliminar y diseño detallado, cada una con objetivos, alcance y productos específicos.

### **1. Diseño Preliminar (También llamado Diseño Arquitectónico o de Alto Nivel)**
#### ¿Qué es?
El diseño preliminar es la primera aproximación estructural al sistema. Consiste en definir la arquitectura general, descomponiendo el sistema en módulos o componentes principales y estableciendo cómo se relacionan entre sí.

#### Objetivos del diseño preliminar
- Establecer la estructura general del sistema.
- Identificar los módulos principales (subsistemas).
- Definir las interacciones entre módulos (interfaces, flujos de datos).
- Seleccionar el estilo arquitectónico (por ejemplo: capas, cliente-servidor, microservicios).
- Garantizar que el diseño cumpla con los atributos de calidad (seguridad, escalabilidad, mantenibilidad).

???+info "Actividades clave"
    - Descomposición del sistema en componentes.
    - Definición de interfaces entre módulos.
    - Selección de tecnologías y plataformas (por ejemplo: usar Spring Boot, PostgreSQL, AWS).
    - Toma de decisiones arquitectónicas (monolítico vs. distribuido, sincrónico vs. asíncrono).
    - Elaboración de diagramas de arquitectura (vistas lógica, de
    despliegue, de componentes).
#### Productos o entregables
- Diagrama de arquitectura del sistema.
- Especificación de módulos y sus responsabilidades.
- Documento de decisiones arquitectónicas (ADRs).
- Diagrama de despliegue (hardware y software involucrado).
- Vista lógica del sistema (qué hace cada componente).

???+Example "Ejemplo práctico (para clase)"
    Para un sistema de gestión de biblioteca: 

    - Módulos: Préstamos, Usuarios, Catálogo, Devoluciones.
    - Arquitectura en capas: Presentación, Lógica de Negocio, Datos.
    - Tecnologías: Frontend con React, Backend con Node.js, base de datos MySQL.
    - Interfaz: API REST entre frontend y backend.

Enfoque pedagógico:
Usa Lucidchart o Draw.io para modelar la arquitectura.
Pide a los estudiantes que propongan al menos dos alternativas de arquitectura (ej: monolítica vs. microservicios) y justifiquen su elección.

### **2. Diseño Detallado (También llamado Diseño de Bajo Nivel)**
#### ¿Qué es?
El diseño detallado profundiza en cada uno de los módulos definidos en el diseño preliminar. Aquí se especifica cómo funciona cada componente internamente, incluyendo estructuras de datos, algoritmos, clases, bases de datos y procesos.

#### Objetivos del diseño detallado:
- Especificar el funcionamiento interno de cada módulo.
- Definir estructuras de datos (tablas, diccionario de datos).
- Detallar clases, métodos, atributos (en entornos orientados a objetos).
- Diseñar la interfaz de usuario (pantallas, formatos de entrada/salida).
- Especificar procesos y flujos de control (diagramas de secuencia, actividad).
- Preparar todo para que los desarrolladores puedan codificar sin ambigüedades.

???+info "Actividades clave"
    - Diseño de bases de datos (modelo entidad-relación, normalización).
    - Creación de diagramas UML (clases, secuencia, estados, componentes).
    - Diseño de interfaces de usuario (mockups, prototipos).
    - Especificación de algoritmos y reglas de negocio.
    - Definición de diccionario de datos (campos, tipos, restricciones).
    - Detalle de APIs (endpoints, parámetros, respuestas).
 
#### Productos o entregables:
- Diagrama de clases.
- Diagrama de secuencia (ej: flujo de "realizar préstamo").
- Modelo de datos (entidad-relación).
- Diccionario de datos.
- Prototipos de interfaces (hechos en Figma u otra herramienta).
- Especificaciones técnicas por módulo.

???+Example "Ejemplo práctico (para clase)"
    **Módulo "Préstamos":**

    - **Clase Prestamo:** atributos (id, fecha, usuario, libro, fecha_devolución).

        - **Método** validarDisponibilidad(), calcularMulta().

    - **Tabla en base de datos:** prestamos(id, id_usuario, id_libro, fecha_inicio, fecha_fin, estado).

    - **Flujo:** Usuario → Sistema verifica disponibilidad → Confirma préstamo → Registra en BD.

???+info "Enfoque pedagógico"
    Realiza un taller guiado donde los estudiantes diseñen el diagrama de clases para un módulo.
    Usa Figma para diseñar una pantalla de préstamo.
    Pide que elaboren un diccionario de datos para las entidades clave.


!!! tip " Concejo"
    -  **El diseño preliminar** Es como los planos generales de una casa: muestra habitaciones, distribución y estructura. 
    
    - **El diseño detallado**  Es como los planos eléctricos, de fontanería y acabados: especifica cómo se construye cada parte. Ambos son esenciales para construir un sistema robusto, escalable y mantenible.