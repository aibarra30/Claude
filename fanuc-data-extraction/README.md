# Sistema de Extracción de Datos — Robot FANUC M-16iB/20

Sistema de extracción de registros de robot FANUC M-16iB/20 para número de parte, cordones de soldadura y parámetros.

## Detalles del robot
- Robot: FANUC M-16iB/20 (ArcTool M-16iB/20, Servo Code V17.00S)
- Controlador con conectividad TCP/IP configurada
- Protocolos disponibles: TCP/IP, TELNET, PPP, PING, FTP
- Red: Subnet 255.255.255.0, Board address 00:E0:E4:01:AA:86
- Estado observado: SRWD-199 Control Stop, MAIN_CAT LINE 0, AUTO ABORTED mode

## Datos requeridos
- Número de parte
- Cantidad de cordones
- Parámetros de soldadura

## Implementación
- 2 scripts Python: captura automática vía FOCAS + captura manual
- Exportación a Excel con formato profesional (colores, bordes, estadísticas)
- Archivo de ejemplo generado: `registros_soldadura.xlsx` (15 ciclos de prueba)

## Stack técnico
- Python
- FOCAS (librería de comunicación FANUC)
- openpyxl / similar para exportación a Excel
