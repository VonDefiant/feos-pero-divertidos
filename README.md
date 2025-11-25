# 🎁 Amigo Secreto - Feos pero divertidos

Aplicación web para sorteo de amigo secreto con sincronización en tiempo real usando JSONBin.io.

## ✨ Características

- 🎲 Asignación aleatoria de amigos secretos
- 🔄 Sincronización automática cada 3 segundos
- 🚫 Reglas de exclusión personalizadas
- 📱 Diseño responsive
- 🎨 Interfaz moderna y festiva
- 🔐 Cada sesión tiene un código único

## 🚀 Cómo subir a GitHub Pages

### Paso 1: Crear repositorio en GitHub

1. Ve a [GitHub](https://github.com) e inicia sesión
2. Click en el botón **"+"** (arriba derecha) → **"New repository"**
3. Nombre del repositorio: `amigo-secreto` (o el que prefieras)
4. Marca como **Public**
5. NO marques "Add a README file"
6. Click en **"Create repository"**

### Paso 2: Subir el archivo

Tienes dos opciones:

#### Opción A: Subir directamente en la web (MÁS FÁCIL)

1. En tu repositorio recién creado, click en **"uploading an existing file"**
2. Arrastra el archivo `index.html` a la zona de subida
3. Escribe un mensaje de commit: "Add amigo secreto app"
4. Click en **"Commit changes"**

#### Opción B: Usar Git en terminal

```bash
git clone https://github.com/TU-USUARIO/amigo-secreto.git
cd amigo-secreto
# Copia el archivo index.html aquí
git add index.html
git commit -m "Add amigo secreto app"
git push origin main
```

### Paso 3: Activar GitHub Pages

1. En tu repositorio, ve a **Settings** (⚙️)
2. En el menú izquierdo, click en **"Pages"**
3. En **"Source"**, selecciona **"Deploy from a branch"**
4. En **"Branch"**, selecciona **"main"** y carpeta **"/ (root)"**
5. Click en **"Save"**
6. ¡Espera 2-3 minutos!

### Paso 4: Acceder a tu app

Tu app estará disponible en:
```
https://TU-USUARIO.github.io/amigo-secreto/
```

Por ejemplo, si tu usuario es `javierlopez`:
```
https://javierlopez.github.io/amigo-secreto/
```

## 📱 Cómo usar la app

### Para el organizador:

1. Abre la URL de tu GitHub Pages
2. Ingresa los nombres de todos los participantes (mínimo 3)
3. Click en **"✨ Crear Sesión"**
4. Se generará un código (ej: `67651ab5ad19ca34f8d3c8b9`)
5. Comparte este código en tu grupo de WhatsApp

### Para los participantes:

1. Abre la misma URL
2. Click en **"🚪 Unirse a Sesión Existente"**
3. Ingresa el código que recibiste
4. Selecciona tu nombre
5. Click en **"🎲 Revelar Mi Amigo Secreto"**

## 🔄 Sincronización

- Los cambios se sincronizan automáticamente cada 3 segundos
- Cuando alguien revela su amigo secreto, su nombre desaparece de la lista
- Todos los participantes ven los cambios en tiempo real

## 🚫 Reglas de Exclusión

Actualmente configuradas en el código:

- Diego no puede tener a Amely ni Darcy
- Darcy no puede tener a Amely ni Diego
- Amely no puede tener a Diego ni Darcy
- Carlos no puede tener a Gaby
- Gaby no puede tener a Carlos

### Cómo modificar las exclusiones:

Edita el archivo `index.html`, busca esta sección:

```javascript
const EXCLUSIONS = {
    'Diego': ['Amely', 'Darcy'],
    'Darcy': ['Amely', 'Diego'],
    'Amely': ['Diego', 'Darcy'],
    'Carlos': ['Gaby'],
    'Gaby': ['Carlos']
};
```

## 🔧 Tecnologías

- HTML5
- CSS3 (con animaciones y gradientes)
- JavaScript (Vanilla)
- JSONBin.io (para almacenamiento y sincronización)
- GitHub Pages (hosting gratuito)

## 📝 Notas

- Los datos se almacenan en JSONBin.io (1000 requests gratis al mes)
- Cada sesión es independiente y tiene su propio código
- Los códigos no expiran
- No se requiere instalación ni configuración adicional

## 🎨 Personalización

Para cambiar colores, edita las variables CSS al inicio del archivo:

```css
:root {
    --primary: #d4145a;    /* Rosa principal */
    --secondary: #fbb034;  /* Naranja */
    --accent: #009688;     /* Verde azulado */
    --dark: #1a1a2e;       /* Oscuro */
    --light: #fff5f5;      /* Claro */
    --success: #4caf50;    /* Verde éxito */
}
```

## 🐛 Solución de problemas

**La app no carga:**
- Verifica que GitHub Pages esté activado
- Espera 2-3 minutos después de activar Pages
- Limpia caché del navegador (Ctrl+F5)

**Los cambios no se sincronizan:**
- Verifica tu conexión a internet
- Asegúrate que todos usan el mismo código
- La sincronización toma hasta 3 segundos

**Error al crear sesión:**
- Verifica que tienes al menos 3 participantes
- Verifica que no hay nombres duplicados
- Recarga la página e intenta de nuevo

## 📄 Licencia

Uso libre para fines personales y no comerciales.

---

Hecho con ❤️ para el grupo "Feos pero divertidos" 😄
