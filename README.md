Arquivo para criar infraestrutura de Sentry usando NGINX com LetsEncrypt como servidor Proxy

Sentry Install:

- Baixe o arquivo docker-compose.yml para uma pasta com nome Sentry
- Altere a variável SENTRY_SECRET_KEY para uma string de caractere randomica, executando:
  "docker run --rm sentry:8.10.0 config generate-secret-key"

- Execute "docker-compose up -d"
- Execute "docker-compose exec sentry sentry upgrade" para configurar o banco de dados e criar o usuário "admin"
    (Opcional) Execute "docker-compose exec sentry pip install sentry-slack" se desejar o plugin do Slack, que também pode ser instalado mais tarde.
- Execute "docker-compose restart sentry"
  Feito, agora o Sentry está rodando na porta pública 9090

