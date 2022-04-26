# Ex1ComputoDistribuido

## Documentacion del codigo

!/usr/bin/env python3

    Copyright (C) 2022 aaronnicruz@gmail.com

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.


import requests 
#importamos la libreria requests de Python, la que nos ayuda a realizar pediticiones HTTP

img_data = requests.get('https://sdo.gsfc.nasa.gov/assets/img/latest/latest_1024_HMIIC.jpg').content
#con la operacion get obtenemos el contenido de la URL

with open('image_name.jpg', 'wb') as handler:  
    handler.write(img_data)
#abrimos la imagen como handler y de esta manera la podemos leer 
