# Configuracion parte practica
**Configuramos modo vtp (server/client)**
enable
conf t 
vtp domain G15
vtp password usac
vtp version 2 
vtp mode server

**Creamos VLANs**
vlan 19
name VLAN10
vlan 29
name VLAN20
vlan 39
name VLAN99
vlan 49
name VLAN99
exit

**Configurampos ports**
int f0/1
**Opcional:** switchport trunk encapsulation dot1q
switchport mode trunk
switchport trunk allowed vlan 19,29,39,49,1002-1005

int f0/2
switchport mode access
switchport access vlan 40

**Guardamos**
do wr 
end

**Confirmamos cambios con sh**
do sh vtp status 
do sh run 
do sh vlan