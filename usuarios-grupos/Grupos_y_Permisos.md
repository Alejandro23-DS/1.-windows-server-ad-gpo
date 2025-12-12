# 🔒 Grupos de Seguridad y Matriz de Permisos (Plan de Diseño)

***

⚠️Este documento detalla el plan de diseño de seguridad que se debe implementar en Active Directory (ADUC). La creación física de estos grupos está **pendiente de finalización**.

***

Este documento explica la finalidad de los grupos de seguridad y cómo se planea usarlos para la gestión de recursos y la aplicación de permisos en el dominio.

## 1. Grupos de Seguridad Planificados

Los siguientes grupos de seguridad se crearán dentro de sus respectivas Unidades Organizativas (OU) para facilitar la administración:

| Grupo de Seguridad | Ubicación (OU) | Tipo | Propósito |
| :--- | :--- | :--- | :--- |
| `g_sg_docentes_lectura` | Docentes | Global | Asignar permisos de **solo lectura** a carpetas y recursos compartidos de uso común para docentes. |
| `g_sg_docentes_escritura` | Docentes | Global | Asignar permisos de **escritura** en carpetas de proyectos y recursos exclusivos. |
| `g_sg_estudiantes_base` | Estudiantes | Global | **Objetivo de la GPO de Bloqueo USB** y punto de partida para permisos mínimos de red. |
| `g_dl_administracion` | Administrativos | Global | Grupo principal para **delegar permisos de administración** sobre las OUs de Docentes y Estudiantes. |

## 2. Roles y Aplicación de Políticas

| Rol | OU Contenedora | Impacto en la GPO y Seguridad |
| :--- | :--- | :--- |
| **Administrativos** | Administrativos | Control total sobre la gestión de identidades (Delegación de Control). |
| **Docentes** | Docentes | Acceso a recursos de enseñanza. Excluidos de las GPOs de máxima restricción. |
| **Estudiantes** | Estudiantes | Acceso limitado. **Sujetos a la GPO de Bloqueo USB** para denegar el acceso a almacenamiento extraíble. |

## 3. Próximos Pasos (Implementación)

Una vez creados, estos grupos se añadirán a los usuarios correspondientes y se usarán en la configuración de permisos de archivos y carpetas, así como en los filtros de seguridad de las GPOs.
