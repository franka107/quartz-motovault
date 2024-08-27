---
id: 1724796314-deocasion-suelto
aliases: []
tags: []
---

# Resumen

DeOcasion es un proyecto con el objetivo principal de subastar vehiculos, la
cual sera una empresa relacionada al core de acceso crediticio. Dentro del
proceso comercial por lo general hay conexiones con financierias, contables,
bancos, pero el objetivo no es llegar hasta ese modelo, solo se busca llegar
hasta los reportes (numero de transacciones, movimientos del dinero). esquema
Erp queda fuera del alcance.

Centrado Operacion y modelo comercial

---

## Desarrollo

### Etapas

#### Step 1 - Creación e eventos

##### Detalle step1

- **Entidad subastadora**: Crea evento con una lista variable de unidades que
  sera evalada.
- **Plataforma**: Programacion de fotos, pasos a seguir, estimacion, con una
  metodologia aun fuera del alcance.
- **Plataforma**: Registra las ofertas del evento creado, crea X cantidad de
  ofertas

##### Adicionales step1

- Terminos y condiciones deben quedar claros, algunos vehiculos por ejemplo
  pueden tener multas.
- Deben quedar claro el tema de impuestos (Gravamen)

---

#### Step 2 - Publicación de eventos

##### Detalle step2

- **Entidad subastadora**: Revision y evaluacion del pinponeo en las ofertas con
  los siguientes resultados:
  - Un debate para establecer un valor
  - La entidad subastadores no esta de acuerdo y la oferta conversada se retira
    de la lista
  - Se confirma la oferta
- **Entidad subastadora**: Confirmacion del resultado con incluso previas
  coordinaciones externas.
  - Despues del pinponio incluso puede cambiarse la fecha de publicacion

##### Adicionales step2

- Hay un valor de inicio (valor de tasacion), suele ser un 50%, cuando se
  publica un evento
- Un evento puede durar generalmente 7 dias, pero las ultimas 2 horas es donde
  suele haber trafico

---

#### Step 3 - Subasta virtual

##### Detalle step3

- **Cliente**: Login, creacion de cuentas
- **Cliente**: Recarga de salgo mediante pasarela de pagos , solo se libera
  dependiendo de las reglas de negocio
- **Cliente**: Puede navegar entre eventos sin la necesidad de loguearse
- **Plataforma**: Validar el saldo del cliente en las pujas
- **Cliente**: En la subasta el cliente puede pujar:
  - Unitaria: Pujas rapidas, enfocadas mas a clientes pequeños
  - Virtual: Permite hacer multiplas pujas
- **Plataforma**: Culmina oferta y **Entidad subastadora** podria haber una
  interaccion en el **Cliente** (contrapropuesta), si es confirmada el cliente
  debe registrar los sustentos del pago de la comision
  - Aparte de la garantia, hay una comision que se le paga a la empresa que
    subasta, lo hace a 2 cuentas diferentes a travez de transferencias
    bancarias, el cliente deberia mandar los vauchers
  - Lo anterior mencionado tiene un tiempo limite, si no ocurre, se pasa al
    siguiente postor y asi sucesivamente
  - **Plataforma** revisa los documentos

##### Adicionales step3

- Siempre existe una garantia (200$ por evento) para evitar faltas de
  expectativa
- Segun la ultima puja puede reiniciar el tiempo a culminar

#### Step 4 - Concrecion de oferta ganadora

#### Step 5 - Entrega de bien

##### Detalle step5

- Trasabilidad despues del entrega del bien
- Documentos segun tipo de cliente
- **Entidad subastadora**: Programa firma de transferencia con su notaria y
  deben comunicar el proceso a travez de la plataforma
- **Cliente** firma y debe registrar la confirmacion y **Entidad subastadora**
  deberia de subir el ancla de entrega donde se indica la conformidad del
  **Cliente**

##### Adicionales step5

- Ofertas descartadas pueden pasar a otro lote , o tal vez el cliente lo vende
  al contado
- Las trasaccion o reportes estaran vinculados a nodefac

---

### Futuras aperturaciones

- Pensando a futuro en tipos de bien (Inicialmente solo vehiculos)
- Tipos de subasta (Con pujas - Vivencial, sobre cerrado o puesta en mano)

---

# Esquema de modelado de procesos

![[Pasted image 20240708091315.png]]

# Competencias

- Superbi
- Yaimi

# Reunion

- Sprint 3

## Preguntas

- Tienen ya un dominio adquirido
- TIenen configurado un servidor de correos?
- **TIenes un plataforma en la nube ? Sistema de archivos, Base de datos,
  Publicacion de la app por ambiente (Staging, Production)**

- Infraestructura local
- 2 servidores (Aplicacion, base de datos)
- De hecho deckerizado
- Usan Swarm
- Automatizacion con Gitlab
-

- Si hay rennvio de correo, valido 24 horas del enlace (Sprint 4) , al super
  admin le llega una notificacion para que reenvie
- Ya esta el correo listo
- Prefijo EVE
- La fecha de inicio y cierrer no puede tern una duracion mayor a 7 dias y que
  la fecha de inicio minimo tiene que tener 2 dias de diferencias a hoy , si hoy
  8 deberia permitiar para el 10 (Srpint 4)
- Cambio en el horario, sera por rango
- TOdos los campos en form de evento es obligatorio

Login y Notificaciones, CRUD de Eventos

3 tipos de notificaciones: Maximo mostrar 7 eventos Si se apreta una se borra si
hay mas las que estan ocultan se mostraran confome se borren

Si se archiva solo los de la vista

Oferta: 2 videos y/o 10 fotos , Anexos, minimammente 1 foto , maximo 10 fotos y
los 2 videos. cada foto 2mb cada video 10m

Description del bien (Texto enriquecido) En dirrecion se coloca una
geolocalizacion La descrpcion del bien tiene un limite de 200 caracteres

(Vehiculos, Inmuebles) Marca MOdelo año relacionado al bien vehicular
Autocalculado por tipo de bien

- Edicion de oferta no esta en sprint 3

- Cuando - Crean evento correcatmente - Visualizar evento
- ![[Pasted image 20240708093945.png]]

Puesta en valor: -Dolares por default -Valor inicial de subasta es calculado
-Todos los campos llenos Miercoles Carlos especifica bien

Repositorio Servidores

76089693

Lista de accesos

- Nombre | Email | DNI
- Frank Claudio Cary Viveros | <frank.cary@mrmisti.com> | 76060672
- Juan Carlos Granda Ramos | <j.granda@mrmisti.com> | 76166875
- Jean Marco Miranda LLanos | <jean.miranda@mrmisti.com> | 72409752
- Brucce Yul Villena Terreros | <brucce.villena@mrmisti.com> | 76089693
- Oliver Granda Ramos | <oliver.granda@mrmisti.com> | 75211693
- Yostin Ysmael Arequipa Puma | <yostin.arequipa@mrmisti.com> | -

Lista de accesos

- Frank Claudio Cary Viveros | <frank.cary@mrmisti.com>
- Juan Carlos Granda Ramos | <j.granda@mrmisti.com>
- Jean Marco Miranda LLanos | <jean.miranda@mrmisti.com>
- Brucce Yul Villena Terreros | <brucce.villena@mrmisti.com>
- Oliver Granda Ramos | <oliver.granda@mrmisti.com>
- Yostin Ysmael Arequipa Puma | <yostin.arequipa@mrmisti.com>

Requerimientos

- Acceso a su gitlab (lista de accesos) con 2 proyectos nuevos, uno para back y
  otro para front.
- Si es posible o una alternativa: Acceso SSH a su servidor para controlar los
  contenedores docker asociados al proyecto.
- Si es posible o una alternativa: Acceso a su proveedor de dominio para setear
  los subdominios o que alguien los establezca apuntando a la direccion ip del
  servidor (staging.deocasion.com.pe, deocasion.com.pe)
- Si es posible o una alternativa: Accesos a las bases de datos a usar dentro de
  su instancia POSTGRESQL
- Acceso a una cuenta de correo para el tema de validacion(por ejemplo
  <app@deocasion.com.pe>)

Estimacion

- Segun lo conversado estimo que este Sprint se cerraria a fines de julio

## Desglose de Actividades para el Sprint (8 - 31 de Julio)

### Semana 1 (8 al 14 de Julio)

- Hsata el viernes 12 Diego debe darnos acceso a los ambientes
- Miercoles 10 —
- **Inicio de Sesión:** Configuración y desarrollo del sistema de inicio de
  sesión.

### Semana 2 (15 al 21 de Julio)

- Creación, Edición y Listado de Eventos
- Creación de Ofertas

### Semana 3 (22 al 28 de Julio)

- **Notificaciones:** Notificaciones para los administradores del sistema
  relacionados a la empresa y para los administradores de la entidad subastadora
  cuando se crea un evento

### Semana 4 (28 al 31 de Julio)

<https://www.figma.com/design/7h5bUXzvQMQYmOc7jNNm4b/Untitled?node-id=1-20&t=RiXBcFssHy3Cq9EM-0>

Un dia antes al interno para verlo

- **Integración Continua:**
  - Configuración y prueba de integración continua.
- **Configuración de Ambientes:**
  - Preparación de ambientes de desarrollo, staging y producción.

---

# Maquetacion

![[Pasted image 20240708170820.png]]

## Sprint 3

- Inicio de sesión como Administrador | 15 de Julio
- Inicio de sesión como Empresa Subastadora | 16 de Julio
- Carga de fotos | 22 de Julio
- Creación de evento | 25 de Julio
- Creación de Ofertas | 25 de Julio
- Notificaciones Administrador y Empresa Subastadora | 30 de Julio

## (Empresa subastadora)

- Confirmación/Debate ofertas | 6 de Agosto
- Evaluación de puja | 6 de Agosto
  - Contrapropuesta de puja
  - Detalle de puja
- Confirmación de abono subastadora | 9 de Agosto
- Confirmación de sustento de transferencia | 14 de Agosto
  - Detalle de sustento
  - Observación de sustento
- Seguimiento de entrega | 16 de Agosto
  - Detalle de programación
  - Programación
- Reporte de eventos | 21 de Agosto

## (Perfil administrador)

- Home administrador
  - Detalle de eventos (6 de agosto)
  - Creación de ofertas –
  - Publicación de subasta (9 de agosto)
  - Confirmación de abono: (14 de agosto)
    - Observación de sustento
    - Detalle de sustento
  - Entrega del bien (21 de agosto)
    - Sustentos de entrega
    - Reporte de eventos

## (Cliente)

- Webhome (26 de Agosto)
- Detalle del evento (29 de Agosto)
- Detalle de la oferta (2 de Septiembre)
- Declaración de términos y condiciones (3 de Septiembre)
- Auditorio virtual (17 de Septiembre)
- Login (19 de Septiembre)
- Mis pujas (26 de Septiembre) - Debate de oferta - Registro de sustentos de
  pago - Registro de sustentos de transferencia
- Mi Monedero (2 de Octubre) - Retiro de fondos - Recarga de saldo
- Notificaciones (3 de octubre)
- Mis recibos (3 de octubre)

## (Deployment)

- Pruebas 4 de Octubre al 6 de Octubre
- **Despliegue 7 de Octubre**

# References

<https://we6akk.axshare.com/?id=oisq7m&p=sign_in__subastadora>\_

---
