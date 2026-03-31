
ComunicaAluno Desktop 🎓
AcademicBridge é uma aplicação desktop desenvolvida em Java para centralizar e organizar a comunicação entre alunos, professores e coordenação acadêmica. O projeto substitui fluxos informais de mensagens por um sistema de chamados e avisos auditáveis, garantindo que solicitações acadêmicas sejam registradas e respondidas com eficiência.

🚀 Funcionalidades Principais
Autenticação Segura: Sistema de login com diferentes níveis de acesso (RBAC).

Gestão de Perfis:

Alunos: Abertura de chamados, consulta de avisos da coordenação e contato com docentes.

Professores: Dashboard para resposta de dúvidas e publicação de avisos por disciplina.

Administradores: Gerenciamento completo de usuários e logs do sistema.

Persistência de Dados: Integração total com banco de dados SQL para histórico de comunicações.

Interface Desktop Nativa: Foco em performance e usabilidade em ambiente Windows/Linux/macOS.

🛠️ Stack Técnica
Linguagem: Java 17+

Interface Gráfica: Java Swing / JavaFX

Banco de Dados: MySQL / PostgreSQL (SQL Nativo)

Persistência/Drivers: JDBC (Java Database Connectivity)

Gerenciador de Dependências: Maven ou Gradle

📂 Estrutura do Banco de Dados
O sistema utiliza um modelo relacional para garantir a integridade dos dados acadêmicos. As principais entidades são:

usuarios (ID, Nome, E-mail, Senha, Tipo_Perfil)

chamados (ID, Aluno_ID, Assunto, Mensagem, Status, Data)

avisos (ID, Autor_ID, Titulo, Conteudo, Destinatario_Tipo)
