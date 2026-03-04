# 📧 Sistema de Correos Masivos PRO v0.0.2

Sistema avanzado de envío de correos masivos con HTML responsivo, tracking de aperturas y métricas detalladas. Desarrollado por **Isaac Esteban Haro Torres**.

---

## 📝 Descripción

Versión profesional del sistema de correo masivo con capacidades avanzadas de personalización, seguimiento y análisis de campañas.

### ¿Qué hace este proyecto?

- **HTML responsivo**: Emails que se adaptan a cualquier dispositivo
- **Tracking de aperturas**: pixel.gif invisible para medir aperturas
- **Métricas detalladas**: Reportes de éxito, bounces, aperturas
- **Plantillas profesionales**: Diseños modernos y personalizables
- **Gestión de bounces**: Manejo automático de emails fallidos

---

## ✨ Características Principales

| Característica | Descripción |
|----------------|-------------|
| 📱 **HTML Responsivo** | Compatible con móvil, tablet y desktop |
| 📊 **Analytics integrado** | Métricas de envío, aperturas, clicks |
| 🔔 **Notificaciones** | Alertas de email enviado/fallido |
| 📈 **Gráficos de rendimiento** | Visualización de KPIs de campaña |
| 🏷️ **Etiquetas y categorías** | Organiza tus campañas |
| 🔄 **Reintentos automáticos** | Reintenta emails fallidos |

---

## 🛠️ Stack Tecnológico

- **Lenguaje**: Python 3.10+
- **Email**: smtplib, email (stdlib)
- **Templates**: Jinja2
- **Datos**: Pandas, NumPy
- **Visualización**: Matplotlib, Seaborn
- **Tracking**: Base de datos SQLite

---

## 🚀 Instalación y Uso

### Instalación

```bash
pip install pandas jinja2 matplotlib seaborn sqlalchemy
```

### Configuración avanzada

```python
from correopron import CampanaCorreo

campana = CampanaCorreo(
    smtp_config={
        'servidor': 'smtp.gmail.com',
        'puerto': 587,
        'usuario': 'tu@email.com',
        'password': 'app_password'
    },
    tracked=True,  # Habilitar tracking
    retry_on_fail=True
)

# Crear campaña
campana.crear(
    nombre="Campaña Enero 2026",
    asunto="¡Descubre nuestras nuevas ofertas!",
    plantilla="promocion_responsive.html",
    contactos="leads.csv"
)

# Ejecutar y obtener métricas
resultados = campana.ejecutar()
campana.generar_reporte()
```

### Plantilla HTML con Tracking

```html
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .btn { background: #2563eb; color: white; padding: 12px 24px; }
        @media (max-width: 600px) { .container { width: 100% !important; } }
    </style>
</head>
<body>
    <div class="container">
        <img src="https://tudominio.com/track/open/{{contacto_id}}" hidden>
        <h1>¡Hola {{nombre}}!</h1>
        <p>Gracias por tu interés en {{empresa}}...</p>
        <a href="{{link Tracking}}" class="btn">Ver más</a>
    </div>
</body>
</html>
```

---

## 📊 Métricas Generadas

- **Tasa de entrega**: Emails exitosos / Total enviados
- **Tasa de apertura**: Emails abiertos / Entregados
- **Tasa de click**: Clicks / Emails abiertos
- **Tasa de bounce**: Fallidos / Total
- **Hora pico de apertura**: Distribución horaria

---

## 📁 Estructura del Proyecto

```
Correos_Masivos_v0.0.2/
├── correos_masivos_colegios_v0_0_2.ipynb
├── config.py
├── plantillas/
│   ├── promocion_responsive.html
│   ├── newsletter.html
│   └── notificacion.html
├── tracker/                     # Sistema de tracking
│   └── app.py
├── database.db                 # SQLite con métricas
└── README.md
```

---

## 💡 Casos de Uso

1. **Marketing automation**: Secuencias de email complejas
2. **CRM integration**: Sincronización con CRM
3. **Newsletters**: Publicaciones periódicas a suscriptores
4. **Drip campaigns**: Emails basados en comportamiento

---

## 🎨 Plantillas Incluidas

| Plantilla | Uso |
|-----------|-----|
| `promocion_responsive.html` | Ofertas y promociones |
| `newsletter.html` | Boletines informativos |
| `notificacion.html` | Alertas del sistema |
| `bienvenida.html` | Onboarding de usuarios |

---

## 📈 Ejemplo de Reporte

```
╔══════════════════════════════════════╗
║     REPORTE DE CAMPAÑA              ║
╠══════════════════════════════════════╣
║  Enviados:      1,000               ║
║  Entregados:      985              ║
║  Abiertos:        450 (45.7%)      ║
║  Clicks:          120 (26.7%)      ║
║  Bounces:           15 (1.5%)      ║
╚══════════════════════════════════════╝
```

---

## 🤝 Contribuciones

¿Mejoraste el sistema de tracking? ¿Agregaste nuevos reportes?
¡Abre un Pull Request!

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.
