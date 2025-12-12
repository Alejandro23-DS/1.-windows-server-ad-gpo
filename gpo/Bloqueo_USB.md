# Política de Grupo: Bloqueo de Almacenamiento Extraíble (USB)

Esta GPO se implementó para denegar el acceso total a los dispositivos de almacenamiento extraíble en la OU de Estudiantes.

## 1. Creación y Vinculación

Se creó la política en GPMC y se vinculó a la Unidad Organizativa (OU) de **Estudiantes**.

* **Creación de GPO:**
    ![Creación de la GPO de Bloqueo USB](./screenshots/09-GPMC-Crear-GPO-BloqueoUSB.png)

* **Vinculación a Estudiantes:**
    ![GPO Vinculada a la OU Estudiantes](./screenshots/10-GPMC-GPO-Vinculada-Estudiantes.png)

## 2. Configuración de la Política

La configuración se realizó en:
`Configuración de Usuario > Políticas > Plantillas Administrativas > Sistema > Acceso a Almacenamiento Extraíble`

Se establecieron los siguientes parámetros para denegar el acceso:

* **Ruta de la Configuración:**
    ![Edición de Acceso a Almacenamiento Extraíble](./screenshots/11-GPMC-Editar-AccesoAlmacenamientoExtraible.png)

* **Configuración Aplicada (Denegar Acceso Total):**
    ![Configuración de Denegar Acceso Total](./screenshots/12-GPMC-Configurar-DenegarAccesoTotal.png)

## 3. Verificación

Se verifica que la GPO esté correctamente aplicada y habilitada en la OU deseada.

* **Verificación Final:**
    ![Verificación de la GPO Vinculada](./screenshots/13-GPMC-Verificacion-GPO-Vinculada.png)

---
**Nota:** Los informes HTML de esta GPO y los archivos de *backup* se añadirán a esta carpeta en el futuro para facilitar la restauración e importación.
