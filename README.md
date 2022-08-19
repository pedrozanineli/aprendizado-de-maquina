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

**Bloco 1**
<br>Resumo do projeto;
<br> O projeto se baseia em ensinar uma máquina (código) a identificar padrões em um conjunto de dados, tentar organizá-los e, se possível, retornar uma resposta. Os dados escolhidos estão relacionados à expressão gênica na pele.
O objetivo do projeto é produzir um código que ajude na identificação de amostras humanas em desastres e estudos forenses, o código está sendo treinado com os seguintes dados: TPM (Transcrito por milhão) dos genes mais expressivos na pele, faixa etária e sexo, e ele deve relacionar esses 3 dados de entrada de treino, fazendo diversas comparações entre as amostras, para entender um padrão do TPM com a faixa etária e o sexo da amostra para que ele receba posteriormente dados de TPM de uma amostra e retorne a faixa etária e sexo da pessoa dona daquela amostra, assim agilizando diversos processos na área de desastres e na área forense.

<br>Treinamento da Máquina;
<br>
O código receberá 3 dados de entrada, mas isso você já sabe, agora como ele aprenderá o que esses dados significam? Bom, nós não estamos dando dados aleatórios, mas sim dados que já estão correlacionados, por exemplo, a amostra X tem um TPM do gene ABCD2: 29803, está na faixa etária 20 – 29 anos (jovem) e é feminina e ele entender que essa faixa etária tem relação com esse número de TPM do gene, mas ela não receberá apenas a amostra X, mas receberá 100 amostras e correlaciona-las.

<br>Código de treinamento;
<br>Aqui temos o código e alguns gráficos gerados a partir dos 3 dados de entrada;


<br>Teste;
<br>Aqui o testamos o código com 10 amostras que já tínhamos os dados resposta e esperamos que a máquina acerte;

<br>Análise estatística dos dados;
<br>Aqui todos os resultados e gráficos vão ser analisados e comparados com a literatura visando confirmá-la ou negá-la.


