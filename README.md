![logo ilum](https://github.com/pedrozanineli/aprendizado-de-maquina/blob/main/logo1.png)

## Aprendizado de Máquina
### Tema: Análise da expressão gênica da derme, com ênfase em estudos forenses

**Membros e respectivos líderes de cada bloco**

- Artur Hosoi Kimura - 220048 - Bloco 2
- Débora van Putten Chaves - 220037 - Bloco 3
- Pedro Henrique Machado Zanineli - 220068 - Bloco  4
- Vitor Eduardo Girotto Barelli - 220072 - Bloco 1

Como forma de desenvolvimento da disciplina de Aprendizado de Máquina do segundo semestre do curso da Ilum Escola de Ciência, o projeto tem como objetivo identificar a idade e sexo de um determinado indivíduo ao analisar um conjunto de dados relacionados à expressão gênica na pele não exposta ao sol, retirados do BioBanco de dados "Portal GTEX".

**Informações importantes do projeto**

O projeto será desenvolvido levando em consideração:
- Features expressas em TPM (transcrito por milhão) dos genes mais expressivos na pele segundi a literatura;
- Faixa etária como target, com subdivisões em faixas que exploram idades entre 20 aos 79 anos;
- Sexo como target, podendo ser classificado como masculino ou feminino.

## Sumário do repositório

***Bloco 1***
- B1 - Coletando os dados:
- B1 - Dados.csv:
- B1 - Diário de bordo:
- B1 - Preparando e analisando os dados:
- B1 - material-de-estudo.md: reúne em um arquivo só os genes que encontramos destacados na literatura e os links para os artigos que continham tais informações.

***Bloco 2***
- B2 - Aplicação dos métodos com conversão randômica de idade:
- B2 - Aplicação dos métodos:
- B2 - Diário de bordo:

***Bloco 3***
- B3 - Agrupamento (clustering):
- B3 - Detecção de valores anômalos:
- B3 - Diário de bordo:
- B3 - PCA:

***Bloco 4***
- B4 - Validação cruzada:

***Geral***
- 'raw_data.zip': contém todos os nossos dados já tratados.
- 'data.csv': pegamos todos os nossos genes e, a partir deles, somamos as suas expressões. Depois disso, analisamos quais deles eram mais expressivos (quais tinham as maiores somas) e selecionamos os 20 (vinte) que aparesentaram maiores resultados.
- 'data_artigo.csv': os genes aqui escolhidos são os que foram obtidos da literatura científica. Os links para os artigos que suportam essas escolhas estão dispostos no arquivo 'material-de-estudo.md'.
