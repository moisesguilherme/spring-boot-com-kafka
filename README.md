# Configuração do Apache Kafka com Spring-Boot
Este projeto é um estudo que utiliza o Kafka em conjunto com o Spring Boot. Ele consiste em dois projetos: um Producer e um Consumer, configurados para interagir com o Kafka.
## Referência Utilizada
Este projeto baseia-se em um tutorial específico, cujo código fonte pode ser encontrado [aqui](https://github.com/eugenp/tutorials/tree/master/spring-kafka)

## Iniciando o Ambiente
Para executar o Kafka, Zookeeper e Kafdrop, utilize o Docker Compose:
```sh
docker compose up
```
Isso iniciará os serviços necessários para o funcionamento do Kafka e do Zookeeper, além do Kafdrop para visualização dos tópicos.

# Estrutura do Projeto

#### Producer
O projeto Spring Boot do tipo Producer é responsável por enviar mensagens para um tópico no Kafka.

#### Consumer
O projeto Spring Boot do tipo Consumer é responsável por consumir mensagens do tópico Kafka.


### Execução
Certifique-se de que o ambiente do Kafka, Zookeeper e Kafdrop está em execução usando o Docker Compose.
1. Certifique-se de que o ambiente do Kafka, Zookeeper e Kafdrop está em execução usando o Docker Compose.
2. Inicie o projeto Producer para enviar mensagens ao tópico Kafka.
3. Inicie o projeto Consumer para consumir as mensagens do tópico Kafka.

Para enviar uma requisição POST para `localhost:8080/mensagem` com um corpo JSON contendo a chave `"mensagem"` e o valor `"Bora Praticar 1"`, utilize o seguinte comando  

```bash
curl --location --request POST 'localhost:8080/mensagem' \
--header 'Content-Type: application/json' \
--data-raw '{
    "mensagem": "Bora Praticar 1"
}'
```