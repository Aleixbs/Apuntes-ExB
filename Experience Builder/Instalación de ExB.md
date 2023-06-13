LINKS DE INFO 

Video de info sobre uso e instalación de ExB  (interno caduca en julio)
https://esriespana923-my.sharepoint.com/personal/carlos_herrera_esri_es/_layouts/15/stream.aspx?id=%2Fpersonal%2Fcarlos%5Fherrera%5Fesri%5Fes%2FDocuments%2FGrabaciones%2FWebinar%20Experience%20Builder%20for%20ArcGIS%20%2D%20Developer%20Edition%2D20230518%5F160302%2DGrabaci%C3%B3n%20de%20la%20reuni%C3%B3n%2Emp4&ga=1

Videos de info sobre instalación (externo)
https://www.youtube.com/watch?v=BcJxNaKuTxg (Instalación de ExB developer)

Videos de info sobre implementación widgets (externo)
https://www.youtube.com/watch?v=qSRovErKutw (widgets en ExB developer)


##### Instalación de Node.js

Antes de instalar ExB necesitamos levantar node

LTS 18.x o superior 

#### Instalación de ExB

Una vez tenemos node.js se ejecuta la instalación dentro del cmd usando node

Client

```
C:\Users\aleix.batlle>node -v
v18.16.0

C:\Users\aleix.batlle>cd ..

C:\Users>cd ..

C:\>cd ArcGISExperienceBuilder

C:\ArcGISExperienceBuilder>cd client

C:\ArcGISExperienceBuilder\client>npm install
```

Server

```
C:\ArcGISExperienceBuilder\client>cd ..

C:\ArcGISExperienceBuilder>cd server

C:\ArcGISExperienceBuilder\server>npm install
```

Comprobar que las instalación ha sido satisfactoria

```
C:\ArcGISExperienceBuilder\server>npm start
```


Consola de comandos completa

```
Microsoft Windows [Versión 10.0.19045.2965]
(c) Microsoft Corporation. Todos los derechos reservados.

C:\Users\aleix.batlle>node -v
v18.16.0

C:\Users\aleix.batlle>cd ..

C:\Users>cd ..

C:\>cd ArcGISExperienceBuilder

C:\ArcGISExperienceBuilder>cd client

C:\ArcGISExperienceBuilder\client>npm install

> exb-client@1.11.0 postinstall
> npm run lerna-bootstrap


> exb-client@1.11.0 lerna-bootstrap
> lerna bootstrap

lerna notice cli v6.1.0
lerna info Bootstrapping 0 package
lerna info Symlinking packages and binaries
lerna success Bootstrapped 0 package

added 2660 packages, and audited 2661 packages in 2m

218 packages are looking for funding
  run `npm fund` for details

11 vulnerabilities (1 moderate, 10 high)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
npm notice
npm notice New minor version of npm available! 9.5.1 -> 9.6.7
npm notice Changelog: https://github.com/npm/cli/releases/tag/v9.6.7
npm notice Run npm install -g npm@9.6.7 to update!
npm notice

C:\ArcGISExperienceBuilder\client>cd ..

C:\ArcGISExperienceBuilder>cd server

C:\ArcGISExperienceBuilder\server>npm install
npm WARN deprecated @types/bson@4.2.0: This is a stub types definition. bson provides its own type definitions, so you do not need this installed.
npm WARN deprecated multer@1.4.4: Multer 1.x is affected by CVE-2022-24434. This is fixed in v1.4.4-lts.1 which drops support for versions of Node.js before 6. Please upgrade to at least Node.js 6 and version 1.4.4-lts.1 of Multer. If you need support for older versions of Node.js, we are open to accepting patches that would fix the CVE on the main 1.x release line, whilst maintaining compatibility with Node.js 0.10.

added 731 packages, and audited 732 packages in 40s

81 packages are looking for funding
  run `npm fund` for details

5 high severity vulnerabilities

To address issues that do not require attention, run:
  npm audit fix

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.

C:\ArcGISExperienceBuilder\server>npm start

> exb-server@0.1.0 start
> cross-env NODE_ENV=production node src/server

Apps folder: C:\ArcGISExperienceBuilder\server\public\apps
Http server running on port 3000
Https server running on port 3001

```


### Comprobamos que la instalación funciona

Entramos al puerto en el cuál está ejecutándose

https://localhost:3001/page/set-portalurl

Hacemos el setup del Experience Builder Developer dentro del ordenador. 

Tenempos que registrar la url del portal y el id de cliente (de una app que esté alojada en ese portal)

Mejor si es propia, ya que controlamos completamente su visibilidad y nos permite hacer una conexión correcta a nuestro portal. 

![[Pasted image 20230601110527.png]]

### Crear una aplicación desde online 

https://developers.arcgis.com/experience-builder/guide/install-guide/

Content > new item > application > web mapping > url de https://localhost:3001  (crear aplicación)

![[Pasted image 20230601120941.png]]

![[Pasted image 20230601121007.png]]


Una vez la aplicación se ha creado, se tiene que ir a settings y registrarla. 
![[Pasted image 20230601120519.png]]

Una vez registrada 

![[Pasted image 20230601120805.png]]

Si el entorno de trabajo cambia se puede ir dentro de la carpeta de Experience Builder,  en el explorador de archivos a la ruta server / public / signing-info.json 

Dentro del signing info.json se tiene que cambiar el url del portal y entonces se tiene que cambiar el id del cliente. 

```json
[

  {

    "portalUrl": "https://eeap.maps.arcgis.com",

    "clientId": "Iftb2hS5P8PP9cmA",

    "supportsOAuth": true,

    "isWebTier": false

  }

]
```
