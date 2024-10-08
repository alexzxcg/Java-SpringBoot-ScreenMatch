# Java Spring ScreenMatch

# Objetivo do Projeto: Streaming de Filmes e Séries
> Este projeto está sendo desenvolvido durante o curso oferecido pela Alura sobre Java, que aborda lambdas, streams e o framework Spring.
> Este projeto visa desenvolver uma aplicação back-end para streaming de filmes e séries, utilizando Java com o framework Spring Boot. A aplicação será projetada sem a camada Web, focando exclusivamente na lógica de servidor.

# Características do Projeto:
- Integração com OMDb API: A aplicação fará requisições à [API OMDb](https://www.omdbapi.com/) para obter informações sobre filmes e séries, processando e manipulando esses dados para fornecer uma experiência robusta de streaming.
- Spring Boot em Ação: O principal objetivo é aprofundar o conhecimento sobre os recursos e funcionalidades do Spring Boot, explorando sua capacidade de lidar com operações de back-end de forma eficiente e escalável.
# Objetivos de Aprendizado:
- Aprimoramento em Spring Boot: Ganhar experiência prática com o framework Spring Boot e suas funcionalidades avançadas, sem a camada Web.
- Manipulação de APIs: Desenvolver habilidades em integrar e trabalhar com APIs externas para enriquecimento dos dados da aplicação.
# O Que Esperar:
- Atualizações Regulares: Acompanhe o progresso do projeto e as etapas concluídas através das atualizações diárias.
- Desafios e Soluções: Explore os desafios enfrentados e as soluções implementadas durante o desenvolvimento.
- Sinta-se à vontade para explorar o código e contribuir com sugestões ou feedback!

# O que foi feito até agora?
- Hoje, dia 12 de setembro de 2024, além da criação do projeto, foi criado o pacote service, que contém a classe ConsumoApi. O objetivo desta classe é receber uma URL passada como parâmetro para o método, construí-la e, assim, obter a resposta da requisição para uma API, armazenando-a para uso posterior. Também foi criado o pacote model, que contém a classe DadosSerie, do tipo record. O objetivo dessa classe é construir objetos com base nos dados resgatados pela requisição da API. Por ser uma classe do tipo record, os objetos criados serão imutáveis.
- No dia 13 de setembro de 2024, foram criados os services responsáveis pelo tratamento dos dados recebidos pela API. Para isso, foi definida uma interface IConverteDados, que contém um método genérico utilizando Generics. A implementação desse método, que usa a biblioteca Jackson      para converter os dados JSON fornecidos pela API para o objeto Java, foi realizada na classe ConverteDados. Essa abordagem foi adotada para garantir que o projeto siga boas práticas e padrões de projeto.

  Foram realizados testes para verificar o comportamento das classes e a conversão dos dados conforme especificado na classe DadosSerie do model. Além disso, foram criadas as classes DadosTemporada e DadosEpisodio dentro do model, que definem quais dados serão utilizados    e tratados para a criação dos objetos.

  Na classe main, foram implementadas e instanciadas os objetos recebidos pela API, incluindo a determinação do número de temporadas da série fornecida e a listagem dos episódios, com todas as suas respectivas informações.
- No dia 16 de setembro de 2024, foi realizada uma refatoração do código na classe main para torná-la mais legível e aderir às boas práticas. Foi criado um novo pacote, que contém uma classe Principal responsável por exibir o menu da aplicação. Além disso, foi implementada uma nova funcionalidade que permite ao usuário digitar o nome da série que deseja buscar, possibilitando a busca e exibição das informações sobre a série. Por fim, foi desenvolvida uma função capaz de iterar sobre as temporadas usando uma expressão lambda, retornando para cada temporada o título de seus episódios.
- No dia 17 de setembro de 2024, com o objetivo de entender melhor o uso de streams e lambdas, foram implementadas três novas funções. Essas funções têm a capacidade de buscar todos os episódios de todas as temporadas, listá-los em ordem por temporada e identificar os cinco episódios mais bem avaliados.
- No dia 18 de setembro de 2024, foram implementadas três novas funcionalidades, sendo duas voltadas para buscas. A primeira permite ao usuário filtrar episódios a partir de uma data informada, mostrando todos os episódios lançados desde essa data. A segunda funcionalidade possibilita ao usuário buscar um episódio com base em um trecho do título, informando em qual temporada o episódio se encontra.

  Além disso, foi criada uma função map com uma stream que calcula a média das avaliações por temporada e a exibe. Também foi explorado o uso da função peek para depuração de streams, permitindo observar seu comportamento durante a execução.
- No dia 19 de setembro de 2024, exploramos o uso da biblioteca "DoubleSummaryStatistics" para implementar uma nova função em stream que calcula e exibe a média total das avaliações dos episódios, considerando apenas aqueles com registro de avaliações. A função também mostra o episódio mais bem avaliado, o menor avaliado e o total de episódios utilizados para calcular a média.

- Após a conclusão dessa aplicação, um desafio foi proposto, cujos detalhes podem ser encontrados em outro repositório.

# Desafio TabelaFipe
- [Link](https://github.com/alexzxcg/Desafio-TabelaFipe/tree/main)
  
# Evoluindo Aplicação
> Nesta etapa do projeto, o foco será aprimorar a aplicação com a integração de um banco de dados, utilizando o Spring Data JPA para gerenciar e acessar os dados de forma eficiente e estruturada.
> [Link](https://github.com/alexzxcg/Java-ScreenMatch-Com-JPA)
