# Projeto N8N com Docker

Este projeto utiliza [n8n](https://n8n.io/) orquestrado via Docker Compose para automação de workflows.

## Pré-requisitos

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)
- [Make](https://www.gnu.org/software/make/) (opcional, para facilitar comandos no terminal)

## Como iniciar

1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-usuario/seu-repo.git
   cd seu-repo
   ```

2. Inicie os serviços:
   ```sh
   docker-compose up -d
   ```
   Ou, se preferir, utilize o comando abaixo no terminal:
   ```sh
   make deploy
   ```

3. Acesse o n8n em [http://localhost:5678](http://localhost:5678).

## Estrutura

- `docker-compose.yml`: Configuração dos serviços Docker.
- `.n8n/` ou `/home/node/.n8n/`: Dados persistentes do n8n (workflows, credenciais, etc).

## Configuração

- O timezone padrão está definido como `America/Sao_Paulo`.
- Os dados do n8n são persistidos no volume local.

## Observações

- Para restaurar ou migrar para uma nova máquina, basta copiar os arquivos do volume `.n8n/`.
- Recomenda-se não versionar arquivos de dados sensíveis ou gerados automaticamente.

## Licença

Este projeto está sob a licença MIT.