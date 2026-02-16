# Trabajo Colaborativo UD4 - Grupo 2

## Descripción

Documento LaTeX sobre diseño de circuitos combinacionales con álgebra de Boole, mapas de Karnaugh y simplificación de funciones lógicas.

## Dependencias

Este documento requiere **XeLaTeX** para compilarse correctamente debido al uso de fuentes del sistema (Verdana).

### macOS

**Opción 1: MacTeX (recomendado)**
```bash
# Instalar con Homebrew
brew install --cask mactex

# O descargar desde: https://tug.org/mactex/
```

**Opción 2: BasicTeX (más ligero)**
```bash
brew install --cask basictex

# Instalar paquetes adicionales necesarios
sudo tlmgr update --self
sudo tlmgr install latexmk collection-fontsrecommended collection-langspanish
```

### Linux (Ubuntu/Debian)

```bash
# Instalación completa
sudo apt update
sudo apt install texlive-full latexmk

# O instalación mínima
sudo apt install texlive-xetex texlive-lang-spanish texlive-fonts-recommended latexmk
```

### Linux (Fedora/RHEL)

```bash
sudo dnf install texlive-scheme-full latexmk

# O instalación mínima
sudo dnf install texlive-xetex texlive-babel-spanish texlive-collection-fontsrecommended latexmk
```

### Linux (Arch)

```bash
sudo pacman -S texlive-most latexmk
```

### Windows

**Opción 1: MiKTeX (recomendado)**
1. Descargar desde: https://miktex.org/download
2. Ejecutar el instalador
3. Durante la instalación, seleccionar "Install missing packages on-the-fly"

**Opción 2: TeX Live**
1. Descargar desde: https://tug.org/texlive/windows.html
2. Ejecutar el instalador
3. Seleccionar instalación completa o añadir los paquetes necesarios

## Compilación

### macOS / Linux

```bash
# Navegar al directorio del proyecto
cd /ruta/al/proyecto/EstudioDeCaso

# Compilar con latexmk (recomendado)
latexmk -xelatex TrabajoColaborativoGrupo2_UD4.tex

# O compilar manualmente (ejecutar dos veces para referencias)
xelatex TrabajoColaborativoGrupo2_UD4.tex
xelatex TrabajoColaborativoGrupo2_UD4.tex
```

### Windows (CMD)

```cmd
REM Navegar al directorio del proyecto
cd C:\ruta\al\proyecto\EstudioDeCaso

REM Compilar con latexmk
latexmk -xelatex TrabajoColaborativoGrupo2_UD4.tex

REM O compilar manualmente
xelatex TrabajoColaborativoGrupo2_UD4.tex
xelatex TrabajoColaborativoGrupo2_UD4.tex
```

### Windows (PowerShell)

```powershell
# Navegar al directorio del proyecto
cd C:\ruta\al\proyecto\EstudioDeCaso

# Compilar con latexmk
latexmk -xelatex TrabajoColaborativoGrupo2_UD4.tex

# O compilar manualmente
xelatex TrabajoColaborativoGrupo2_UD4.tex
xelatex TrabajoColaborativoGrupo2_UD4.tex
```

## Limpiar archivos auxiliares

### macOS / Linux

```bash
latexmk -C
```

### Windows

```cmd
latexmk -C
```

## Estructura del proyecto

```
EstudioDeCaso/
├── TrabajoColaborativoGrupo2_UD4.tex    # Documento principal
├── macros/
│   └── karnaugh.tex                      # Macros para diagramas de Karnaugh
├── imagenes/
│   ├── S1.png                            # Circuito S1
│   ├── S2.png                            # Circuito S2
│   ├── S3.png                            # Circuito S3
│   └── SIM_0.png ... SIM_15.png          # Capturas del simulador
└── README.md                             # Este archivo
```

## Nota sobre fuentes

El documento usa la fuente **Verdana** del sistema. Si la fuente no está disponible:

- **macOS**: Verdana viene preinstalada
- **Windows**: Verdana viene preinstalada
- **Linux**: Instalar las fuentes Microsoft:
  ```bash
  # Ubuntu/Debian
  sudo apt install ttf-mscorefonts-installer
  
  # Fedora
  sudo dnf install curl cabextract xorg-x11-font-utils fontconfig
  sudo rpm -i https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm
  ```

## Solución de problemas

### Error: "Font Verdana not found"

En Linux, instalar las fuentes Microsoft (ver sección anterior) o modificar el preámbulo del documento para usar una fuente alternativa:

```latex
% Cambiar esta línea:
\setmainfont{Verdana}

% Por:
\setmainfont{DejaVu Sans}
```

### Error: "Package not found"

Instalar el paquete faltante con `tlmgr`:

```bash
# macOS/Linux
sudo tlmgr install nombre-del-paquete

# Windows (ejecutar como administrador)
tlmgr install nombre-del-paquete
```

### Error de compilación con caracteres especiales

Asegurarse de que el archivo esté guardado con codificación **UTF-8**.

## Autores

- Manuel del Campo Abril
- Igor Lambarri Ostolaza
- Carlos Rodríguez San Miguel
- Juan Manuel Solsona Sagrado
