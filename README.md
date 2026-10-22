# Psytech Edu 

**Psytech Edu** es una aplicación móvil desarrollada en Kodular orientada a la evaluación y seguimiento del bienestar emocional y psicológico en entornos educativos. El sistema integra autenticación de usuarios, persistencia local y remota, y un motor de evaluación basado en la escala de Likert con visualización de resultados tipo semáforo.

---

##  Arquitectura del Sistema e Integración

La aplicación utiliza un esquema de arquitectura híbrida para garantizar la seguridad, fluidez en la navegación y almacenamiento eficiente de los datos:

* **Navegación:** Flujo continuo e integrado desde la pantalla de bienvenida hasta la vista final de resultados (Pantallas 1 a 6).
* **Autenticación (Firebase Authentication):** Gestión segura del registro e inicio de sesión de usuarios (mediante correo electrónico y proveedor de Google).
* **Persistencia Local (TinyDB):** Mantenimiento del estado de la sesión activa directamente en el dispositivo del usuario para optimizar los tiempos de carga.
* **Persistencia Remota / Base de Datos (Airtable / Spreadsheet):** Almacenamiento centralizado y estructurado de las respuestas recolectadas en los formularios de evaluación.

---

##  Metodología de Evaluación

El instrumento de recolección de información utiliza preguntas estructuradas bajo una **Escala de Likert de 5 puntos**:

1. **Nunca** (1 pto)
2. **Casi nunca** (2 ptos)
3. **A veces** (3 ptos)
4. **Casi siempre** (4 ptos)
5. **Siempre** (5 ptos)

Los puntajes calculados permiten clasificar cuantitativamente el estado evaluado mediante un **sistema de semaforización (Verde, Amarillo, Rojo)** para entregar recomendaciones personalizadas de manera inmediata al usuario.

---

##  Pruebas de Rendimiento y Optimización

Para cumplir con los criterios de optimización técnica, el sistema fue sometido a pruebas de rendimiento tanto en desarrollo como en la nube:

### 1. Tiempos de Respuesta (Medición en Kodular)
Mediante la captura de instantes con el componente `Clock.SystemTime`, se evaluó la diferencia de tiempo en milisegundos ($ms$) previa y posterior a la optimización de assets e hilos de ejecución:

| Proceso Evaluado | Tiempo Pre-optimización | Tiempo Post-optimización | Mejora Obtenida |
| :--- | :---: | :---: | :---: |


### 2. Validación en la Nube (Firebase Test Lab - Robo Test)


---

##  Criterios de Accesibilidad

La interfaz gráfica fue optimizada y auditada bajo estándares de usabilidad y accesibilidad móvil:
* **Contraste:** Relación de contraste adecuada entre texto y fondo para facilitar la lectura.
* **Áreas Táctiles:** Botones y controles interactivos dimensionados para evitar pulsaciones erróneas.
* **Claridad Visual:** Jerarquía tipográfica clara e iconos intuitivos para guiar al usuario a lo largo de las 6 pantallas.

---

## Tecnologías Utilizadas

* **Entorno de Desarrollo:** [Kodular](https://www.kodular.io/)
* **Autenticación:** Firebase Authentication
* **Base de Datos Remota:** Airtable / Google Sheets API (`Spreadsheet`)
* **Almacenamiento Local:** TinyDB
* **Pruebas y Analítica:** Firebase Test Lab (Robo Test)

---

## Licencia y Créditos
Proyecto académico desarrollado para la asignatura de desarrollo/evaluación de aplicaciones móviles - **Psytech Edu**.
