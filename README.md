# Arquitectura de Software - Actividad # 10 - Práctica .NET: Crear solución multi-proyecto

## 👨‍💻 Información del Estudiante

- **Nombre:** Jesús Omar Uc Domínguez
- **Matrícula:** SW2509031
- **Grupo:** 3B
- **Cuatrimestre:** 3er Cuatrimestre
- **Carrera:** TSU en Desarrollo e Innovación de Software
- **Profesor:** Jorge Javier Pedrozo Romero

---

# 🎮 GameCatalog (Catálogo de Videojuegos - ASP.NET MVC)

Este proyecto es un **catálogo de videojuegos web desarrollado en C# con ASP.NET Core MVC (.NET)**, cuyo propósito principal es aplicar una **arquitectura en capas** y conceptos de desarrollo web como autenticación por sesión, persistencia en JSON y separación de responsabilidades.

El proyecto implementa un CRUD de videojuegos con sistema de usuarios y reseñas, aplicando los principios de organización vistos en clase mediante capas **Domain, Application, Infrastructure y Presentation**.

El objetivo no es solamente que la aplicación funcione, sino entender por qué una arquitectura bien organizada facilita el mantenimiento, escalabilidad y reutilización del código.

---

## 📌 Características

- Catálogo de videojuegos con filtro por género.
- Sistema de registro e inicio de sesión de usuarios.
- Contraseñas hasheadas con SHA256.
- Reseñas con calificación de estrellas (1-5).
- **Restricción:** solo usuarios logueados pueden agregar juegos o reseñas.
- Persistencia de datos en archivos JSON.
- Arquitectura en 4 capas (Domain, Application, Infrastructure, Presentation).
- Tema visual oscuro estilo gaming.

---

## 📸 Capturas de Pantalla

Inicio:
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/cafb246b-6488-4f69-8aad-84899ddab09d" />

Iniciar Sesión:
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/babd1e98-0cd2-49d0-97f9-4cfbf9326079" />

Agregar videojuego:
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/f14c90bd-1fc1-4693-a486-ce0ae8cee7c9" />

Reseñas:
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/eb3a74fc-df33-40c3-8e64-13550a49c7b7" />

Reseñas (sin sesión iniciada):
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/4c07ea9a-f0e4-4d15-9d0b-1e8c9d0c7727" />



---

## 📁 Estructura del proyecto

```
CatalogoApp/
├─ CatalogoApp.Domain/
│  ├─ Models/
│  │  ├─ Item.cs
│  │  ├─ Usuario.cs
│  │  ├─ Resena.cs
│  │  └─ ErrorViewModel.cs
│  └─ Interfaces/
│     └─ IItemRepository.cs
│
├─ CatalogoApp.Application/
│  └─ Services/
│     └─ ItemService.cs
│
├─ CatalogoApp.Infrastructure/
│  └─ Repositories/
│     ├─ JsonItemRepository.cs
│     ├─ JsonUsuarioRepository.cs
│     └─ JsonResenaRepository.cs
│
└─ CatalogoApp.Presentation/
   ├─ Controllers/
   │  ├─ CatalogoController.cs
   │  ├─ UsuarioController.cs
   │  └─ ResenaController.cs
   ├─ Views/
   │  ├─ Catalogo/
   │  │  ├─ Index.cshtml
   │  │  ├─ Detalle.cshtml
   │  │  └─ Agregar.cshtml
   ├─ Usuario/
   │  ├─ Login.cshtml
   │  └─ Registro.cshtml
   ├─ Data/
   │  ├─ items.json
   │  ├─ usuarios.json
   │  └─ resenas.json
   └─ Program.cs
```

---


## 🔐 Restricciones de acceso

| Acción              | Sin sesión | Con sesión |
|---------------------|:----------:|:----------:|
| Ver catálogo        | ✅         | ✅         |
| Ver detalle         | ✅         | ✅         |
| Agregar videojuego  | ❌         | ✅         |
| Escribir reseña     | ❌         | ✅         |

---

## 🛠️ Tecnologías utilizadas

- **C#**
- **.NET 10.0**
- **ASP.NET Core MVC**
- **Razor Views**
- **Bootstrap 5**
- **JSON** como base de datos ligera
- **Arquitectura en Capas**
- **Principios SOLID**

---

## 🤝 Agradecimientos

- **Profesor Jorge Javier Pedrozo Romero** por la estructura del curso y la práctica
- **Tecnológico de Software** por la formación integral

---

## 📧 Contacto

- **Email Institucional:** jesus.uc@tecdesoftware.edu.mx
- **GitHub:** [JesusUc18](https://github.com/JesusUc18)

---

## 📄 Licencia

Este proyecto es parte de las actividades académicas del **Tecnológico de Software** y está bajo la licencia MIT.

---

<div align="center">

**⭐ Si te gustó este proyecto, dale una estrella ⭐**

</div>
