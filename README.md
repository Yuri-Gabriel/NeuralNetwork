# NeuralNetwork

## Visão geral

Este projeto implementa uma rede neural multicamadas para reconhecer dígitos manuscritos usando arquivos no formato IDX (MNIST). A arquitetura foi construída manualmente em Java, sem bibliotecas de aprendizado de máquina, com foco em entender o funcionamento interno de uma rede neural.

## Funcionalidades

- Leitura de dados MNIST em formato IDX
- Criação de uma rede neural com múltiplas camadas ocultas
- Treinamento com backpropagation
- Teste da rede sobre imagens de validação
- Visualização ASCII das imagens e resultados da previsão
- Implementação de operações matriciais em Java

## Estrutura do projeto

```text
NeuralNetwork/
├── pom.xml
├── README.md
└── src/
    └── main/
        ├── java/
        │   └── com/
        │       └── example/
        │           ├── DataSet.java
        │           ├── Loader.java
        │           ├── Main.java
        │           ├── RedeNeural.java
        │           └── Treinamento.java
        └── resources/
            └── input/
                ├── train-images-idx3-ubyte/
                ├── train-labels-idx1-ubyte/
                ├── t10k-images-idx3-ubyte/
                └── t10k-labels-idx1-ubyte/
```

## Tecnologias

- Java 17
- Maven
- Dataset MNIST

## Pré-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

- JDK 17+
- Maven 3.8+

## Como executar

1. Clone o repositório:

```bash
git clone https://github.com/Yuri-Gabriel/NeuralNetwork.git
cd NeuralNetwork
```

2. Compile o projeto:

```bash
mvn clean compile
```

3. Execute a classe principal:

```bash
java -cp target/classes com.example.Main
```

## Como funciona

A aplicação realiza os seguintes passos:

1. Carrega os arquivos MNIST de treino e teste
2. Normaliza os pixels para valores entre 0 e 1
3. Cria uma rede neural com camadas ocultas de 512, 256, 128 e 64 neurônios
4. Treina a rede usando propagação direta + backpropagation
5. Testa a rede em imagens de validação
6. Exibe a previsão e o valor esperado em console

## Classe principal

A entrada do projeto está em:

- `src/main/java/com/example/Main.java`

Essa classe carrega os dados, instancia a rede, executa o treinamento e realiza a avaliação final.

## Observações

- Os dados de entrada estão em `src/main/resources/input`.
- O projeto foi desenvolvido com fins acadêmicos e didáticos.
- A implementação é manual e usa operações matemáticas próprias para matrizes.

## Licença

Este projeto não possui uma licença definida explicitamente no repositório. Caso queira usar ou adaptar o código, verifique com o autor antes de distribuir.

## Autor

Yuri Gabriel
