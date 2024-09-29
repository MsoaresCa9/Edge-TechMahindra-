# Edge-TechMahindra-
# CP4-edge-Firewaal descomplicado 
Integrantes: Caio Soares Rossini, Lucas Serrrano, Pedro Henrique Nobre e Thomaz
RM: 555084, 557789,55170, 557454
1ESPJ
# FIWARE Descomplicado

Este repositório contém um projeto dedicado à instalação e verificação do FIWARE Descomplicado em ambientes Linux, bem como a realização de testes de health check nos componentes principais da plataforma.

## Índice

- [Descrição do Projeto](#descrição-do-projeto)
- [Instalação](#instalação)
- [Health Check](#health-check)
- [Vídeo de Apresentação](#vídeo-de-apresentação)
- [Licença](#licença)

## Descrição do Projeto

O FIWARE Descomplicado é uma iniciativa para facilitar a instalação e o uso da plataforma FIWARE em máquinas Linux. O projeto aborda a instalação de componentes essenciais e a realização de verificações de saúde dos serviços.

## Instalação

Siga os passos abaixo para realizar a instalação do FIWARE Descomplicado em uma máquina Linux:

1. **Pré-requisitos:**
   - Certifique-se de que você possui um sistema Linux atualizado.
   - Instale as dependências necessárias:
     ```bash
     sudo apt-get update
     sudo apt-get install -y <dependências necessárias>
     ```

2. **Clone o repositório:**
   ```bash
   git clone https://github.com/seuusuario/fiware-descomplicado.git
   cd fiware-descomplicado
   ```

3. **Configuração do ambiente:**
   - Edite o arquivo de configuração conforme suas necessidades:
     ```bash
     nano config.env
     ```

4. **Iniciar os serviços:**
   ```bash
   docker-compose up -d
   ```

5. **Verifique se os serviços estão em execução:**
   ```bash
   docker ps
   ```

## Health Check

Para garantir que os componentes da plataforma estão funcionando corretamente, execute os métodos HTTP de health check dos seguintes serviços:

1. **Orion Context Broker:**
   - Execute a requisição:
     ```bash
     curl -i http://<endereço_do_orion>:1026/version
     ```

2. **STH-Comet:**
   - Execute a requisição:
     ```bash
     curl -i http://<endereço_do_sth>:8668/version
     ```

3. **IoT Agent MQTT:**
   - Execute a requisição:
     ```bash
     curl -i http://<endereço_do_iot_agent>:4041/version
     ```

As requisições acima devem retornar o status 200 OK e as versões dos respectivos componentes. Para mais detalhes, consulte a coleção do Postman disponível no [GitHub da Plataforma FIWARE Descomplicado](https://github.com/fiware/fiware-desk).

## Vídeo de Apresentação

Para uma apresentação detalhada do projeto, assista ao vídeo disponível no YouTube:  
https://youtu.be/o24WOOdvXbY


## Licença

Este projeto está licenciado sob a MIT License. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
