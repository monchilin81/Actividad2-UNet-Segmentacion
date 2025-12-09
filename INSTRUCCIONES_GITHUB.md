# Instrucciones para Subir el Repositorio a GitHub

Sigue estos pasos para crear y subir el repositorio a GitHub:

## Paso 1: Crear el repositorio en GitHub

1. Ve a [GitHub](https://github.com) e inicia sesión con tu usuario `monchilin81`
2. Haz clic en el icono **+** en la esquina superior derecha y selecciona **New repository**
3. Completa los datos:
   - **Repository name:** `Actividad2-UNet-Segmentacion`
   - **Description:** "Evaluación exhaustiva de parámetros en UNet para segmentación de vasos sanguíneos"
   - **Public:** Selecciona esta opción (ya que quieres que sea público)
   - **Initialize this repository with:** NO marques nada (ya tienes archivos locales)
4. Haz clic en **Create repository**

## Paso 2: Inicializar Git en tu máquina local

Abre una terminal en la carpeta `Actividad2-UNet-Segmentacion` y ejecuta:

```bash
git init
git config user.name "Damián Vidal"
git config user.email "tu_email@example.com"
git add .
git commit -m "Initial commit: Actividad 2 UNet Segmentation"
```

## Paso 3: Conectar con GitHub y subir

Ejecuta los siguientes comandos (reemplaza `<URL_DEL_REPO>` con la URL que GitHub te proporcione):

```bash
git branch -M main
git remote add origin https://github.com/monchilin81/Actividad2-UNet-Segmentacion.git
git push -u origin main
```

**Nota:** Si GitHub te pide autenticación, usa:
- Usuario: `monchilin81`
- Contraseña: Tu token de acceso personal (PAT) o contraseña de GitHub

## Paso 4: Verificar

1. Ve a tu repositorio en GitHub: https://github.com/monchilin81/Actividad2-UNet-Segmentacion
2. Verifica que todos los archivos estén presentes
3. El repositorio debería verse así:
   - ✅ Carpeta `notebooks/`
   - ✅ Carpeta `codigos_parametros/`
   - ✅ Carpeta `resultados/`
   - ✅ Archivo `README.md`
   - ✅ Archivo `.gitignore`

## Paso 5: Obtener el enlace para la entrega

El enlace de tu repositorio es:
```
https://github.com/monchilin81/Actividad2-UNet-Segmentacion
```

Incluye este enlace en tu entrega del proyecto.

## Comandos útiles para futuras actualizaciones

Si necesitas hacer cambios después:

```bash
# Ver estado
git status

# Agregar cambios
git add .

# Hacer commit
git commit -m "Descripción del cambio"

# Subir cambios
git push origin main
```

## Solución de problemas

**Error: "fatal: not a git repository"**
- Asegúrate de estar en la carpeta correcta: `cd Actividad2-UNet-Segmentacion`

**Error: "Permission denied (publickey)"**
- Configura tu clave SSH en GitHub o usa HTTPS con tu token de acceso

**Error: "remote origin already exists"**
- Ejecuta: `git remote remove origin` y luego vuelve a agregar el remote

---

¡Listo! Tu repositorio debería estar ahora en GitHub y accesible para la entrega.
