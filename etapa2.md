# Exercícios de Banco de Dados - Etapa 2

## CRUD - Cadastro geral

### Cadastre pelo menos 5 cursos: 

1. Front-End, carga horária 40h
2. Back-End, carga horária 80h
3. UX/UI Design, carga horária 30h
4. Figma, carga horária 10h
5. Redes de Computadores, carga horária 100h

**Atenção:** por enquanto, deixe o campo professor_id como nulo

---

### Cadastre pelo menos 5 professores: 

1. Jon Oliva, área infra
2. Lemmy Kilmister, área design
3. Neil Peart, área design
4. Ozzy Osbourne, área desenvolvimento
5. David Gilmour, área desenvolvimento

**Atenção:** durante o cadastro dos professores, associe cada professor a um curso na ordem contrária dos registros. 

Exemplos: 

- O primeiro professor (Jon Oliva, infra) será atribuido ao último curso (Redes de Computadores)
- O segundo professor (Lemmy, design) será atribuido ao penúltimo curso (Figma)

---

### Atualize os dados do campo professor_id da tabela cursos, associando cada curso ao seu professor correspondente.

---

### Cadastre pelo menos 10 alunos distribuidos aleatoriamente dentre os cursos, com datas de nascimento variadas, notas baixas e altas (sempre entre 0.00 e 10.00).

```sql

INSERT INTO cursos (titulo, cargaHoraria) VALUES
    ('Front-End', 40),
    ('Back-End', 80),
    ('UX/UI Design', 30),
    ('Figma', 10),
    ('Redes de Computadores', 100);

INSERT INTO professores (nome, areaAtuacao, cursos_id) VALUES
    ('Jon Oliva', 'infra', 5),
    ('Lemmy Kilmister', 'design', 4),
    ('Neil Peart', 'design', 3),
    ('Ozzy Osbourne', 'desenvolvimento', 2),
    ('David Gilmour', 'desenvolvimento', 1);

    



```

