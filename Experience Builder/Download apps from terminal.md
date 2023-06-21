https://community.esri.com/t5/arcgis-experience-builder-blog/experience-builder-devops-generating-the-app/ba-p/1112247


Desde la carpeta padre de ArcGISExperienceBuilder puedes ejecutar un comando de node para descargar la app en un zip

```cmd
C:\ArcGISExperienceBuilder>node -e "require('./server/src/middlewares/dev/apps/app-download.js').zipApp('5', 'pruebadescargaTerminal.zip');"
Apps folder: C:\ArcGISExperienceBuilder\server\public\apps
Done.

C:\ArcGISExperienceBuilder>node -v
v18.16.0
```
