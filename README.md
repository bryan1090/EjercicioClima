# EjercicioClima
Un api de servicios rest que consulta el clima desde un servicio público. Implementa diversos temas del ecosistema spring. 
La aplicación está realizada con spring boot 3.
Para ejecutarla:
- Clonar el repositorio.
- Abrirlo con el ide de preferencia.
- Construir con dependencias (gradle).
- Ejecutar la clase principal WeatherApplication
Los servicios se encuentran protegidos por un tokenización provista por Auth0, por lo tanto para poder acceder a los servicios se hacer lo siguiente:
- Obtener el token con el siguiente servicio:
    curl --location "https://dev-5all2xaynseahlw1.us.auth0.com/oauth/token" --header "content-type: application/json" --header "Cookie: auth0=s%3Av1.gadzZXNzaW9ugqZoYW5kbGXEQPKDiSohFuZAsh9FxwtkEZzXBPrt2Zr3a_1BHlYzZpsebz30z8TTdWDFnFGEbHrT7pyefrjlts-3qmlIkc2yxmmmY29va2llg6dleHBpcmVz1__CEp4AZSXrHa5vcmlnaW5hbE1heEFnZc4PcxQAqHNhbWVTaXRlpG5vbmU.WTNRobxo0Te%2FLkrMkD6KzflNfXTSU8kg7%2F%2B7UL%2BD%2BS4; auth0_compat=s%3Av1.gadzZXNzaW9ugqZoYW5kbGXEQPKDiSohFuZAsh9FxwtkEZzXBPrt2Zr3a_1BHlYzZpsebz30z8TTdWDFnFGEbHrT7pyefrjlts-3qmlIkc2yxmmmY29va2llg6dleHBpcmVz1__CEp4AZSXrHa5vcmlnaW5hbE1heEFnZc4PcxQAqHNhbWVTaXRlpG5vbmU.WTNRobxo0Te%2FLkrMkD6KzflNfXTSU8kg7%2F%2B7UL%2BD%2BS4; did=s%3Av0%3Af8a61300-6570-11ee-ae2c-93c066a0d831.MgokNKngiV1HgDMzWKTU%2F7TaWNADYdof%2FzXf77nqoKA; did_compat=s%3Av0%3Af8a61300-6570-11ee-ae2c-93c066a0d831.MgokNKngiV1HgDMzWKTU%2F7TaWNADYdof%2FzXf77nqoKA" --data "{\"client_id\":\"3FpuERLXhvDOhr2QZeDa3Uzy6hkxqtjx\",\"client_secret\":\"LV3gWonyb3Grtekla7DaEfsumxnvO4lzh5iFIuP48wNS0D2NQlNrZKiZ-mNAPPp_\",\"audience\":\"weather\",\"grant_type\":\"client_credentials\"}"
- Agregar un header de autorización de tipo Bearer con dicho token a cada petición

Incluye:
Junit, mock request, environment, Json, Java post request, H2 DB,  Swagger, Oauth2 Auth0 Client Credentials Flow Machine2Machine, lombok, slf4j, spring security.
