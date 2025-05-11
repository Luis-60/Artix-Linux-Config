# Artix-Linux-Config
Documentação de Configuração do Artix Linux


## Especificações do Sistema 

```
OS: Artix Linux x86_64
                'ooxoo'                    Host: 81FD (Lenovo ideapad 330-15IKB)
               'ooxxxoo'                   Kernel: Linux 6.14.5-artix1-1
              'oookkxxoo'                  Uptime: 2 hours, 44 mins
             'oiioxkkxxoo'                 Packages: 833 (pacman)
            ':;:iiiioxxxoo'                Shell: bash 5.2.37
               `'.;::ioxxoo'               Display (AUO71EC): 1366x768 @ 60 Hz "
          '-.      `':;jiooo'              DE: Xfce4 4.20
         'oooio-..     `'i:io'             WM: Xfwm4 (X11)
        'ooooxxxxoio:,.   `'-;'            WM Theme: Default
       'ooooxxxxxkkxoooIi:-.  `'           Theme: Adwaita-dark [GTK2/3/4]
      'ooooxxxxxkkkkxoiiiiiji'             Icons: matefaenzadark [GTK2/3/4]
     'ooooxxxxxkxxoiiii:'`     .i'         Font: Roboto (11pt) [GTK2/3/4]
    'ooooxxxxxoi:::'`       .;ioxo'        Cursor: Premium
   'ooooxooi::'`         .:iiixkxxo'       Terminal: xfce4-terminal 1.1.5
  'ooooi:'`                `'';ioxxo'      Terminal Font: Roboto Mono (11pt)
 'i:'`                          '':io'     CPU: Intel(R) Core(TM) i3-6006U (4) z
'`                                   `'    GPU: Intel HD Graphics 520 @ 0.90 GH]
                                           Memory: 2.23 GiB / 7.66 GiB (29%)
                                           Swap: 0 B / 8.80 GiB (0%)
                                           Disk (/): 11.28 GiB / 210.05 GiB (5%4
                                           Local IP (wlan0): 192.168.0.8/24
                                           Battery (L16M2PB1): 100% [AC Connect]
                                           Locale: pt_BR.UTF-8
```
## Instalação do Docker

```
  sudo pacman -S docker-openrc \
  sudo pacman -S docker-compose \
  sudo rc-update add docker default \
  sudo rc-service docker start \
  docker run hello-world \
  sudo usermod -aG docker $USER
  ```

## Troubleshooting 

*makepkg -si: ==> ERROR: cannot find fakeroot binary*

*Explicação:* Não há bibliotecas para compilar pacotes

*Solução:*
```
   sudo pacman -S base-devel
   ```
