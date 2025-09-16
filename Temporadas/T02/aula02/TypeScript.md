# Estruturas de decisão

*"Seus programa mais inteligente"*.

Fazendo com que nosso programa não somente crie variáveis, mas também tome *decisões*.

## Tipos de estruturas condicionais

Vamos aprender 3 tipos de estruturas condicionais:

* If / Else
* Switch
* Operador Ternário

Essas estruturas deixam seu programa mais inteligente, não como uma *I.A* e sim que ele toma decisões simples com operadores lógicos que comparam valores.

## If / Else (Se / Senão)

Nós precisamos criar caminhos baseados em **decisões de verdadeiro ou falso**.

Se é verdadeiro ele entra em um fluxo de execução, se for falso executa outro.

Exemplo:

```typescript
if (age: number >= 18) {
    alert('Usuário maior de idade');
} else {
    alert('Usuário menor de idade');
}
```

```typescript
if (age: number >= 18 && creditCard) {
    alert('Usuário maior de idade');
} else (parentalPermission === true && creditCard) {
    alert('Usuário menor de idade, com permissão');
} else {
    alert('Usuário menor de idade, sem permissão');
}
```

O IF / ELSE pode ser uma maravilha, mas ele tem um preço que é a complexidade.

Podemos resolver a complexidade com *``Design Patterns``*.

## Switch

Quando não temos operações condicionais complexas, com muitos operadores lógicos, talvez o switch seja uma boa escolha.

Quando se varia entre muitos *valores diferentes*, o switch pode ser uma boa escolha.

Exemplo:

```typescript
switch(option: number) {
    case 1: // deseja falar conosco tecle 1 [!LEMBRE-SE]
        // Faça algo que o optional seja igual a 1
        break;
    case 2:
        // Faça algo que o optional seja igual a 2
        break;
    case 3:
        // Faça algo que o optional seja igual a 3
        break;
    case 4:
        // Faça algo que o optional seja igual a 4
        break;        
}
```

* Funciona bem quando você só precisa analisar um valor de variável sem condicionais complexas.
* Ele não analisa com operadores ``>``, ``<``, e demais.

## Operador Ternário

*Utilizando para tomadas de decisões simples*, retornando valores diferentes para uma condicional.

Como se escreve:

```typescript
const variable = operation ? IF : ELSE
```

Exemplo:

```typescript
const prefix = user.gender === Gender.FEMALE ? "Sra." : "Sr."
```

Que é a mesma coisa que isso em If / Else:

```typescript
let prefix = ""

if (user.gender === Gender.FEMALE) {
    prefix = "Sra."
} else {
    prefix = "Sr."
}
```

O Ternário deixa nosso código mais simples e legível, oque é legal.