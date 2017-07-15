# IDE4PLC

A libre Programming Software for PLC comply with IEC 61131-3.

![Imagen "IDE4PLCv1-0-5.png" no encontrada](docs/assets/img/IDE4PLCv1-0-4.png "IDE4PLC v1.0.5")

## License

Copyright 2012-2017 Eric Nicolás Pernia.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>.

```
  Para más información acerca de la licencia lea los archivos 
  COPYING.LESSER.txt y COPYING.txt ubicados en el directorio 
  IDE4PLC_LICENSE.
```

## Información del proyecto IDE4PLC

- Sitios web:
    - https://ide4plc.org/
    - http://www.proyecto-ciaa.com.ar/devwiki/doku.php?id=desarrollo:software-plc
- E-mail del proyecto IDE4PLC: ide4plc@gmail.com
- Grupo de desarrollo del Soft-PLC del proyecto CIAA: https://groups.google.com/forum/#!forum/ciaa-software-plc
   
### Acerca del autor
   
- Ing. Eric Nicolás Pernia (ericpernia@gmail.com). Quilmes, Buenos Aires, Argentina.
- Docente-Investigador en la Universidad Nacional de Quilmes (UNQ).
- Responsable de Software-PLC en el Proyecto CIAA.
   
### Colaborador en diseño del software y codificación

- Dr. Lic. Carlos Lombardi.
- Sub-responsable de Software-PLC en el Proyecto CIAA.
   
### Colaboradores en el port del Firmware de IDE4PLC a la EDU-CIAA-NXP

- Mariano Cerdeiro. Responsable de Firmware en el Proyecto CIAA.
- Pablo Ridolfi. Responsable de Hardware en el Proyecto CIAA.
- Juan Cecconi. Sub-responsable de CIAA-IDE.
- Leandro Kollenberger.

### Colaborador en difusión de software y testing

- Gerardo Sager.
- María de los Angeles Gómez López.

### Colaborador en testing de software y documentación

- Marcelo Chichiri.

## Notass de la release actual, 1.0.5

- Fecha de release 15/07/2017.
- Sistemas Operativos compatibles: Windows, GNU/Linux x86 y GNU/Linux x64.
- Soporta de paltaformas: CIAA-NXP y EDU-CIAA-NXP.
- Se agregó detección de tipos de datos e indicación de errores.
- Internacionalización de la GUI, permitiendo cambiar entre Inglés y Español.

Este software se encuentra desarrollo. La presente versión puede 
programar las plataformas CIAA-NXP y EDU-CIAA-NXP en lenguaje 
LADDER DIAGRAM IEC 61131-3. 

El programa generado corre en una única tarea periódica cada 20ms 
llamada MAIN_TASK. Esta tarea dispara una Unidad de Organización de 
programa (POU) del tipo Programa llamada MAIN_PROGRAM.

MAIN_PROGRAM es la única POU que permite modificar el programa, 
contiene declaradas previamente variables de interfaz de Entradas
y Salidas Digitales, y algunas variables internas.

En la CIAA-NXP las Entradas Digitales son I0 a I7 y las Salidas 
Digitales corresponden son de Q0 a Q7. No soporta entradas o 
salidas analógicas.

En la EDU-CIAA-NXP las Entradas Digitales son TEC1 a TEC4 y las
Salidas Digitales corresponden a LEDR, LEDG, LEDB, LED1, LED2 
y LED3. No soporta entradas o salidas analógicas.

### ¿Cómo abrir el IDE4PLC?

Para abrirlo debe ejecutar el entorno Pharo-Smalltak:

- Linux: Abrir una terminal y ejecutar ./ide4plc
- Windows: abrir el ejecutable Pharo.exe
   
### Utilización de IDE4PLC

Abra IDE4PLC, cree un programa en lenguaje LADDER DIAGRAM mediante 
el editor de POUs (que se abre desde el icono correspondiente).

- **Generar código C**: genera el código C en la carpeta:
  IDE4PLC/IDE4PLC_user_projects/plc_application.
- **Build**: Ejecuta el comando "make" que compila el código C.
- **Download**: Ejecuta el comando "make download" que descarga 
  el ejecutable a la flash del microcontrolador.
- **Generar código C, Build y Download**: Ejecuta los 3 pasos 
  anteriores.
- **Clean**: Ejecuta el comando "make clean" que borra los archivos 
  generados por la compilación de C previa. Necesario al cambiar 
  de placa.
