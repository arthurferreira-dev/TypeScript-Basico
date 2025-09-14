# O que é TypeScript?

Quem desenvolve para a Web concerteza conhece a linguagem JavaScript, em algum momento ouviu em TypeScript.

TypeScript é um ***superset* de JavaScript**.

| O que é um *superset*? |
| ---------- |
| Superset é uma extensão da linguagem, adiciona novas funcionalidades |

Essa linguagem foi publicada pela primeira vez em 2012, pela Microsoft com o intuito de melhorar o desenvolvimento de aplicações de larga escala que utiliza Javascript.

## Melhorar o desenvolvimento? Como assim?

Typescript traz ao Javascript a mesma habilidade que outras linguagens também tem, o poder de específicar o tipo dos dados com estamos trabalhando (**Tipagem**), mostrar com clareza oque uma variável está guardando, os inputs e os outputs de um método e melhor a capacidade da linguagem de **P**rogramação **O**rientada a **O**bjetos (**POO**).

## Como o TypeScript funciona?

O Typescript é convertido para JavaScript.

O Typescript é uma "[syntax sugar](https://pt.wikipedia.org/wiki/A%C3%A7%C3%BAcar_sint%C3%A1tico)", sendo necessário converter o código para o Javascript (Este processo é chamado de **Transpilação**).

### Exemplo em TypeScript

```typescript
// Typescript
enum Gender {
    MALE = 'MALE',
    FEMALE = 'FEMALE'
}

const username: string = 'Arthur';
const userage: number = 13;
const usergender: Gender = Gender.MALE;
```

```javascript
// Javascript
"use strict";
var Gender;
(function (Gender) {
    Gender["MALE"] = "MALE";
    Gender["FEMALE"] = "FEMALE";
})(Gender || (Gender = {}));
const username = 'Arthur';
const userage = 13;
const usergender = Gender.MALE;
```

[Transpilador Typescript](https://www.typescriptlang.org/play)