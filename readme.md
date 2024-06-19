

### case tech Felipe_Reis_DDF_DATAENG_062024

# Item 1 - Sobre Storytelling e Apresentação

## Apresentação da solução

### Principal problema a ser resolvido

Na arquitetura atual o cliente faz a leitura, tratamento e armazenamento dos dados gerados na sua operação.
Para alcançar o objetivo de fornecer modelos de IA para melhorar a experiência de compra dos clientes, é necessário uma complementação desta arquitetura no sentido de
viabilizar a parte analítica do processo que vai ser essencial para o treinamento dos modelos de IA.

### Diagrama da solução com Dadosfera

Apresentamos a solução DADOSFERA com 2 cenários: 
- no primeiro cenário sugerimos a migração completa da coleta para a Dadosfera junto com a ampliação da arquitetura para atender analytics
e data apps dentro da DADOSFERA consolidado todas as etapas do processo.
- o segundo cenário considera a ampliação para analytics e data apps no ambiente dadosfera e a integração com a coleta e data lake já existentes.

[Link para o diagrama](https://app.eraser.io/workspace/jv24ayPmOmPFkkuhCnfD?origin=share)


### Oportunidades e ganhos futuros de se adotar a DADOSFERA, frente a solução atual

A solução DADOSFERA permite de fato extrair valor dos dados gerados e alcançar o objetivo de fornecer modelos de IA para as tomadas de decisão que vão melhorar a experiência dos clientes.
Existem duas principais vantagens em se adotar a DADOSFERA:

 - Single strike point - processo global de montagem dos modelos em um único ambiente integrado que pode ser operado por não especialistas.
 - One ticket, all rides - substituição do custo da arquitetura atual para a DADOSFERA com entrega da solução completa.


[Link para vídeo de apresentação](https://youtu.be/6gPQH5IskJA)


# Item 2 - Sobre a Dadosfera

## Carregamento

Pipeline de importação do dataset
![Print do pipeline](./assets//imagens/amazon_review_polarity.png)


## Análise descritiva

Na busca por possíveis anomalias, foram encontradas instancias que tinham a feature principal do dataset, review, nula. Para mitigar os efeitos indesejados, estas instâncias foram filtradas do dataset utilizando um pipeline jupyter no modulo Integliência.



# Item 3 - Sobre GenAI e LLMs

Dentro do projecto FELIPE_REIS_DDF_ENG_DADOS_062024 foi criado um pipeline para recuperação dos dados, tratamento e classificação.

![Print do pipeline modulo inteligencia](./assets//imagens/projeto_modulo_inteligencia.png)

Neste pipeline a idéia foi enriquecer o dataset com uma nova feature por meio de LLM.

A princípio o dataset contém as features:
 - Polaridade : binária indicando se o cliente deu uma review positiva ou negativa
 - Título : campo texto com o heading da review
 - Review : campo texto com a review

Nesse cenário seria interessante entender sobre qual produto ou categoria de produto a revisão está relacionada. Assim seria possível entender qual tipo de produto está sendo melhor aceito pelos clientes e, a partir desta informação, tomar medidas para melhorar as vendas dos produtos que estão sendo desqualificados.

Pensando dessa forma, foi utilizado LLM por meio da importação da biblioteca da openai para criar a feature "Categoria" dentro do dataset. 
![Print do pipeline](./assets//imagens/definicao_funcao_productname.pngcateg)

Exemplo da feature Category dentro do dataset
![Print da nova feature](./assets//imagens/category.png)



# Item 4 - Sobre SQL e Python

# Item 5 - Sobre Data Apps
