para poder usar Arduino con labview temenos tres requisites 

-Arduino ide 1.05 R2 0 Arduino ide 1.06 versiones posteriors 1.08 en Adelante ya no son compatibles con el toolkit LIFA(LabVIEW Interface For Arduino) ya que se dejo de dar soporte temenos una alternativa maker hub como alternativa. y la paqueteria NI VISA este software no tiene limitante este nos permite realizer conexiones entre puertos por ejemplo el gpib en este caso el Puerto serial.

para que funcione lifa_base cualquier version en versions recientes de Arduino es necesario modificar en la pestaña labviewinterface.ino de la siguiente manera

Antes:
// Compute Packet Checksum
unsigned char checksum_Compute(unsigned char command[])
{
  unsigned char checksum;

Despues:
// Compute Packet Checksum
unsigned char checksum_Compute(unsigned char command[])
{
  unsigned char checksum = 0;

Con esto ya Podemos trabajar con cualquier version de lifa Base con cualquier version de Arduino.