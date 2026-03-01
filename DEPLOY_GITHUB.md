# DAS1 Bridge Generator - Despliegue con GitHub + Netlify

## 🚀 GUÍA COMPLETA DE DESPLIEGUE

---

## **PASO 1: Subir código a GitHub**

### **1️⃣ Crear nuevo repositorio:**
1. Ve a: https://github.com/new
2. Nombre del repositorio: `das1-bridge-generator`
3. Descripción: "DAS1 Bridge Generator for Amazon"
4. Visibilidad: **Private** (recomendado) o Public
5. **NO marques** "Add a README file"
6. Click **"Create repository"**

### **2️⃣ Subir archivos:**
GitHub te mostrará instrucciones. Sigue la opción:
**"uploading an existing file"**

1. Click en **"uploading an existing file"**
2. Arrastra TODOS los archivos de esta carpeta:
   - `index.html`
   - `netlify.toml`
   - `package.json`
   - `README.md`
   - `.gitignore`
   - **Carpeta completa `netlify/`** (arrastra la carpeta entera)
3. En el campo "Commit changes" escribe: `Initial commit`
4. Click **"Commit changes"**

---

## **PASO 2: Conectar GitHub con Netlify**

### **1️⃣ Ir a Netlify:**
1. Ve a: https://app.netlify.com
2. Click en **"Add new site"** → **"Import an existing project"**

### **2️⃣ Conectar GitHub:**
1. Selecciona **"Deploy with GitHub"**
2. Autoriza Netlify a acceder a tu GitHub (si es la primera vez)
3. Busca y selecciona el repositorio: **`das1-bridge-generator`**

### **3️⃣ Configurar el deploy:**
1. **Build command**: (déjalo vacío)
2. **Publish directory**: `.` (punto)
3. Click **"Deploy site"**

---

## **PASO 3: Configurar API Key**

### **1️⃣ Una vez desplegado:**
1. Ve a **Site settings**
2. **Environment variables**
3. **Add a variable**:
   - Key: `ANTHROPIC_API_KEY`
   - Value: [Tu API key de Anthropic]
4. **Save**

### **2️⃣ Re-desplegar:**
1. Ve a **Deploys**
2. Click **"Trigger deploy"** → **"Deploy site"**

---

## **PASO 4: ¡Listo!**

Tu app estará disponible en: `https://tu-sitio.netlify.app`

---

## **✅ VENTAJAS DE USAR GITHUB:**

- ✅ Las functions se despliegan correctamente siempre
- ✅ Control de versiones (puedes ver todos los cambios)
- ✅ Fácil actualizar el código en el futuro
- ✅ Puedes dar acceso a tus compañeros al código
- ✅ Deploys automáticos cuando haces cambios

---

## **📞 TROUBLESHOOTING:**

**Error: "No functions deployed"**
→ Asegúrate de subir la carpeta `netlify/` completa a GitHub

**Error: "Missing API key"**
→ Verifica que añadiste `ANTHROPIC_API_KEY` en Environment variables

**Error: CORS**
→ El backend ya maneja CORS, debería funcionar automáticamente

---

## **🔄 ACTUALIZAR EL CÓDIGO EN EL FUTURO:**

1. Ve a tu repositorio en GitHub
2. Click en el archivo que quieres editar
3. Click en el lápiz ✏️ (Edit)
4. Haz los cambios
5. Click **"Commit changes"**
6. Netlify re-desplegará automáticamente

---

¡Listo para usar! 🎉
