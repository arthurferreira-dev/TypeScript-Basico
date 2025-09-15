# Por que usar o Typesscript em projetos pequenos ou em projetos?

**Vantangens do TypeScript**

1. [Tipagem](#tipagem)
1. [Ajuda a descobrir falhas e bugs](#ajuda-a-descobrir-falhas-e-bugs)
1. [Comunição entre equipes](#comunição-entre-equipes)
1. [Não altera a performace do código](#não-altera-a-performace-do-código)

## Tipagem

*JavaScript é uma linguagem "fracamente tipada"*.

Um exemplo:

```javascript
console.log('2' + 2) // output: 22
```

Em aplicações em larga escala um erro desse não pode ser percebido!

Outro exemplo:

```javascript
const fullName = (user) => {
    return `${user.firstName} ${user.lastName}`
}

const user = {
    firstName: "Arthur",
    middleName: "Ferreira"
}

fullName(user); // output: error
```

O TypeScript não veio para tipar tudo que existe, afinal ele é convertido para Javascript no final.

O benefício do Typescript está na clareza do código.

Um código legível evita futuros bugs.

Facilidade de extensão e manuntenção da aplicação.

Agora vamos para o exemplo em TypeScript:

```typescript
type User = {
    firstName: string,
    lastName: string
}

const fullName = (user: User): string => {
    return `${user.firstName} ${user.lastName}`
}

const user = {
    firstName: "Arthur",
    middleName: "Ferreira" // Mostra um erro antes de você executar qualquer coisa
}
```

## Ajuda a descobrir falhas e bugs

Quando definimos explicitamente valores que estamos trabalhando reduz a propabilidade de bugs no nosso código.

A [IDEs](https://pt.wikipedia.org/wiki/Ambiente_de_desenvolvimento_integrado) como o **Visual Studio Code**, eles usam o autocomplete para verificar o código digitado e deixando sempre claro o tipo dos valores que estamos lidando.

Evitando problemas como `'2' + 2 = 22`.

```typescript
const sum = (n1: number, n2: number): number => {
    return n1 + n2;
}

const total = sum('2', 2); // Ao passar o mouse em cima
```

## Comunição entre equipes

Como vemos o TypeScript traz benefícios de manutenção e escalabilidade.

Quando desenvolvemos em Typescript normalmente não desenvolvimemos sozinhos, outros devs vão ajudar (Trabalho em equipe).

Sendo assim qualidade de código é crucial para crescer a aplicação com menos bugs.

## Não altera a performace do código

TypeScript não irá alterar a performace do seu código, ele só faz uma migração para JS e você pode específicar a versão do NodeJS.

```json
{
    "compilerOptions": {
        "target": "es5"
    }
}
```