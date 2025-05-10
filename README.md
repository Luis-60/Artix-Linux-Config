# Artix-Linux-Config
Documentação de Configuração do Artix Linux

## Instalação do Docker

```
  sudo pacman -S docker-openrc \
  sudo rc-update add docker default \
  sudo rc-service docker start \
  docker run hello-world \
  sudo usermod -aG docker $USER
  ```
