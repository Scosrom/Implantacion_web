Configuración de Apache para Redirect:
Notas del Vídeo:
Uso de Redirect en Apache:

El comando Redirect en Apache utiliza la siguiente sintaxis: Redirect url_origen url_destino. Ejemplo:

apache
Copy code
Redirect /buscador http://www.google.es
Aunque Redirect puede tener efectos similares a Alias, la diferencia radica en que se fuerza al navegador a realizar una nueva petición a la URL de destino. Además, al usar Redirect, se cambia la barra de direcciones del navegador.

Ejercicios:
Configuración con Alias:

Abre el archivo de configuración de Apache:

bash
Copy code
sudo nano /etc/apache2/sites-available/000-default.conf
Añade la siguiente línea para configurar Alias:

apache
Copy code
Alias /mas_info /www/sitio1/mas_informacion
Guarda y cierra el archivo.

Reinicia Apache para aplicar los cambios:

bash
Copy code
sudo service apache2 restart
Configuración con Redirect:

Añade la siguiente línea para configurar Redirect:

apache
Copy code
Redirect /mas_info http://www.sitio1.com/mas_informacion
Guarda y cierra el archivo.

Reinicia Apache para aplicar los cambios:

bash
Copy code
sudo service apache2 restart
Prueba de Diferencia entre Alias y Redirect:

Abre tu navegador y accede a http://tu-sitio.com/mas_info. Observa el comportamiento de la barra de direcciones y cómo se muestra la página.

Luego, modifica la configuración para utilizar Redirect en lugar de Alias. Reinicia Apache y prueba nuevamente.

Observa las diferencias en el comportamiento entre Alias y Redirect.