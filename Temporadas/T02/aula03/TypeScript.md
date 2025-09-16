# Estruturas de Repetição

*"Escutar repetidamente determinadas ações"*.

## Formas de executar uma ação repetidamente

* [For, forIn e forEach](#for-forin-e-foreach)
* [While](#while)

## For, forIn e forEach

Uma forma simples de fazer o código repetir uma ação é usando o operador ``for``, que pode ser utilizado de três formas.

*Como escolher um operador*?

Em todos os casos vamos trabalhar com o conceito de índice, pode ser entendido como um número da página de uma livro, ou seja uma variável que vai armazenar um valor númerico indicando em qual interação o for se encontra em sua execução.

### For

Exemplo:

```typescript
for (let index: number; index >= 10; index++) {
    console.log(users[index]);
}
```

Como se usa:

```typescript
for (variavel; condicional; incremento) {
    // Execute seu código com a variavel
}
```

### forIn

Usando o ```forIn``:

```typescript
for (const index in users) {
    console.log(users[index]);
}
```

Como se usa:

```typescript
for (variable in list/object) {
    console.log(list[variable]);
}
```

### forEach

Utilizando o ``forEach``:

```typescript
users.forEach((user) => {
    console.log(user)
});
```

Como utilizar:

```typescript
const array = [el1, el2, el3];

array.forEach((value, index, array) => { // pode digitar apenas 1 dos args mas eles vem dessa ordem
    console.log(value) // output: el1, el2, el3
});
```

## While

Quando temos a necessidade de entrada de looping com um valor indefinido, podemos recorrer ao while.

Exemplo:

```typescript
while (!user.full()) {
    user.eat(bread);
}
```