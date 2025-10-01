RESUMO DO PROJETO
Restaurantes frequentemente enfrentam dificuldades na gestão de cardápios, mantendo pratos que não são rentáveis ou pouco procurados. Essa falta de controle impacta negativamente os lucros, aumenta o desperdício de ingredientes e reduz a competitividade no mercado. O sistema PagZap foi desenvolvido como uma solução inteligente para apoiar restaurantes na gestão de pedidos e pagamentos digitais, e agora foi expandido para incluir um Otimizador de Cardápios baseado em análise de dados. Essa evolução permite que os gestores tomem decisões estratégicas sobre quais pratos devem ser promovidos, ajustados ou removidos, resultando em maior rentabilidade e eficiência operacional.

DEFINIÇÂO DO PROBLEMA
A gestão de cardápios em restaurantes é frequentemente realizada de forma empírica, baseada apenas na experiência ou intuição dos gestores. Essa abordagem pode gerar consequências negativas como manutenção de pratos pouco vendidos, definição inadequada de preços e desperdício de insumos. Segundo Kotler & Keller (2012), decisões estratégicas em negócios de serviços devem ser embasadas em dados confiáveis para garantir competitividade e sustentabilidade.

De acordo com um levantamento do SEBRAE (2023), cerca de 34% dos restaurantes encerram suas atividades em até dois anos, sendo o mau controle de custos e a má gestão dos insumos fatores determinantes para esse cenário. Nesse contexto, soluções digitais que apoiem a análise de rentabilidade dos pratos tornam-se fundamentais.

Projetos correlatos incluem sistemas de PDV (Ponto de Venda) que registram pedidos e estoques, mas em sua maioria não oferecem relatórios inteligentes de otimização de cardápio. O diferencial do PagZap está na integração entre pedidos digitais via QR Code, pagamento online com API do Mercado Pago e o novo módulo de análise inteligente do cardápio, que transforma dados de vendas em recomendações práticas.

OBJETIVOS
Objetivo Geral:

Desenvolver uma solução web integrada que permita a restaurantes otimizar seus cardápios a partir da análise de dados de vendas e rentabilidade dos pratos, aliando gestão de pedidos e pagamentos digitais.

Objetivos Específicos:

Implementar um sistema de pedidos digitais com integração ao Mercado Pago para facilitar o processo de pagamento.

Registrar automaticamente o histórico de vendas por prato.

Desenvolver relatórios visuais interativos (tabelas e gráficos) que exibam receita, margem de lucro e percentual de participação dos pratos.

Fornecer recomendações inteligentes de otimização do cardápio (promover, revisar ou remover pratos).

Reduzir desperdícios e apoiar gestores na tomada de decisão baseada em dados.

STACK TECNOLÓGICO
O projeto foi desenvolvido com uma stack moderna e acessível, composta por:

Front-end (HTML, CSS, JavaScript): Responsável pela interface do cliente e apresentação das comandas. Foi utilizada a biblioteca Chart.js para geração de gráficos interativos, devido à sua simplicidade e ampla documentação oficial (Chart.js, 2024
).

Back-end (Node.js + Express): Estrutura responsável pelas rotas de pedidos, integração com pagamentos e análise de vendas. O Express foi escolhido por sua leveza e compatibilidade com REST APIs (Express.js, 2024
).

Banco de Dados (JSON local / MySQL em expansão): Os pedidos e vendas foram inicialmente armazenados em arquivo JSON, simulando persistência. O MySQL será considerado em versões futuras para escalabilidade, por sua robustez e ampla utilização em sistemas corporativos (MySQL, 2024
).

Integração de Pagamentos (API Mercado Pago): A API de Checkout Transparente foi utilizada em ambiente Sandbox para simular pagamentos online. Essa escolha garante praticidade e segurança, além de preparar o sistema para o uso real em produção (Mercado Pago Developers, 2024
).

DESCRIÇÂO DA SOLUÇÃO
O PagZap é uma solução inteligente que unifica gestão de comandas digitais, pagamentos online e análise de cardápio em uma única plataforma.

No processo de uso, o cliente acessa o cardápio digital via QR Code, seleciona os itens desejados e finaliza o pedido, que é enviado automaticamente à cozinha e registrado no sistema. Em seguida, o sistema gera um link de pagamento pelo Mercado Pago.
Paralelamente, cada pedido atualiza a base de dados de vendas, registrando a quantidade e receita por prato. Esses dados são processados pelo módulo Otimizador de Cardápios, que gera relatórios visuais em uma interface web dedicada.

O relatório exibe:
Tabela detalhada com quantidade vendida, receita total, margem em R$, percentual de margem e recomendação (promover, revisar, remover).

Gráfico de Barras com a receita absoluta por prato.

Gráfico de Pizza com a participação percentual de cada prato no faturamento total.

Essa abordagem oferece aos gestores uma visão clara e prática do desempenho do cardápio, permitindo decisões estratégicas embasadas em dados. Como consequência, espera-se uma redução do desperdício de insumos, maior eficiência operacional e aumento da lucratividade dos restaurantes que adotarem a solução.
