# EcomCore

> Seu sistema fala, a gente escuta.

Sistema de monitoramento de recursos de servidores voltado a plataformas de **e-commerce**, desenvolvido como projeto acadêmico do **Grupo 08 da São Paulo Tech School (SPTech)**.

O EcomCore tem como proposta coletar, armazenar e apresentar métricas de **CPU, memória RAM, disco e rede**, ajudando equipes de suporte a identificar sobrecargas e tomar decisões para manter a disponibilidade da operação.

> Este README foi elaborado com base na documentação do projeto. As funcionalidades descritas representam o escopo previsto; seu estado de implementação não foi verificado no código-fonte.

## Sumário

- [Sobre o projeto](#sobre-o-projeto)
- [Objetivos](#objetivos)
- [Recursos monitorados](#recursos-monitorados)
- [Funcionalidades previstas](#funcionalidades-previstas)
- [Perfis de uso](#perfis-de-uso)
- [Fluxo de funcionamento](#fluxo-de-funcionamento)
- [Tecnologias e ferramentas](#tecnologias-e-ferramentas)
- [Requisitos não funcionais](#requisitos-não-funcionais)
- [Instalação e execução](#instalação-e-execução)
- [Contexto acadêmico e documentação](#contexto-acadêmico-e-documentação)

## Sobre o projeto

Plataformas de comércio eletrônico dependem de uma infraestrutura disponível para processar consultas, pedidos e transações. Em períodos de grande demanda, como Black Friday e Natal, o aumento do consumo de recursos pode causar lentidão, falhas de serviços e indisponibilidade.

O EcomCore propõe centralizar indicadores sobre as condições dos servidores em um painel de monitoramento. Com métricas atualizadas, histórico de utilização e alertas, a equipe de TI poderá acompanhar o ambiente e investigar situações que comprometam a experiência dos clientes.

## Objetivos

- Dar visibilidade ao consumo dos recursos dos servidores.
- Identificar situações de atenção e criticidade a partir de limites definidos.
- Apoiar a investigação e o acompanhamento de incidentes.
- Disponibilizar histórico para análise de tendências e planejamento de capacidade.
- Contribuir para reduzir impactos de lentidão e indisponibilidade na operação do e-commerce.

## Recursos monitorados

| Recurso | Acompanhamento previsto | Riscos que o monitoramento ajuda a identificar |
| --- | --- | --- |
| CPU | Nível de utilização do processador | Sobrecarga e atrasos no processamento de requisições |
| Memória RAM | Consumo e capacidade disponível | Esgotamento de memória e interrupção de processos |
| Disco / armazenamento | Utilização e capacidade disponível | Falta de espaço para dados, registros e arquivos da aplicação |
| Rede | Utilização e tráfego de rede | Saturação que pode comprometer o acesso e a comunicação entre serviços |

## Funcionalidades previstas

| Código | Funcionalidade | Descrição |
| --- | --- | --- |
| RF01 | Coleta de métricas | Coletar automaticamente dados de CPU, memória RAM, disco e rede dos servidores monitorados. |
| RF02 | Painel de indicadores | Exibir os níveis de utilização dos recursos de forma clara e atualizada. |
| RF03 | Identificação de sobrecarga | Classificar situações como de atenção ou críticas quando os limites definidos forem ultrapassados. |
| RF04 | Alertas | Gerar alertas para utilização de recursos acima dos limites estabelecidos. |
| RF05 | Consulta por servidor | Permitir a visualização das métricas de um servidor específico. |
| RF06 | Histórico de métricas | Armazenar os dados coletados para consultas posteriores. |
| RF07 | Filtros | Filtrar indicadores e alertas por servidor, recurso, período e criticidade. |
| RF08 | Registro de incidentes | Permitir a criação de incidentes a partir de alertas identificados. |
| RF09 | Acompanhamento de incidentes | Acompanhar o status dos incidentes até sua resolução. |
| RF10 | Controle de acesso | Disponibilizar acesso conforme o perfil do usuário, como gestor ou analista de suporte. |

As histórias de usuário também apontam necessidades de notificações críticas por e-mail ou aplicativo, análise do comportamento em períodos de pico e acompanhamento de SLA e disponibilidade. Esses itens expressam necessidades do produto e não confirmam integrações ou recursos já implementados.

## Perfis de uso

- **Gestor de suporte:** acompanha indicadores, incidentes prioritários e prazos de resolução para apoiar decisões de escalonamento e capacidade.
- **Analista de suporte:** consulta métricas por servidor, filtra alertas, investiga problemas e acompanha incidentes até sua resolução.
- **Administrador de usuários:** perfil apresentado nas proto-personas, voltado à administração de usuários e permissões de acesso.

## Fluxo de funcionamento

O fluxo abaixo resume a proposta funcional, sem definir a arquitetura técnica da implementação:

1. Coletar automaticamente métricas dos recursos dos servidores.
2. Armazenar as medições para consulta e análise histórica.
3. Apresentar os indicadores no painel de monitoramento.
4. Comparar a utilização com os limites definidos e gerar alertas.
5. Permitir que a equipe registre e acompanhe incidentes relacionados aos alertas.

## Tecnologias e ferramentas

Tecnologias citadas na documentação:

| Categoria | Tecnologias / ferramentas |
| --- | --- |
| Linguagens e tecnologias web | HTML, CSS, JavaScript, SQL, Java e Python |
| Banco de dados e administração | MySQL / MySQL Workbench* |
| Infraestrutura | Amazon EC2 (AWS) |
| Desenvolvimento | Visual Studio Code e IntelliJ IDEA |
| Gestão e colaboração | Planner e GitHub |

\* A documentação identifica o MySQL Workbench na seção de banco de dados. O Workbench é uma ferramenta de administração; a versão e a configuração do servidor de banco de dados precisam ser confirmadas na implementação.

## Requisitos não funcionais

| Código | Requisito | Comportamento esperado |
| --- | --- | --- |
| RNF01 | Disponibilidade | Permitir consultas durante o período de operação da plataforma de e-commerce. |
| RNF02 | Desempenho | Apresentar indicadores rapidamente, sem atrasos significativos na consulta. |
| RNF03 | Atualização | Atualizar as métricas automaticamente em intervalos definidos pelo sistema. |
| RNF04 | Segurança | Utilizar autenticação para controlar o acesso às informações. |
| RNF05 | Usabilidade | Apresentar informações de forma simples e intuitiva para a equipe de suporte. |
| RNF06 | Persistência | Manter métricas e registros de incidentes armazenados para consultas posteriores. |

Os intervalos de coleta, limites de utilização e metas mensuráveis de desempenho e disponibilidade não são especificados no documento de referência.

## Instalação e execução

A documentação fornecida não apresenta um procedimento de instalação ou execução. Para completar esta seção com instruções reproduzíveis, é necessário consultar o repositório e confirmar:

- Versões das tecnologias e dependências necessárias.
- Configuração do banco de dados e scripts de inicialização.
- Variáveis de ambiente utilizadas pela aplicação.
- Comandos para iniciar a coleta de métricas e a aplicação web.
- Configuração de acesso aos servidores monitorados.
- Procedimentos de teste e, quando aplicável, implantação na AWS.

## Contexto acadêmico e documentação

- **Instituição:** São Paulo Tech School (SPTech).
- **Equipe:** Grupo 08.
- **Tema:** monitoramento de recursos físicos de um servidor de e-commerce.
- **Documento de referência:** `documentacao-EcomCore.pdf`.

A relação de integrantes, a URL do repositório e a licença de uso não foram informadas na documentação disponibilizada.
