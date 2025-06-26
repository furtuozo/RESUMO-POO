
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
Escrver daqui em diante
-------------------------------------------------------------------------------------------
## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/furtuozo/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/joaofurtuozo/)


## Referência

 - [Documentação Oficial do Java](https://dev.java/learn/)




