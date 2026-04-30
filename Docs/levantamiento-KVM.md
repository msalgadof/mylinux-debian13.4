# Instalacion de Hipervisor

* **QEMU:** Es el emulador que imita el hardware.

`sudo apt install qemu-system-x86`

* **Libvirt:** Es la API (el traductor).

`sudo apt install libvirt-daemon-system libvirt-clients`

* **Bridge-utils:** Permite crear puentes virtuales para que tus VMs tengan internet o se vean entre ellas en la red.

`sudo apt install bridge-utils`

## Permisos de usuario requeridos

sudo adduser $USER libvirt
sudo adduser $USER kvm

* **La lógica:** Estás agregando tu usuario ($USER) a los "clubes" que tienen permiso para hablar con el hipervisor.

   **Grupo libvirt: Permiso para gestionar máquinas.**

   **Grupo kvm: Permiso para usar la aceleración de hardware (para que la VM no sea lenta).**

## Instalacion de interfaz de control

`sudo apt install virt-manager`

> **NOTA:** Luego de realizado el proceso es importante reiniciar la sesion del usuario (cerrando sesion o reiniciando el equipo).

> **VALIDACION:** `virt-host-validate`

