# Java-Spring-ScreenMatch

# Sobre
Este projeto está sendo desenvolvido durante o curso oferecido pela Alura sobre Java, que aborda lambdas, streams e o framework Spring.

# Projeto
- Objetivo
> O projeto tem como propósito criar uma aplicação de streaming de filmes e séries para o back-end em Java, utilizando o framework Spring Boot sem a camada Web.
> O objetivo principal é aprofundar o conhecimento sobre os recursos do Spring Boot e suas funcionalidades.

# O que foi feito até agora?
- Hoje, dia 12/09/2024, além da criação do projeto, foi criado o pacote service, que contém a classe ConsumoApi. O objetivo desta classe é receber uma URL passada como parâmetro para o método, construí-la e, assim, obter a resposta da requisição para uma API, armazenando-a para uso posterior. Também foi criado o pacote model, que contém a classe DadosSerie, do tipo record. O objetivo dessa classe é construir objetos com base nos dados resgatados pela requisição da API. Por ser uma classe do tipo record, os objetos criados serão imutáveis.
- No dia 13/09/2024, foram criados os services responsáveis pelo tratamento dos dados recebidos pela API. Para isso, foi definida uma interface IConverteDados, que contém um método genérico utilizando Generics. A implementação desse método, que usa a biblioteca Jackson      para converter os dados JSON fornecidos pela API para o objeto Java, foi realizada na classe ConverteDados. Essa abordagem foi adotada para garantir que o projeto siga boas práticas e padrões de projeto.

  Foram realizados testes para verificar o comportamento das classes e a conversão dos dados conforme especificado na classe DadosSerie do model. Além disso, foram criadas as classes DadosTemporada e DadosEpisodio dentro do model, que definem quais dados serão utilizados    e tratados para a criação dos objetos.

  Na classe main, foram implementadas e instanciadas os objetos recebidos pela API, incluindo a determinação do número de temporadas da série fornecida e a listagem dos episódios, com todas as suas respectivas informações.
