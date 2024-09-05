# INSTALL-PARTY-IA 🎉

> ⚠️ **Advertencia**:  
> Los usuarios de **Mac** no necesitan instalar WSL, ya que su terminal es de Linux por defecto.

## Instalar WSL en Windows:
1. **PowerShell**:  
    ```wsl --install``` 
   *(El parámetro `-d ubuntu` es opcional, ya que Ubuntu es el sistema predeterminado).*

3. **Documentación**:
   - [Instalación de WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
   - [Configuración del entorno WSL](https://learn.microsoft.com/en-us/windows/wsl/setup/environment)

4. **Comprobar versión de WSL**:  
   Para verificar la versión instalada, ejecuta en la terminal :
   ```wsl -l -v```

### Primer arranque de WSL:
- **Enter UNIX username:** nombre de usuario.
- **Password:** (los caracteres no se muestran en pantalla).

### Si aparece el error:
`Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.`

- Solución: [Habilitar la virtualización en Windows](https://support.microsoft.com/en-us/windows/enable-virtualization-on-windows-11-pcs-c5578302-6e43-4b4b-a449-8ced115f58e1).

### Otros errores:
- **Error 0x8024001e**: Desactiva el antivirus temporalmente.
- **Actualizar kernel**: Ejecuta```wsl --update```para actualizar el kernel de WSL.
- **Error 0x80370114**: No se pudo iniciar la operación porque no se instaló una característica requerida.

### Soluciones posibles:
1. Busca `Hyper-V` y asegúrate de que las siguientes opciones estén habilitadas:
   - Virtual Machine Platform
   - Windows Subsystem for Linux

2. **Activar virtualización en la BIOS**:
   - Para ver cómo activarla, ejecuta: `cmd > msinfo32 > Producto de placa base`.
   - Una vez dentro de la BIOS:
     - **Interfaz moderna**: Ve a Opciones avanzadas > Configuración de la CPU > VT / Tecnología de virtualización / Virtualization Technology / VTX / SVM.
     - **Interfaz clásica**: Ve a Configuración de procesador > Virtualization Technology.
---

## Configuración de GitHub para todos los dispositivos:

### Generar una SSH Key:
- Sigue esta guía para [generar una SSH Key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

### Añadir SSH Key a tu cuenta de GitHub:
- [Instrucciones para añadir SSH Key a tu cuenta de GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).
---

## Instalar Homebrew en Mac:
- [Instalar Homebrew](https://brew.sh/).

---

## Instalar **wget**:
- **En WSL**: Usa `sudo apt install wget` para instalarlo.
- **En Mac**: Ejecuta `brew install wget` si tienes Homebrew instalado.

## Instalar **curl**:
- **En WSL**: Usa `sudo apt install curl` para instalarlo.
- **En Mac**: Ejecuta `brew install curl` con Homebrew.

---

## Visual Studio Code:
- Descarga [VSCode aquí](https://code.visualstudio.com/).

### Reinicia el PC después de instalar VSCode.

### VSCode en Mac:
Si al escribir `code` en la terminal no se abre VSCode:
1. Abre VSCode manualmente.
2. Presiona `shift + command + p`.
3. Escribe `shell` y selecciona la opción "Instalar el comando code en Path".

---


