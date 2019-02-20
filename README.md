## of_vscode.sh

Script para generar un proyecto openFrameworks para VSCode con Intellisense habilitado en Linux:
- Debian 9
- openFrameworks 0.10.1 gcc6
- Microsoft Visual Studio Code IDE 1.27.2

Requerimientos adicionales: GNU Global, para generar tags y clang, para analisis estatico en depuracion:
```
    sudo apt-get install global clang
```

# Instalacion:
- Bajar VSCode  [.deb package](https://code.visualstudio.com/docs/?dv=linux64_deb) e instalar
`sudo dpkg -i code_*`.
- Una vez en VSCode: `Ctrl+Shift+X` abre el instaldor de extensiones. Buscar `C/C++ Intellisense` by Microsoft e instalar.

# Preferencias:

Habilitar `Files: Insert Final Newline` (todos los archivos de texto/codigo en linux deben terminar con newline).
Deshabilitar opciones de Telemetry.

Se puede usar VSCode desde CLI con el comando `code`. Para abrir un proyecto de oF hay que abrir el archivo del workspace file, asi:
```console
   code ~/path/to/your/app.code-workspace
```
Para compilar y correr `Ctrl+Shift+B`.

# Instalacion del script of_code.sh:
```console
    git clone https://github.com/npisanti/of_vscode.git
    cd of_vscode
    sudo sh install.sh
```
Si la carpeta para `of_vscode.sh` cambia despues de la instalacion habra que correrla de nuevo.

# Uso:
```console
   of_vscode.sh ~/ruta del proyecto/
```
o
```console
   cd ~/ruta del proyecto/
   of_vscode.sh
```
cualquiera de estas dos opciones generara el workspace de VSCode para ese proyecto.

# Addons
El script intentara agregar automaticamente las rutas en `src` y `libs` de cada addon presente. Si el addon incluye otra ruta tendra que agregarse escribiendo un archivo `.paths` con una lista de las rutas para ese addon especifco en la carpeta `paths`. El archivo `.paths` incluido es un  claro ejemplo.

# Creditos
Proyecto original en ingles [npisanti](https://github.com/npisanti/of_vscode), a su vez inspirado por el ejemplo de  [Roberto Fazio VS Code / oF example](https://github.com/robertofazio/openFrameworks_VisualStudioCode_Example).
