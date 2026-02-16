# bspwmctl

[![Version](https://img.shields.io/badge/version-v0.1.0-blue.svg)](https://github.com/bspwmctl/bspwmctl)
[![Status](https://img.shields.io/badge/status-Pre--Alpha-red.svg)]()
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

**bspwmctl** es un instalador y gestor automatizado diseñado para desplegar un entorno de escritorio bspwm totalmente configurado sin complicaciones manuales.

!> **ADVERTENCIA: SOFTWARE PRE-ALPHA**<br>
Esta versión (v0.1.0) es un lanzamiento **Pre-Alpha**. Está destinado para propósitos de prueba en instalaciones limpias.<br>

---


## 🧩 ¿Qué es bspwm?

Para aquellos nuevos en el ecosistema, **bspwm** (Gestor de Ventanas de Partición Binaria del Espacio) es un gestor de ventanas tipo mosaico (*tiling*) para X11.

A diferencia de los entornos de escritorio tradicionales (como GNOME o KDE), bspwm:
* **Organiza las ventanas automáticamente:** En lugar de superponer ventanas, divide la pantalla para que puedas ver todo a la vez.
* **Es extremadamente ligero:** Usa recursos mínimos de RAM y CPU.
* **Está controlado por scripts:** Su configuración se maneja mediante un simple script de shell, haciéndolo increíblemente modificable y flexible.

**bspwmctl** cierra la brecha entre una instalación limpia de Linux y un entorno bspwm hermoso y completamente funcional.


## ✨ Características (v0.1.0)

- 🐧 **Soporte multi-distribución**: Probando actualmente en Debian, Arch y Fedora.
- 📦 **Instalación inteligente**: Detecta tu gestor de paquetes e instala las dependencias automáticamente.
- 🎨 **Inyección de Dotfiles**: Despliega configuraciones preestablecidas para:
  - `bspwm` (Gestor de ventanas)
  - `sxhkd` (Atajos de teclado)
  - `polybar` (Barra de estado)
  - `picom` (Compositor/Transparencia)
  - `kitty` (Emulador de terminal)
- 🚀 **Basado en CLI**: Interfaz de línea de comandos simple (futuras versiones incluirán un binario compilado).


## 🚀 Inicio Rápido

Recuerda: **No uses sudo**.

```bash
# 1. Clonar el repositorio
git clone [https://github.com/bspwmctl/bspwmctl.git](https://github.com/bspwmctl/bspwmctl.git)
cd bspwmctl

# 2. Hacer ejecutable el script
chmod +x bspwmctl

# 3. Instalar (Modo por defecto / Mínimo)
./bspwmctl install

# Opción: Instalar con paquetes estándar
./bspwmctl install --standard
```


## Siguientes Pasos

- 📖 [Guía de Instalación](installation/) - Instrucciones de instalación detalladas
- 🎯 [Guía de Uso](usage/) - Aprende cómo usar bspwmctl
- 🤝 [Contribuir](contributing/) - Ayuda a mejorar bspwmctl


## 🤝 Contribuir

¿Encontraste un error? ¿Quieres añadir soporte para tu distro?
Revisa la [Guía de Contribución](contributing/README.md) o abre un [Issue](https://github.com/bspwmctl/bspwmctl/issues).


## 📄 License

bspwmctl se publica bajo la [Licencia MIT](https://github.com/bspwmctl/bspwmctl/blob/main/LICENSE).
