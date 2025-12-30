# API Overview Template

## 📋 Meta-información
- **Audiencia objetivo:** Desarrolladores que integrarán con tu API
- **Tiempo de lectura estimado:** 5-7 minutos
- **Última actualización:** Diciembre 2025
- **Nivel técnico:** Intermedio

## 🎯 Objetivo
Esta plantilla te ayuda a crear una documentación completa de overview para tu API REST.

---

## [NOMBRE DE TU API]

### Descripción General
[Describe en 2-3 párrafos qué hace tu API, qué problema resuelve y por qué es útil]

**Ejemplo:**
La API de Pagos XYZ permite a los comercios procesar transacciones de forma segura y eficiente. Con una integración simple, puedes aceptar pagos con tarjeta de crédito, débito y billeteras digitales en minutos.

### Características Principales
- ✅ Procesamiento en tiempo real
- ✅ Soporte para múltiples métodos de pago
- ✅ Webhooks para notificaciones automáticas
- ✅ Dashboard de monitoreo incluido

---

## 🚀 Primeros Pasos

### Base URL
```
https://api.tuempresa.com/v1
```

### Autenticación
Todas las peticiones requieren un API Key en el header:
```bash
curl -H "Authorization: Bearer TU_API_KEY" \
  https://api.tuempresa.com/v1/endpoint
```

**Obtener tu API Key:**
1. Crea una cuenta en [tu-plataforma.com]
2. Ve a Configuración > API Keys
3. Genera una nueva clave

---

## 📚 Recursos Disponibles

| Recurso | Descripción | Endpoint |
|---------|-------------|----------|
| **Users** | Gestión de usuarios | `/users` |
| **Products** | Catálogo de productos | `/products` |
| **Orders** | Procesamiento de órdenes | `/orders` |
| **Payments** | Gestión de pagos | `/payments` |

---

## 💡 Casos de Uso Comunes

### 1. Crear un Nuevo Usuario
Permite registrar nuevos usuarios en tu plataforma.
```bash
curl -X POST https://api.tuempresa.com/v1/users \
  -H "Authorization: Bearer TU_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Juan Pérez",
    "email": "juan@ejemplo.com",
    "role": "customer"
  }'
```

**Respuesta:**
```json
{
  "id": "usr_123456",
  "name": "Juan Pérez",
  "email": "juan@ejemplo.com",
  "created_at": "2025-12-30T10:30:00Z"
}
```

### 2. Procesar un Pago
Crea una transacción de pago.
```bash
curl -X POST https://api.tuempresa.com/v1/payments \
  -H "Authorization: Bearer TU_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "amount": 1500,
    "currency": "ARS",
    "customer_id": "usr_123456",
    "description": "Compra en tienda online"
  }'
```

---

## 📖 Próximos Pasos

1. **Autenticación completa:** Lee la [guía de autenticación](./template-authentication.md)
2. **Referencia de endpoints:** Explora todos los [endpoints disponibles](./template-endpoint-reference.md)
3. **Manejo de errores:** Revisa los [códigos de error](./template-error-codes.md)
4. **Webhooks:** Configura [notificaciones automáticas](./template-webhooks.md)

---

## 📊 Límites y Cuotas

| Plan | Requests/minuto | Requests/día |
|------|-----------------|--------------|
| Free | 60 | 1,000 |
| Basic | 600 | 50,000 |
| Pro | 6,000 | 500,000 |
| Enterprise | Ilimitado | Ilimitado |

---

## 💬 Soporte

- 📧 **Email:** support@tuempresa.com
- 💬 **Chat en vivo:** [Link a tu canal]
- 📚 **Documentación completa:** https://docs.tuempresa.com
- 🐛 **Reportar bugs:** https://github.com/tuempresa/issues

---

## ✅ Checklist de Calidad

Antes de publicar tu documentación de API, verifica:

- [ ] La base URL está correcta y actualizada
- [ ] Los ejemplos de código funcionan
- [ ] Los parámetros obligatorios están marcados claramente
- [ ] Incluye ejemplos de respuestas exitosas y errores
- [ ] Los límites de rate limiting están documentados
- [ ] Información de contacto de soporte está visible
- [ ] La fecha de última actualización está al día

---

*Plantilla creada por [María Nadal](https://github.com/nadalm344) - Technical Writer*
