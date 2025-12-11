# Active Directory – Gestión de Usuarios, Grupos y GPO

Repositorio con toda la configuración realizada en **Windows Server 2022**, incluyendo:

- Administración de Active Directory  
- Gestión de usuarios y grupos  
- Organización mediante OU  
- Implementación de políticas de seguridad  
- Buenas prácticas en entornos Windows Server  

---

## 📂 Estructura del repositorio

/
├── screenshots/ # Capturas de pantalla usadas en el informe
├── usuarios-grupos/ # Documentación de OUs, usuarios y grupos creados
├── gpo/ # Documentación de políticas aplicadas
├── notas-tecnicas.md # Explicaciones adicionales
└── README.md # Este archivo


---

## 🏗️ 1. Instalación de Active Directory y DNS

Se documenta la instalación de los roles **AD DS** y **DNS**, la promoción del servidor y la creación del dominio:

colegiodm.local


Incluye:

- Roles instalados  
- Comprobación de AD DS  
- Nivel funcional del dominio  
- Nivel funcional del bosque  

---

## 🗂️ 2. Estructura Organizacional (OU)

Se creó una estructura ordenada para la administración:

- AulaComputo  
- Administrativos  
- Estudiantes  
- Docentes  
- Grupos vinculados a cada área  

Incluye:

- Usuarios organizados  
- Grupos (Docentes-Matemática, Docentes-Ciencias, Estudiantes-Aula, etc.)  

---

## 👥 3. Creación de Usuarios y Grupos

Cada OU contiene sus usuarios correspondientes.

Se incluyen:

- Nombre del usuario  
- Usuario de inicio de sesión  
- (Las contraseñas administrativas no se muestran en capturas por seguridad)  
- Grupos creados manualmente  
- Evidencias mediante capturas  

---

## 🛑 4. Políticas de Grupo (GPO)

En la carpeta **/gpo** se muestran las políticas implementadas:

### ✔ Bloqueo de USB  
Evita que dispositivos USB no autorizados sean usados.

### ✔ Restricción de almacenamiento extraíble  
Limita acceso a unidades externas.

### ✔ Control de navegación básica  
Ejemplo: impedir descargas o restringir navegadores.

### ✔ Verificación de GPO vinculada  
Captura final que demuestra la aplicación correcta.

---

## 📸 5. Capturas de pantalla

Todas las imágenes se encuentran en la carpeta:

/screenshots


Con nombres ordenados, por ejemplo:

- 01-Panel-RolesInstalados.png  
- 02-Asistente-ConfirmacionRolesADDS-DNS.png  
- …  
- 13-GPMC-Verificacion-GPO-Vinculada.png  

---

## 📝 6. Documentación técnica adicional

Archivo:

notas-tecnicas.md


Incluye explicaciones sobre:

- Qué es AD DS  
- Qué es un dominio  
- Cómo funcionan las OU  
- Qué es una GPO y cómo se aplica  
- Buenas prácticas básicas de administración  

---

## 🎯 Objetivo del proyecto

Este repositorio busca demostrar habilidades en:

- Administración de Active Directory  
- Gestión de usuarios y grupos  
- Organización mediante OU  
- Implementación de políticas de seguridad  
- Buenas prácticas en entornos Windows Server  

---
