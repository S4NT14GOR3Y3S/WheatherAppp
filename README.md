

# 🌦️ WeatherApp

Aplicación Android desarrollada en Kotlin que permite consultar el clima en tiempo real de diferentes ciudades utilizando una API externa. Implementa arquitectura moderna con **MVVM**, consumo de servicios REST y manejo de datos dinámicos en la interfaz.

---

## 📱 Características

* Consulta del clima actual por ciudad
* Lista de ciudades populares (ej: Bogotá, Medellín, Madrid, etc.)
* Visualización de:

  * Temperatura
  * Descripción del clima
  * Icono representativo
* Interfaz dinámica con actualización en tiempo real
* Manejo de estados (cargando, éxito, error)

---

## 🧱 Arquitectura

El proyecto sigue el patrón **MVVM (Model - View - ViewModel)**:

```
UI (Activity)
   ↓
ViewModel
   ↓
Repository
   ↓
API (Retrofit)
```

### Capas:

* **View (MainActivity)**
  Maneja la interfaz de usuario y observa los datos del ViewModel.

* **ViewModel (WeatherViewModel)**
  Gestiona la lógica de presentación y comunica la UI con el repositorio.

* **Repository (WeatherRepository)**
  Se encarga de obtener los datos desde la API.

* **API (Retrofit)**
  Define y ejecuta las peticiones HTTP.

* **Model**
  Representa la estructura de los datos del clima.

---

## 🛠️ Tecnologías utilizadas

* **Kotlin**
* **Android SDK**
* **Retrofit** – Consumo de APIs REST
* **LiveData / ViewModel** – Manejo de estado
* **Glide** – Carga de imágenes
* **View Binding** – Acceso seguro a vistas

---

## 📂 Estructura del proyecto

```
com.tuapp.wheatherapp
│
├── api/
│   ├── RetrofitClient.kt
│   ├── WeatherApiService.kt
│   └── WeatherResponse.kt
│
├── model/
│   ├── CurrentWeather.kt
│   ├── WeatherData.kt
│   └── weather.kt
│
├── repository/
│   └── WeatherRepository.kt
│
├── viewmodel/
│   └── WeatherViewModel.kt
│
└── MainActivity.kt
```

---

## 🚀 Instalación y ejecución

1. Clona el repositorio:

   ```bash
   git clone https://github.com/tuusuario/weatherapp.git
   ```

2. Abre el proyecto en **Android Studio**

3. Configura tu API Key (si aplica) en:

   * `WeatherApiService.kt` o archivo de configuración

4. Ejecuta la app en un emulador o dispositivo físico

---

## 🌐 API utilizada

La app consume datos desde una API de clima (probablemente OpenWeather o similar).

Ejemplo de endpoint:

```
GET /weather?q={city}&appid={API_KEY}
```

---

## 📌 Mejoras futuras

* Geolocalización automática
* Pronóstico extendido (5 días)
* Modo oscuro 🌙
* Guardado de ciudades favoritas
* Manejo offline

---

## 👨‍💻 Autor

* Santiago Reyes Vanegas


