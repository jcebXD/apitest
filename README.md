apitest
=======

Wonka application for api testing

## How it works

Para implementar nuevas pruebas solo basta con llamar la función **add**:

###add

Esta función recibe el nombre de la prueba y una función.

Dentro de esta función debes definir un data object que contenga los siguientes atributos:

* method [string]('get','post','put','delete')
* resource [string]
* params [Hash]

Y finalmente llamar la función window.tests.call que recibe ese data object.

Por ejemplo:

```javascript
window.tests.add('citiesTest', function() {
  var data = {
    method: 'get',
    resource: uri('countries'),
    params: null
  };
  window.tests.call(data);
});
```
