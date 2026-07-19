# Unlocker VoLTE + VoWifi - Android 17 Fix (España)

Este repositorio aloja un fork automatizado orientado a activar las tecnologías VoLTE, VoWiFi y VoNR en dispositivos **Google Pixel dentro de España** bajo las versiones beta de **Android 17**[cite: 1].

Está especialmente diseñado para solucionar los problemas de red en terminales **importados de otras regiones** (como Estados Unidos, Japón o Reino Unido) y es compatible con **todos los operadores españoles** (Pepephone[cite: 1], Movistar, O2, Orange, Vodafone, Digi, Yoigo, etc.).

---

## 📚 Créditos y Reconocimientos

Este parche no sería posible sin el trabajo previo de los desarrolladores de la comunidad:
1. **Código original:** Desarrollado inicialmente por **[vvb2060/carrier-ims-for-pixel](https://github.com/vvb2060/carrier-ims-for-pixel)**.
2. **Compatibilidad con Android 17:** Basado en el parche y código puente del **Pull Request #61** diseñado por **[ryfineZ](https://github.com/ryfineZ)**.

---

## ⚙️ Automatizaciones añadidas de fábrica

El flujo de este repositorio modifica el código fuente antes de compilar para pre-configurar los siguientes parámetros:
* **Fuerza la región de red en España** (`sim_country_iso_override_string = "es"`) para engañar al módem extranjero.
* **Bypassea el servidor de Entitlement** (`carrier_wfc_entitlement_status_required_bool = false`)[cite: 1].
* **Pre-activa los interruptores** de VoLTE y VoWiFi por defecto para evitar configuraciones manuales en los menús internos de la app.

---

## 📥 Descarga e Instalación

1. Dirígete a la sección **Releases** en la barra lateral derecha de este repositorio.
2. Descarga el archivo ejecutable **`app-release.apk`**.
3. Asegúrate de tener **Shizuku** configurado y ejecutándose en tu Pixel.
4. Instala el APK, concédele acceso a Shizuku, abre la app y pulsa el botón principal para registrar la configuración.
5. Activa el **Modo Avión** durante 15 segundos y desactívalo para reiniciar el módem de red.
