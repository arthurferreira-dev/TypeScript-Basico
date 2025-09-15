# Variáveis e Constantes

Como armazenar dados corretamente em TypeScript.

## Existem formas *otimizadas* de se armazenar variáveis

Por exemplo, se esse valor que você precisa armazenar será alterado mais a frente ou não. É só por isso, já muda a forma de se declarar essas variáveis.

## A tipagem muda o *gerenciamento de recursos*

Números e textos dependem de quantidades diferentes de memória.

## Vamos dar um passo para trás

Antes de pensar se é um number, uma string... Você precisa saber se a variável vai se comportar como uma [constante](#o-valor-de-uma-constante-não-pode-ser-alterado).

## O valor de uma constante não pode ser *alterado*

Uma vez atríbuido um valor, esta constante permanece assim até o final da execução desse programa.

Veja um exemplo:

```typescript
const name = "Eduardo"
name = "Jão" // Error
```

Agora vamos ver com uma API:

```typescript
const customers = getCustomers()
```

A const não proíbe alterar o valor de uma lista ou de um object, apenas de ser atríbuida novamente.

```typescript
const customers = getCustomers()
customers = [] // errado
```

```typescript
const customers = getCustomers()
customers.push(anotherCustomers) // novo e certo
```

Para deixar o object com imutabilidade:

```typescript
const customers = getCustomers()
Object.freeze(customers) // não será mudado!
```

Nem toda hora precisamos de algo constante.

```typescript
let name = "Adalberto"
name = "Jão"
```

## Quando usar const ou let?

Sempre usa const, mas quando precisar alterar a variável use let. Bem simples!