# Guía de Despliegue en GitHub Pages

## Pasos para desplegar

### 1. Inicializar repositorio Git (si no lo has hecho)

```bash
cd /Users/albertomeouchi/Desktop/CODE/perdida
git init
git add .
git commit -m "Initial commit: La Gran Pérdida visualization"
```

### 2. Crear repositorio en GitHub

1. Ve a [GitHub](https://github.com) y crea un nuevo repositorio
2. **NO** inicialices con README, .gitignore o licencia (ya los tenemos)
3. Copia la URL del repositorio (ej: `https://github.com/tu-usuario/la-gran-perdida.git`)

### 3. Conectar y subir archivos

```bash
git remote add origin https://github.com/tu-usuario/la-gran-perdida.git
git branch -M main
git push -u origin main
```

### 4. Activar GitHub Pages

1. Ve a tu repositorio en GitHub
2. Click en **Settings** (Configuración)
3. En el menú lateral, click en **Pages**
4. En **Source**, selecciona:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click en **Save**

### 5. Acceder a tu sitio

Tu sitio estará disponible en:
```
https://[tu-usuario].github.io/[nombre-repositorio]/
```

Por ejemplo:
```
https://albertomeouchi.github.io/la-gran-perdida/
```

## Notas importantes

- ⚠️ **El despliegue puede tardar 1-2 minutos** después de activar GitHub Pages
- ✅ El archivo `.nojekyll` está incluido para evitar problemas con Jekyll
- ✅ Todas las rutas son relativas y funcionarán correctamente
- ✅ Los archivos GeoJSON en `files/` se servirán correctamente

## Verificar que todo funciona

1. Abre tu sitio en el navegador
2. Abre la consola del navegador (F12)
3. Verifica que no haya errores 404 al cargar los archivos GeoJSON
4. Prueba la visualización interactiva

## Actualizar el sitio

Cada vez que hagas cambios:

```bash
git add .
git commit -m "Descripción de los cambios"
git push
```

Los cambios se reflejarán en GitHub Pages automáticamente (puede tardar 1-2 minutos).

