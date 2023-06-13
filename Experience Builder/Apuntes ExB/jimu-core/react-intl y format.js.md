```tsx
import {FormattedMessage} from 'jimu-core'
```
https://formatjs.io/docs/react-intl/components/#formattedmessage

FormattedMessage es un componente de 'react-intl' mantenido por format.js


Formatted Message utiliza las props que són pasadas al MessageDescriptor para su definición, traducción y formateo de forma simultánea a la ejeccución ('on runtime')
```
props: MessageDescriptor &
  {
    values: object,
    tagName: string,
    children: (chunks: ReactElement) => ReactElement,
  }
```

### Message Descriptor[​](https://formatjs.io/docs/react-intl/api/#message-descriptor "Direct link to heading")

React Intl tiene un concepto de Descriptores de Mensajes que se utiliza para definir los mensajes/cadenas predeterminados de tu aplicación y se pasan a **_formatMessage_**. Los Descriptores de Mensajes funcionan muy bien para proporcionar los datos necesarios para tener las cadenas/mensajes traducidos, y contienen las siguientes propiedades:

- **`id`:** A unique, stable identifier for the message
- **`description`:** Context for the translator about how it's used in the UI
- **`defaultMessage`:** The default message (probably in English)

```json
type MessageDescriptor = {  
	id: string,  
	?defaultMessage: string,  //Opcional 
	?description: string | object //Opcional
}
```

##### En el SDK de Experience Builder se usa mucho para las etiquetas

Uso de **_.formatMesage_**

```tsx
            <Switch
              className="can-x-switch"
              checked={(this.props.config && this.props.config.goto) || false}
              data-key="goto"
              onChange={(evt) => {
                this.onToolsChanged(evt.target.checked, 'goto')
              }}
              //Uso de FormattedMessage con su método .formatMessage
              aria-label={this.props.intl.formatMessage({
                id: 'goto',
                defaultMessage: defaultMessages.goto
              })}
            />
```

Puede también usarse para formattear de forma dinámica un mensaje según el valor de una variable

```tsx
<FormattedMessage
  id="app.greeting"
  description="Greeting to welcome the user to the app"
  defaultMessage="Hello, {name}!"
  values={{
    name: 'Man',
  }}
/>

//Output: 
Hello, Man!

<FormattedMessage id="title">{txt => <h1>{txt}</h1>}</FormattedMessage>

//Output: 
<h1>title</h1>

etc... Más ejemplos en el link de Live Editor
```

Otros links de ayuda: 

- Componente FormattedMessage
https://formatjs.io/docs/getting-started/message-declaration/#using-react-api-formattedmessage
- Live Editor para probar su funcionalidad
https://formatjs.io/docs/react-intl/components/#formattedmessage
- React-intl
https://formatjs.io/docs/react-intl/
- Github format.js
https://github.com/formatjs/formatjs
- Tooling CLI 
https://formatjs.io/docs/tooling/cli/