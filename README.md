# Exercícios de modelagem e operações em banco de dados

Faça as atividades de acordo com as orientações em cada etapa.

```sql
CREATE DATABASE tecinternet_escola_vitorGama CHARACTER SET utf8mb4;
```

```sql
CREATE TABLE cursos (
    id  TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    titulo NOT NULL VARCHAR(30),
    cargaHoraria NOT NULL TINYINT ,
    professores_id TINYINT NULL
);

CREATE TABLE professores (
    id  TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome  VARCHAR(50) NOT NULL,
    areaAtuacao  ENUM('design', 'desenvolvimento', 'infra') NOT NULL,
    cursos_id TINYINT NOT NULL 
);

CREATE TABLE alunos (
    id  TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome  VARCHAR(50) NOT NULL,
    dataDeNascimento DATE NOT NULL ,
    primeiraNota DECIMAL(4,2) NOT NULL ,
    segundaNota DECIMAL(4,2) NOT NULL ,
    cursos_id TINYINT NOT NULL 
);

```

```sql
ALTER TABLE cursos
    ADD CONSTRAINT fk_cursos_professores1
    FOREIGN KEY (professores_id) REFERENCES professores(id);

ALTER TABLE professores 
    ADD CONSTRAINT fk_professores_cursos1
    FOREIGN KEY (cursos_id) REFERENCES cursos(id); 

    ALTER TABLE alunos
    ADD CONSTRAINT fk_alunos_cursos
    FOREIGN KEY (cursos_id) REFERENCES cursos(id); 










```