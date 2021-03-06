<img src="https://avatars1.githubusercontent.com/u/35275557?v=4&s=200" width="128px" height="128px" align="left"/>

# Nata.house JavaScript Style Guide

Nosso style guide é baseado no [Airbnb's](https://github.com/airbnb/javascript). Com algumas alterações.

## Instalando...

```shell
$ yarn add @natahouse/eslint-config
```

Para incluir no projeto, crie o arquivo `.eslintrc` com a seguinte config:

```json
{
  "extends": ["@natahouse"]
}
```

## Regras adicionadas

### Ponto e vírgula

Ponto e vírgula não precisa serem usadas. [motivo](https://flaviocopes.com/javascript-automatic-semicolon-insertion/)

Errado:
```js
const nata = 'house';
```

Certo:
```js
const nata = 'house'
```

### Quebras de linha dentro de parênteses de função

Errado:
```js
hello(nata,
  house)
```

Certo:
```js
hello(
  nata,
  house,
)
```

### Vírgula em array, object multiline, menos em parâmetros de funções

Errado:
```js
const array = [1, 2, 3,]
```

Certo:
```js
const array = [1, 2, 3]
```

Errado:
```js
const array = [
  1,
  2,
  3
]
```

Certo:
```js
const array = [
  1,
  2,
  3,
]
```

Errado:
```js
const obj = {
  a: 1,
  b: 2,
  c: 3
}
```

Certo:
```js
const obj = {
  a: 1,
  b: 2,
  c: 3,
}
```

`Vírgula em parâmetros pode causar erros`

Errado:
```js
Object.assign(
  {},
  b,
  c,
)
```

Certo:
```js
Object.assign(
  {},
  b,
  c
)
```

### Comprimento de linha

90 caracteres, incluindo espaços.


### Parâmetros máximos na definição da função

Máximo 3 parâmetros


Errado:
```js
const nata = (arg1, arg2, arg3, arg4, arg5, arg6, arg7) => ...
```

Certo:
```js
const nata = (arg1, arg2, arg3) => ...
```


### Múltiplas linhas vazias


Errado:
```js
const a = 'hello nata.house'


console.log(a)
```

Certo:
```js
const a = 'hello nata.house'

console.log(a)
```

### Aspas duplas ao redor de strings

Apenas para seguir o padrão adotado pelo typescript e para minimizar a confusão com `` que é usado para concatenar strings com variáveis.

Errado:
```js
const a = 'hello nata.house'
```

Certo:
```js
const a = "hello nata.house"
```

### Usar template string ao invés de +

Melhora a leitura do código

Errado:
```js
const name = "nata.house"
const a = "hello" + name
```

Certo:
```js
const name = "nata.house"
const a = `hello ${nata.house}`
```

### Usar Number() ao invés de + para converter string para number

Melhora a leitura do código

Errado:
```js
const value = "65"
const a = 15 + ~value
```

Certo:
```js
const value = "65"
const a = 15 + Number(value)
```

### Usar String() ao invés de + "" para converter number para string

Melhora a leitura do código

Errado:
```js
const value = 1
const a = value + ""
```

Certo:
```js
const value = 1
const a = String(value)
```

## Contribuindo

Sinta-se a vontade para abrir uma PR
