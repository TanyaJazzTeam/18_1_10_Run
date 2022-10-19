Primer encabezado | Segundo encabezado
--- | ---
Celda de contenido | Celda de contenido
Celda de contenido | Celda de contenido

Primer encabezado | Segundo encabezado
--- | ---
Celda de contenido | Celda de contenido
Celda de contenido | Celda de contenido

![Ciudadela](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Alineado a la izquierda | Centro alineado | Alineado a la derecha
:-- | :-: | --:
columna 3 es | algún texto prolijo | **$1600**
columna 2 es | centrado | $12
rayas de cebra | están limpios | ~~$1~~

Dillinger es un editor HTML5 Markdown habilitado para la nube, listo para dispositivos móviles, con almacenamiento fuera de línea y potenciado por AngularJS.

- Escriba algo de Markdown a la izquierda
- Ver HTML a la derecha
- magia

# verdadero

- Importe un archivo HTML y observe cómo se convierte mágicamente en Markdown
- Arrastra y suelta imágenes (requiere que tu cuenta de Dropbox esté vinculada)

Tú también puedes:

- Importe y guarde archivos desde GitHub, Dropbox, Google Drive y One Drive
- Arrastre y suelte archivos Markdown y HTML en Dillinger
- Exportar documentos como Markdown, HTML y PDF

Markdown es un lenguaje de marcado ligero basado en las convenciones de formato que la gente usa naturalmente en el correo electrónico. Como escribe [John Gruber] en el [sitio de Markdown][df1]

> El objetivo principal del diseño de la sintaxis de formato de Markdown es hacer que sea lo más legible posible. La idea es que un documento con formato de Markdown se pueda publicar tal cual, como texto sin formato, sin que parezca que ha sido marcado con etiquetas o instrucciones de formato.

¡Este texto que ves aquí en *realidad* está escrito en Markdown! Para tener una idea de la sintaxis de Markdown, escriba un texto en la ventana de la izquierda y observe los resultados en la derecha.

### falso

Dillinger utiliza una serie de proyectos de código abierto para funcionar correctamente:

- [AngularJS] - ¡HTML mejorado para aplicaciones web!
- [Ace Editor] - increíble editor de texto basado en la web
- [markdown-it] - Analizador Markdown bien hecho. Rápido y fácil de extender.
- [Twitter Bootstrap]: gran plantilla de interfaz de usuario para aplicaciones web modernas
- [node.js] - E/S con eventos para el backend
- [Express] - framework de aplicación de red rápido node.js [@tjholowaychuk]
- [Gulp] - el sistema de compilación de transmisión
- [Breakdance](https://breakdance.github.io/breakdance/) - Conversor de HTML a Markdown
- [jQuery] - claro

Y, por supuesto, Dillinger en sí es de código abierto con un [repositorio público][eneldo] en GitHub.

### Instalación

![Ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Dillinger requiere [Node.js](https://nodejs.org/) v4+ para ejecutarse.

Instale las dependencias y devDependencies e inicie el servidor.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Para entornos de producción...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Complementos

Dillinger está actualmente ampliado con los siguientes complementos. Las instrucciones sobre cómo usarlos en su propia aplicación están vinculadas a continuación.

Enchufar | LÉAME
--- | ---
buzón | [complementos/dropbox/README.md][PlDb]
GitHub | [complementos/github/README.md][PlGh]
Google Drive | [plugins/googledrive/README.md][PlGd]
OneDrive | [complementos/onedrive/README.md][PlOd]
Medio | [plugins/medium/README.md][PlMe]
Google analitico | [plugins/googleanalytics/README.md][PlGa]

### Desarrollo

## alternativa

Las métricas que componen Core Web Vitals [evolucionarán](#evolving-web-vitals) con el tiempo. El conjunto actual para 2020 se centra en tres aspectos de la experiencia del usuario: *carga* , *interactividad* y *estabilidad visual* , e incluye las siguientes métricas

¿Quieres contribuir? ¡Excelente!

Dillinger usa Gulp + Webpack para un desarrollo rápido. ¡Haga un cambio en su archivo y vea instantáneamente sus actualizaciones!

Abre tu Terminal favorita y ejecuta estos comandos.

Primera pestaña:

```sh
$ node app
```

Segunda pestaña:

```sh
$ gulp watch
```

(opcional) Tercero:

```sh
$ karma test
```

#### Edificio para fuente

Para lanzamiento de producción:

```sh
$ gulp build --prod
```

Generación de archivos zip preconstruidos para su distribución:

```sh
$ gulp build dist --prod
```

### Estibador

Dillinger es muy fácil de instalar e implementar en un contenedor Docker.

De forma predeterminada, Docker expondrá el puerto 8080, así que cámbielo dentro del Dockerfile si es necesario. Cuando esté listo, simplemente use Dockerfile para construir la imagen.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Esto creará la imagen de dillinger y extraerá las dependencias necesarias. Asegúrese de intercambiar `${package.json.version}` con la versión real de Dillinger.

Una vez hecho esto, ejecute la imagen de Docker y asigne el puerto a lo que desee en su host. En este ejemplo, simplemente mapeamos el puerto 8000 del host al puerto 8080 del Docker (o cualquier puerto que esté expuesto en el Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verifique la implementación navegando a la dirección de su servidor en su navegador preferido.

```sh
127.0.0.1:8000
```

#### Kubernetes + Nube de Google

Ver [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Todos
