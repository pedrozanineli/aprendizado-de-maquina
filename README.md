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
<br>

**Como esse projeto funciona?"**
<br> O projeto se baseia em ensinar uma máquina (código) a identificar padrões em um conjunto de dados, tentar organizá-los e, se possível, retornar uma resposta. Os dados escolhidos estão relacionados à expressão gênica na pele (não exposta ao sol) e retirados do BioBanco de dados "Portal GTEX" e devem retornar a idade e o sexo da amostra.
<br>

**Objetivos do projeto**
<br> O objetivo do projeto é produzir uma máquina (código) que ajude na identificação de amostras de tecido humano em desastres e estudos forenses. 
<br> O código está sendo treinado com os seguintes dados:
<br> - TPM (Transcrito por milhão) dos genes mais expressivos na pele. (genes de interesse: 20)
<br> - Faixa etária. (20 aos 79 anos)
<br> - Sexo. (Masculino e Feminino)
<br> Ele deve relacionar esses 3 dados de entrada de treino, fazendo diversas comparações entre as amostras, para encontrar um padrão entre os 3 tipos de dados, após o padrão ser encontrado, a máquina (código) passará por um teste para definir a eficiência desse padrão.
<br> Por fim, o padrão eficiente deve conseguir receber os TPMs da amostra e retornar a faixa etária e o sexo da amostra de tecido da derme humana.
<br>

**Links relevantes até o momento**
<br> Base de dados: <https://gtexportal.org/home/biobank#search>
<br> Base de dados - Expressão gênica em diferentes tecidos (gráfico): <https://gtexportal.org/home/tissue/Skin_Sun_Exposed_Lower_leg?tissueSelect=Skin_Sun_Exposed_Lower_leg>
