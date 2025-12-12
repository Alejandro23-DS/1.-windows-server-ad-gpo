# Notas Técnicas y Fundamentos del Proyecto

Este documento proporciona el contexto teórico y las explicaciones técnicas detrás de la configuración y el diseño implementado en el dominio *colegiodm.local*. Sirve como manual conceptual para comprender el porqué de la estructura del proyecto.

---

## 1. Fundamentos de Active Directory Domain Services (AD DS)

### 1.1 ¿Qué es AD DS?

Active Directory Domain Services (Servicios de Dominio de Active Directory) es un servicio de directorio jerárquico y distribuido que se ejecuta en Windows Server. Su propósito principal es la administración centralizada de los recursos de red, la seguridad, las identidades y los permisos. Actúa como la base de datos de la organización.

* **Función Clave:** Permite la autenticación (verificar la identidad de un usuario) y la autorización (determinar qué puede hacer el usuario) en la red.


### 1.2 El Dominio y el Bosque

* **Dominio:** Es la frontera administrativa y de seguridad principal. En este proyecto, el dominio es **`colegiodm.local`**. Todos los usuarios, grupos y equipos de este dominio comparten una política de seguridad común.
* **Bosque (Forest):** Es la colección de uno o más dominios que comparten un esquema (definiciones de clases y atributos de objetos), configuración y catálogo global. Es el límite superior de la estructura de AD.

---

## 2. Unidades Organizativas (OU)

### 2.1 Propósito de las OU

Las Unidades Organizativas (OU) son contenedores lógicos dentro de un dominio que permiten crear una *jerarquía administrativa organizada*. No son un límite de seguridad estricto, pero son cruciales para dos tareas:

1.  **Delegación de Control:** Permiten delegar tareas administrativas a usuarios o grupos específicos (por ejemplo, permitir que un administrador local gestione solo las cuentas en la OU `Docentes`).
2.  **Aplicación de GPO:** Son el nivel más bajo al que se pueden vincular las Políticas de Grupo (GPO), permitiendo aplicar reglas específicas solo a un subconjunto de usuarios o equipos.

### 2.2 Diseño de Segmentación

El diseño de OUs (`Administrativos`, `Docentes`, `Estudiantes`) facilita la **segmentación de políticas**.

* **Ejemplo:** La GPO de Bloqueo USB se aplica exclusivamente a la OU `Estudiantes`. Si se hubiera aplicado al nivel de Dominio, también afectaría a `Docentes` y `Administrativos`, lo cual no es deseado.

---

## 3. Políticas de Grupo (GPO)

### 3.1 Fundamentos de GPO

Una Política de Grupo (GPO) es un conjunto de reglas y configuraciones que se aplican a usuarios o equipos. El procesamiento de las GPO sigue un orden estricto conocido como **L-S-D-O**:

1.  **Local:** Políticas aplicadas al equipo local.
2.  **Sitio (Site):** Políticas aplicadas a la ubicación física (Sitio de AD).
3.  **Dominio (Domain):** Políticas aplicadas a todo el dominio.
4.  **OU (Unidad Organizativa):** Políticas aplicadas a la OU específica. (El último en aplicarse tiene prioridad).

### 3.2 La GPO de Bloqueo USB

Esta GPO fue configurada como una medida de *seguridad preventiva* crítica.

