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
- Hoje, dia 12/09/2024, além da criação do projeto, foi criado o pacote service, que contém a classe ConsumoApi. O objetivo desta classe é receber uma URL passada como parâmetro para o método, construí-la e, assim, obter a resposta da requisição para uma API, armazenando-a para uso posterior. Também foi criado o pacote model, que contém a classe DadosSerie, do tipo record. O objetivo dessa classe é construir objetos com base nos dados resgatados pela requisição da API. Por ser uma classe do tipo record, os objetos criados serão imutáveis.
- No dia 13/09/2024, foram criados os services responsáveis pelo tratamento dos dados recebidos pela API. Para isso, foi definida uma interface IConverteDados, que contém um método genérico utilizando Generics. A implementação desse método, que usa a biblioteca Jackson      para converter os dados JSON fornecidos pela API para o objeto Java, foi realizada na classe ConverteDados. Essa abordagem foi adotada para garantir que o projeto siga boas práticas e padrões de projeto.

  Foram realizados testes para verificar o comportamento das classes e a conversão dos dados conforme especificado na classe DadosSerie do model. Além disso, foram criadas as classes DadosTemporada e DadosEpisodio dentro do model, que definem quais dados serão utilizados    e tratados para a criação dos objetos.

  Na classe main, foram implementadas e instanciadas os objetos recebidos pela API, incluindo a determinação do número de temporadas da série fornecida e a listagem dos episódios, com todas as suas respectivas informações.
- No dia 16/09/2024, foi realizada uma refatoração do código na classe main para torná-la mais legível e aderir às boas práticas. Foi criado um novo pacote, que contém uma classe Principal responsável por exibir o menu da aplicação. Além disso, foi implementada uma nova funcionalidade que permite ao usuário digitar o nome da série que deseja buscar, possibilitando a busca e exibição das informações sobre a série. Por fim, foi desenvolvida uma função capaz de iterar sobre as temporadas usando uma expressão lambda, retornando para cada temporada o título de seus episódios.
- No dia 17/09/2024, com o objetivo de entender melhor o uso de streams e lambdas, foram implementadas três novas funções. Essas funções têm a capacidade de buscar todos os episódios de todas as temporadas, listá-los em ordem por temporada e identificar os cinco episódios mais bem avaliados.
