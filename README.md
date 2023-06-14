## CtrlERA

Control ERA: Es un patrón de arquitectura de software para proyectos web (__PHP__), que responde a un modelo de Programación Modular y quizás a un aire de __POA__ ( programación orientada a aspectos ), trabaja con un enrutador (__ctrl.php__) para mantener la interacción en un mismo plano, para facilitar el posicionamiento, peticiones y respuestas del sistema, separando los códigos de acuerdo a su funcionalidad en una carpeta base y en tres ramas principales:


```
CtrlERA/
└── base/
│    ├── E/
│    ├── R/
│    └── A/
│
```

__CtrlERA__ permite una versatilidad a la hora de estructurar el sistema para que la programación sea más cómoda.

## Jerarquia básica
```
CtrlERA/
├── base/
│   ├── E/
│   ├── R/
│   └── A/
├── ctrl.php
└── index.php
```

> #### Idea: CtrlERA no es más que una manera de ordenar tu proyecto web (PHP) en carpetas específicas en una estructura flexible.

#### Logo
![ctrlera](base/E/img/icon/icon.png)

## CTRL

__ctrl.php__: Control hace referencia al archivo que funciona como enrutador de peticiones y respuestas del sistema, mediante el método GET (url), permitiendo la transacción de información sin que el usuario tenga una referencia de la posición lógica de los archivos en ejecución, ctrl.php sólo debe responder a peticiones del mismo sistema.

> #### Idea: ctrl.php no es más que el archivo que ejerce el direccionamiento del sistema.


## E/ (Estructura)
En esta carpeta se almacenará todo lo necesario a nivel visual y comportamiento del lado del cliente (css, js, img, let, maq y otros).

```
├── base/
│   └── E/
│       ├── E/css/ (hojas de estilos) - basica
│       ├── E/img/ (imagenes) - basica
│       ├── E/js/  (javascript) - basica
│       ├── E/let/ (fuentes) - basica
│       ├── E/maq/ (maquetación) - basica
│       ├────────── OPCIONALES
│       ├── E/aud/ (audios) - opcional
│       ├── E/des/ (archivos descargables) - opcional
│       ├── E/doc/ (documentos) - opcional
│       ├── E/med/ (media [CMS]) - opcional
│       ├── E/swf/ (flash) - opcional
│       └── index.php (seguridad) - recomendado
│
```
> #### Idea: E/ no es más que la carpeta donde estarán las tecnologías que interactúan con el lado del cliente (FRONTEND).

## R/ (Respuesta)
En esta carpeta se almacenará los archivos que procesarán las peticiones del cliente, procesos de formularios, se pueden trabajar Modularmente y/o de manera simple:

 ```
├── base/
│   ├── E/
│   └── R/
│       ├── actx/      (actualizar)
│       ├── aggx/      (agregar)
│       ├── brrx/      (borrar)
│       ├── conx/      (consultar)
│       ├─────── Alternativas
│       ├── sistemaxR/    (módulo de sistema X)
│       ├── sistemayR/    (módulo de sistema Y)
│       └── index.php     (seguridad) - recomendado
│
```
Cuando se trabaja modularmente se recomienda que los módulos se trabajen en 2 carpetas de acuerdo a su comportamiento en __CtrlERA (sistemaA/ y sistemaR/)__ que son las donde se alojará lo necesario para que corra el módulo incrustado.


> #### Idea: R/ no es más que la carpeta donde estarán los archivos que procesarán la información del sistema en lado del servidor (BACKEND).

## A/ (Almacén)
Acá están los archivos de preconfiguración que necesite la aplicación (conexiones DB, recursos, funciones y otros ),junto a subcarpetas ([de ser necesario], phpmailer, fpdf, phpqrcode, captcha, phpodt y otros) , un archivo principal (configX.php) que incluye las demás configuraciones que a su vez le da comportamiento a las demás tecnologías:

 ```
├── base/
│   ├── E/
│   ├── R/
│   └── A/
│       ├── sistemaxA/     (módulo de sistema A)
│       ├── sistemayA/     (módulo de sistema B)
│       ├── configX.php    (conf. general)
│       ├── configZ.php    (conf. base de datos)
│       ├── funciones.php  (comportamiento)
│       ├── conectarBd.php (clase PDO)
│       └── index.php      (seguridad) - recomendado
│
```

> #### Idea: A/ no es más que la carpeta donde estarán los archivos de configuración y las tecnologías programables del sistema en lado del servidor (BACKEND).

## 

#### ESTE PATRÓN DE ARQUITECTURA DE SOFTWARE YA HA SIDO PROBADO CON DISTINTAS TECNOLOGÍAS FRONTEND (FRAMEWORK CSS, JS / LIBRERÍAS DE JS ) ALGUNAS DE ELLAS DEBIERON SER  MODIFICADAS A NIVEL DE NÚCLEO ( DEBIDO A SU COMPOSICIÓN PROPIA AL HACER LLAMADO DE OBJETOS) PARA LOGRAR SU ADAPTACIÓN A CTRL ERA.



> #### Cuando vayas a programar no pienses en TODO, piensa en TODOS...
###### -Nerio Villalobos
