#Base de dados aeródromos_BR_final
##Base de dados do ROTAER
-1. Primeiramente é necessário baixar o pdf mais atualizado do Rotaer completo. O caminho mais fácil é pesquisar no google Rotaer completo 2025 e já aparece no início o pdf completo com a data. Ou também é possível [acessar este link]( https://aisweb.decea.mil.br/?i=aerodromos), e baixar  o rotear completo clicando no link azul completo, no final da página.
-2. Baixar esta base e salvar na pasta pdf, dentro da pasta BD_07
-3.  O código de edição deste pdf é o código 1_rotaer_v1
-4. A função deste código é extrair as informações do código OACI, RDONAV, RFFS (Categoria Contra Incêndio).
-5. A base final que é gerada com este código é a base_rotaer_final. Ela vai ser concatenada posteriormente com a base de cadastro de aeroportos.
-6.Em um segundo momento é necessário baixar os dados cadastrais dos aeroportos, [acessando o site]( https://www.gov.br/anac/pt-br/assuntos/regulados/aeroportos-e-aerodromos/lista-de-aerodromos-civis-cadastrados)

##Base de dados de cadastro dos aeródromos
-1. Primeiramente é necessário baixar as bases de aeródromos civis privados e públicos cadastrados na ANAC [acessando o site]( https://www.gov.br/anac/pt-br/assuntos/regulados/aeroportos-e-aerodromos/lista-de-aerodromos-civis-cadastrados).
-2. Salvar na pasta csv, dentro da pasta BD_07.
-3. O código de edição destas bases de dados é o 2_base_anac.
-4.Este código agrupa os aeroportos cadastrados no Brasil, e mantém na base apenas as informações importantes para o EC Data.
-4. A base final é aero_ANAC.

#Base de dados ADC – Auxílios visuais 
#Base de auxílios visuais – Cartas ADC
-A base de auxílios visuais é criada manualmente em uma planilha do excel.
-1. [Primeiramente acessar o site do Aisweb, na sessão de cartas de aeródromos]( https://aisweb.decea.mil.br/?i=cartas)
-2. Filtrar o tipo de carta para Carta ADC.
-3. Analisar as datas de efetivação das cartas, e atentar para as cartas que possuem a data de atualização posterior a data da última atualização da plataforma.
-4. Baixar apenas as cartas com atualização recente.
-5. O código 3_ADC pode ser utilizado para descompactar as pastas e extrair os pdfs (as cartas vem com várias subpastas desnecessárias).
-5. Analisar os auxílios visuais estão presentes sempre na segunda página da carta ADC, na segunda tabela, na coluna AUXÍLIOS/AIDS.   Nesta tabela, a primeira coluna é RWY, que se refere a cabeceira da pista na qual o auxílio está presente. Então é necessário observar a cabeceira e os auxílios correspondentes para fazer a atualização.
-6. É NECESSÁRIO SALVAR A PLANILHA ATUALIZADA NA SUBPASTA "csv" da PASTA "data"


#Junção final da base do ROTAER (base_rotaer_final) , com a base das cartas ADC (AIDS_aero) e  com a base da ANAC (aero_ANAC).
-1. O código que faz a função final das bases é o código 4_unir_bases 
-2. O código une as bases: aero_ANAC, base_rotaer_final e AIDS_aero.
-3. A base final que é resultado deste código é aerodromos_BR_final.
-4. Esta base que foi utilizada para atualizar o site do EC Data.
-5. COLAR MANUALMENTE A BASE aerodromos_BR_final NA PASTA de csv da rotina BD_07


