## Capítulo VII: DevOps Practices
### 7.1. Continuous Integration

#### 7.1.1. Tools and Practices.

#### 7.1.2. Build & Test Suite Pipeline Components.

### 7.2. Continuous Delivery

#### 7.2.1. Tools and Practices.

#### 7.2.2. Stages Deployment Pipeline Components.

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
