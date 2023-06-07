# k_bench_tests

Neste repositorio encontram-se alguns casos de testes feitos com o auxilio da ferramenta [K-bench](https://github.com/vmware-tanzu/k-bench). Nesse documento temos instruções para executar os testes e a definição de todos os cenários disponibilizados.

### Descrição dos testes
No diretório `config/`, temos todos os testes organizados de forma semelhante. Cada caso de teste é definido por um diretório (nomeado com o nome do teste) que contém o arquivo `config.json` com as definições dos testes. Atualmente esses são os testes já implementados:

| Teste | Descrição | Cenário |
| --- | --- | --- |
| cp_25clients | Nesse teste temos 25 clientes simultaneos, executando as seguintes operações Create, List, Get, Update e Delete para um Pod, um Deployment (Configurado com 5 réplicas), um Service e um NameSpace | Usado para testar o desempenho do cluster com 25 clientes simultaneos |
| cp_50clients | Nesse teste temos 50 clientes simultaneos, executando as seguintes operações Create, List, Get, Update e Delete para um Pod, um Deployment (Configurado com 5 réplicas), um Service e um NameSpace |  Usado para testar o desempenho do cluster com 50 clientes simultaneos |
| cp_100clients | Nesse teste temos 100 clientes simultaneos, executando as seguintes operações Create, List, Get, Update e Delete para um Pod, um Deployment (Configurado com 5 réplicas), um Service e um NameSpace |  Usado para testar o desempenho do cluster com 100 clientes simultaneos  |
| cp_150clients | Nesse teste temos 150 clientes simultaneos, executando as seguintes operações Create, List, Get, Update e Delete para um Pod, um Deployment (Configurado com 5 réplicas), um Service e um NameSpace |  Usado para testar o desempenho do cluster com 150 clientes simultaneos |

### Adicionando novos testes
Para adicionar novos testes, simplismente crie um novo diretório da seguinte forma `config/<nome-do-teste>/config.json`. Esse arquivo `config.json` deve conter as configurações do teste. Para referencias de como configurar os testes, você pode consultar a [documentação da ferramenta](https://github.com/vmware-tanzu/k-bench#top-level-configuration-options).

### Rodando os testes
