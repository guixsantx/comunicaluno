# 🎓 ComunicAluno

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/Desktop-Application-blue?style=for-the-badge" alt="Desktop" />
  <img src="https://img.shields.io/badge/Status-Em%20Desenvolvimento-green?style=for-the-badge" alt="Status" />
</p>

> **Solução robusta de comunicação acadêmica centralizada, desenvolvida em Java para integrar alunos, docentes e coordenação de forma auditável e segura.**

---

## 📌 Sobre o Projeto

O **ComunicAluno** nasce para mitigar o abismo informacional nas instituições de ensino. Diferente de aplicativos de mensagens instantâneas genéricos, nossa solução desktop foca na **formalidade e rastreabilidade**, garantindo que avisos oficiais e solicitações críticas não se percam em fluxos de conversas informais.

### 🎯 Problema vs. Solução
* **Problema:** Comunicação fragmentada, perda de prazos e dificuldade de acesso à coordenação.
* **Solução:** Um ecossistema desktop único com permissões granulares (RBAC) e persistência de dados em SQL para histórico institucional.

---

## 👥 Equipe de Engenharia

| Nome | Registro Acadêmico (RA) |
| :--- | :--- |
| **Vinícius Pampolim Silva** | 823157424 |
| **Lucas Felipe Dias** | 823116804 |
| **Raul Bertolla Silveira** | 82318856 |
| **Gabriel Coelho Bononi** | 823156221 |
| **Eduardo de Paiva Mantovam** | 82316154 |
| **Guilherme Dos Santos Santana** | 823159723 |

---

## 🛠️ Stack Tecnológica

* **Linguagem Core:** Java 17 (LTS)
* **Interface Gráfica:** Java Swing / JavaFX
* **Camada de Dados:** JDBC (Java Database Connectivity)
* **Banco de Dados:** SQL (MySQL / PostgreSQL)
* **Arquitetura:** MVC (Model-View-Controller)

---

## ⚙️ Arquitetura e Funcionalidades

### 🔐 Níveis de Acesso (RBAC)
1.  **Módulo Aluno:** Interface simplificada para abertura de tickets, consulta de avisos por disciplina e repositório de comunicados.
2.  **Módulo Docente:** Dashboard de gestão para resposta de dúvidas e disparo de notificações em lote para turmas específicas.
3.  **Módulo Admin (Devs):** Painel de controle de usuários, auditoria de logs e manutenção de tabelas.

### 📊 Modelagem de Dados (Entity-Relationship)
A persistência é garantida por um schema SQL normalizado:
* `Tbl_Usuarios`: Autenticação e definição de privilégios.
* `Tbl_Chamados`: Ciclo de vida das solicitações (Aberto, Em Análise, Concluído).
* `Tbl_Mural`: Mensagens globais ou segmentadas por curso/turma.

---

## 🚀 Guia de Instalação

### Pré-requisitos
* Java Development Kit (JDK) 17+
* Instância SQL ativa (Local ou Cloud)

### Execução
1.  **Clone o projeto:**
    ```bash
    git clone [https://github.com/seu-usuario/comunicaluno.git](https://github.com/seu-usuario/comunicaluno.git)
    ```
2.  **Configuração do DB:** Execute o script `setup_database.sql` disponível na pasta `/assets`.
3.  **Configuração de Ambiente:** Edite o arquivo `src/main/resources/db.properties` com suas credenciais.
4.  **Build & Run:**
    ```bash
    mvn clean install
    mvn exec:java
    ```
<p align="center">Desenvolvido com foco em Engenharia de Software Aplicada.</p>
