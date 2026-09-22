📦 OptiStock
Sistema Inteligente de Otimização de Estoque e Gestão de Inventário



OptiStock é uma aplicação web voltada à análise, otimização e gestão inteligente de estoques, utilizando conceitos de Engenharia de Produção, Logística e Gestão de Operações para apoiar decisões de reposição e compras.

🔗 Acessar o sistema

📋 Sobre o Projeto
O OptiStock foi desenvolvido para centralizar indicadores e ferramentas de gestão de estoque em uma única interface.

A aplicação permite cadastrar e analisar SKUs, acompanhar níveis de estoque, calcular parâmetros de reposição e identificar quais produtos exigem atenção imediata.

O sistema utiliza conceitos clássicos de gestão de inventário, como:

EOQ — Economic Order Quantity

ROP — Reorder Point

Estoque de Segurança

Curva ABC / Análise de Pareto

Custo Total de Estoque

Lead Time

Nível de Serviço

MRP Lite

Análise de demanda e valor movimentado

O objetivo é transformar dados operacionais em informações que facilitem o planejamento de compras e o controle do capital imobilizado em estoque.

🎯 Objetivos
O projeto busca oferecer uma ferramenta capaz de:

Reduzir decisões de compra baseadas apenas em percepção.

Identificar produtos que atingiram o ponto de reposição.

Calcular lotes econômicos de compra.

Estimar níveis de estoque de segurança.

Auxiliar na definição do ponto de pedido.

Classificar produtos conforme seu impacto financeiro.

Visualizar custos relacionados ao estoque.

Centralizar indicadores operacionais em um dashboard.

Gerar sugestões de pedidos de compra.

🚀 Funcionalidades
📊 Dashboard Executivo
Painel central para acompanhamento dos principais indicadores do inventário.

Entre os indicadores apresentados estão:

Valor total em estoque

Alertas de reabastecimento

Giro anual estimado

Média de inventário

Custo anual de posse

Armazenamento e capital

Relação entre estoque atual e ROP

A aplicação também apresenta uma visão dos SKUs que estão abaixo ou no ponto de pedido. 
N
Neemi4s

📦 Gestão de SKUs
O sistema permite cadastrar produtos e manter os principais parâmetros necessários para os cálculos de estoque.

Dados utilizados
Campo	Descrição
SKU	Código de identificação do produto
Categoria	Grupo ao qual o produto pertence
Produto	Nome ou descrição do item
Custo Unitário	Valor individual do produto
Demanda Anual	Quantidade estimada de consumo anual
Custo de Pedido	Custo associado à realização de um pedido
Estoque Atual	Quantidade disponível
Lead Time	Tempo esperado para reposição
Desvio Padrão	Variabilidade da demanda

📐 Otimizador EOQ
O módulo de EOQ — Economic Order Quantity, ou Lote Econômico de Compra, permite calcular uma quantidade de pedido que busca equilibrar os custos relacionados a pedidos e manutenção de estoque.

A aplicação utiliza como parâmetros:

Demanda anual (D)

Custo de pedido (S)

Custo unitário (C)

Taxa de carregamento/manutenção (H)

Lead Time

Nível de serviço desejado

O sistema apresenta como resultados:

Lote Econômico (EOQ)

Estoque de Segurança

Ponto de Pedido (ROP)

Custo Mínimo Total

Também é disponibilizada uma curva para análise do custo total em função do tamanho do lote. 
N
Neemi4s

Fórmula clássica do EOQ
       _________
EOQ = √(2DS / H)

Onde:

D = demanda anual

S = custo por pedido

H = custo anual de manutenção por unidade

🚨 Ponto de Pedido — ROP
O Reorder Point (ROP) representa o nível de estoque utilizado como gatilho para iniciar uma reposição.

A aplicação utiliza o conceito de:

ROP = Demanda durante o Lead Time + Estoque de Segurança

Isso permite identificar produtos que estão próximos ou abaixo do nível necessário para uma nova compra.

Os itens que atingem esse gatilho são destacados no módulo de Sugestão de Pedidos de Compras. 
N
Neemi4s

🛡️ Estoque de Segurança
O estoque de segurança funciona como uma proteção contra incertezas relacionadas principalmente à demanda e ao tempo de reposição.

O OptiStock considera o nível de serviço desejado e o desvio padrão da demanda como parâmetros para auxiliar nessa análise.

Isso permite trabalhar com diferentes níveis de proteção de estoque conforme a estratégia operacional adotada.

📈 Curva ABC — Pareto
O módulo de Classificação ABC organiza os produtos de acordo com seu impacto financeiro acumulado.

A análise considera:

Valor Anual Movimentado =
Demanda Anual × Custo Unitário

Os produtos são então distribuídos entre as classes:

🅰️ Classe A
Representa aproximadamente os itens responsáveis pela maior parcela do valor movimentado.

Normalmente exige:

Controle mais rigoroso

Monitoramento frequente

Contagens cíclicas

Maior atenção às políticas de reposição

🅱️ Classe B
Representa uma faixa intermediária de impacto financeiro.

Pode receber:

Monitoramento periódico

Revisões regulares

Políticas de controle intermediárias

🅲️ Classe C
Representa produtos de menor impacto financeiro individual, normalmente associados a uma quantidade maior de SKUs.

A aplicação também apresenta uma Curva de Pareto, mostrando o percentual acumulado do valor do inventário. 
N
Neemi4s

🛒 Sugestão de Pedidos de Compra
O módulo de MRP Lite identifica produtos cujo estoque atual está igual ou abaixo do ponto de pedido.

Para esses itens, o sistema apresenta informações como:

Informação	Utilidade
SKU / Produto	Identificação do item
Estoque Atual	Situação atual do inventário
ROP	Gatilho de reposição
EOQ	Lote sugerido
Custo Unitário	Valor por unidade
Custo Total	Valor estimado do lote

Isso cria uma ponte entre a análise do estoque e a tomada de decisão de compra. 
N
Neemi4s

🔄 Fluxo de Utilização
┌─────────────────────┐
│     Cadastro SKU    │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Dados de Demanda    │
│ e Custos            │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Cálculos EOQ / ROP  │
│ + Estoque Segurança  │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Classificação ABC   │
│ / Curva de Pareto   │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Identificação dos   │
│ SKUs críticos       │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Sugestão de Compra  │
│       MRP Lite      │
└─────────────────────┘

🖥️ Interface
O sistema foi estruturado em módulos para facilitar a navegação entre diferentes perspectivas da gestão de estoque:

OptiStock
│
├── 📊 Painel Executivo
│
├── 📦 Gestão de SKUs
│
├── 📐 Simulador EOQ & ROP
│
├── 📈 Curva ABC / Pareto
│
└── 🛒 Ordens de Compra

💾 Exportação de Dados
A aplicação disponibiliza funcionalidade para exportação dos dados em CSV, facilitando a utilização das informações em planilhas, ferramentas de BI ou outros sistemas de análise. 
N
Neemi4s

🧮 Principais Conceitos
Conceito	Aplicação no sistema
EOQ	Determinação do lote econômico de compra
ROP	Definição do gatilho de reposição
Estoque de Segurança	Proteção contra variabilidade
ABC	Priorização dos SKUs por impacto financeiro
Pareto	Visualização da concentração de valor
Lead Time	Consideração do tempo de reposição
Nível de Serviço	Definição do grau de proteção desejado
MRP Lite	Apoio à geração de pedidos de compra

🌐 Demonstração
A aplicação está disponível publicamente através do GitHub Pages:

👉 Acessar o OptiStock
🏗️ Estrutura Conceitual
O projeto foi pensado seguindo uma arquitetura funcional baseada em três camadas principais:

                    ┌───────────────────┐
                    │      Usuário      │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │    Dashboard      │
                    │     Executivo     │
                    └─────────┬─────────┘
                              │
             ┌────────────────┼────────────────┐
             ▼                ▼                ▼
       ┌───────────┐    ┌───────────┐    ┌───────────┐
       │    EOQ    │    │    ROP    │    │    ABC    │
       └─────┬─────┘    └─────┬─────┘    └─────┬─────┘
             │                │                │
             └────────────────┼────────────────┘
                              ▼
                    ┌───────────────────┐
                    │  Análise de SKUs  │
                    └─────────┬─────────┘
                              ▼
                    ┌───────────────────┐
                    │ Sugestão de       │
                    │ Compras / MRP     │
                    └───────────────────┘

🎓 Aplicações
O OptiStock pode ser utilizado como ferramenta de apoio em contextos como:

Gestão de estoques

Planejamento de materiais

Gestão de compras

Logística

Engenharia de Produção

Supply Chain

Planejamento e Controle da Produção

Estudos acadêmicos

Simulações de políticas de estoque

⚠️ Observação
Os resultados gerados pelo sistema são dependentes da qualidade dos dados fornecidos, incluindo demanda, custos, lead time, estoque disponível e parâmetros de serviço.

Os cálculos devem ser interpretados dentro do contexto operacional de cada empresa e não substituem análises específicas de políticas de estoque, fornecedores, restrições de capacidade ou características particulares da cadeia de suprimentos.

🚀 Roadmap
Possíveis evoluções para versões futuras:

 Persistência de dados em banco de dados

 Autenticação e gerenciamento de usuários

 Histórico de movimentações

 Integração com ERP

 Importação de SKUs via CSV

 Relatórios em PDF

 Dashboard com filtros avançados

 Histórico de ordens de compra

 Alertas automáticos de reposição

 Previsão de demanda

 Integração com APIs externas

 Controle de múltiplos estoques e centros de distribuição

📌 Status do Projeto
OptiStock v2.5 Pro

O projeto encontra-se disponível para utilização através do GitHub Pages.

🚀 Transformando dados de estoque em decisões mais estruturadas de reposição e compras.

👨‍💻 Autor
Desenvolvido por neemi4s.

🌐 Projeto:
https://neemi4s.github.io/Sistema-de-Otimiza-o-de-Estoque/

📄 Licença
Este projeto está disponibilizado sob a licença definida no repositório.

Consulte o arquivo LICENSE para obter os termos completos de utilização.

Esse README evita inventar informações sobre frameworks, linguagens ou arquitetura interna que não consegui confirmar pela página publicada. A descrição das funcionalidades foi baseada diretamente na aplicação disponível. 
N
Neemi4s

Se você me mandar também o link do repositório GitHub, consigo fazer uma versão ainda mais profissional, incluindo stack tecnológica real, estrutura de pastas, instalação, execução local, arquitetura, screenshots, badges corretos, exemplos de uso e seção de contribuição.
