# Ambiente de Testes PostGIS

> Já contem os dados iniciais do workshop, trazendo várias informações da cidade de Nova Yorque.

## Uso Básico

Para subir o ambiente basta rodar o comando:

```bash
sudo docker compose up -d
```

## Acesso ao pgAdmin

O `pgAdmin` pode ser acessado com as seguintes credênciais, através do localhost pela porta `1080`. Ou se necessário o uso de outra porta o mesmo pode ser alterado no arquivo `docker-compose.yml`.

Usuário:

```text
testing@testing.com
```

Senha:

```text
302010
```

## Acesso ao Banco de Dados

Por padrão o banco de dados rodará na porta `1032`. O mesmo pode ser alterado no arquivo `docker-compose.yml`

Usuário:

```text
testing
```

Senha:

```text
302010
```

## Acesso Direto

Os containers recebem o apelido `workshop_postgis` e `workshop_pgadmin`, podendo o banco de dados ser acessado diretamente através do comando:

```bash
sudo docker exec -it workshop_postgis 'bin/bash'
```

> Normalmente, o acesso pelo pgAdmin ou outro editor sql é o suficiente.
