### Actividad 1. Ejercicios de unidad

**1. Define las funciones del administrador de la base de datos.**  
- Diseñar la estructura de la base de datos.  
- Supervisar el rendimiento y optimización.  
- Garantizar la seguridad y control de accesos.  
- Realizar copias de seguridad y recuperación ante fallos.  
- Administrar usuarios y permisos.  
- Actualizar el software del SGBD.

**2. Indica las diferencias existentes entre las funciones de manipulación y de descripción.**  
- Las funciones de **descripción** permiten definir la estructura de la base de datos (tablas, relaciones, etc.).  
- Las funciones de **manipulación** permiten consultar, insertar, actualizar o eliminar datos.

**3. ¿Qué tipos de usuarios interaccionan con una base de datos?**  
- Administrador de base de datos (DBA).  
- Usuarios finales.  
- Desarrolladores de aplicaciones.  
- Usuarios avanzados (analistas).

**4. Indica qué es un lenguaje huésped y un lenguaje anfitrión.**  
- **Lenguaje anfitrión**: Lenguaje de programación principal (ej. Java, Python).  
- **Lenguaje huésped**: Lenguaje embebido dentro del anfitrión, como SQL, para gestionar bases de datos.

**5. La gestión del espacio de almacenamiento, ¿a qué nivel de la arquitectura ANSI/SPARC pertenece? ¿Qué es la arquitectura ANSI/SPARC?**  
- Pertenece al **nivel interno**.  
- La **arquitectura ANSI/SPARC** es un modelo de tres niveles (externo, conceptual e interno) para separar la forma en que los usuarios ven los datos, cómo se organizan lógicamente y cómo se almacenan físicamente.

**7. Indica las principales funciones realizadas por el SGBD.**  
- Gestión de datos.  
- Seguridad y control de acceso.  
- Control de concurrencia.  
- Mantenimiento de la integridad.  
- Recuperación ante fallos.

**8. Explica la diferencia entre la independencia física y lógica de los datos.**  
- **Independencia física**: Cambios en el almacenamiento físico no afectan a la estructura lógica.  
- **Independencia lógica**: Cambios en la estructura lógica no afectan a las aplicaciones que usan los datos.

**9. ¿Qué es el diccionario de datos?**  
Es una base de datos que almacena metadatos: definiciones, estructuras, restricciones, usuarios, etc.

**10. Diferencias entre el LDD y LMD de un sistema gestor de base de datos.**  
- **LDD (Lenguaje de definición de datos)**: Define estructuras (CREATE, ALTER).  
- **LMD (Lenguaje de manipulación de datos)**: Manipula los datos (SELECT, INSERT, UPDATE, DELETE).

**11. Indica los componentes principales de un sistema gestor de base de datos.**  
- Motor de almacenamiento.  
- Procesador de consultas.  
- Control de transacciones.  
- Control de concurrencia.  
- Módulo de recuperación.  
- Manejador de catálogos (diccionario de datos).

**12. ¿Qué es un modelo de datos?**  
Es una representación conceptual de los datos y sus relaciones. Ejemplos: relacional, documental, jerárquico, en red, etc.

**13. ¿Qué son los lenguajes de cuarta generación? Pon ejemplos.**  
Son lenguajes diseñados para ser más cercanos al lenguaje humano, orientados a tareas específicas.  
Ejemplos: SQL, MATLAB, Informix 4GL.

**14. Indica las principales ventajas de un sistema de bases de datos. ¿Existen algunas desventajas?**  
**Ventajas:**  
- Reducción de redundancia.  
- Integridad y seguridad.  
- Mejora en el acceso y manipulación de datos.  

**Desventajas:**  
- Costo inicial elevado.  
- Complejidad en la administración.

---

### Clasificación: Sistemas de ficheros vs. Sistemas de bases de datos

| Elemento                                      | Clasificación               |
|----------------------------------------------|-----------------------------|
| Almacenamiento en archivos CSV               | Sistema de ficheros         |
| Oracle Database                               | Sistema de bases de datos   |
| MongoDB con documentos JSON                   | Sistema de bases de datos   |
| MySQL con tablas relacionales                 | Sistema de bases de datos   |
| Archivos de texto plano con datos de clientes| Sistema de ficheros         |

---

### Relación: Tipo de base de datos y descripción

| Tipo de base de datos        | Descripción                                                 |
|-----------------------------|-------------------------------------------------------------|
| Base de datos clave-valor   | Almacena datos como pares clave-valor, ideal para cachés    |
| Base de datos relacional    | Organiza datos en tablas con relaciones entre ellas         |
| Base de datos de grafos     | Representa datos como nodos y relaciones entre ellos        |
| Base de datos documental    | Almacena datos en documentos flexibles (JSON/BSON)          |

---

### Bases de datos centralizadas vs. distribuidas

**Centralizadas:**  
- **Ventajas**:  
  - Administración más sencilla.  
  - Mayor control de seguridad.  
- **Desventajas**:  
  - Punto único de fallo.  
  - Acceso lento desde ubicaciones remotas.

**Distribuidas:**  
- **Ventajas**:  
  - Alta disponibilidad.  
  - Mejor rendimiento geográficamente.  
- **Desventajas**:  
  - Complejidad en la sincronización.  
  - Mayor dificultad en la administración.

---

### Cinco funciones principales del SGBD

1. **Gestión de datos**: Almacenamiento, acceso y actualización de datos.  
2. **Control de concurrencia**: Permite acceso simultáneo sin conflictos.  
3. **Seguridad**: Define permisos de acceso a los datos.  
4. **Recuperación ante fallos**: Restaura el sistema tras errores.  
5. **Mantenimiento de la integridad**: Asegura la validez de los datos.

---

### Clasificación de SGBD según tipo y licencia

| SGBD         | Tipo             | Licencia        |
|--------------|------------------|-----------------|
| MySQL        | Relacional        | Open Source     |
| Oracle DB    | Relacional        | Comercial       |
| MongoDB      | Documental        | Open Source     |
| Redis        | Clave-valor       | Open Source     |
| PostgreSQL   | Relacional        | Open Source     |
| Neo4j        | Grafos            | Comercial / OSS |

---

### Caso práctico para usar base de datos distribuida

**Ejemplo: Empresa global de e-commerce.**  
**Justificación:**  
1. Acceso más rápido desde múltiples regiones del mundo.  
2. Alta disponibilidad para evitar interrupciones.  
3. Escalabilidad horizontal para manejar grandes volúmenes de tráfico.

---

### Teorema CAP

**Significado:**  
- **C**: Consistencia.  
- **A**: Disponibilidad.  
- **P**: Tolerancia a particiones.  

**Impacto:**  
- En sistemas distribuidos, solo se pueden garantizar dos de las tres propiedades al mismo tiempo.  
- La mayoría de los sistemas actuales eligen **Disponibilidad** y **Tolerancia a particiones** (ej. Cassandra, DynamoDB).

---

### Fragmentaciones de la tabla EMPLEADOS

**a) Fragmentación horizontal (por departamento):**  
```sql
-- Departamento Ventas
SELECT * FROM EMPLEADOS WHERE departamento = 'Ventas';

-- Departamento Marketing
SELECT * FROM EMPLEADOS WHERE departamento = 'Marketing';
