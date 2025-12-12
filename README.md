# Active Directory (AD) & Group Policy Management (GPO) Project

Este repositorio documenta la configuración completa de un entorno de Active Directory implementado sobre **Windows Server 2022**. El objetivo es demostrar habilidades en la gestión de identidades, la organización jerárquica y la implementación de políticas de seguridad.

## 🎯 Objetivo Principal

El proyecto busca demostrar las habilidades en:

* Diseño e implementación de la infraestructura de Active Directory Domain Services (AD DS).
* Gestión de usuarios, grupos y Unidades Organizativas (OU).
* Aplicación de políticas de seguridad a través de GPO.
* Documentación de buenas prácticas en la administración de entornos Windows Server.

---

## 📂 Estructura del Repositorio

| Directorio / Archivo | Contenido y Propósito |
| :--- | :--- |
| **`screenshots/`** | Imágenes ordenadas que documentan cada paso de la configuración. |
| **`gpo/`** | Documentación y plan de diseño de las Políticas de Grupo (GPO) implementadas. |
| **`usuarios-grupos/`** | Documentación del plan de diseño de OUs, usuarios y grupos de seguridad. |
| **`notas-tecnicas.md`** | Explicaciones teóricas y conceptuales sobre AD DS, dominios, OUs y GPO. |
| `README.md` | (Este archivo) Visión general y un índice de todo el proyecto. |

---

## ⚙️ I. Implementación de Infraestructura (AD DS y DNS)

Se documenta la instalación y promoción del servidor a Controlador de Dominio, estableciendo el dominio principal: **`colegiodm.local`**.

* Roles de servidor instalados y verificados.
* Configuración inicial y comprobación del servicio DNS.
* Validación del nivel funcional del bosque y dominio.

## 🗂️ II. Diseño y Gestión de Unidades Organizativas (OU)

Se implementó una estructura jerárquica para la administración lógica de recursos y la aplicación eficiente de políticas.

* **OUs Principales:** `Administrativos`, `Docentes`, `Estudiantes`, y `AulaComputo`.
* **Gestión de Cuentas:** Documentación de usuarios, plantillas de inicio de sesión y la creación de grupos de seguridad vinculados a cada área.
* **Plan de Grupos:** La carpeta **`/usuarios-grupos`** contiene el plan de diseño de seguridad (`Grupos_y_Permisos.md`) detallando la función de cada grupo.

## 🛡️ III. Políticas de Grupo (GPO)

La carpeta **`/gpo`** documenta las políticas de seguridad implementadas para cumplir con los requisitos del entorno, especialmente en áreas de alto riesgo como el aula de cómputo.

### 🛑 Políticas Destacadas

| Nombre de la Política | Objetivo de Seguridad | Estado de Documentación |
| :--- | :--- | :--- |
| **Bloqueo de USB** | Prevenir el uso de dispositivos de almacenamiento extraíble no autorizados. | Detallada en `gpo/Bloqueo_USB.md` |
| **Restricción de Almacenamiento** | Limitar el acceso a unidades externas, reforzando la seguridad. | |
| **Control de Navegación** | Restricción de descargas y uso de navegadores para entornos controlados. | |

* Se incluye la verificación final (`GPMC-Verificacion-GPO-Vinculada.png`) que demuestra la correcta aplicación y vinculación de las políticas.

---

## 📖 Documentación Adicional

### 🗒️ Notas Técnicas (`notas-tecnicas.md`)

Este archivo amplía la información conceptual y práctica del proyecto, actuando como un **manual de referencia** sobre:

* Conceptos clave de Active Directory y Dominios.
* Fundamentos y buenas prácticas de la herencia y aplicación de GPOs.

### 🖼️ Evidencias Gráficas (`screenshots/`)

Todas las evidencias visuales están ordenadas secuencialmente, desde la **`01-Panel-RolesInstalados.png`** hasta la **`13-GPMC-Verificacion-GPO-Vinculada.png`**, para facilitar el seguimiento paso a paso de la implementación.
