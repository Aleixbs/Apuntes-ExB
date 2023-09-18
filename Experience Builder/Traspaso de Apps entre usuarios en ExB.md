No puedes traspasar las apps de los usuarios ni dentro de la misma organización. (Teóricamente si se puede. Cambiando en el info.json (archivo que se encuentra dentro de la carpeta de App en el server) las siguientes propiedades: )


```JSON
{
  "created": 1686640896568,
  "description": "",
  "id": "2",
  "modified": 1687259580743,
  "owner": "aleix.batlle", //Cambiando el OWNER por el nombre de usuario del nuevo
  "tags": [],
  "thumbnail": null,
  "title": "Untitled experience 1",
  "type": "Web Experience",
  "snippet": "",
  "typeKeywords": [
    "EXB Experience",
    "Ready To Use",
    "JavaScript",
    "status: Published",
    "version:1.11.0"
  ],
  "portalUrl": "https://ssaelo.esrilab.es/portal",
  "username": "aleix.batlle", //Cambiando el username por el nombre usuario del nuevo
  "url": null
}
```