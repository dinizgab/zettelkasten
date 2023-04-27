28-03-2023 - 15:47
Status: #idea
Tags: [[ideas]]

# API - MVV presença

Notas sobre a arquitetura da API do app de presença das escolas.

Uma aproximação com TDD 

### Rotas que vão estar dentro da API
- Logar usuário;
- Validação de login de usuário;
- Troca de senha do usuário;
- Patch de aluno presente na aula;
- Get de todos os alunos que estão presentes naquela aula;
- Get de todos os alunos que estão naquela turma;

### Modelo de tabelas BD
![[Model API presence|center|600]]

### Pontos para se analisar
- [x] Tabela instituição
- [ ] Justificativa de faltas (?)

---
# Referências