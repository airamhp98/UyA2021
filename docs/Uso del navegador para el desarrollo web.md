
# Práctica destinada al uso del navegador para el desarrollo web.

## 0. Pasos previos.

Antes de comenzar a realizar la práctica, hemos hecho algunos pasos previos para facilitar el uso de la herramienta de inspección así como su visualización.
Tanto en **Chrome**, como en **Mozilla**, hemos cambiado el theme a Dark puesto que es más cómodo debido a que el fondo de la mayoría de páginas web se encuentra en blanco. Y apretamos el botón que se muestra a continuación para desplegar la pestaña en la parte inferior en lugar de la derecha, lo cual nos hace más cómoda su utilización.
## 1. Peticiones que desencadena la consulta y sus tipos.
Accedemos a la [página web de cita previa del gobierno de canarias](https://www3.gobiernodecanarias.org/citasalud/).
Apretamos la tecla *F12* en ambos navegadores para abrir la opciones de *DevsTool* y poder visualizar las peticiones de la web, y encontramos que  nos pide recargar la página. 
Podemos observar, que a la hora de cargar una página *http* realizamos peticiones **GET*** para conseguir los recursos del sitio(scripts, imagenes, códigos *javascript*, *html*, tablas...).
**GET***: Es decir, que los recursos a los que queremos acceder se encuentran directamente en la URL.
![imagen](https://i.imgur.com/u4mPyTR.png)

## 2. Código de estatus devuelto

* En chrome, encontramos que todas las peticiones nos devuelven el código de estatus **200**, el cual significa OK. 
![status](https://i.imgur.com/htC86JA.png)
* En firefox, también son códigos 200, pero las imagenes nos devuelven el **304**(Not Modified) que es una redirección, esto significa que la imagen estaba guardada en caché porque se ha visitado con anterioridad.

## 3. DNS e IP del servidor

Al buscar la dirección **DNS**, encontramos el Domain: *ww3.gobiernodecanarias.org* 

![DNS](https://i.imgur.com/r12fLdG.png)

El resultado es el mismo en ambos navegadores.
Ahora, buscamos la dirección **IP**, el resultado de la misma es *93.188.136.126:443*
Al igual que con el **DNS**, el resultado es el mismo, y el proceso de búsqueda es el siguiente: 
* En primer lugar, hacemos click en una petición.
* Posteriormente, abrimos la pestaña *cabeceras*
* y dentro de la misma desplegamos el **GET** y encontramos la dirección IP, como se muestra en la siguiente imagen: 
* ![IP](https://i.imgur.com/zNSyKAG.png)

## 4. Cookies

Hemos realizado la búsqueda en ambos navegadores, y encontramos solo una, la cual es: **ASP.NET_SessinId** cuya finalidad es retener la información de la sesión de un usuario.

## 5. Idiomas que aceptan

Los idiomas aceptados son Español(España) e Inglés(US). 
![Idiomas](https://i.imgur.com/4BpeqoJ.png)

## 6. Líneas de código (JavaScript, HTML, CSS)
A continuación mostramos algunos fragmentos:

**JavaScript**:
~~~~
Codigo Java Script: !function(n, t) {
    "object" == typeof module && "object" == typeof module.exports ? module.exports = n.document ? t(n, !0) : function(n) {
        if (!n.document)
            throw new Error("jQuery requires a window with a document");
        return t(n)
    }
    : t(n)
}("undefined" != typeof window ? window : this, function(n, t) {
    function ri(n) {
        var t = n.length
          , r = i.type(n);
        return "function" === r  i.isWindow(n) ? !1 : 1 === n.nodeType && t ? !0 : "array" === r  0 === t || "number" == typeof t && t > 0 && t - 1 in n
    }
~~~~

![js](https://i.imgur.com/SGP2hq6.png)

**CSS**:
~~~~
Codigo CSS: .fa,.fab,.fal,.far,.fas {
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    display: inline-block;
    font-style: normal;
    font-variant: normal;
    text-rendering: auto;
    line-height: 1
}
~~~~

![css](https://i.imgur.com/BM88pDA.png)

**HTML**:
~~~
Html :: <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="">
    <meta name="author" content="">
    <link href="/citasalud/favicon.ico" rel="shortcut icon" type="image/x-icon" />
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">
    <title>Inicio - Cita Salud</title>
    <link href="/citasalud/bundles/cssbootstrap?v=QQg5M9d15mx7qJ7AChDA6KUWTCi4O3zxlFThbYePWYE1" rel="stylesheet"/>

    <link href="/citasalud/bundles/css?v=tSQQeOHJAnpPUiYoz3Lhhm5z0TsKAsgZ_0MeVw_TGsA1" rel="stylesheet"/>

    <script src="/citasalud/bundles/jquery?v=EEZBCVzQe1TpkEUeLfjEm53wpuqSSXGjiXFWAVaewp81"></script>

    <script src="/citasalud/bundles/bootstrap?v=ESck_wvaWCiF5JsitLMh765lhMnw7BVBtZE-YUTa4Ns1"></script>

    <link href="/citasalud/bundles/font-awesome?v=3iEv8vqPidB6TVfgNOGrLoJr-SPH_mV3YwpggEk2_ao1" rel="stylesheet"/>

    <script src="/citasalud/bundles/iniciosesion?v=VlZATGdOzPosJajHFr45yfKEwO26iM5RSxmyJ-naluI1"></script>

~~~~

![html](https://i.imgur.com/Jx8cHlM.png)

## 7. Conclusión
Esta práctica nos ha parecida sencilla pero bastante útil porque con una herramienta simple, sin descargar nada adicional, podemos acceder a bastante información que nos puede resultar útil ya sea para diseñar nuestra propia web u obtener información de la misma. Nos hemos dado cuenta de que para realizar este tipo de consultas, es mejor utilizar el navegador **Mozilla Firefox** antes que **Chrome**, porque a pesar de que aparentemente son iguales, **Firefox** nos da una mayor información y más precisa.
