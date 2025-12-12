# 🔒 Grupos de Seguridad y Matriz de Permisos

Este documento detalla la finalidad de los grupos de seguridad creados en las Unidades Organizativas (OU) y la delegación de permisos o roles que se les ha asignado.

## 1. Grupos de Seguridad Creados

Se han creado grupos de seguridad específicos en las OUs `Docentes` y `Administrativos` para facilitar la gestión de recursos y la aplicación de políticas.

| Grupo de Seguridad | Ubicación (OU) | Propósito |
| :--- | :--- | :--- |
| `g_sg_docentes_lectura` | Docentes | Asignar permisos de lectura a recursos compartidos solo a docentes. |
| `g_sg_docentes_escritura` | Docentes | Asignar permisos de escritura a recursos compartidos y carpetas de proyecto. |
| `g_sg_estudiantes_base` | Estudiantes | Grupo base para aplicar políticas (como la GPO de Bloqueo USB) y permisos mínimos. |
| `g_dl_administracion` | Administrativos | Grupo para delegar permisos de administración sobre OUs específicas. |

## 2. Tipos de Usuarios y Roles

| Rol | OU Contenedora | Funciones Principales |
| :--- | :--- | :--- |
| **Administrativos** | Administrativos | Gestión de usuarios, equipos y GPOs. |
| **Docentes** | Docentes | Acceso a recursos de enseñanza, creación de contenidos y acceso completo a USB. |
| **Estudiantes** | Estudiantes | Acceso a PCs y red con restricciones, y **acceso denegado al almacenamiento extraíble (USB)**. |

## 3. Delegación de Control

* **Administrativos:** Tienen delegación de control total sobre las OUs `Docentes` y `Estudiantes` para la gestión diaria de cuentas de usuario.
* **Docentes:** No tienen permisos delegados de administración de dominio, solo permisos de acceso a recursos.
