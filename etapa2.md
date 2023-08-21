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

UPDATE cursos SET professores_id = 5 WHERE id = 1;
UPDATE cursos SET professores_id = 4 WHERE id = 2;
UPDATE cursos SET professores_id = 3 WHERE id = 3;
UPDATE cursos SET professores_id = 2 WHERE id = 4;
UPDATE cursos SET professores_id = 1 WHERE id = 5;

INSERT INTO alunos (nome, dataDeNascimento, primeiraNota, segundaNota, cursos_id) VALUES
    ('Maria Silva', '1982-03-15', 8.00, 4.00, 4),
    ('João Santos', '1990-07-05', 7.00, 9.00, 5),
    ('Ana Rodrigues ', '1975-09-22', 9.00, 3.00,3),
    ('Pedro Oliveira', '2001-01-10', 6.00, 8.45, 2),
    ('Sofia Pereira', '1988-04-30', 10.00, 7.80, 1),
    ('Luis Mendes', '1967-08-12', 5.05, 6.95, 1),
    ('Carolina Almeida', '1995-10-25', 8.00, 9.00, 2),
    ('Miguel Ferreira', '1984-12-07', 9.00, 8.20, 3),
    ('Ines Costa', '2000-06-18', 5.00, 8.00, 4),
    ('Andre Ramos', '1979-02-03', 6.00, 10.00, 5);
    






```

