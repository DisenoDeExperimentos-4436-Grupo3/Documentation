## Capítulo VII: DevOps Practices
### 7.1. Continuous Integration

#### 7.1.1. Tools and Practices.

#### 7.1.2. Build & Test Suite Pipeline Components.

### 7.2. Continuous Delivery

El objetivo de la estrategia de Continuous Delivery (CD) en ManageWise es mantener el software en un estado constante de disponibilidad para ser desplegado en producción, con altos estándares de calidad y trazabilidad. Si bien no se realiza un despliegue automático inmediato (como en Continuous Deployment), se asegura que cada versión del software pase por validaciones y esté lista para ser liberada cuando se apruebe.

#### 7.2.1. Tools and Practices.

**Herramientas utilizadas:**

- **GitHub Actions**: Utilizado para definir y ejecutar workflows de CI/CD. En el caso de CD, se configura el pipeline para realizar pruebas automáticas y generar artefactos listos para producción, dejando el despliegue en espera de una aprobación manual.
- **Docker**: Se emplea para contenerizar la aplicación, asegurando que los entornos de desarrollo, staging y producción sean coherentes y repetibles.
- **Trello** o **Jira**: Herramientas de gestión de tareas para coordinar el proceso de revisión y autorización del despliegue, estableciendo puntos de control antes del pase a producción.
- **Railway/Render/Netlify (según el entorno de despliegue)**: Se configuran ambientes intermedios (como staging) donde se despliega automáticamente después del pipeline, pero la liberación a producción requiere intervención humana.

**Prácticas implementadas:**

- **Feature Branching y Pull Requests**: Todo nuevo desarrollo se realiza en ramas independientes y se integran a `main` tras una revisión y validación automatizada.
- **Pipeline de Validación en Staging**: Los cambios se despliegan automáticamente en un entorno de staging donde se pueden realizar pruebas manuales, regresivas o de aceptación antes de su aprobación para producción.
- **Despliegue Semiautomático**: El pipeline prepara y entrega el build listo para producción, pero el despliegue final requiere una aprobación manual dentro del repositorio o por gestión del equipo.
- **Aprobación Manual**: Una etapa del pipeline queda en espera hasta que un miembro autorizado (Scrum Master o responsable técnico) aprueba el despliegue. Esto proporciona un mayor control y supervisión.
- **Rollback Manual**: En caso de errores críticos, se cuenta con mecanismos para realizar rollbacks controlados por el equipo técnico desde versiones etiquetadas previamente.

#### 7.2.2. Stages Deployment Pipeline Components.

**Integración Continua (CI):**

Cada vez que se hace `push` a una rama de desarrollo, el pipeline ejecuta pruebas unitarias, de integración y de linting. Si todas las validaciones son exitosas, se genera un artefacto listo para ser probado en staging.

**Validación en Staging:**

Se despliega automáticamente en un entorno de staging tras la CI. Aquí se hacen pruebas funcionales, validación de criterios de aceptación y pruebas exploratorias por parte del equipo QA o desarrolladores asignados.

**Despliegue Manual a Producción:**

Una vez validado el entorno de staging, un desarrollador o administrador aprueba manualmente el paso final del pipeline. El sistema está listo para producción, pero el despliegue no se realiza hasta que se confirme explícitamente.

**Monitoreo y Feedback:**

Durante y después del despliegue en staging o producción, se habilitan herramientas de monitoreo (por ejemplo, logs de servidor o alertas de error) que permiten validar el comportamiento del sistema y recoger retroalimentación antes del pase completo.

**Control de Aprobación:**

La etapa final del pipeline espera confirmación humana. Solo un miembro autorizado puede activar la última acción de despliegue, asegurando control total sobre la liberación en entornos productivos.

### 7.3. Continuous deployment

El objetivo principal de Continuous deployment es que los cambios realizados y aprobados en el código (que pasen todas las pruebas de validación) pasen de manera automática desde el desarrollo hasta la producción, evitando asi la intervención manual

#### 7.3.1. Tools and Practices.

Practicas y herramientas para el despliegue continuo:

**Tools:**

* GitHub Actions: Para automatizar el pipeline de CI/CD. Estas herramientas permiten configurar workflows que incluyen la ejecución de pruebas y el despliegue automático a diferentes entornos (desarrollo, staging, producción).
* Docker: Para contenerizar la aplicación backend (Spring Boot). Nos permite crear images y subirlas en Docker.hub, empaquetando asi todas las dependencias necesarias para correr la aplicación.
* Render: Como plataforma para despliegue de base de datos de PostgreSQL.
* Render: Esta plataforma se encargará del despliegue automático del backend en Spring Boot, ofreciendo monitoreo y escalabilidad automática.
* Vercel: Para el frontend en Angular, automatiza los despliegues de la aplciación al conectarse con github actions.

**Practices:**

* Utilizamos una estrategia de ramas en Git donde los desarrolladores trabajan en nuevas
funcionalidades dentro de ramas separadas. Una vez completadas y probadas, estas ramas se
fusionan a la rama develop, que es la encargada de gestionar los despliegues a producción.


#### 7.3.2. Production Deployment Pipeline Components.

#### Componentes del Pipeline de la Base de Datos (Render + PostgreSQL)

1. **Gestión de Migraciones Automáticas:**  
   A través de Spring Boot y sus herramientas de persistencia (JPA/Hibernate), el sistema aplica automáticamente los cambios en las entidades al esquema de la base de datos PostgreSQL desplegado en Render. Esto garantiza que los modelos del backend estén siempre sincronizados con la estructura de datos en producción.

2. **Backups Automáticos:**  
   Render gestiona copias de seguridad periódicas de la base de datos PostgreSQL. Antes de ejecutar migraciones críticas o durante despliegues importantes, Render permite restaurar versiones anteriores de la base de datos, reduciendo el riesgo ante errores imprevistos.

3. **Monitoreo del Rendimiento:**  
   Render proporciona un panel de monitoreo que permite al equipo de desarrollo observar el uso de CPU, memoria y tráfico de la base de datos. Se pueden configurar alertas automáticas en caso de degradación del rendimiento o fallas en el servicio.

4. **Validación de Esquema y Datos:**  
   Después de las migraciones, se ejecutan pruebas de integración y validaciones de esquema para asegurar que las nuevas estructuras (tablas, relaciones, columnas) se hayan creado correctamente. Estas pruebas están integradas en el pipeline de GitHub Actions.

5. **Despliegue Automatizado y Sincronizado:**  
   Los cambios en el modelo de datos se despliegan automáticamente a la base de datos productiva mediante migraciones controladas y validadas. Esto permite mantener una sincronización constante entre el backend y la base de datos sin intervención manual.


#### Componentes del Pipeline del Backend (Render para Spring Boot)

1. **Integración Continua con GitHub Actions:**  
   Al hacer un push a la rama `develop`, GitHub Actions ejecuta automáticamente pruebas unitarias e integración del backend desarrollado en Spring Boot. Si todo es exitoso, Render detecta los cambios y ejecuta el despliegue.

2. **Construcción de Imagen Docker:**  
   El backend es contenerizado con Docker. Las imágenes son construidas automáticamente y almacenadas en Docker Hub. Esto garantiza un entorno consistente entre desarrollo, staging y producción.

3. **Despliegue en Render:**  
   Render toma la nueva imagen del backend y la despliega en el entorno de producción. Este proceso es completamente automático y puede realizarse múltiples veces al día si hay cambios disponibles.

4. **Monitoreo y Alertas en Tiempo Real:**  
   El backend desplegado es monitoreado constantemente. Render permite observar logs en tiempo real y configurar alertas para notificar al equipo ante errores 5xx, caídas de servicio o comportamientos anómalos.


#### Componentes del Pipeline del Frontend (Vercel para Angular)

1. **Compilación Automática del Frontend:**  
   Vercel está integrado directamente con GitHub. Al detectar nuevos commits en la rama `develop`, inicia automáticamente el proceso de construcción de la aplicación Angular en modo producción.

2. **Pruebas Automatizadas:**  
   Antes del despliegue, se ejecutan pruebas unitarias para verificar el correcto funcionamiento de los componentes del frontend. En versiones futuras, se incluirán pruebas E2E como parte del flujo.

3. **Despliegue en Vercel:**  
   Si las pruebas son exitosas, Vercel publica automáticamente la nueva versión del frontend en producción. El contenido es servido desde su CDN global, lo cual mejora el rendimiento y disponibilidad para los usuarios.

4. **Invalidación de Caché:**  
   Vercel gestiona la invalidación automática de la caché, asegurando que todos los usuarios accedan a la última versión de la interfaz sin necesidad de borrar datos localmente.



### Conclusiones

- John Telesforo Arevalo Meza: <br>
  ------<br>

- Michael Stefano Carmelino Dueñas <br>
 ----
 <br>
  

- Rodrigo Manuel Chirinos Zúñiga <br>
  -----
  <br>
 
- Fabian Alonso Reyes Trujillano <br>
  -----
 <br>

- Alessandro Netto Zevallos Linares<br>
  ----
   <br>


### Bibliografia

- Biblioteca UPC. (2024). _Biblioteca virtual de la Universidad Peruana de Ciencias Aplicadas_. https://biblioteca.upc.edu.pe
- Miro. (2024). _Miro_. Miro Corporation. https://miro.com
- LucidChart. (2024). _LucidChart_. Lucid Software Inc. https://www.lucidchart.com
- Cohn, M. (2006). Historias de usuario: Un enfoque ágil. Pearson Educación.https://www.scrummanager.com/files/scrum_manager_historias_usuario.pdf
- Pressman, R. S. (2010). Ingeniería de Software: Un enfoque práctico. McGraw-Hill.https://www.javier8a.com/itc/bd1/ld-Ingenieria.de.software.enfoque.practico.7ed.Pressman.PDF
- The C4 model for visualising software architecture. (2024). https://c4model.com/
- Structurizr. (2024). https://www.structurizr.com/

### Anexos

**ANEXO FRONTEND Y BACKEND DESPLEGADO**: https://frontend-test-managewise.vercel.app/sign-in

**ANEXO FRONTEND**: https://frontend-test-managewise.vercel.app

**ANEXO BACKEND**: https://managewise-ffbua6fpfmbteaeq.brazilsouth-01.azurewebsites.net/api/v1/

Anexo A:<br>https://miro.com/welcomeonboard/NHhiOEg2U2ZETmc0SnFSTG10R3djVFdBdGVCMGQwQkVoakZxcnZNRWhpUU44d0xjMGFBWFF6dUtUTXRuNDl1eXwzNDU4NzY0NTQzNjk5MTEyMTEwfDI=?share_link_id=979016695371

Anexo B:<br>https://miro.com/welcomeonboard/NHhiOEg2U2ZETmc0SnFSTG10R3djVFdBdGVCMGQwQkVoakZxcnZNRWhpUU44d0xjMGFBWFF6dUtUTXRuNDl1eXwzNDU4NzY0NTQzNjk5MTEyMTEwfDI=?share_link_id=979016695371

Anexo C:<br>https://miro.com/welcomeonboard/NHhiOEg2U2ZETmc0SnFSTG10R3djVFdBdGVCMGQwQkVoakZxcnZNRWhpUU44d0xjMGFBWFF6dUtUTXRuNDl1eXwzNDU4NzY0NTQzNjk5MTEyMTEwfDI=?share_link_id=979016695371

Anexo D:<br>https://miro.com/welcomeonboard/NHhiOEg2U2ZETmc0SnFSTG10R3djVFdBdGVCMGQwQkVoakZxcnZNRWhpUU44d0xjMGFBWFF6dUtUTXRuNDl1eXwzNDU4NzY0NTQzNjk5MTEyMTEwfDI=?share_link_id=979016695371

Anexo E:<br>https://miro.com/welcomeonboard/RTA3b0ZrRzFmckk5Z3BneTVwc3d5Z1BBYko4c3d4SmpUaVMwTG93c0JjUmc2cERSNzJ5ZkxjOTZDWG5CbThHd3wzNDU4NzY0NTQzNjk5MTEyMTEwfDI=?share_link_id=839908059772

Anexo F:<br>https://drive.google.com/file/d/1AQQxatIfwUWjgvnbWb-nLQKARzIHEPDS/view?usp=sharing

Anexo G:<br>https://drive.google.com/file/d/1mH4Wulu81QrwmgZ2DWM8nT87ZtzNcduh/view?usp=sharing

Anexo H:<br>https://www.figma.com/design/PQMlg7QzupwYT1ef3eXdEG/LandingPage-WireFrame-ManageWise?node-id=15-131&t=DZEsag5WhuvjGmZk-1

Anexo I:<br>https://www.figma.com/design/mz9XRI1PRFgIvEPIuqHzgd/webapp-managewis?node-id=1-2&t=YdZHXwLmNin9xC6s-1

Anexo J:<br>https://lucid.app/lucidchart/1e63a43a-a627-478b-a4e2-397bbd5407b9/edit?viewport_loc=-24225%2C-5250%2C27750%2C11925%2C0_0&invitationId=inv_2dbf5bda-cf33-4d4a-bbc1-c27a42d84ac8

Anexo J:<br>https://www.figma.com/proto/mz9XRI1PRFgIvEPIuqHzgd/webapp-managewis?page-id=1%3A2&node-id=118-122&node-type=CANVAS&viewport=-385%2C681%2C0.08&t=grI8nuvCu1Ox92G5-1&scaling=scale-down&content-scaling=fixed&starting-point-node-id=118%3A122
