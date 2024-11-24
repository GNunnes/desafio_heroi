# Classe Hero em JavaScript

Este projeto implementa uma classe `Hero` que representa um herói em um jogo. A classe possui propriedades como nome, idade e tipo, além de um método para realizar ataques.

## Código

```javascript
class Hero {
    constructor(nome, idade, tipo) {
        this.nome = nome;
        this.idade = idade;
        this.tipo = tipo;
    }

    atacar() {
        let ataque;

        switch (this.tipo) {
            case "mago":
                ataque = "magia";
                break;
            case "guerreiro":
                ataque = "espada";
                break;
            case "monge":
                ataque = "artes marciais";
                break;
            case "ninja":
                ataque = "shuriken";
                break;
            default:
                ataque = "ataque desconhecido";
        }

        console.log(`o ${this.tipo} atacou usando ${ataque}`);
    }
}

// Exemplo de uso
const heroi1 = new Hero("Gandalf", 300, "mago");
heroi1.atacar();  // Saída: o mago atacou usando magia

const heroi2 = new Hero("Conan", 35, "guerreiro");
heroi2.atacar();  // Saída: o guerreiro atacou usando espada

const heroi3 = new Hero("Li", 28, "monge");
heroi3.atacar();  // Saída: o monge atacou usando artes marciais

const heroi4 = new Hero("Shin", 22, "ninja");
heroi4.atacar();  // Saída: o ninja atacou usando shuriken
