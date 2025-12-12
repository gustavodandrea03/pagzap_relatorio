# PagZap: Solução Inteligente para Restaurantes

_Gustavo D´andrea_

Este artigo tem como objetivo ilustrar a documentação de um projeto final na unidade curricular Projeto de Desenvolvimento II dos cursos Análise e Desenvolvimento de Sistemas, Sistemas para Internet e Ciência de Dados e Inteligência Analítica do Centro Universitário Senac-RS.

## Resumo do Projeto

Restaurantes frequentemente enfrentam dificuldades na gestão de cardápios, mantendo pratos que não são rentáveis ou pouco procurados. Essa falta de controle impacta negativamente os lucros, aumenta o desperdício de ingredientes e reduz a competitividade no mercado. O sistema PagZap foi desenvolvido como uma solução integrada para gestão de pedidos e pagamentos digitais, e foi expandido para incluir o módulo Otimizador de Cardápios (Menu Engineering). Essa evolução permite que os gestores tomem decisões estratégicas sobre quais pratos devem ser promovidos, ajustados ou removidos (Estrela, Arado, Quebra-cabeça, Cão), resultando em maior rentabilidade e eficiência operacional.

## Definição do Problema

A gestão de cardápios em restaurantes é frequentemente realizada de forma empírica, baseada apenas na experiência ou intuição dos gestores. Essa abordagem pode gerar consequências negativas como manutenção de pratos pouco vendidos, definição inadequada de preços e desperdício de insumos. Segundo Kotler & Keller (2012), decisões estratégicas em negócios de serviços devem ser embasadas em dados confiáveis para garantir competitividade e sustentabilidade.

De acordo com um levantamento do SEBRAE (2023), cerca de 34% dos restaurantes encerram suas atividades em até dois anos, sendo o mau controle de custos e a má gestão dos insumos fatores determinantes para esse cenário. Nesse contexto, soluções digitais que apoiem a análise de rentabilidade dos pratos tornam-se fundamentais.

Projetos correlatos incluem sistemas de PDV (Ponto de Venda) que registram pedidos e estoques, mas em sua maioria não oferecem relatórios inteligentes de otimização de cardápio. O diferencial do PagZap está na integração entre pedidos digitais via QR Code, a simulação de pagamento PIX instantâneo via Mercado Pago e o novo módulo de Engenharia de Cardápio, que classifica os pratos em categorias estratégicas (Estrela, Arado, Quebra-cabeça e Cão) para transformar dados de vendas em recomendações práticas.


## Objetivos

Objetivos
Objetivo Geral: Desenvolver uma solução web integrada que permita a restaurantes otimizar seus cardápios a partir da análise de dados de vendas e rentabilidade dos pratos, utilizando a metodologia de Engenharia de Cardápio, aliando gestão de pedidos e pagamentos digitais.

Objetivos Específicos:

Implementar um sistema de pedidos digitais com simulação de pagamento PIX (Checkout Transparente) para facilitar o processo de pagamento.

Registrar automaticamente o histórico de vendas por prato.

Desenvolver relatórios visuais interativos (tabelas e gráficos) que exibam receita, margem de lucro e percentual de participação dos pratos.

Fornecer recomendações inteligentes de otimização do cardápio, classificando pratos em categorias estratégicas de Engenharia de Cardápio (Estrela, Arado, Quebra-cabeça, Cão).

Melhorar a usabilidade das interfaces de Gestão e Cliente, proporcionando feedback visual rápido e fluxo de trabalho otimizado (Ex: Adicionar múltiplos itens ao pedido com um clique, entre outros).

Reduzir desperdícios e apoiar gestores na tomada de decisão baseada em dados.


## Stack Tecnológico

O projeto foi desenvolvido com uma stack moderna e acessível, composta por:

Front-end (HTML, CSS, JavaScript): Responsável pela interface do cliente e gestão. Foi utilizada a biblioteca Chart.js para geração de gráficos interativos, devido à sua simplicidade e ampla documentação oficial (Chart.js, 2024).

Back-end (Node.js + Express): Estrutura responsável pelas rotas de pedidos, integração com pagamentos e análise de vendas. O Express foi escolhido por sua leveza e compatibilidade com REST APIs (Express.js, 2024).

Banco de Dados (JSON local): Os pedidos e vendas foram armazenados inicialmente em arquivo JSON, simulando persistência, permaneceu até o fim do desenvolvimento pela simplicidade e escolha pessoal.

Integração de Pagamentos (API Mercado Pago): A API de Checkout Transparente foi utilizada em ambiente Sandbox para simular pagamentos online e a geração do QR Code PIX. Essa escolha garante praticidade e segurança, além de preparar o sistema para o uso real em produção (Mercado Pago Developers, 2024).

## Descrição da Solução

O PagZap é uma solução inteligente que unifica gestão de comandas digitais, pagamentos online e análise de cardápio em uma única plataforma, dividida em três interfaces principais:

Interface do Cliente (QR Code): Acessível por link direto (index.html?mesa=X), apresenta o cardápio com um visual moderno e responsivo. Permite ao cliente adicionar múltiplos itens ao pedido com um único clique (com feedback visual de seleção), visualizar o resumo do pedido e gerar o pagamento PIX. O fluxo de pagamento é simplificado para simular uma transação real, focando no QR Code.

Painel da Cozinha: Exibe os pedidos recebidos em tempo real para controle de produção (não detalhado aqui).

Interface do Gestor (gestor.html): Permite o Cadastro, Edição e Remoção (CRUD) dos itens do cardápio. O painel também exibe estatísticas resumidas (Total de Pratos, Categorias e Vendas) e o link para o relatório analítico.

O coração da solução é o Módulo de Engenharia de Cardápio, que processa as vendas registradas e classifica dinamicamente cada prato em uma das quatro categorias estratégicas (Estrela, Arado, Quebra-cabeça, Cão), baseando-se na Popularidade Média e na Margem de Lucro Média do cardápio. O resultado é apresentado de forma visual e tabulada no relatório, oferecendo ações diretas (promover, revisar, remover) aos gestores.


## Arquitetura

O projeto está organizado em camadas simples, refletindo uma arquitetura Cliente-Servidor:

Camada de Apresentação (Front-end): Interfaces web (HTML/CSS/JS) para o Cliente e Gestor.

Camada de Aplicação (Back-end): Servidor em Node.js com Express, responsável pela lógica de negócios, geração de relatórios de Menu Engineering e integração com a API Mercado Pago.

Camada de Dados: Persistência em db.json (simulação de banco local).

Serviços Externos: Integração com a API Mercado Pago (pagamentos sandbox).


## Artefatos
Elevator Pitch - É, Não É, Faz, Não Faz - Canvas MVP: https://github.com/gustavodandrea03/pagzap_relatorio/blob/main/modelagem%20de%20negocio.pdf
...
Definição do Projeto: https://github.com/gustavodandrea03/pagzap_relatorio/blob/main/Gustavo%20-%202025-2%20-%20PD2%20-%20Entrega%201%20-%20Definição%20do%20Projeto.pdf
...
Diagrama de Sequência: https://github.com/gustavodandrea03/pagzap_relatorio/blob/main/diagrama_de_sequencia.png
...
Benchmarking: https://github.com/gustavodandrea03/pagzap_relatorio/blob/main/Benchmarking_PagZap.xlsx



## Validação

A validação foi dividida em duas frentes:

Validação Funcional e Técnica: Testes de ponta a ponta (Estratégia de Validação por Simulação, já prevista).

Validação de Usabilidade e Conformidade (Substituindo Pesquisa Real): Esta etapa comprovou que a solução está alinhada com as necessidades do público-alvo, utilizando:

Avaliação Heurística Simplificada: Feedbacks qualitativos coletados de colegas e mentores, focando na praticidade das interfaces (Gestor e Cliente) e no fluxo de trabalho.

Validação de Clareda de Relatórios (Conformidade com a Metodologia): O relatório de Engenharia de Cardápio foi validado por sua aderência total à Matriz de Engenharia de Cardápio padrão da indústria (Estrela, Arado, Quebra-cabeça, Cão), comprovando que as recomendações são as esperadas e que o relatório é claro o suficiente para a tomada de decisão gerencial, conforme o padrão de referência (Kasavana & Smith, década de 80).

### Estratégia
Simulação de pedidos em diferentes combinações, verificando se o relatório gera recomendações corretas.

### Consolidação dos Dados Coletados
Os resultados da validação funcional demonstraram que o sistema gera relatórios com clareza e potencial de apoio na tomada de decisão. A matriz de Menu Engineering, baseada em dados reais simulados, classifica os pratos em quatro quadrantes.

A clássica nomenclatura da indústria (Estrela, Arado, Quebra-cabeça, Cão) é autoexplicativa e dispensa treinamento complexo, pois cada classificação implica em uma ação gerencial imediata e clara (promover, revisar, remover ou reajustar preço).

O design visual dos relatórios (uso de gráficos do Chart.js) e a interface limpa do Gestor foram validados por feedbacks qualitativos (de pares e mentores) como práticos e intuitivos, mitigando a necessidade de grandes testes de usabilidade com usuários finais nesta fase.

### Limitações do Projeto e Perspectivas Futuras

Limitações:

Ausência de validação empírica (Testes AB): O potencial de aumento de lucratividade não pôde ser medido em um cenário real com usuários finais e pedidos reais.

...

Perspectivas Futuras:

- Migrar para MySQL para escalabilidade.

Implementação de Testes Controlados em Campo (A/B Testing): Após a migração para MySQL, o sistema poderá ser implantado em um parceiro real para medir o impacto da Engenharia de Cardápio nas vendas e na margem de lucro, comprovando os resultados.

## Conclusões
Conclusões
O PagZap com o módulo Otimizador de Cardápios demonstrou atender aos objetivos definidos:

Permitiu gerenciar pedidos digitais, pagamentos via API e cadastro de pratos com usabilidade aprimorada.

Registrou e analisou vendas automaticamente, aplicando a metodologia de Engenharia de Cardápio.

Gerou relatórios visuais que apoiam decisões estratégicas sobre a rentabilidade do cardápio.

Retomando o problema inicial (falta de gestão baseada em dados), o sistema mostrou-se capaz de fornecer informações concretas que, quando seguidas, reduzem desperdício, aumentam a rentabilidade e melhoram a competitividade de restaurantes.


## Referências Bibliográficas

Dados do SEBRAE sobre o fechamento de restaurantes
Segundo a Associação Brasileira de Bares e Restaurantes (Abrasel), de cada 100 estabelecimentos abertos nesse setor, 35 fecham em até dois anos. 
Sebrae
https://sebrae.com.br/sites/PortalSebrae/artigos/os-ingredientes-para-abrir-um-restaurante-sem-prazo-de-validade%2C0667db5cc9d41810VgnVCM100000d701210aRCRD?utm_source=chatgpt.com

📚 Referência teórica de Kotler & Keller (2012)

O livro "Administração de Marketing" de Philip Kotler e Kevin Lane Keller (14ª edição, 2012) aborda a importância de decisões estratégicas baseadas em dados confiáveis para garantir competitividade e sustentabilidade em negócios de serviços. 
Biblioteca UnISCED
