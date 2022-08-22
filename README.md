## Aprendizado de Máquina
### Tema: Análise da expressão genica da derme, com enfase em estudos florences

**Membros do grupo & RM's**:
<br> - Artur Hosoi Kimura - 220048
<br> - Débora van Putten Chaves - 220037
<br> - Pedro H. M. Zanineli - 220068
<br> - Vitor E. G. Barelli - 220072

**Respectivos lideres de cada bloco**:
<br> - Bloco 1 - Vitor E. G. Barelli
<br> - Bloco 2 - Artur Hosoi Kimura
<br> - Bloco 3 - Débora van Putten Chaves
<br> - Bloco 4 - Pedro Henrique Machado Zanineli

**Links relevantes até o momento**
<br> Base de dados: <https://gtexportal.org/home/biobank#search>
<br> Base de dados - Expressão gênica em diferentes tecidos (gráfico): <https://gtexportal.org/home/tissue/Skin_Sun_Exposed_Lower_leg?tissueSelect=Skin_Sun_Exposed_Lower_leg>
<br>
**Bloco 1**
<br> Resumo do projeto;
<br> O projeto se baseia em ensinar uma máquina (código) a identificar padrões em um conjunto de dados, tentar organizá-los e, se possível, retornar uma resposta. Os dados escolhidos estão relacionados à expressão gênica na pele.
O objetivo do projeto é produzir um código que ajude na identificação de amostras humanas em desastres e estudos forenses, o código está sendo treinado com os seguintes dados: TPM (Transcrito por milhão) dos genes mais expressivos na pele, faixa etária e sexo, e ele deve relacionar esses 3 dados de entrada de treino, fazendo diversas comparações entre as amostras, para entender um padrão do TPM com a faixa etária e o sexo da amostra para que ele receba posteriormente dados de TPM de uma amostra e retorne a faixa etária e sexo da pessoa dona daquela amostra, assim agilizando diversos processos na área de desastres e na área forense.
<br>
<br> ***Treinamento da Máquina;***
<br>
<br> O código receberá 3 dados de entrada, mas isso você já sabe, agora como ele aprenderá o que esses dados significam? Bom, nós não estamos dando dados aleatórios, mas sim dados que já estão correlacionados, por exemplo, a amostra X tem um TPM do gene ABCD2: 29803, está na faixa etária 20 – 29 anos (jovem) e é feminina e ele entender que essa faixa etária tem relação com esse número de TPM do gene, mas ela não receberá apenas a amostra X, mas receberá 100 amostras e correlacioná-las.
<br>
<br> ***Código de treinamento;***
<br> Aqui temos o código inicial e alguns gráficos gerados(análise exploratória dos dados) a partir dos dados de entrada;
<br>
<br> Para começar devemos importar algumas coisas para permitir o trabalho: numpy, pandas, seaborn, matplotlib.pyplot e desse ultimo devemos importar o figure e o is_numeric_dtype ;
<br>
![image](https://user-images.githubusercontent.com/106676956/185798516-6022152c-4050-49c8-b651-66e159bd65c9.png)
<br>
<br> Okay, com as importações feitas devemos criar um dataframe com todos os dados coletados, mas pera lá, o que é um dataframe? Bom, dataframe é uma tabela com diversas colunas e linhas que podem armazenar diferentes tipos de dados...
<br> OBS: o dataframe inicial contem todos os TPMs dos genes do banco, mas nós sabemos que trabalhar com 56.200 colunas de TPMs não é realistico par ao nosso número de amostras, então mais pra frente vamos criar um novo dataframe!
<br> Assim que se cria um dataframe; (é bom lembrar que para criar um dataframe é necessário ter o dados em alguma outra aba que o jupyterlLab tenha acesso)
<br>
![image](https://user-images.githubusercontent.com/106676956/185798697-1bbd967b-7d67-47bb-b606-8eac59923516.png)
<br>
<br> Agora com o dataframe criado, vamos chamá-lo;
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185798748-301f51ad-88ed-4dc6-8f72-69272b7d6b13.png)
<br>
<br>Nesse dataframe temos 5 linhas de amostras e diversas colunas que definem informações diferentes como sexo, faixa etária e o TPM (Transcritos Por Milhão) dos genes escolhidos!
<br>
<br> Hmmmm, mas aqui nós só temos dados numéricos de faixa etária, que tal se transformarmos isso em um dado categórico? Bom vamos lá...
<br> Mas eu ainda não entendi, qual a diferença entre um dado numérico e um categoórico? Bom dados numéricos são aqueles com valores em números, já os dados categóricos são aqueles com duas ou mais opções, tipo você gosta de melancia? Sim ou Não, nesse caso "sim ou não" entram como dados categóricos!
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185798925-8a977d48-cb14-4388-9c10-28c15fe3b57e.png)
<br>
<br>Então, definimos uma função para dar novos atributos as faixas etárias e também para criar uma coluna que vamos integrar no dataframe...
<br>
<br>Espero que tu tenhas entendido todo o processo até aqui, pois agora eu vou te explicar um pouco dos tipos de valores e de como fizemos a normalização dos dados de TPM dos genes;
<br>
<br> Tipos de dados;
<br> É sempre muito importante entender com quais tipos de dados estamos trabalhando, para dar o devido tratamento;
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185799131-a8470592-d87e-4a1b-bb6d-fc9c7eb5859b.png)
<br>
<br> Bom a primeira coluna() armazena dados do tipo float, a segunda() dados do tipo object, a terceira, quarta e quinta armazenam dados category
<br>
<br> A normalização: ela serve para organizar os dados nos mesmos parâmetros, corrigir erros, dados faltantes entre outros, mas aqui usamos apenas para padronizar o TPM dos genes do nosso dataframe;
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185799410-42bd12e7-aa3e-49b2-8e78-bc434eec7271.png)
<br>
<br> ***Análise exploratória;***
<br> A seguir temos alguns gráficos gerados, mas antes temos que entender melhor nossas amostras iniciais, por exemplos quantas amostras temos de cada faixa etária;
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185799687-cb4d05cb-717b-4197-b116-cd301330c4aa.png)
<br>
<br> Agora vamos organizar os genes pelos seus valores de TPM, no caso os 20 maiores valores...
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185799740-16178f8c-f28c-4c62-804c-2da634482266.png)
<br>
<br>Com os 20 maiores TPMs selecionados e organizados, vamos criar um dataframe com esses genes e vamos chamá-los de "genes de interesse"
<br>![image](https://user-images.githubusercontent.com/106676956/185799876-b2661da4-2081-42b8-8bb2-eada69867f74.png)
<br>![image](https://user-images.githubusercontent.com/106676956/185799899-9584dff2-1b37-4e12-8804-d725b92178db.png)
<br>
<br> Lembra lá no início quando eu falei que íamos usar 100 amostras, então isso será mais para frente, agora vamos trabalhar apenas com 30 e seria interessante saber quais são os TPMs dos genes de interesse por amostra, então vamos fazer um mapa de calor disso;
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185800030-ec7a6898-316e-4c31-a0c1-fc7de2ff16ec.png)
<br>![image](https://user-images.githubusercontent.com/106676956/185800042-045559f5-0494-41e8-ac07-6c09e9d2bc5c.png)
<br>
<br> Bom agora que já temos o mapa de calor, seria legal ver uns gráficos correlacionando os TPMs dos genes de interesse com a idade das amostras né, então vamos fazer isso, mas de forma demonstrativa, logo vamos fazer só com os 4 primeiros genes...
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185800135-19ad2604-092b-4a00-80fd-57f10f73ac7e.png)
<br>Esse código vai gerar o seguinte gráfico;
<br>![image](https://user-images.githubusercontent.com/106676956/185800159-a7de285d-888e-4a63-8060-1c0caed5e61b.png)
<br>
<br>Certo, temos 2 gráficos muito importantes para a análise estatística que vai ser feita posteriormente, mas bom, sinto que está faltando algo...
<br>
<br>AH, A MATRIZ DE COVARIÂNCIA: ela vai identificar padrões nos dados (no caso entre os genes de interesse), deixando bem claro as similaridades e as diferenças;
<br>
<br>![image](https://user-images.githubusercontent.com/106676956/185800270-102baae8-546e-44ba-a9f7-81af9ef411aa.png)
<br>OBS: Não vou mostras aqui a matriz de covariância em sí, pois ela ficou bem grande AHAHAH, mas vou te mostras o gráfico produzido a partir dela;
<br>![image](https://user-images.githubusercontent.com/106676956/185800316-2640ccd4-30d7-452b-b093-b47eb91f1a6a.png)
<br>
<br> ***Teste;***
<br>Aqui o testamos o código com 10 amostras que já tínhamos os dados resposta e esperamos que a máquina acerte;
<br>Esse teste vai ocorrer mais para frente, te peço calma...
<br>
<br> ***Análise estatística dos dados;***
<br>Aqui todos os resultados e gráficos vão ser analisados e comparados com a literatura visando confirmá-la ou negá-la.
<br>
<br> Primeiro vamos fazer uma análise sobre os gráficos gerados:
