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



## Arquitetura

Arquitetura

O projeto está organizado em camadas simples, refletindo uma arquitetura cliente-servidor:

Camada de Apresentação (Front-end): interfaces web desenvolvidas em HTML, CSS e JavaScript, acessíveis por navegadores.

Camada de Aplicação (Back-end): servidor em Node.js com Express, responsável por rotas de pedidos, integração com pagamentos e geração de relatórios.

Camada de Dados: persistência em db.json (simulação de banco local), podendo evoluir para MySQL em produção.

Serviços Externos: integração com a API Mercado Pago (pagamentos sandbox).


## Artefatos
https://github.com/gustavodandrea03/pagzap_relatorio/blob/main/modelagem%20de%20negocio.pdf
https://github.com/gustavodandrea03/pagzap_relatorio/blob/main/Gustavo%20-%202025-2%20-%20PD2%20-%20Entrega%201%20-%20Definição%20do%20Projeto.pdf


## Validação
Validação

A validação do sistema será realizada em duas etapas:

Testes funcionais: criação de pedidos, pagamentos simulados via Mercado Pago Sandbox e análise automática de vendas.

Avaliação com usuários reais: pesquisa com  gestores e funcionários de restaurantes (público-alvo), para avaliar praticidade, clareza dos relatórios e potencial de apoio na tomada de decisão.

### Estratégia
Simulação de pedidos em diferentes combinações, verificando se o relatório gera recomendações corretas.

### Consolidação dos Dados Coletados
Os resultados serão consolidados em:

Gráficos de barras e pizza (já implementados com Chart.js) para representar a distribuição de vendas e participação de pratos.

Relatórios qualitativos com observações dos usuários sobre pontos fortes e pontos a melhorar.

## Conclusões
O PagZap com o módulo Otimizador de Cardápios demonstrou atender aos objetivos definidos:

Permitiu gerenciar pedidos digitais e integrar pagamentos via API.

Registrou e analisou vendas automaticamente.

Gerou relatórios visuais que apoiam decisões estratégicas sobre o cardápio.

Retomando o problema inicial (falta de gestão baseada em dados), o sistema mostrou-se capaz de fornecer informações concretas que reduzem desperdício, aumentam a rentabilidade e melhoram a competitividade de restaurantes.

Limitações do Projeto e Perspectivas Futuras
Banco de dados ainda em JSON local, sem robustez para ambientes de alta escala.

Custos de produção dos pratos estimados de forma simplificada (percentual do preço).

Testes limitados a sandbox do Mercado Pago, sem simulação de transações reais.

Perspectivas Futuras:

Migrar para MySQL para escalabilidade.

Calcular custos de forma mais precisa, incluindo insumos detalhados.

Integrar relatórios de desempenho histórico (semanal/mensal).


## Referências Bibliográficas

Dados do SEBRAE sobre o fechamento de restaurantes
Segundo a Associação Brasileira de Bares e Restaurantes (Abrasel), de cada 100 estabelecimentos abertos nesse setor, 35 fecham em até dois anos. 
Sebrae
https://sebrae.com.br/sites/PortalSebrae/artigos/os-ingredientes-para-abrir-um-restaurante-sem-prazo-de-validade%2C0667db5cc9d41810VgnVCM100000d701210aRCRD?utm_source=chatgpt.com

📚 Referência teórica de Kotler & Keller (2012)

O livro "Administração de Marketing" de Philip Kotler e Kevin Lane Keller (14ª edição, 2012) aborda a importância de decisões estratégicas baseadas em dados confiáveis para garantir competitividade e sustentabilidade em negócios de serviços. 
Biblioteca UnISCED
