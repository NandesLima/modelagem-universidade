# Projeto de Universidade


## Narrativa – Alunos

- A universidade possui diversos alunos que podem estar matriculados em mais de um curso (graduação)
- Os alunos podem fazer cursos extras fornecidos externa e internamente (universidade) para contar como horas complementares.
- Não há restrição de matérias puxadas se não houver sobreposição de horários.
- Os alunos são submetidos a duas provas por semestre para cada disciplina. Eventuais trabalhos devem ser tratados pelo professor para compor a nota da prova.

## Narrativa – Disciplina

- Cada disciplina é fornecida por um professor. Restrição: apenas por este professor.
- Algumas disciplinas possuem pré-requisitos. Um mesmo pré-requisito pode ser associado a mais de uma disciplina.
- As disciplinas podem ser comuns a cursos distintos. Ex: Cálculo 1 para computação e engenharia.
- O ciclo de vida da disciplina é semestral.

## Narrativa -  Professores

- Professores que ministram as disciplinas estão associados as coordenações de seus respectivos cursos. Ex: Computação, Física, Engenharia…




# Levantamento de requisitos

## Entidades:

Pessoa: Nome, CPF, Data de nascimento, e-mail, telefone, endereço
- Aluno – Matrícula, data de matrícula
- Professor – Registro
Disciplina: Nome, área, carga horária
Curso: Nome, duração, professor coordenador
Departamento: Nome, professor coordenador, campus
Pré-requisitos: Nome do curso
Período: Ano, semestre
Sala: Nome
Extensão: Nome, área, instituição, carga horária, data de conclusão,comprovante


## Relações:

Aluno x Disciplina (N, M): Matriculado na disciplina
Aluno x Curso (N, M): Matriculado no curso
Pré-requisito x Disciplina (N, M): Pré-requisito das disciplinas
Professor X Disciplina (1, N): Professor da disciplina
Professor x Departamento (N, 1): Departamento do professor
Professor x Departamento (1, 1): Coordenação do departamento
Curso x Departamento (N, 1): Departamento do curso
Disciplina x Período X Curso X Sala (N, M): Oferta da disciplina
Sala X Departamento (N, 1): Departamento da sala
Aluno x Extensão (N, M): Horas complementares
Curso x Professor (1, 1): Coordenador do curso
