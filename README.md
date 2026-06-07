# Comandos Básicos de Git

Git es un sistema de control de versiones distribuido que te permite rastrear cambios en tu código. Aquí están los comandos básicos que necesitas conocer:

## 1. **git init** - Inicializar un repositorio

Crea un nuevo repositorio Git en tu directorio actual.

```bash
git init
```

**Ejemplo:**
```bash
cd mi-proyecto
git init
# Salida: Initialized empty Git repository in /ruta/a/mi-proyecto/.git/
```

Este comando crea una carpeta oculta `.git` que almacena toda la información del repositorio.

---

## 2. **git clone** - Clonar un repositorio

Descarga una copia completa de un repositorio remoto a tu máquina local.

```bash
git clone <URL-del-repositorio>
```

**Ejemplo:**
```bash
git clone https://github.com/usuario/mi-repositorio.git
# Salida: Cloning into 'mi-repositorio'...
```

Esto crea una carpeta llamada `mi-repositorio` con todos los archivos y el historial completo del proyecto.

---

## 3. **git status** - Ver el estado actual

Muestra el estado de tu directorio de trabajo y el área de preparación (staging area).

```bash
git status
```

**Ejemplo:**
```bash
git status
# Salida:
# On branch main
# Changes not staged for commit:
#   modified:   archivo.txt
# 
# Untracked files:
#   nuevo-archivo.js
```

Te muestra qué archivos han cambiado, cuáles están listos para confirmar y cuáles son nuevos.

---

## 4. **git add** - Preparar archivos para confirmar

Añade archivos al área de preparación (staging area) antes de hacer commit.

```bash
git add <archivo>
git add .
```

**Ejemplos:**
```bash
# Agregar un archivo específico
git add archivo.txt

# Agregar todos los cambios
git add .

# Agregar todos los archivos de una carpeta específica
git add src/
```

Después de ejecutar esto, los archivos están listos para ser confirmados.

---

## 5. **git commit** - Confirmar cambios

Registra los cambios preparados en el historial del repositorio con un mensaje descriptivo.

```bash
git commit -m "Mensaje descriptivo del cambio"
```

**Ejemplo:**
```bash
git commit -m "Añadir función de autenticación"
# Salida:
# [main a1b2c3d] Añadir función de autenticación
#  1 file changed, 25 insertions(+), 5 deletions(-)
```

El mensaje debe ser claro y conciso, explicando qué cambios se realizaron.

**Consejo:** Usa commits frecuentes con mensajes descriptivos para mantener un historial limpio.

---

## 6. **git push** - Enviar cambios al repositorio remoto

Sube tus commits locales al repositorio remoto (como GitHub).

```bash
git push <rama-remota> <rama-local>
git push origin main
```

**Ejemplo:**
```bash
git push origin main
# Salida:
# Enumerating objects: 5, done.
# Counting objects: 100% (5/5), done.
# Writing objects: 100% (3/3), 250 bytes | 250.00 KiB/s, done.
# Total 3 (delta 2), reused 0 (delta 0), reused pack 0 (delta 0)
# To https://github.com/usuario/mi-repositorio.git
#    a1b2c3d..e4f5g6h  main -> main
```

Esto envía tus cambios locales al servidor remoto para que otros desarrolladores puedan acceder a ellos.

---

## 7. **git pull** - Descargar cambios del repositorio remoto

Descarga e integra los cambios del repositorio remoto a tu rama local.

```bash
git pull <rama-remota> <rama-local>
git pull origin main
```

**Ejemplo:**
```bash
git pull origin main
# Salida:
# remote: Enumerating objects: 3, done.
# Unpacking objects: 100% (3/3), 250 bytes | 250.00 KiB/s, done.
# From https://github.com/usuario/mi-repositorio.git
#    a1b2c3d..e4f5g6h  main       -> origin/main
# Updating a1b2c3d..e4f5g6h
# Fast-forward
#  archivo.txt | 2 +-
#  1 file changed, 1 insertion(+), 1 deletion(-)
```

Esto integra los cambios que otros han hecho en el repositorio remoto con tu trabajo local.

---

## Flujo de Trabajo Típico

Aquí está el flujo típico de usar estos comandos juntos:

```bash
# 1. Clonar un repositorio
git clone https://github.com/usuario/mi-repositorio.git
cd mi-repositorio

# 2. Crear o modificar archivos
echo "Nuevo contenido" > archivo.txt

# 3. Ver qué cambió
git status

# 4. Preparar los cambios
git add archivo.txt

# 5. Confirmar los cambios
git commit -m "Actualizar archivo.txt con nuevo contenido"

# 6. Descargar cambios del equipo (opcional pero recomendado)
git pull origin main

# 7. Enviar tus cambios al repositorio remoto
git push origin main
```

---

## Resumen de Comandos

| Comando | Función |
|---------|---------|
| `git init` | Inicializar un repositorio Git nuevo |
| `git clone <URL>` | Descargar un repositorio remoto |
| `git status` | Ver el estado de los archivos |
| `git add <archivo>` | Preparar cambios para confirmar |
| `git commit -m "mensaje"` | Registrar cambios en el historial |
| `git push` | Enviar cambios al repositorio remoto |
| `git pull` | Descargar cambios del repositorio remoto |

Con estos comandos básicos, puedes comenzar a trabajar con Git de manera efectiva. ¡A medida que ganes experiencia, descubrirás comandos más avanzados que te ayudarán a manejar situaciones más complejas!
