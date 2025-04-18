# Objetivo: Criar o diagrama dimensional – star schema – com base no diagrama relacional disponibilizado.

Fui desafiado pelo curso de Análise de Dados com Power Bi a converter o modelo relacional em um Modelo Dimensional utilizando o Star Schema.

## Foco:

### Professor – objeto de análise

Vocês irão montar o esquema em estrela com o foco na análise dos dados dos professores. Sendo assim, a tabela fato deve refletir diversos dados sobre professor, cursos ministrados, departamento ao qual faz parte.... Por aí vocês já têm uma ideia do que deve compor a tabela fato do modelo em questão.

Obs.: Não é necessário refletir dados sobre os alunos!

O modelo que iremos trabalhar está ilustrado na imagem abaixo.

![image](https://github.com/user-attachments/assets/05622eae-f63a-4ae6-8889-1ffd565f4e30)

Para converter o modelo relacional mostrado na imagem para um modelo dimensional usando o star schema, vamos focar em criar tabelas de fato e dimensão a partir das entidades presentes removendo a visão do aluno e focando na visão do professor. Um modelo dimensional em star schema se caracteriza por ter uma tabela de fato centralizada, que se conecta às tabelas de dimensão, através de chaves estrangeiras.

### Passos para transformar o modelo relacional em Star Schema:

### Passo 1: Criar Tabela Fato

Campos:
* IDDepartamento
* IDProfessor
* IDDisciplina
* IDCurso
* CargaHoraria (horas da disciplina)
* Semestre (semestre da disciplina)
* StatusDisciplina (ativa ou inativa)

### Passo 2: Criar Tabelas Dimensão

🎓 Dimensão Professor
* IDProfessor
* Nome
*	Sobrenome
*	NívelAcademico
*	DataNascimento
*	Email
*	SalarioBase
*	Especialidade
*	Formacao
*	QtdAulas

📚 Dimensão Disciplina
*	IDDisciplina 
*	Nome
*	Descricao
*	CargaHoraria
*	Semestre

🏫 Dimensão Curso
*	ID_Curso 
*	Nome
*	Descricao
*	CargaHoraria
*	Modalidade (presencial, distância)
*	Turno (manhã, tarde, noite)
*	Vagas
*	Duracao
  
🏢 Dimensão Departamento
*	IDDepartamento 
*	Nome
*	Campus
*	Endereço

### Resultado Final (Diagrama):

![Modelo Star Schema](https://github.com/user-attachments/assets/42ce3bbf-bd0c-4333-9af4-ba1257a5450e)

### Considerações Finais

O modelo dimensional em star schema oferece uma estrutura simples, intuitiva e de alta performance para análise de dados, especialmente em ferramentas de BI como o Power BI. Com ele, consultas ficam mais rápidas, já que a tabela de fato centraliza os dados quantitativos e se conecta diretamente às dimensões, permitindo análises dinâmicas e flexíveis. Além disso, facilita o entendimento para usuários não técnicos, melhora a manutenção e expansão do banco de dados e otimiza o desempenho de agregações e filtros, sendo ideal para cenários de tomada de decisão e geração de relatórios gerenciais.




