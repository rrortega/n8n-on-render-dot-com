# 🚀 n8n en Render con Docker

Instalación rápida y sencilla de **n8n** en [Render](https://render.com/) usando Docker como blueprint.  
¡Automatiza tus flujos sin complicarte la vida!

---

## 🧰 ¿Qué es esto?

Este repositorio contiene todo lo necesario para desplegar una instancia funcional de [n8n](https://n8n.io/) en Render, utilizando un contenedor Docker.

Ideal si quieres tener tu propio entorno de automatización en la nube con unos pocos clics.

---

## 📦 Instalación

1. Entra a tu [Render Dashboard](https://dashboard.render.com/)
2. Haz clic en **"New Web Service"** y selecciona **"Deploy from a Blueprint"**
3. Usa este repositorio como referencia para el blueprint:  
   `https://github.com/rrortega/n8n-on-render-dot-com`
4. Render instalará automáticamente n8n usando Docker.

---

## 📁 Importante si usas disco persistente

> Si decides montar un disco persistente en Render (recomendado para mantener flujos y credenciales entre reinicios), **debes conservar la ruta de montaje tal como está configurada en este repo**:
```env
/home/node/.n8n
```

⚠️ Cambiar esta ruta puede provocar que n8n no guarde tus datos correctamente.

---

## 🔧 Variables de entorno

El archivo `.env` incluido en este repo contiene ejemplos de variables que puedes agregar manualmente en la sección **Environment Variables** de Render.

Una de las más importantes es:

```env
WEBHOOK_URL=https://tudominio.com/
```

## 🧪 Versión

Este blueprint utiliza:
```env
n8n v1.85.4
```
Puedes actualizar la versión modificando el tag en el Dockerfile.


##  🧠 Recomendaciones
Asegúrate de proteger tu instancia con autenticación (ver la variable N8N_BASIC_AUTH_*)

Considera activar backups si manejas flujos críticos.

Explora la documentación oficial para sacarle todo el jugo a tu instancia.


##  ❤️ Créditos
Hecho con amor por @rrortega
Basado en la magia de la comunidad n8n.

##  🤝 Contribuciones
¡Las contribuciones son bienvenidas! Si deseas agregar soporte para nuevas redes o mejorar la lógica existente, siéntete libre de abrir un issue o enviar un pull request.

##  📝 Licencia
Este proyecto está bajo la licencia MIT.

----
TAMBIÉN PUEDES REGÁLAME UN CAFECITO 👉 [https://ko-fi.com/rrortega](https://ko-fi.com/rrortega)
![RRORTEGA KO-FI.COM](<rrortega-ko-fi.jpg>)