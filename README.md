# Projecto-de-Analise-exploratoria-sobre-a-Loggi
 Neste projeto apresento uma analise profunda sobre possiveis problemas que afetam o dia-dia da empresa Loggi, que utiliza tecnologia para conectar empresas e clientes a entregadores independentes...
 
Objetivo da analise:
Visualizar e mapear as entregas de forma analitica, para facilitar a compreensão dos problemas e nos ajudar de forma visual na eficiencia de tomada de decisões no dia a dia das entregas...

1 - importei os Pacotes e bibliotecas que serão usadas e que vai ajudar a explorar a nossa base de dados.

2 - Explorei os dados, onde foi possivel realizar o meu primeiro contacto com a base dados e baixar ele no meu notebook para realização da exploração de dados.

3 - Transformei os dados em um Dataframe para melhor observação dos dados.

4 - Observei que no dataframe a coluna ORIGIN contém dados NESTED ou aninhados na estrutura do json. Normalizei a coluna com uma operação conhecida como FLATTEN ou achatamento que transforma cada chave do Json em uma nova coluna.

5 - Tambem observei que na coluna "deliveries" apresenta dados NESTED na estrutura do JSON. Para organizá-los, apliquei a operação EXPLODE para transformar cada elemento da lista em uma linha. Em seguida, utilizei novamente a operação "flatten" e renomeiei para referenciar o resultado obtido da coluna.

6 - Na Exploração do schema, depois de obter os dados tratados, aprofundei o conhecimento na estrutura resultante, visualizei o dataframe, peguei as informações, consultei se existia colunas ou dados vazios, explorei o tipo de dados presentes, selecionei os atributos categoricos e numericos.

7 - Fiz a manipulação, apliquei a geocodificação reversa nas coordenadas das regiões para extrair informações das cidades e bairros, ultilizei o pacote geopy para fazer a operação reversa e enriquecer o DataFrame principal.

8 - Fiz a Verificação e Controle de qualidade, verifiquei os dados faltantes onde Identificamos dados incorretos em nosso DataFrame, tanto o bairro quanto a cidade apresentam o valor "Brasília". Felizmente, para o nosso caso, a percentagem de erro não deverá impactou significativamente nos resultados.

9 - Na visualização de dados, fiz o download dos dados do mapa do Distrito Federal do site oficial do IBGE através do link para criar o DataFrame mapa onde percebi que as alocações das entregas aos seus respectivos hubs estão corretas. No entanto, vale ressaltar que os hubs das regiões 0 e 2 realizam entregas em locais distantes do centro e entre si, o que pode resultar em tempos de entrega e custos mais elevados.


Conclusão:
1. As alocações das entregas dos hubs estão confirmadas e felizmente corretas.

2. Segundo a analise percebemos que os hubs das regiões 0 e 2 realizam entregas em locais distantes do centro, o que pode resultar em tempos de entrega e custos mais elevados.
3.As entregas estão concentradas nos hubs das regiões 1 e 2, em detrimento do hub da região 0. Recomendamos fortemente a realocação estratégica de veículos para as regiões com maior volume de tráfego. Isso reduzirá custos e melhorará os tempos de entrega.

3. identificamos que o tamanho das entregas está predominantemente concentrado na faixa de 1 a 8. O fato de que o tamanho das entregas está predominantemente concentrado na faixa de 1 a 8 é crucial para o planejamento de logística e a gestão eficaz dos recursos disponíveis.
