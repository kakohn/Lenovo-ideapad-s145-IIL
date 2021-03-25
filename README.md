# Lenovo-Ideapad-s145-14IIL 
![Captura_21_01_11_13-03](https://user-images.githubusercontent.com/65475712/104226602-b43aea00-540d-11eb-9a61-29e191b2e068.png)

## WIFI ✔

### Chip WIFI Realtek rama "rtw88", rtw_8723de(rtl8723de), rtw_8822be(rtl8822be), rtw_8822ce(rtl8822ce).
_Paquetería necesaria para compilar los módulos al kernel._

#### _Debian/Ubuntu_

    # apt update && sudo apt upgrade
    # apt install make git gcc build-essential linux-headers-$(uname -r)

#### _Void Linux_

    # xbps-install -Su
    # xbps-install -S make git gcc base-devel linux-headers-$(uname -r)

#### _Arch Linux_

    # pacman -Suy
    # pacman -S make git gcc base-devel linux-headers-$(uname -r)

#### _Solus Linux_

    # eopkg update
    # eopkg install -c system.devel
    # eopkg install make git gcc linux-headers-$(uname -r)

#### _Clonar módulo rtw_8822ce rtw_8723de rtw_8822be_ 🔧

    $ git clone https://github.com/lwfinger/rtw88.git
    $ cd rtw88
    $ make 
    # make install
    # modprobe <dev_name>
    <dev_name> = rtw_8723de 
                 rtw_8822be 
                 rtw_8822ce 

#### _Si el kernel cambiase, compilar de nuevo_

    $ cd rtw88
    $ sudo make install
    $ sudo modprobe <dev_name>
    <dev_name> = rtw_8723de 
                 rtw_8822be 
                 rtw_8822ce 
             
## Touchpad ✔
### Elantech Touchpad

Agregar una linea a GRUB en el archivo configuración *"/etc/default/grub"*

    # nano /etc/default/grub

_Agregar una nueva linea a GRUB_

![Captura_21_01_11_13-02](https://user-images.githubusercontent.com/65475712/104226553-9bcacf80-540d-11eb-9c15-da35329b3ea5.png)


    GRUB_CMDLINE_LINUX_DEFAULT="... i8042.nonpnp=1 pci=nocrs ..."

_Guardar_ ```ctrl+o``` _y salir_ ```ctrl+x```

#### _Debian/Ubuntu/Void Linux_

    # update-grub
    # reboot

#### _Arch/openSUSE_

    # grub2-mkconfig -o /boot/grub2/grub.cfg
    # reboot

## Compilar Kernel ✔

### _Paquetes necesarios_

#### _Debian/ubuntu_

    # apt install build-essential libssl-dev libncurses5-dev gcc bc bison flex libelf-dev

#### [_Código fuente Kernel linux_](https://www.kernel.org/)

    $ mkdir linux
    $ cd linux
    $ mv ~/Descargas/linux-*.tar.xz ~/linux
    $ mkdir linux_kernel
    $ tar xvf linux-* -C linux_kernel/ --strip-components=1
    $ cd linux_kernel/
    $ make localmodconfig               || localmodconfig = [Coge solamente el hardware conectado]
    $ make deb-pkg

## [Personalización LXDE ✔](https://youtu.be/pzQiQrm0Ei4)
![2020-07-06-124157_1366x768_scrot](https://user-images.githubusercontent.com/65475712/86627824-22e24b00-bf86-11ea-9325-eeca4c793d1f.png)

<br>

## [Personalización Budgie ✔](https://youtu.be/jX36ehyIXgQ)
![Captura de pantalla de 2020-07-30 12-05-22](https://user-images.githubusercontent.com/65475712/89587992-f9744380-d7ff-11ea-838d-96d7102e5f3d.png)

<br>

## ¡Espero haberte ayudado!
### Grupos de Telegram

#### Windows/GNU/Linux/BSD ✔

[Karla's Project](https://t.me/KarlasProject)

#### Software libre y/o Opensource ✔

[DriveMeca](https://t.me/drivemeca_opensource)

#### Canal de música Lo-Fi Hip Hop ✔

[low fidelity _-](https://t.me/lowfidelitycc)
