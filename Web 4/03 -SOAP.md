# Descripción

Este reto explotaba una vulnerabilidad en un servicio web que manejaba la comunicación mediante el protocolo **SOAP**, el cual está basado en **XML** [00:00:15]. El analizador XML del servidor estaba mal configurado, permitiendo el procesamiento de **Entidades Externas XML (XXE)**, un fallo que se puede utilizar para acceder a archivos internos del sistema de archivos.

# Solución

El ataque se denominó **Inyección de Entidad Externa XML (XXE)**:

1. **Intercepción:** Se utilizó un _proxy_ interceptor (como Burp Suite) para capturar la solicitud XML enviada por la aplicación al servidor.
2. **Definición de Entidad Externa:** Se modificó la solicitud XML inyectando una declaración de tipo de documento (`<!DOCTYPE ...>`) para definir una nueva entidad, por ejemplo `&xxe;`.
3. **Carga de Archivo Local:** La entidad `&xxe;` fue definida para cargar un recurso del sistema de archivos local utilizando el descriptor `SYSTEM`, apuntando a la ubicación esperada de la _flag_ (e.g., `SYSTEM "file:///flag"`).
4. **Inyección:** Finalmente, se insertó la referencia a la entidad (`&xxe;`) en un campo de datos de la solicitud (e.g., dentro de la etiqueta `<ID>`). Al procesar la solicitud, el analizador XML del servidor leyó el contenido del archivo `/flag` y lo sustituyó por la referencia a la entidad, devolviendo el contenido sensible en la respuesta al atacante.

# Notas adicionales

La vulnerabilidad XXE ocurre cuando el analizador XML del servidor tiene habilitada la función de procesamiento de entidades externas. Es un fallo crítico que puede llevar a la divulgación de archivos locales, ejecución remota de código (RCE) en algunos casos, y ataques _Denegación de Servicio_ (DoS) a través de la "Bomba XML" (Billion Laughs Attack).

# Referencias
- Reto PicoCTF: SOAP
- Vector de Ataque: XML External Entity (XXE)
- Protocolo: SOAP/XML