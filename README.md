# 📦 Proyecto Frontend - React + Vite

## Arquitectura: MVVM + Redux + Module Pattern + Observer Pattern

---

## 📌 Descripción

Este proyecto corresponde a una aplicación frontend desarrollada con **React + Vite**, cuyo objetivo es implementar una arquitectura moderna basada en patrones de diseño y buenas prácticas de desarrollo.

La aplicación permite gestionar una lista de tareas (crear, listar y eliminar), aplicando separación de responsabilidades y manejo eficiente del estado global.

---

## 🎯 Objetivos del Proyecto

- Aplicar el patrón **MVVM (Model-View-ViewModel)** en React
- Implementar **Redux** como gestor de estado global
- Utilizar el **Observer Pattern** para manejar cambios de estado
- Organizar el código mediante **Module Pattern**
- Separar lógica de negocio, presentación y datos

---

## 🧠 Patrones de Diseño Utilizados

### 🔁 Observer Pattern

Redux implementa este patrón:

- El **store** actúa como sujeto (observable)
- Los componentes React se suscriben a los cambios
- Cuando el estado cambia, la UI se actualiza automáticamente

---

### 🧱 MVVM (Model - View - ViewModel)

| Capa      | Descripción                     |
| --------- | ------------------------------- |
| Model     | Representación de datos         |
| View      | Componentes React (UI)          |
| ViewModel | Hooks personalizados con lógica |

---

### 📦 Module Pattern

Cada funcionalidad se organiza en módulos independientes:

```
modules/
 └── todo/
      ├── model/
      ├── view/
      ├── viewmodel/
      ├── service/
      └── todoSlice.js
```

Esto permite:

- Escalabilidad
- Mantenimiento sencillo
- Bajo acoplamiento

---

## 🏗️ Estructura del Proyecto

```
src/
├── app/
│   └── store.js              # Configuración Redux
│
├── modules/
│   └── todo/
│       ├── model/
│       │   └── Todo.js
│       │
│       ├── view/
│       │   └── TodoView.jsx
│       │
│       ├── viewmodel/
│       │   └── useTodoViewModel.js
│       │
│       ├── service/
│       │   └── todoService.js
│       │
│       └── todoSlice.js      # Redux (estado global)
│
├── App.jsx
└── main.jsx
```

---

## 🔄 Flujo de la Aplicación

```
View (React)
   ↓
ViewModel (Hooks)
   ↓
Redux (Estado Global - Observer)
   ↓
Service (lógica / API)
```

---

## ⚙️ Instalación y ejecución

```bash
npm install
npm run dev
```

---

## 🧪 Funcionalidades

- ✅ Crear tarea
- ✅ Listar tareas
- ✅ Eliminar tarea
- 🔁 Actualización automática de la interfaz

---

## 🧩 Ejemplo de flujo (Agregar tarea)

1. El usuario escribe en el input
2. La vista llama al ViewModel
3. El ViewModel ejecuta `dispatch(addTodo)`
4. Redux actualiza el estado
5. React re-renderiza automáticamente

---

## 🚀 Tecnologías utilizadas

- React
- Vite
- Redux Toolkit
- JavaScript

---

## 📚 Conclusión

Este proyecto demuestra cómo aplicar patrones de diseño en frontend moderno, logrando:

- Código modular
- Separación de responsabilidades
- Alta escalabilidad
- Mantenimiento sencillo

---

## 👨‍🏫 Autor

Eduardo Valenzuela

---
