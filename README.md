# 💳 Alke Wallet

Aplicación de billetera digital para Android, desarrollada en Java con Android Studio. Permite a los usuarios registrarse, iniciar sesión y gestionar transferencias de dinero de forma sencilla e intuitiva.

---

## 📋 Descripción

**Alke Wallet** es una app móvil que simula una billetera digital. El flujo de la aplicación incluye una pantalla de bienvenida (splash screen), registro e inicio de sesión de usuarios, pantalla de inicio con balance, envío y recepción de dinero, historial de transacciones y perfil de usuario.

---

## 🚀 Funcionalidades

- **Splash Screen** — Pantalla de bienvenida con logo que se muestra automáticamente por 3 segundos al iniciar la app.
- **Bienvenida / Selección** — Pantalla para elegir entre crear una cuenta nueva o iniciar sesión.
- **Inicio de sesión** — Formulario con validación de campos (correo y contraseña requeridos).
- **Registro de cuenta** — Formulario con nombre, correo, contraseña y confirmación de contraseña. Valida que los campos estén completos y que las contraseñas coincidan.
- **Pantalla de inicio (Home)** — Muestra el balance total del usuario, botones para enviar y recibir dinero, y acceso al perfil.
- **Enviar dinero** — Pantalla para ingresar el monto y el motivo de la transferencia.
- **Recibir dinero** — Pantalla para gestionar la recepción de fondos.
- **Perfil de usuario** — Vista con información personal, tarjetas, opciones y centro de ayuda.

---

## 🗂️ Estructura del Proyecto

```
AlkeWallet/
├── app/
│   └── src/
│       └── main/
│           ├── java/com/example/alkewallet/
│           │   ├── MainActivity.java        # Splash Screen (punto de entrada)
│           │   ├── MainActivity2.java       # Bienvenida / Selección de acción
│           │   ├── MainActivity3.java       # Inicio de sesión
│           │   ├── MainActivity4.java       # Registro de cuenta nueva
│           │   ├── MainActivity5.java       # Pantalla de inicio (Home)
│           │   ├── MainActivity6.java       # Pantalla adicional (en desarrollo)
│           │   ├── MainActivity7.java       # Recibir dinero
│           │   ├── MainActivity8.java       # Enviar dinero
│           │   └── MainActivity9.java       # Perfil de usuario
│           ├── res/
│           │   ├── layout/                  # Archivos XML de interfaz de usuario
│           │   ├── drawable/                # Imágenes, íconos y fondos
│           │   ├── values/                  # Colores, strings y temas
│           │   └── font/                    # Fuentes personalizadas
│           └── AndroidManifest.xml
├── build.gradle.kts
└── settings.gradle.kts
```

---

## 🔄 Flujo de Navegación

```
MainActivity (Splash)
    └──► MainActivity2 (Bienvenida)
              ├──► MainActivity3 (Login)
              │         └──► MainActivity5 (Home)
              └──► MainActivity4 (Registro)
                        └──► MainActivity5 (Home)
                                  ├──► MainActivity8 (Enviar dinero)
                                  ├──► MainActivity7 (Recibir dinero)
                                  └──► MainActivity9 (Perfil)
```

---

## 🛠️ Tecnologías y Dependencias

| Tecnología / Librería | Versión |
|---|---|
| Android Gradle Plugin | 8.13.2 |
| Java | 11 |
| Min SDK | 26 (Android 8.0) |
| Target SDK | 36 |
| AndroidX AppCompat | 1.7.1 |
| Material Design | 1.13.0 |
| ConstraintLayout | 2.2.1 |
| AndroidX Activity | 1.12.4 |
| JUnit | 4.13.2 |
| Espresso (UI Tests) | 3.7.0 |

---

## ⚙️ Requisitos Previos

- **Android Studio** Hedgehog o superior
- **JDK 11** o superior
- **Android SDK** con API Level 26 como mínimo
- Dispositivo físico o emulador con Android 8.0+

---

## 📦 Instalación y Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/DeniBeatriz/AlkeWallet.git
   ```

2. **Abrir el proyecto en Android Studio:**
   - Ir a `File > Open` y seleccionar la carpeta `AlkeWallet-master`.

3. **Sincronizar dependencias:**
   - Android Studio sincronizará automáticamente las dependencias de Gradle. Si no lo hace, ir a `File > Sync Project with Gradle Files`.

4. **Ejecutar la aplicación:**
   - Seleccionar un dispositivo o emulador en la barra de herramientas.
   - Presionar el botón **Run** (▶️) o usar el atajo `Shift + F10`.

---

## ✅ Validaciones Implementadas

| Pantalla | Validación |
|---|---|
| Inicio de sesión | Campos de correo y contraseña no pueden estar vacíos |
| Registro | Todos los campos son obligatorios |
| Registro | Las contraseñas deben coincidir |
| Recuperar contraseña | Muestra mensaje: funcionalidad no disponible |

---

## 🎨 Recursos de Diseño

- **Paleta de colores:** azul claro (`#84BFEE`), azul oscuro (`#1A87DD`), verde (`#72DB31`), gris (`#D3D3D3`)
- **Fuentes personalizadas:** ABeeZee, Acme, Baloo Bhaijaan, Coming Soon
- **Fondos personalizados** para splash screen, login, registro, home y perfil

---

## 🧪 Pruebas

El proyecto incluye pruebas básicas configuradas:

- `ExampleUnitTest.java` — Prueba unitaria local de ejemplo
- `ExampleInstrumentedTest.java` — Prueba instrumental de ejemplo ejecutada en el dispositivo

Para ejecutar las pruebas:
```bash
./gradlew test           # Pruebas unitarias
./gradlew connectedTest  # Pruebas instrumentales (requiere dispositivo/emulador)
```

---

## 👩‍💻 Autora

**Deni Beatriz**
- GitHub: [@DeniBeatriz](https://github.com/DeniBeatriz)

---

## 📄 Licencia

Este proyecto fue desarrollado con fines educativos.
