# mf-rootconfig

## 📌 Descripción general
`mf-rootconfig` es el microfrontend raíz del sistema. Se encarga de:

- Configuración inicial
- Bootstrap de Single SPA
- Registro de microfrontends
- Definición de rutas base
- Validaciones globales
- Integración con seguridad (tokens, roles, permisos)

## 🚀 Tecnologías
- Vue 3
- Single SPA
- JavaScript
- Module Federation (opcional)

## 🧩 Subcomponentes relacionados
- mf-notifications
- mf-dashboard
- mf-profile
- mf-settings

## 🛠 Flujo de inicialización
1. Carga de configuración
2. Inicialización de router
3. Registro de microfrontends remotos
4. Montaje del shell
5. Renderizado dinámico

## 🔧 Configuración clave
```ts
import { registerApplication, start } from "single-spa";

registerApplication(
  "mf-dashboard",
  () => import("mf-dashboard/App"),
  () => true
);

start();
