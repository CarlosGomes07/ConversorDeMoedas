# Alura Challenge | Oracle One | ConversorDeMoedas

Este repositório apresenta o desafio do Conversor de Moedas. O projeto visa construir uma ferramenta interativa via console, utilizando APIs para obter taxas de câmbio em tempo real e realizar conversões entre diferentes moedas.  Ao longo do desafio, os participantes serão guiados através dos requisitos, configuração do ambiente, integração com a API Extended Rate e quebra do projeto em tarefas gerenciáveis no Trello. O objetivo final é criar um programa que ofereça no mínimo seis opções de conversão de moedas, interaja com o usuário, obtenha as taxas de câmbio dinamicamente e forneça o valor final convertido. A documentação detalhada no repositório orienta os participantes em cada etapa do processo, desde a configuração inicial até a conclusão do desafio. A colaboração e a comunicação são incentivadas, com suporte disponível no Discord para esclarecimento de dúvidas. Este desafio não apenas fortalece as habilidades técnicas em Java e integração com APIs, mas também promove a prática autônoma e a resolução de problemas, habilidades essenciais para o desenvolvimento de software.

<a href="https://docs.oracle.com/en/java/javase/20/"><img height= "35" src= "https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white"></a>
href="https://docs.oracle.com/en/java/javase/20/"><img height= "35" src= "https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white"

## <a name="configuracao"> Configuração do Ambiente Java </a>
Para o Desafio do Conversor de Moedas, configurei o ambiente de desenvolvimento Java. Garanti a presença do Java JDK, versão 17 ou superior, a instalação da biblioteca Gson, utilização do Postman para testes de APIs e o VS Code como minha IDE opcional.

Foi crucial entender a API de taxas de câmbio, revisar sua documentação e obter a chave necessária para acesso aos dados. Segui as instruções da API para preparar as solicitações e obter informações atualizadas.

Essas etapas foram essenciais para o sucesso do projeto, proporcionando um ambiente de trabalho adequado e conhecimento sobre como acessar e manipular os dados da API.

<p align="right">
  <a href="#topo" style="text-decoration: none; background-color: #007bff; color: white; padding: 10px 20px; border-radius: 5px;">Voltar ao Topo</a>
</p>

## <a name="integração-de-apis">  Integração de APIs </a>

A construção do cliente para solicitações à API de taxas de câmbio foi realizada utilizando a classe HttpClient em Java fornecida pelo site da API. Esta classe simplifica a conexão e a obtenção de respostas, fornecendo uma base sólida para operações HTTP estruturadas e versáteis. Explorar o HttpClient otimizou o processo de solicitação de dados.

Além disso, a construção da requisição com a classe HttpRequest permitiu configurar e personalizar as solicitações de acordo com as necessidades específicas do projeto.

A interface HttpResponse foi fundamental para gerenciar as respostas da API, permitindo acesso e análise de diferentes elementos, como códigos de status, cabeçalhos e corpo da resposta, geralmente em formato JSON.

> [!NOTE]
> Classes: [Conversor](cambio-moeda/src/Conversor.java)
>     Esta classe é responsável por realizar a conversão de moedas. Ela faz uma solicitação HTTP para a API do ExchangeRate e usa a resposta para calcular o valor convertido.
> Métodos:  converterMoeda(String moedaOrigem, String moedaDestino, Scanner scanner): Este método recebe a moeda de origem, a moeda de destino e um objeto Scanner como parâmetros. Ele faz uma solicitação HTTP para a API do ExchangeRate, obtém a taxa de câmbio mais recente e calcula o valor convertido.

Essas práticas fortaleceram as habilidades de desenvolvimento e prepararam para desafios semelhantes em projetos futuros.

<p align="right">
  <a href="#topo" style="text-decoration: none; background-color: #007bff; color: white; padding: 10px 20px; border-radius: 5px;">Voltar ao Topo</a>
</p>

## <a name="consumo"> Consumo da API </a>

A análise de respostas em formato JSON foi realizada utilizando a biblioteca Gson em Java. A manipulação de dados JSON é fundamental, já que muitas APIs fornecem respostas nesse formato. Utilizei ferramentas como o Postman para compreender a estrutura dos dados retornados pela API.

> [!NOTE]
> Classes: [DigitarMoeda](cambio-moeda/src/DigitarMoeda.java)
>     Esta classe é responsável por solicitar ao usuário que insira a moeda de origem e a moeda de destino que deseja converter.
> Métodos:  digitar(Scanner scanner): Este método recebe um objeto Scanner como parâmetro. Ele solicita ao usuário que insira a moeda de origem e a moeda de destino e, em seguida, chama o método converterMoeda da classe Conversor para realizar a conversão.

## <a name="analise"> Análise da Resposta JSON </a>

A filtragem de moedas foi realizada explorando a estrutura JSON das respostas da API. A seleção das moedas desejadas foi feita através de atributos como "Currency Code", personalizando o conjunto de moedas para tornar a aplicação mais relevante e útil para os usuários.

## <a name="filtro"> Filtro de Moedas </a>

Na fase de conversão de valores entre moedas, criei métodos e funções específicas para realizar os cálculos. Isso tornou o código mais organizado e compreensível, representando o ponto culminante do projeto.

## <a name="exibicao"> Exibição de Resultados aos Usuários </a>

Interagir com o usuário foi uma parte emocionante do desafio. Implementei uma interface de texto no console, permitindo ao usuário escolher entre várias opções de conversão de moedas. A realização de testes abrangentes foi crucial para garantir o funcionamento correto do programa.

> [!NOTE]
> Classes: [Menu](cambio-moeda/src/Menu.java)
>   Esta classe exibe um menu para o usuário e lida com a entrada do usuário. Dependendo da escolha do usuário, ele chamará a classe Conversor para converter entre moedas predefinidas ou a classe DigitarMoeda para permitir que o usuário insira suas próprias moedas.
> Métodos:  exibir(): Este método exibe um menu para o usuário e lida com a entrada do usuário. Ele chama o método converterMoeda da classe Conversor ou o método digitar da classe DigitarMoeda, dependendo da escolha do usuário.

<p align="right">
  <a href="#topo" style="text-decoration: none; background-color: #007bff; color: white; padding: 10px 20px; border-radius: 5px;">Voltar ao Topo</a>
</p>

## <a name="badge-certificados"> Badge e Certificado </a>