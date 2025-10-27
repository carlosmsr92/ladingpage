# Portfolio Carlos Manuel Suárez Rivero
## Data Scientist & AI Specialist

Portfolio profesional en HTML/CSS/JavaScript puro, optimizado para GitHub Pages.

---

## 📋 Contenido

- [Características](#características)
- [Configuración Inicial](#configuración-inicial)
- [Deployment a GitHub Pages](#deployment-a-github-pages)
- [Configuración de Dominio Personalizado](#configuración-de-dominio-personalizado)
- [Modificar Contenido](#modificar-contenido)

---

## ✨ Características

- ✅ **100% Gratis**: Hosting en GitHub Pages sin costos
- ✅ **Tema Adaptativo**: Se adapta automáticamente a modo oscuro/claro del navegador
- ✅ **Responsive**: Diseño perfecto en móvil, tablet y desktop
- ✅ **Formulario funcional**: Integrado con Formspree (gratis hasta 50 emails/mes)
- ✅ **Diseño profesional**: Gradientes, animaciones, logo personalizado
- ✅ **SEO optimizado**: Meta tags y estructura semántica
- ✅ **Sin dependencias**: HTML/CSS/JS puro, carga ultra rápida

---

## 🚀 Configuración Inicial

### **Paso 1: Configurar Formspree (Formulario de Contacto)** - 5 minutos

1. Ve a [formspree.io](https://formspree.io/) y crea una cuenta **GRATIS**
2. Click en **"+ New Form"**
3. Dale un nombre: **"Portfolio Contact"**
4. Copia el **Form ID** que te dan (ejemplo: `mnnqkpdg`)
5. Abre el archivo `index.html` en un editor de texto
6. Busca la línea ~402 (aproximadamente):
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="contact-form" id="contactForm">
   ```
7. Reemplaza `YOUR_FORM_ID` con tu Form ID de Formspree:
   ```html
   <form action="https://formspree.io/f/mnnqkpdg" method="POST" class="contact-form" id="contactForm">
   ```
8. Guarda el archivo

**Configuración adicional en Formspree (Recomendado):**
- En tu dashboard de Formspree → Settings:
  - **Email Address**: `carlosmsr1992@gmail.com` (donde quieres recibir los mensajes)
  - **Reply-To**: ✅ Activa "Use sender's email as reply-to"
  - **Spam Protection**: ✅ Activa "reCAPTCHA v3"

**✅ Listo:** Tu formulario ya funciona - recibirás los mensajes en tu email

---

## 📤 Deployment a GitHub Pages

### **Opción A: Con GitHub Desktop (Más fácil)**

1. **Descarga GitHub Desktop**: https://desktop.github.com/
2. **Instala y abre** GitHub Desktop
3. Click en **"File" → "New Repository"**:
   - Name: `portfolio` (o el nombre que quieras)
   - Local Path: Selecciona la carpeta `static-portfolio`
   - ✅ Check "Initialize this repository with a README"
4. Click en **"Create Repository"**
5. Click en **"Publish repository"**:
   - ✅ Desactiva "Keep this code private" (debe ser público para GitHub Pages)
   - Click **"Publish Repository"**
6. Ve a **tu repositorio en GitHub** (se abre automáticamente)
7. Click en **"Settings"** → **"Pages"** (en el menú lateral)
8. En **"Source"**:
   - Branch: `main`
   - Folder: `/ (root)`
9. Click **"Save"**
10. **Espera 2-3 minutos** y recarga la página
11. Tu sitio estará en: `https://TU-USUARIO.github.io/portfolio`

---

### **Opción B: Con Git (Línea de comandos)**

```bash
# 1. Abre terminal/cmd en la carpeta static-portfolio

# 2. Inicializa Git
git init

# 3. Añade todos los archivos
git add .

# 4. Haz el primer commit
git commit -m "Portfolio inicial"

# 5. Crea repositorio en GitHub.com (hazlo desde la web):
# - Ve a https://github.com/new
# - Name: portfolio
# - Public
# - NO inicialices con README
# - Crea el repositorio

# 6. Conecta tu carpeta al repositorio (reemplaza TU-USUARIO):
git remote add origin https://github.com/TU-USUARIO/portfolio.git

# 7. Sube el código
git branch -M main
git push -u origin main

# 8. Activa GitHub Pages:
# - Ve a tu repositorio en GitHub
# - Settings → Pages
# - Source: main branch, / (root)
# - Save

# 9. Tu sitio estará en:
# https://TU-USUARIO.github.io/portfolio
```

---

## 🌐 Configuración de Dominio Personalizado

### **¿Qué necesitas?**
- Dominio comprado en IONOS, GoDaddy, Namecheap, etc.
- Portfolio ya publicado en GitHub Pages

### **Pasos:**

#### **1. Configurar DNS en tu proveedor de dominio (IONOS, GoDaddy, etc.)**

**Opción A: Con subdominio www (Recomendado)**

Añade estos registros DNS:

| Tipo | Host/Nombre | Valor/Destino | TTL |
|------|-------------|---------------|-----|
| **A** | @ | 185.199.108.153 | 3600 |
| **A** | @ | 185.199.109.153 | 3600 |
| **A** | @ | 185.199.110.153 | 3600 |
| **A** | @ | 185.199.111.153 | 3600 |
| **CNAME** | www | TU-USUARIO.github.io | 3600 |

**Opción B: Solo dominio raíz (sin www)**

Añade solo los 4 registros A de arriba.

**Ejemplo para IONOS.es:**
1. Login en IONOS → **Dominios & SSL**
2. Click en tu dominio → **DNS**
3. **Añadir registro** (para cada uno de los de arriba)
4. Guarda los cambios

#### **2. Configurar dominio en GitHub**

1. Ve a tu repositorio en GitHub
2. **Settings** → **Pages**
3. En **"Custom domain"** escribe: `www.tudominio.com` (o `tudominio.com`)
4. Click **"Save"**
5. **Espera 10-60 minutos** para que DNS se propague
6. ✅ Activa **"Enforce HTTPS"** cuando esté disponible (certificado SSL gratis)

#### **3. Verifica que funciona**

Después de 10-60 minutos, prueba:
- `https://www.tudominio.com` → Debe cargar tu portfolio
- `https://tudominio.com` → Debe redirigir a www (si configuraste así)

---

## ✏️ Modificar Contenido

### **Añadir nuevo proyecto:**

1. Abre `index.html`
2. Busca la sección `<!-- Projects Section -->` (línea ~224)
3. **Copia** todo el bloque `<div class="project-card">...</div>`
4. **Pégalo** debajo del proyecto existente
5. Modifica:
   - Título del proyecto
   - Descripción
   - Tecnologías (badges)
   - Link del dashboard
   - Imagen: guarda tu imagen en `images/` y actualiza la ruta

**Ejemplo:**
```html
<div class="project-card" data-testid="card-project-1">
    <div class="project-grid">
        <div class="project-image">
            <img src="images/tu-nuevo-proyecto.png" alt="Título del Proyecto">
            <div class="project-image-overlay"></div>
        </div>
        <div class="project-content">
            <h3 class="project-title">Tu Nuevo Proyecto</h3>
            <p class="project-description">
                Descripción detallada de tu proyecto...
            </p>
            <div class="project-tech">
                <span class="tech-badge">Python</span>
                <span class="tech-badge">Power BI</span>
            </div>
            <a href="https://tu-dashboard.com" target="_blank" class="btn btn-primary">
                Ver Dashboard
                <svg>...</svg>
            </a>
        </div>
    </div>
</div>
```

### **Cambiar colores:**

Abre `styles.css` y modifica las variables en `:root` (líneas 6-31):

```css
:root {
    /* Cambia estos valores */
    --color-primary: hsl(199, 89%, 48%);  /* Azul principal */
    --color-chart-2: hsl(174, 72%, 56%);  /* Verde/cyan */
    /* ... */
}
```

### **Actualizar info de contacto:**

En `index.html`, busca y modifica:
- LinkedIn URL (3 lugares)
- GitHub URL (3 lugares)

---

## 🔄 Actualizar tu sitio después de cambios

### **Con GitHub Desktop:**
1. Haz tus cambios en los archivos
2. Abre GitHub Desktop
3. Verás los cambios listados
4. Escribe un mensaje (ej: "Añadido nuevo proyecto")
5. Click **"Commit to main"**
6. Click **"Push origin"**
7. Espera 1-2 minutos → Tu sitio se actualiza automáticamente

### **Con Git (terminal):**
```bash
git add .
git commit -m "Descripción de tus cambios"
git push
```

---

## 📞 Soporte

### **Problemas comunes:**

**❌ Formulario no envía emails**
- Verifica que reemplazaste `YOUR_FORM_ID` con tu ID real de Formspree
- Revisa spam en tu email
- Verifica configuración en dashboard de Formspree

**❌ Dominio no funciona después de 1 hora**
- Verifica registros DNS en tu proveedor
- Asegúrate que el dominio está guardado en GitHub Pages settings
- Algunos proveedores tardan hasta 48h (poco común)

**❌ Página muestra error 404**
- Verifica que el repositorio es **público**
- Confirma que GitHub Pages está activado (Settings → Pages)
- Verifica que la rama es `main` y folder es `/ (root)`

**❌ Imágenes no cargan**
- Verifica que las rutas son correctas: `images/nombre-archivo.png`
- Las rutas son case-sensitive (mayúsculas/minúsculas importan)
- Asegúrate que subiste la carpeta `images/` al repositorio

---

## 💰 Costos

- **GitHub Pages**: GRATIS para siempre
- **Formspree**: GRATIS hasta 50 emails/mes
- **Dominio personalizado**: ~12€/año (opcional)
- **SSL/HTTPS**: GRATIS (incluido en GitHub Pages)

**Total**: 0€/mes (o ~1€/mes si compras dominio)

---

## 📝 Licencia

Código creado para Carlos Manuel Suárez Rivero - CMSR92
© 2025 Todos los derechos reservados

---

**¿Necesitas ayuda?** Revisa la sección de Problemas Comunes arriba o contacta por LinkedIn.

¡Tu portfolio está listo para impresionar! 🚀
