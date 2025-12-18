# Assistente Virtual de Agendamento Clínico (n8n + Telegram)
Este projeto foi desenvolvido como parte da capacitação Keep Chat, onde foi selecionado como Projeto Destaque. Trata-se de um ecossistema de automação low-code que gerencia agendamentos, remarcações e cancelamentos de consultas em tempo real.

# Funcionalidades
- Gestão de Cadastros: Identifica novos usuários via Chat ID e solicita o e-mail para registro automático no banco de dados.

- Agendamento Inteligente: Consulta horários disponíveis em uma planilha do Google Sheets e gera botões interativos no Telegram.

- Fluxo de Cancelamento/Remarcação: Lógica para identificar agendamentos ativos e liberar horários automaticamente na planilha.

- Notificações Multicanal: Envio de confirmações detalhadas via Telegram e Gmail para o paciente.

# Tecnologias Utilizadas
- n8n: Orquestração de todos os fluxos e lógica de nós (If, Switch, HTTP Request).

- Telegram Bot API: Interface principal para interação com o usuário.

- Google Sheets API: Utilizado como banco de dados dinâmico para controle de agenda e pacientes.

- Gmail API: Automação de e-mails de confirmação.

- JavaScript (JSON): Manipulação de expressões e dados entre os nós.

# Estrutura do Fluxo
- Trigger: Recebimento de mensagens ou comandos (/start) via Telegram.

- Validação: Verificação de existência do usuário na base de dados (Google Sheets).

- Lógica de Negócio: Separação de rotas para informações da clínica, agendar, remarcar ou cancelar.

- Finalização: Atualização da planilha para o status "Ocupado" e disparo de notificações.

# Como visualizar este projeto:
1.Crie uma conta no n8n.io.

2.Importe o arquivo Versao_final.json presente neste repositório.

3.Configure suas credenciais de API para Telegram, Google Sheets e Gmail.

# Imagem do fluxo completo
<img width="871" height="400" alt="Captura de tela 2025-12-17 225220" src="https://github.com/user-attachments/assets/f2bb8624-0703-48ec-8098-7fc87ae9a091" />

