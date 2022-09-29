![logo ilum](https://github.com/pedrozanineli/aprendizado-de-maquina/blob/main/logo1.png)

## Aprendizado de Máquina
### Tema: Análise da expressão gênica da derme, com ênfase em estudos forenses

**Membros do grupo, RM's e respectivos lideres de cada bloco**;
<br> - Artur Hosoi Kimura - 220048 - Bloco 2
<br> - Débora van Putten Chaves - 220037 - Bloco 3
<br> - Pedro Henrique Machado Zanineli - 220068 - Bloco 1
<br> - Vitor Eduardo Girotto Barelli - 220072 - Bloco 4

**Como nosso projeto funciona?**
<br> O projeto se baseia em ensinar uma máquina a identificar padrões a partir de um conjunto de dados organizados, objetivando obter como retorno uma resposta que preveja algum comportamento de amostras definidas. Os dados escolhidos estão relacionados à expressão gênica na pele não exposta ao sol. Tais dados foram retirados do BioBanco de dados "Portal GTEX" e, com eles, esperamos ser capazes de prever faixa etária na qual se encaixa e sexo de uma pessoa fornecedora de amostra a partir da análise de sua expressão gênica.

**Objetivos do projeto**
<br> O objetivo do projeto é construir uma ferramenta que consiste em uma máquina que aprendeu a identificar informações como faixa etária e sexo de amostras de diferentes doadores. Essa ideia pode ser muito útil principalmente em situações de desastres naturais ou não que afetem grupo de pessoas, asssim como estudos forenses em que há algum entrave em relação ao acesso de dados pessoais dos indivíduos;
<br> A máquina está sendo treinada com os seguintes dados:
<br> - TPM (transcrito por milhão) dos genes mais expressivos na pele (sendo 20 os nossos genes de interesse);
<br> - Faixa etária (subdivisões em faixas que exploram a idade de 20 aos 79 anos);
<br> - Sexo (entre masculino e feminino);
<br> Ela deve relacionar esses 3 dados de entrada de treino, fazendo diversas comparações entre as amostras, para encontrar um padrão entre os 3 tipos de dados, após o padrão ser encontrado, a máquina passará por um teste para definir a eficiência desse padrão.
<br> Por fim, o padrão eficiente deve conseguir receber os TPMs da amostra e retornar a faixa etária e o sexo referentes à amostra de tecido da derme humana.

**Descrição dos arquivos do GitHub**
1. 'raw_data.zip'
<br> Descrição: contém todos os nossos dados já tratados.
2. 'data.csv'
<br> Descrição: pegamos todos os nossos genes e, a partir deles, somamos as suas expressões. Depois disso, analisamos quais deles eram mais expressivos (quais tinham as maiores somas) e selecionamos os 20 (vinte) que aparesentaram maiores resultados.
3. 'data_artigo.csv'
<br> Descrição: os genes aqui escolhidos são os que foram obtidos da literatura científica. Os links para os artigos que suportam essas escolhas estão dispostos no arquivo 'material-de-estudo.md'.
4. 'material-de-estudo.md'
<br> Descrição: reúne em um arquivo só os genes que encontramos destacados na literatura e os links para os artigos que continham tais informações.

**Links relevantes até o momento**
<br> Base de dados: <https://gtexportal.org/home/biobank#search>
<br> Base de dados - Expressão gênica em diferentes tecidos (gráfico): <https://gtexportal.org/home/tissue/Skin_Sun_Exposed_Lower_leg?tissueSelect=Skin_Sun_Exposed_Lower_leg>
