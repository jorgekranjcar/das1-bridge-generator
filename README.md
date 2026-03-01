# DAS1 Bridge Generator - Netlify Deployment

## 📦 CONTENIDO DEL PACKAGE:
- `index.html` - Frontend de la aplicación
- `netlify.toml` - Configuración de Netlify
- `package.json` - Dependencias Node.js
- `netlify/functions/generate-bridge.js` - Backend serverless

## 🚀 PASOS PARA DESPLEGAR:

### 1️⃣ Preparar archivos
- Descarga TODA esta carpeta
- Comprímela en un archivo ZIP

### 2️⃣ Subir a Netlify
1. Ve a: https://app.netlify.com/drop
2. Arrastra el ZIP completo a la zona de drop
3. Espera a que se despliegue

### 3️⃣ Configurar API Key
1. Una vez desplegado, ve al dashboard de tu sitio en Netlify
2. Ve a: **Site settings** → **Environment variables**
3. Añade una nueva variable:
   - **Key**: `ANTHROPIC_API_KEY`
   - **Value**: Tu API key de Anthropic (desde console.anthropic.com/settings/keys)
4. Guarda los cambios
5. Ve a **Deploys** → Click en **Trigger deploy** → **Deploy site**

### 4️⃣ ¡Listo!
Tu app estará disponible en: `https://tu-sitio.netlify.app`

## 🔑 OBTENER API KEY DE ANTHROPIC:

1. Ve a: https://console.anthropic.com/settings/keys
2. Crea una nueva API key
3. Cópiala (solo se muestra una vez)
4. Úsala en el paso 3️⃣ arriba

## 💰 COSTOS:

- **Netlify**: GRATIS (100GB bandwidth/mes)
- **Anthropic API**: Pay-as-you-go (muy barato para uso interno)
  - Claude Sonnet 4: ~$3 por millón de tokens input
  - Un bridge típico usa ~2000 tokens = $0.006 por bridge

## 🔒 SEGURIDAD:

- La API key está en variables de entorno (seguro)
- Solo tu dominio de Netlify puede usar el backend
- No se expone la API key al cliente

## ⚙️ TROUBLESHOOTING:

**Error: "Missing API key"**
→ Revisa que configuraste ANTHROPIC_API_KEY en Environment variables

**Error: "Function not found"**
→ Asegúrate de subir TODO el ZIP, incluyendo la carpeta netlify/

**Error: CORS**
→ El backend ya maneja CORS, debería funcionar automáticamente

## 📞 SOPORTE:

Si tienes problemas, revisa:
1. Que la API key esté configurada correctamente
2. Que hayas desplegado después de añadir la API key
3. Los logs en Netlify: Functions → Ver logs de generate-bridge

---

¡Listo para usar! 🎉
