# Documentando um Projeto Final de ADS/SPI/CD

_Gustavo D´andrea_

Este artigo tem como objetivo ilustrar a documentação de um projeto final na unidade curricular Projeto de Desenvolvimento II dos cursos Análise e Desenvolvimento de Sistemas, Sistemas para Internet e Ciência de Dados e Inteligência Analítica do Centro Universitário Senac-RS.

## Resumo do Projeto

Restaurantes frequentemente enfrentam dificuldades na gestão de cardápios, mantendo pratos que não são rentáveis ou pouco procurados. Essa falta de controle impacta negativamente os lucros, aumenta o desperdício de ingredientes e reduz a competitividade no mercado. O sistema PagZap foi desenvolvido como uma solução inteligente para apoiar restaurantes na gestão de pedidos e pagamentos digitais, e agora foi expandido para incluir um Otimizador de Cardápios baseado em análise de dados. Essa evolução permite que os gestores tomem decisões estratégicas sobre quais pratos devem ser promovidos, ajustados ou removidos, resultando em maior rentabilidade e eficiência operacional.


## Definição do Problema

A gestão de cardápios em restaurantes é frequentemente realizada de forma empírica, baseada apenas na experiência ou intuição dos gestores. Essa abordagem pode gerar consequências negativas como manutenção de pratos pouco vendidos, definição inadequada de preços e desperdício de insumos. Segundo Kotler & Keller (2012), decisões estratégicas em negócios de serviços devem ser embasadas em dados confiáveis para garantir competitividade e sustentabilidade.

De acordo com um levantamento do SEBRAE (2023), cerca de 34% dos restaurantes encerram suas atividades em até dois anos, sendo o mau controle de custos e a má gestão dos insumos fatores determinantes para esse cenário. Nesse contexto, soluções digitais que apoiem a análise de rentabilidade dos pratos tornam-se fundamentais.

Projetos correlatos incluem sistemas de PDV (Ponto de Venda) que registram pedidos e estoques, mas em sua maioria não oferecem relatórios inteligentes de otimização de cardápio. O diferencial do PagZap está na integração entre pedidos digitais via QR Code, pagamento online com API do Mercado Pago e o novo módulo de análise inteligente do cardápio, que transforma dados de vendas em recomendações práticas.


## Objetivos

Objetivo Geral:

Desenvolver uma solução web integrada que permita a restaurantes otimizar seus cardápios a partir da análise de dados de vendas e rentabilidade dos pratos, aliando gestão de pedidos e pagamentos digitais.

Objetivos Específicos:

Implementar um sistema de pedidos digitais com integração ao Mercado Pago para facilitar o processo de pagamento.

Registrar automaticamente o histórico de vendas por prato.

Desenvolver relatórios visuais interativos (tabelas e gráficos) que exibam receita, margem de lucro e percentual de participação dos pratos.

Fornecer recomendações inteligentes de otimização do cardápio (promover, revisar ou remover pratos).

Reduzir desperdícios e apoiar gestores na tomada de decisão baseada em dados.


## Stack Tecnológico

O projeto foi desenvolvido com uma stack moderna e acessível, composta por:

Front-end (HTML, CSS, JavaScript): Responsável pela interface do cliente e apresentação das comandas. Foi utilizada a biblioteca Chart.js para geração de gráficos interativos, devido à sua simplicidade e ampla documentação oficial (Chart.js, 2024
).

Back-end (Node.js + Express): Estrutura responsável pelas rotas de pedidos, integração com pagamentos e análise de vendas. O Express foi escolhido por sua leveza e compatibilidade com REST APIs (Express.js, 2024
).

Banco de Dados (JSON local / MySQL em expansão): Os pedidos e vendas foram inicialmente armazenados em arquivo JSON, simulando persistência. O MySQL será considerado em versões futuras para escalabilidade, por sua robustez e ampla utilização em sistemas corporativos (MySQL, 2024
).

Integração de Pagamentos (API Mercado Pago): A API de Checkout Transparente foi utilizada em ambiente Sandbox para simular pagamentos online. Essa escolha garante praticidade e segurança, além de preparar o sistema para o uso real em produção (Mercado Pago Developers, 2024
).

## Descrição da Solução

O PagZap é uma solução inteligente que unifica gestão de comandas digitais, pagamentos online e análise de cardápio em uma única plataforma.

No processo de uso, o cliente acessa o cardápio digital via QR Code, seleciona os itens desejados e finaliza o pedido, que é enviado automaticamente à cozinha e registrado no sistema. Em seguida, o sistema gera um link de pagamento pelo Mercado Pago.
Paralelamente, cada pedido atualiza a base de dados de vendas, registrando a quantidade e receita por prato. Esses dados são processados pelo módulo Otimizador de Cardápios, que gera relatórios visuais em uma interface web dedicada.

O relatório exibe:
Tabela detalhada com quantidade vendida, receita total, margem em R$, percentual de margem e recomendação (promover, revisar, remover).

Gráfico de Barras com a receita absoluta por prato.

Gráfico de Pizza com a participação percentual de cada prato no faturamento total.

Essa abordagem oferece aos gestores uma visão clara e prática do desempenho do cardápio, permitindo decisões estratégicas embasadas em dados. Como consequência, espera-se uma redução do desperdício de insumos, maior eficiência operacional e aumento da lucratividade dos restaurantes que adotarem a solução.




///// Sem Mudanças  


## Arquitetura

Este tópico deve apontar para o repositório que contém a listagem de artefatos que foram gerados ao longo do desenvolvimento do sistema.

A figura abaixo ilustra uma visão geral de arquitetura (camadas do sistema)

![image](https://github.com/user-attachments/assets/9a0fc9b4-0aeb-4246-a863-06eefcf19758)

Exemplo de visão geral da arquitetura do sistema.

Devem ser realizados no mínimo 5 artefatos.

A seguir são apresentados exemplos de artefatos que podem ser apresentados:
* Benchmarking (tabela comparativa)
* Project Model Canvas, Business Model Canvas, MVP Canvas
* Personas
* Casos de uso, histórias do usuário, classes de teste; lista de backlog, entre outros
* Diagrama ER, XML schema, JSON schema
* Protótipos de interface, sitemaps, wireframes de baixa fidelidade, wireflows
* Listagem de componentes reutilizados e detalhamento de sua aplicação no projeto
* Documentação de processos de verificação e validação: sprint review, sprint retrospective, status report
* Registros/atas de reunião com stakeholders
* Plano de Negócios

Exemplos de repositórios:


[https://github.com/gbmachado/projetoFinal](https://github.com/gbmachado/projetoFinal)

[https://github.com/fga-eps-mds/2018.1-IncluCare](https://github.com/fga-eps-mds/2018.1-IncluCare)

## Validação
Aqui, deve-se apresentar um resumo de como será feita a validação do sistema e como ela irá implicar no desenvolvimento do projeto e no resultado final.

### Estratégia
Este tópico descreve como o aluno comprovou que os objetivos foram alcançados, utilizando mecanismos tais como: simulação, pesquisa com usuários, entrevistas, questionários, entre outros, baseado em alguma norma, por exemplo, ISO. É importante deixar claro o contexto de validação, por exemplo, se for entrevista, quantos usuários, com quais perfis, em qual momento, etc.

### Consolidação dos Dados Coletados
O aluno deve expressar os resultados, na forma de gráficos, médias, etc, trazendo uma discussão sobre a análise realizada acerca desses resultados.

## Conclusões
Descrição de resultados obtidos ou considerações acerca da satisfação dos mesmos, retomando o problema identificado, os objetivos estabelecidos e a solução implementada.

Limitações do Projeto e Perspectivas Futuras
Discutir sobre as limitações do projeto e trabalhos futuros, envolvendo o TCC em questão.

## Referências Bibliográficas
Lista de todo material bibliográfico utilizado para a realização deste documento, incluindo: livros, sites, artigos, etc.

Exemplo:

WAZLAWICK, Raul Sidnei. Metodologia de pesquisa para ciência da computação. Rio de Janeiro: Elsevier, 2009
