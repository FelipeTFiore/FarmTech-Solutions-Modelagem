# 🌱 FarmTech Solutions - Modelagem de Banco de Dados

**Curso:** IA  
**Disciplina:** Banco de Dados  
**Autor:** [Felipe Tavares Fiore] - RM[RM560763]  

---

## 📌 Objetivo
Sistema de monitoramento agrícola que:
- Coleta dados de sensores (umidade, pH, nutrientes)
- Armazena leituras em tempo real
- Sugere ajustes na irrigação e adubação

### Tabelas
| Tabela    | Descrição                          |
|-----------|-----------------------------------|
| `CULTURA` | Armazena dados das plantações     |
| `SENSOR`  | Cadastro dos sensores de campo    |
| `LEITURA` | Registro das medições dos sensores|

---

## ⚙️ Script SQL
O script completo de criação do banco está disponível em:  
[modelagem/FarmTech_DDL.sql](modelagem/FarmTech_DDL.sql)

Exemplo de criação das tabelas:
```sql
CREATE TABLE CULTURA (
    ID_CULTURA NUMBER PRIMARY KEY,
    NOME VARCHAR2(50) NOT NULL,
    AREA_PLANTADA NUMBER(10,2) CHECK (AREA_PLANTADA > 0)
);
