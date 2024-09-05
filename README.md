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
```
sudo apt update
```
```
sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev git
```
### Python OpenSSL

### Descargar e instalar pyenv:
``` curl https://pyenv.run | bash ```

### Agregar pyenv al archivo de configuración del shell:
```
echo -e '\n# Pyenv configuration' >> ~/.bashrc  
echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/.bashrc  
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc  
echo 'eval "$(pyenv init --path)"' >> ~/.bashrc  
echo 'eval "$(pyenv init -)"' >> ~/.bashrc  
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
```
### Aplicar los cambios al archivo de configuración:
```
source ~/.bashrc
```
### Instalar la última versión de Python disponible:
```
LATEST_PYTHON=$(pyenv install --list | grep -E "^\s*[0-9]+\.[0-9]+\.[0-9]+$" | tail -1 | tr -d '[:space:]')  
pyenv install $LATEST_PYTHON
```
### Establecer la versión global de Python:
```
pyenv global $LATEST_PYTHON
```
### Descargar el script de instalación de Anaconda:
```
curl -O https://repo.anaconda.com/archive/Anaconda3-2024.06-1-Linux-x86_64.sh
```
### Hacer que el script de instalación sea ejecutable:
```
chmod +x Anaconda3-2024.06-1-Linux-x86_64.sh
```
### Ejecutar el script de instalación de Anaconda:
```
./Anaconda3-2024.06-1-Linux-x86_64.sh
```

1. Presiona Enter para revisar el acuerdo de licencia. Luego mantén presionada la tecla Enter para desplazarte.

2. Escribe "yes" para aceptar el acuerdo de licencia.

3. Presiona Enter para aceptar la ubicación de instalación predeterminada.

4. Anaconda recomienda que ingreses "yes" para inicializar Anaconda Distribution ejecutando `conda init`.

5. Cierra y vuelve a abrir tu terminal.

6. Si no aparece el entorno `(base)`, ejecuta:  
`conda config --set auto_activate_base True`.

7. Para finalizar, ejecuta `anaconda-navigator` para comprobar su funcionamiento.

# MYSQL
---
```sudo apt install mysql-server -y```
```mysql -sfu root -proot < "MYSQL_SECURE_INSTALL.sql"```
```systemctl status mysql.service```

Una vez instalado entramos en mysql

```mysql -u root```
Dentremos ejecutamos lo siguiente : 
```use mysql```
```UPDATE user SET plugin='mysql_native_password' WHERE User='root';```
```FLUSH PRIVILEGES;```
