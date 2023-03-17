# Filius-Router

## DHCP Server

Il server DHCP è un dispositivo configurato appositamente nella rete per distribuire indirizzi IP e molte altre informazioni in modo automatico.

Queste informazioni vengono distribuite a tutti i dispositivi che si connettono alla rete per la prima volta.

Oltre a garantire che ogni indirizzo IP assegnato sia univoco in tutta la LAN, fornisce anche informazioni come il **default gateway**, il **server DNS**, la **subnet mask** etc.

## Problemi Vari

Come prima cosa il laptop della rete **192.168.1.0/24** non ha attivato la DHCP configuration, perciò il DHCP server non gli distribuiva né un indirizzo IP valido, né il default gateway con cui potersi interfacciare con l’altra sottorete.

Nella rete **192.168.0.0/24** invece il DHCP server non aveva configurato il default gateway, rendendolo anche in questo caso inabile a trasmettere questa informazione al laptop.

## Protocollo del Ping

Il comando ping sfrutta il protocollo **ICMP** (Internet Control Message Protocol).

Questo comando viene sfruttato per testare la comunicazione tra dispositivi della stessa sottorete o di reti esterne.  
Per far ciò viene inviato un messaggio ICMP di “**echo request**” all'indirizzo IP di destinazione.

Se il dispositivo di destinazione è raggiungibile e in grado di rispondere, invierà un messaggio ICMP di "**echo reply**" che conterrà l’esito della comunicazione.
