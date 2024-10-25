# Escuintla (corto)
192.148.15.0/24
- subnetting (preguntar en gpt)
- VLAN
- VTP (del router al sw) 
- RPVST (router y sw)

## Configurar las VLANs en el switch SW5: 

Switch>enable
Switch#configure terminal
Switch(config)#vlan 18
Switch(config-vlan)#name RRHH
Switch(config-vlan)#exit
Switch(config)#vlan 38
Switch(config-vlan)#name Ventas
Switch(config-vlan)#exit

## Asignar interfaces a las VLANs:
Switch(config)#interface fastEthernet 0/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 18
Switch(config-if)#exit
Switch(config)#interface fastEthernet 0/2
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 38
Switch(config-if)#exit



# Quiche (largo)
192.178.15.0/24
- subnetting
- subinterfaces (?) (router)
- - VLAN
- - VTP (de esw a sw)

# Peten (corto)
192.158.15.0/24
- subnetting
- VLAN
- VTP (opcional de esw a sw)

# Izabal (corto)
192.167.15.0/24
- subnetting
- interfaces virtuales (?)
- VTP (de esw a sw)
- RPVST (esw y sw)


## Configurar las VLANs en el switch SW6
'''
Switch>enable
Switch#configure terminal
Switch(config)#vlan 18
Switch(config-vlan)#name RRHH
Switch(config-vlan)#exit
Switch(config)#vlan 38
Switch(config-vlan)#name Ventas
Switch(config-vlan)#exit
Switch(config)#vlan 28
Switch(config-vlan)#name Contabilidad
Switch(config-vlan)#exit
'''

## Asignar interfaces a las VLANs

'''
Switch(config)#interface fastEthernet 0/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 38
Switch(config-if)#exit
Switch(config)#interface fastEthernet 0/2
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 18
Switch(config-if)#exit
'''

