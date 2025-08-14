## **Elementos del Diseño de Software**

El diseño de software es una fase crítica del ciclo de vida del desarrollo de sistemas, en la que se traducen los requisitos del sistema (obtenidos en la fase de análisis) en una representación estructurada y técnica que guiará la implementación. Este proceso no es arbitrario, sino que se basa en cinco elementos fundamentales:


    “¿Por qué algunos sistemas se caen con muchos usuarios y otros no? Todo empieza en el diseño.” 

## **1. Objetivos del Diseño**
### ¿Qué son?
Los objetivos son las metas o propósitos que se busca alcanzar con el diseño del software. Definen qué se espera lograr desde el punto de vista funcional, técnico y de calidad.

### **Tipos de objetivos**

- **Funcionales:** Cumplir con las funcionalidades requeridas por el usuario (ej: registrar usuarios, generar reportes).
- **No funcionales (atributos de calidad):**
    -   Rendimiento: El sistema debe responder en menos de 2 segundos.
    -   Seguridad: Protección de datos sensibles.
    -   Usabilidad: Interfaz intuitiva.
    -   Escalabilidad: Capacidad de crecer con más usuarios.
    -   Mantenibilidad: Fácil de modificar y actualizar.

**Enfoque pedagógico :** Planteamiento

        "Si van a diseñar un sistema de inscripciones académicas, ¿cuáles serían sus objetivos principales?”

## **2.Restricciones del Diseño**
### ¿Qué son?
Son limitaciones externas o internas que el diseño debe respetar. No se pueden ignorar ni modificar fácilmente.

### Tipos de restricciones:

- #### Tecnológicas
    Uso obligatorio de ciertas herramientas (ej: Java, PostgreSQL, AWS).
- #### Presupuestales
    Límite de gasto en infraestructura o licencias.
- #### Temporales
    Plazos de entrega ajustados.
- #### Legales o normativas
    Cumplimiento de normas como GDPR (protección de datos) o estándares ISO.
- #### Recursos humanos
    Equipo con experiencia limitada en ciertas tecnologías.

???+Example "Ejemplo práctico"
    “El sistema debe desarrollarse en .NET por decisión corporativa, aunque el equipo conoce más de Python.”

Esto ilustra cómo una restricción tecnológica influye en el diseño. 

???+info "Actividad sugerida"
    identificar al menos 3 restricciones en el caso de uso de tu proyecto integrador


## **3. Alternativas de Diseño**
### ¿Qué son?
Son diferentes opciones o enfoques que se pueden tomar para resolver un mismo problema de diseño. Elegir entre ellas implica análisis de trade-offs (costos/beneficios).

???+Example "Ejemplos de alternativas"
    | Aspecto | Alternativa A | Alternativa B |
    |--------|---------------|---------------|
    | Arquitectura | Monolítica | Microservicios |
    | Base de datos | SQL (PostgreSQL) | NoSQL (MongoDB) |
    | Frontend | React | Angular |
    | Despliegue | Servidor local | Nube (AWS) |

### Proceso de selección:

Se evalúan alternativas según:

- Alineación con los objetivos.
- Viabilidad bajo las restricciones.
- Impacto en calidad (rendimiento, mantenibilidad, etc.).

???+info "En clase"
    Realiza una lluvia de ideas grupal para generar alternativas de diseño sobre un sistema sencillo. Luego, haz una tabla comparativa y voten la mejor opción.


## **4. Representaciones del Diseño**
### ¿Qué son?
Son las formas visuales o simbólicas en que se expresa el diseño para que sea comprensible por desarrolladores, arquitectos y stakeholders.

### Tipos de representaciones

#### *Gráficas*
- Diagramas UML (clases, secuencia, componentes).
- Diagrama de arquitectura (vistas lógica, de despliegue).
- Diagrama de flujo de datos.

#### *Tabulares*
- Tablas de mapeo de entidades.
- Matrices de trazabilidad requisitos-diseño.
- Textuales:
- Especificaciones técnicas.
- Pseudocódigo.

#### *Híbridas*
- Documentos que combinan texto, tablas y diagramas.


**Importancia**
Una buena representación permite:

- Comunicar el diseño de forma clara.
- Detectar errores tempranos.
- Facilitar la revisión técnica.

???+Infor "Actividad en clase"
    Usa Lucidchart o Draw.io para que los estudiantes dibujen un diagrama de clases o de arquitectura basado en un caso de uso.

## **5. Soluciones de Diseño**
### ¿Qué son?
Es la propuesta concreta y final que integra los objetivos, restricciones, alternativas evaluadas y representaciones elegidas. Es el resultado del proceso de diseño.

#### Características de una buena solución:

- Coherente con los requisitos del sistema.
- Técnicamente viable.
- Documentada y comunicable.
- Flexible para futuros cambios.

???+Example "Ejemplo de solución"
    “Para el sistema de gestión de biblioteca, se propone una arquitectura en capas (presentación, lógica de negocio, datos), usando Spring Boot (Java), base de datos MySQL y despliegue en AWS. Se modelará con diagramas UML y se documentará en un informe técnico.” 


## **Resumen**
| Elemento | Pregunta clave | Ejemplo |
|----------|----------------|--------|
| Objetivos | ¿Qué queremos lograr? | Sistema rápido, seguro y fácil de usar |
| Restricciones | ¿Qué nos limita? | Debe usarse PostgreSQL y entregar en 3 meses |
| Alternativas | ¿Qué opciones tenemos? | Arquitectura monolítica vs. microservicios |
| Representaciones | ¿Cómo lo mostramos? | Diagrama de clases, pseudocódigo, tablas |
| Soluciones | ¿Qué vamos a implementar? | Arquitectura en capas con Spring Boot y MySQL |

???+Info "Enfoque docente"
    Guíar a los estudiantes para que, al final de la semana, elaboren una pequeña propuesta de solución de diseño para su proyecto grupal, integrando los cinco elementos.

???+Warning "Proposito del Diseño" 
    El diseño no es solo dibujar diagramas; es tomar decisiones técnicas con base en objetivos, limitaciones y alternativas.” 