#  Simulador de Gestión de Procesos (1 CPU, 1 GB RAM)

**Estado:** listo para correr · **Lenguaje:** Python · **Interfaz:** Tkinter · **Gráfica:** Matplotlib  
Este proyecto simula un sistema con **1 CPU** y **1 GB de RAM**, con **cola de espera por memoria**, **liberación automática**, y **gráfica en tiempo real del uso de RAM**.

---

##  Estructura del repositorio
```
.
├─ simumem_gui.py              # Aplicación principal con GUI
├─ README.md                   # Este archivo
└─ docs/
   ├─ INSTALACION.md           # Guía detallada de instalación
   ├─ Manual_Usuario.md        # Cómo usar la app paso a paso
   ├─ Manual_Tecnico.md        # Arquitectura y detalles técnicos
   └─ capturas/                # Evidencias y screenshots para el informe
```



---

## Requisitos
- **Windows 10/11** (recomendado) o Linux/macOS
- **Python 3.10+** (se probó con 3.12)  
- Dependencias:
  - `matplotlib` (única dependencia externa)

---

##  Instalación rápida
En **PowerShell** (Windows):
```powershell
# (Opcional) Permitir scripts en esta sesión
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

# 1) Crear y activar entorno virtual
py -m venv .venv
.\.venv\Scripts\Activate

# 2) Instalar dependencia
py -m pip install --upgrade pip
py -m pip install matplotlib

# 3) Ejecutar
py simumem_gui.py
```

En **Linux/macOS**:
```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install --upgrade pip
python3 -m pip install matplotlib
python3 simumem_gui.py
```

---

##  Uso básico
1. Ejecuta la app y verifica la **memoria** (parte superior).  
2. Crea procesos con **Nombre**, **Memoria (MB)** y **Duración (s)**.  
3. Si no hay RAM disponible, el proceso queda en **Esperando RAM**.  
4. El planificador es **Round‑Robin (quantum = 1 s)** con **1 CPU**.  
5. Al terminar un proceso, la memoria se **libera automáticamente** y se admite lo que esté en espera.  
6. Observa la **gráfica en tiempo real** del uso de RAM en la parte inferior.

> Captura obligatoria: pantalla principal con **procesos en ejecución**, **cola de espera** y **gráfica**.

---


---

##  Solución de problemas
- **No abre la ventana:** verifica versión de Python (`py --version`) y que activaste el entorno.  
- **ImportError: matplotlib:** instala con `py -m pip install matplotlib`.  
- **Permisos en PowerShell:** ejecuta `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` antes de activar `.venv`.

---

