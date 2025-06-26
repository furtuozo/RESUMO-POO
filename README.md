
# POO em Java ☕

Como sabemos, em Java temos 4 pilares que na verdade são os 4 pilares da Programação Orientada a Objetos (POO), o paradigma no qual o Java foi construído. Para entender e compreender Java, é necessário primeiramente entender como esses 4 pilares funcionam.

Os pilares são: [Encapsulamento - Herança - Polimorfismo - Abstração ]

Vamos entender como eles funcionam de uma forma simples e fácil.

## Encapsulamento 

É o conceito de "empacotar" os dados (atributos) e os métodos de uma classe. Também podemos dizer que é um jeito de escondermos os dados e métodos da nossa classe do mundo exterior.

Uma forma de pensarmos em Encapsulamento é imaginarmos um controle remoto. Para usá-lo, necessitamos apenas apertar os botões e não nos preocupamos em saber como funcionam os circuitos por dentro. Nós apenas apertamos os botões e as ações funcionam na nossa televisão.

#### ⚙️ Funcionamento 

-Para proteger os dados (atributos) dentro de uma classe, usamos o modificador de acesso private. Com isso, garantimos que o atributo só pode ser acessado de dentro da própria classe, ficando protegido do "mundo exterior".

-Mas e se precisarmos ler ou alterar esses dados de forma controlada? Para isso, criamos métodos públicos conhecidos como Getters (para obter o valor) e Setters (para definir um novo valor).

## 💻 Exemplo Prático

    public class ContaBancaria {
    // O saldo está encapsulado e protegido. Ninguém de fora pode alterá-lo diretamente.
    private double saldo;

    // Construtor
    public ContaBancaria(double saldoInicial) {
        if (saldoInicial > 0) {
            this.saldo = saldoInicial;
        }
    }

    // Método público (Getter) para acessar o saldo de forma segura
    public double getSaldo() {
        return this.saldo;
    }

    // Método público (Setter controlado) para depositar
    public void depositar(double valor) {
        if (valor > 0) {
            this.saldo += valor;
            System.out.println("Depósito realizado com sucesso.");
        } else {
            System.out.println("Valor de depósito inválido.");
        }
    }

    }

   
### ✅ Conclusão
Após vermos o resumo e o exemplo de código, fica claro como o Encapsulamento é fundamental. Ele nos permite criar classes mais seguras e robustas, evitando que outras partes do nosso sistema alterem dados importantes de forma indevida, o que poderia gerar grandes problemas.

Portanto, encapsular os dados de uma classe é uma boa prática essencial para escrever um código mais seguro, organizado e de fácil manutenção.
-------------------------------------------------------------------------------------------
## 👨‍👩‍👧‍👦 Herança
A Herança é um dos pilares de POO mais usados no dia a dia dos programadores. Como o seu próprio nome diz, uma classe irá herdar os métodos e atributos de sua classe pai (ou superclasse, assim chamada), e a classe que herda fica conhecida como classe filha (ou subclasse).

Isso promove a reutilização de código, e o programador não precisa escrever o mesmo código várias vezes.

Mas vale lembrar: para usar a herança, a relação entre as classes precisa fazer sentido. A regra principal é a do tipo "é um". Por exemplo, um Carro é um Veiculo, então a herança faz sentido. Eu não vou herdar da classe Carro se minha classe é Bicicleta, pois não há uma relação lógica entre elas.

- 🧬 Analogia Biológica: Herdamos características dos nossos pais, como a cor do cabelo, a cor dos olhos ou o tipo de cabelo. No entanto, nós temos nossas próprias características, que são únicas.

- 🏦 Outro exemplo: ContaCorrente e ContaPoupanca. Ambas são Contas, compartilhando características básicas. Porém, cada uma tem métodos e atributos específicos que as diferenciam.

#### ⚙️ Funcionamento 
- Para uma classe herdar os atributos e métodos de outra, ela precisa usar a palavra-chave extends. Com o uso dessa palavra-chave, a nossa subclasse irá herdar o comportamento da superclasse.

## 💻 Exemplo Prático

    // Superclasse (Pai)
    public class Veiculo {
    String marca;
    String modelo;

    public void acelerar() {
        System.out.println("O veículo está acelerando.");
        }
    }


    // Subclasse (Filha) - Herda tudo de Veiculo
    public class Carro extends Veiculo {
    int numeroDePortas;

    // O Carro já possui o método acelerar() por herança!
    }

    // Classe principal para testar nosso código
    public class Main {
    public static void main(String[] args) {
        // Criando um objeto Carro
        Carro meuCarro = new Carro();

        meuCarro.marca = "Fiat";           // Atributo herdado de Veiculo
        meuCarro.modelo = "Uno";           // Atributo herdado de Veiculo
        meuCarro.numeroDePortas = 2;       // Atributo próprio de Carro

        // Chamando um método herdado de Veiculo
        meuCarro.acelerar(); // Saída: O veículo está acelerando.

        System.out.println("Meu carro é um " + meuCarro.marca + " " + meuCarro.modelo);
        }
    }

    

### ✅ Conclusão
Com isso, vemos que a Herança é muito interessante e pode ir muito mais além disso. Com ela, podemos poupar tempo evitando escrever o mesmo código mais de uma vez. Além disso, a herança ajuda a deixar nosso código mais limpo, legível e permite que possamos organizá-lo em hierarquias lógicas.
 
-------------------------------------------------------------------------------------------
Escrever a partir daqui
-------------------------------------------------------------------------------------------
## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/furtuozo/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/joaofurtuozo/)


## Referência

 - [Documentação Oficial do Java](https://dev.java/learn/)




