graph TD
    %% Telas Base
    TelaLogin[Tela de Login\nCPF ou E-mail e Senha]
    TelaCadastro[Tela de Cadastro\nNome, E-mail, Senha, Tipo de Perfil]
    graph TD
    %% Decisão de Acesso
    TelaLogin -->|Possui Cadastro?| ValidaAcesso{Status da Conta}
    TelaLogin -->|Não Possui| TelaCadastro
    graph TD
    %% Fluxo de Cadastro e Status Pendente
    TelaCadastro -->|Escolhe Perfil| TipoCadastro{Qual o seu perfil?}
    graph TD
    TipoCadastro -->|Sou Professor| PendenteAdmin[Conta Criada!\nStatus: PENDENTE_ADMIN\nAguarde liberação da Coordenação]
    TipoCadastro -->|Sou Aluno| PendenteProf[Conta Criada!\nStatus: PENDENTE_PROFESSOR\nAguarde liberação do seu Professor]
    graph TD
    PendenteAdmin --> RetornaLogin1[Voltar para Login]
    PendenteProf --> RetornaLogin1
    graph TD
    %% Fluxo de Validação no Login
    ValidaAcesso -->|Status: PENDENTE| MsgBloqueio[Erro: Sua conta ainda\nnão foi aprovada.]
    ValidaAcesso -->|Status: ATIVO| RoteadorPerfil{Redirecionar\npor Perfil}
    graph TD
    %% Dashboards Ativos
    RoteadorPerfil -->|ADMIN| DashAdmin[Dashboard Admin\n- Gerir Sistema\n- Aprovar Professores Pendentes]
    RoteadorPerfil -->|PROFESSOR| DashProf[Dashboard Professor\n- Postar Avisos\n- Aprovar Alunos Pendentes]
    RoteadorPerfil -->|ALUNO| DashAluno[Dashboard Aluno\n- Ver Avisos\n- Abrir Chamados]
graph TD
    %% Ações de Aprovação
    DashAdmin -.->|Clica em Aprovar| AtualizaProf[(Atualiza BD: Professor -> ATIVO)]
    DashProf -.->|Clica em Aprovar| AtualizaAluno[(Atualiza BD: Aluno -> ATIVO)]
