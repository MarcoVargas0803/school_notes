¿Cuál es el grupo de direcciones privadas disponibles y en cual RFC se especifica?¿Cómo se accede de los dominios privados al público?

## ¿Qué es una IP Privada?

"Una **IP privada** es una dirección reservada para uso exclusivo dentro de redes internas. No es enrutable en Internet, lo que añade una capa natural de aislamiento." (Davantel, Al, 2026).

*La IANA ha reservado tres bloques de direcciones IPv4 para que las compañías las utilicen en sus redes privadas. Estas direcciones aparecen definidas en [RFC 1918, Address Allocation for Private Internets](http://www.ietf.org/rfc/rfc1918.txt?number=1918). Puede utilizar estas **direcciones privadas**, conocidas también como direcciones 1918, para los sistemas de las redes locales de una intranet corporativa. Sin embargo, las direcciones privadas no son válidas en Internet. No las utilice en sistemas que deban comunicarse fuera de la red local.* (Oracle, 2010).

*La tabla siguiente muestra los intervalos de direcciones IPv4 privadas y sus correspondientes máscaras de red.* (Oracle, 2010).

| Intervalo de direcciones IPv4 | Máscara de red | Prefix | Rango |
| ----------------------------- | -------------- | ------ | ----- |
| 10.0.0.0 - 10.255.255.255     | 10.0.0.0       | /8     | A     |
| 172.16.0.0 - 172.31.255.255   | 172.16.0.0     | /12    | B     |
| 192.168.0.0 - 192.168.255.255 | 192.168.0.0    | /16    | C     |
## ¿Qué es NAT?

"**NAT (Network Address Translation)**, introducido en RFC 1631, es el proceso mediante el cual un router o firewall traduce direcciones IP privadas a una IP pública (y viceversa), permitiendo que múltiples dispositivos internos compartan una única dirección pública para comunicarse con Internet." (Davantel, Al, 2026).

### ¿Cómo funciona la NAT (traducción de direcciones de red)?

*La NAT generalmente se implementa en un enrutador, un dispositivo que conecta dos redes. Cuando un dispositivo en la red privada envía datos a un dispositivo en la red pública, el enrutador intercepta los datos y reemplaza la dirección IP de origen con su propia dirección IP pública. Luego, el enrutador envía los datos al dispositivo de destino.* (Fortinet, 2026).

*Cuando el dispositivo de destino devuelve datos al enrutador, el enrutador intercepta estos datos y reemplaza la dirección IP pública con la dirección IP de origen original. Luego, el enrutador envía los datos al dispositivo fuente original. Este proceso es transparente para los dispositivos en ambas redes* (Fortinet,2026).


Referencias: 
Uso de direcciones IPv4 privadas. 2010, Oracle Corporation and/or its affiliates. Sacado de https://docs.oracle.com/cd/E19957-01/820-2981/ewpop/index.html. 

Tutorial: IP Pública, IP Privada, NAT y Acceso Remoto Corporativo. (10/07/2026), Davantel, Al. Sacado de https://www.davantel.com/tutorial-ip-publica-ip-privada-nat-y-acceso-remoto-corporativo.

Definición de traducción de direcciones de red (NAT). (2026) Fortinet, Inc. Sacado de https://www.fortinet.com/lat/resources/cyberglossary/network-address-translation. 





