# Graph-Database
Projeto de Orientação - Tópicos Avançãdos de Banco de Dados - 6º Ciclo - Ciencias da Computação
<br>

# Aluno

 - Juan Caio Paronitti Galera - RA: 22.122.067-6

# Descrição 

O objetivo deste projeto é criar uma estrutura de Graph Database, onde os dados são organizados em coleções de nós (nodes) e relacionamentos (edges), representando entidades e suas associações. Essas coleções permitem armazenar informações complexas do sistema acadêmico em um formato flexível e escalável, adequado para consultas de relacionamento. Abaixo, está a descrição das coleções de nós e relacionamentos criados para armazenar os dados:

 ### Coleções de Nós (Nodes):

- **Aluno:** <br>
A coleção "Aluno" armazena informações sobre os alunos. Cada nó possui os atributos id_aluno (identificador único) e nome (nome do aluno).
  
- **Professor:** <br>
A coleção "Professor" contém dados sobre professores, com cada nó possuindo id_professor (identificador único) e nome (nome do professor).

- **Disciplina:** <br>
A coleção "Disciplina" armazena as disciplinas, onde cada nó tem os atributos id_disciplina (identificador único) e nome (nome da disciplina).

- **Departamento:** <br>
"Departamento" contém nós para representar os departamentos, com id_departamento (identificador único) e nome (nome do departamento).

- **Curso:** <br>
A coleção "Curso" armazena os cursos oferecidos, onde cada nó possui id_curso (identificador único) e nome (nome do curso).

- **Matriz_Curricular:** <br>
"Matriz_Curricular" representa as diferentes matrizes curriculares associadas aos cursos, com o atributo id_matriz (identificador único da matriz).

- **Historico_Escolar:** <br>
Esta coleção armazena o histórico escolar dos alunos, com id_historico (identificador único), ano (ano letivo), semestre (semestre do ano) e nota_final (nota final do aluno).

- **Grupo_de_TCC:** <br>
"Grupo_de_TCC" representa os grupos de TCC, onde cada nó possui id_grupo_tcc (identificador do grupo) e tema (tema do TCC).

- **Nota:** <br>
A coleção "Nota" contém informações sobre as notas atribuídas, com id_nota (identificador único) e nota (valor da nota).
  
### Coleções de Relacionamentos (edges):

- **ESTUDA_EM:** <br>
Conecta um "Aluno" a um "Curso", representando o curso em que o aluno está matriculado.

- **POSSUI_HISTORICO:** <br>
Liga um "Aluno" a um "Historico_Escolar", indicando o histórico escolar associado ao aluno.

- **PERTENCE_A:** <br> 
Relaciona um "Historico_Escolar" a uma "Disciplina", associando o desempenho do aluno em uma disciplina específica.

- **MINISTRA:** <br>
Conecta um "Professor" a uma "Disciplina", representando a disciplina ministrada pelo professor.

- **CHEFIA:** <br>
Liga um "Professor" a um "Departamento", representando o chefe de departamento.

- **OFERECIDO_POR:** <br>
Relaciona um "Curso" a um "Departamento", representando o departamento que oferece o curso.

- **TEM:** <br>
Conecta um "Curso" a uma "Matriz_Curricular", associando a matriz curricular oferecida pelo curso.

- **INCLUI:** <br>
Conecta um "Grupo_de_TCC" a um "Aluno", representando a participação do aluno no grupo de TCC.

- **ORIENTADO_POR:** <br>
Liga um "Grupo_de_TCC" a um "Professor", indicando o professor orientador do grupo de TCC.

- **DESEMPENHO:** <br>
Conecta um "Historico_Escolar" a uma "Nota", representando a nota obtida no histórico.

# Funcionamento do Código

 É necessario acessar um site ou compilador que consiga rodar Cypher (Neo4j).
 <br>
 Copie e rode o código contido no arquivo [Criação de Tabelas e Relações](https://github.com/RafLeal/Graph-Database/blob/main/Cria%C3%A7%C3%A3o%20de%20Tabelas%20e%20Rela%C3%A7%C3%B5es). 
 <br>
 Com isso, serão criadas todas os Nodes, as keys e os edges, para a criação das tabelas de relatórios.

  ### 1. Historico dos Alunos

   Este relatório retorna o historico do aluno de sua escolha, contendo o(s) código(s) e nome(s) da(s) disciplina(s), o semestre, ano e nota final.
  <br>
   Copiar o código contido em [Historico de Aluno](https://github.com/RafLeal/Graph-Database/blob/main/Historico%20de%20Aluno). Substitua a '#' contida no código, pelo número de matricula do aluno ( 1 a 6 ). Depois disto, basta rodar o código. 

  ### 2. Disciplinas mistradas pelas Professores

  Este relatório retorna os professores e as disciplinas as quais eles ministram, trazendo nome do professor e da disciplina, junto do semestre e o ano em que foram mistradas.
  <br>
   Copiar código contido em [Disciplinas Professor](https://github.com/RafLeal/Graph-Database/blob/main/Disciplinas%20Professor) e roda-lo.

  ### 3. Alunos Formados

  Este relatório retorna os alunos que se formaram em determinado semestre e ano. O relatório traz o(s) ID(s) e nome(s) do(s) aluno(s).
  <br>
   Copiar código contido em [Alunos formados](https://github.com/RafLeal/Graph-Database/blob/main/Alunos%20formados). Substitua o '#' pelo ano ( 2022 a 2024 ), e a '!' pelo semestre ( 1 ou 2 ). Após isto, basta rodar o código.

  ### 4. Professores Chefes de Departamentos

  Este relatório retorna os professores e os departamentos os quais eles chefiam.
  <br>
   Copiar código contido em [Professores Chefes de Departamentos](https://github.com/RafLeal/Graph-Database/blob/main/Professores%20Chefes%20de%20Departamentos) e roda-lo.

  ### 5. Grupos de TCC e seus orientadores

  Este relatório retorna os grupos de TCC criados, fornecendo os nomes dos alunos, o tema do TCC, e o professor orientador.
  <br>
   Copiar código contido em [Grupo TCC](https://github.com/RafLeal/Graph-Database/blob/main/Grupo%20TCC) e roda-lo.
 
