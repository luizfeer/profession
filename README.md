# Profissões do Brasil Array

Para acelerar formulários que necessitam das profissões em português, em JS para uso em autocomplete, select e etc.

Veja este [exemplo](https://codepen.io/luizalmeida7/pen/RwarYmo) em Vue.Js!
## Estrutura
Código e nome da profissão.
```json
  code: 1,  name: 'Engenheiro(a)'
```

## Exportando com outras variáveis
```javascript
const  profissoesFormated  =  PROFISSOES.map(v  => ({
  text:  v.name,
  value:  v.code
}))
export  default  profissoesFormated
```
## Exemplo de select em Vue.js
```html

<label>
  <span >Profissão:</span>
  <select  v-model="profession">
    <option
    v-for="option in profissoesFormated"
    :key="option.value"
    :value="option.text"
    >
      {{ option.text }}
    </option>
  </select>
</label>
```
