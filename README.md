# 🚀 Angular 20 + TailwindCSS 4 + PrimeNG + CSS

Proyecto base configurado con Angular 20, TailwindCSS 4, PrimeNG, y PrimeUI, ideal para construir aplicaciones modernas, escalables y rápidas.

---

## 🧩 Tecnologías y versiones principales

| Herramienta | Versión  |
| :---------- | :------- |
| Node.js     | v22.20.0 |
| Angular CLI | v20.3.6  |
| TailwindCSS | v4.1.14  |
| PrimeNG     | v20.2.0  |
| PrimeUI     | v0.6.1   |
| PrimeIcons  | v7.0.0   |

---

## 📦 Requisitos previos

Verificar instalación de Node.js:

```bash
node --version
```

Si no lo tienes instalado o deseas usar la versión del proyecto (`v22.20.0`):

[🔗 Descargar Node.js](https://nodejs.org/es/download/)

Luego de instalar:

```bash
node --version
```

---

## 🅰️ Crear y configurar un proyecto Angular

1. **Verificar Angular CLI**

   ```bash
   ng version
   ```

2. **(Opcional) Actualizar Angular CLI**

   ```bash
   npm uninstall -g @angular/cli
   npm cache verify
   npm install -g @angular/cli@latest
   ```

3. **Crear un nuevo proyecto**

   ```bash
   ng new angular20-primeng-tailwind4
   ```

   Seleccionar:

   - `Stylesheet format`: `CSS`
   - `SSR/SSG`: `No`
   - `Zoneless`: `(Yes/No según preferencia)`
   - `AI tools`: `None`

4. **Iniciar aplicación**
   ```bash
   ng serve --open
   ```

---

## 🅱️ Instalar y configurar TailwindCSS 4

1. **Instalar dependencias**

   ```bash
   npm install tailwindcss @tailwindcss/postcss postcss --force
   ```

2. **Crear archivo `.postcssrc.json` en la raíz:**

   ```json
   {
     "plugins": {
       "@tailwindcss/postcss": {}
     }
   }
   ```

3. **En `src/styles.css`, importar Tailwind:**

   ```css
   @import 'tailwindcss';
   ```

4. **Borrar el contenido de `app.component.html` y probar:**

   ```html
   <h1 class="text-3xl font-bold underline bg-amber-500">Hola mundo!</h1>
   ```

5. **Extensiones recomendadas**

   - [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
   - [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)

6. **Ejecutar**
   ```bash
   ng serve
   ```

---

## 🅾️ Instalar y configurar PrimeNG

1. **Instalar paquetes**

   ```bash
   npm install primeng @primeuix/themes
   ```

2. **En `app.config.ts`, importar:**

   ```typescript
   import { provideAnimationsAsync } from '@angular/platform-browser/animations/async';
   import { providePrimeNG } from 'primeng/config';
   import Aura from '@primeuix/themes/aura';
   ```

3. **Agregar en `providers`:**
   ```typescript
   provideAnimationsAsync(),
   providePrimeNG({
     theme: {
       preset: Aura,
     },
   }),
   ```

> ⚠️ **Nota:** El aviso “deprecated” en `provideAnimations` es normal. PrimeNG lo usa hasta Angular v23.

4. **En `app.ts` (o el componente donde lo uses), importar el módulo:**

   ```typescript
   import { ButtonModule } from 'primeng/button';
   // ...
   imports: [..., ButtonModule];
   ```

5. **En `app.html`, probar:**
   ```html
   <p-button label="Check" />
   ```

---

## 🆎 Integrar PrimeNG con TailwindCSS (PrimeUI)

1. **Instalar plugin**

   ```bash
   npm i tailwindcss-primeui
   ```

2. **En `src/styles.css`, reemplazar la importación de Tailwind por:**
   ```css
   @import 'tailwindcss-primeui';
   ```

> 💬 **Para TailwindCSS 3:** Este plugin se agrega en `tailwind.config.js`.

---

## ⚙️ Configuración Opcional

### Configuración global de PrimeNG

En `app.config.ts`, puedes agregar opciones de configuración global:

```typescript
options: {
  prefix: 'p',
  darkModeSelector: 'system',
  cssLayer: false
}
```

### Archivo de imports global de PrimeNG

1. **Crear `src/app/prime-imports.ts`** con los módulos de PrimeNG que uses.

2. **En tu `app.ts` (o `app.module.ts`), importar:**

   ```typescript
   import { PrimeImportsModule } from './prime-imports';
   // ...
   imports: [..., PrimeImportsModule];
   ```

3. **(Si usas Charts o Editor):**

   ```bash
   npm install quill chart.js
   ```

4. **Verificar dependencias base:**
   ```bash
   npm install rxjs tslib
   ```

### 🔤 PrimeIcons

Instalar e importar íconos:

```bash
npm install primeicons
```

En `styles.css`:

```css
@import 'primeicons/primeicons.css';
```

Probar en HTML:

```html
<i class="pi pi-spin pi-spinner text-3xl"></i> <i class="pi pi-cog pi-spin text-3xl"></i>
```

---

## 🧱 Recursos adicionales

Componentes gratuitos y compatibles con TailwindCSS 4:

- [🔗 HyperUI](https://www.hyperui.dev)

---

## 🧰 Clonar y ejecutar este proyecto

```bash
git clone https://github.com/08edu02/angular20-tailwind4-primeng.git
cd angular20-primeng-tailwind4
npm install
ng serve --open
```

---

## 💬 Sobre este proyecto

Este proyecto sirve como base de desarrollo para nuevas aplicaciones Angular modernas, integrando lo mejor de:

- ⚡ Angular 20 (zoneless, SSR opcional)
- 🎨 TailwindCSS 4
- 🧱 PrimeNG + PrimeUI + PrimeIcons

Ideal para desarrollos rápidos, prototipos o proyectos de producción.

---

## 🧑‍💻 Autor

**08edu02**

- [📘 YouTube/Tutorial del proyecto](https://youtu.be/TB_MIvRlrEU)
- [🐙 GitHub](https://github.com/08edu02)

---

⭐ Si te fue útil, ¡dale una estrella al repo!

```

```
