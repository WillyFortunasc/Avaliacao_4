# Sistema de Tarefas com Prazo - Django

Atividade desenvolvida com Django + Bootstrap 5  
Entrega: Sistema de gerenciamento de tarefas com prazo e status de conclusão.

## Funcionalidades Implementadas

- [x] Listagem de tarefas  
- [x] Adicionar nova tarefa com título e prazo (opcional)  
- [x] Marcar/desmarcar como concluída com checkbox bonito  
- [x] Tarefas com prazo vencido ficam em vermelho automaticamente  
- [x] Tarefas concluídas ficam riscadas e não aparecem em vermelho (mesmo com prazo vencido)  
- [x] Excluir tarefa com confirmação  
- [x] Design moderno e responsivo (funciona no celular)  
- [x] Ícones profissionais com Bootstrap Icons  

## Requisitos Atendidos (exatamente como pedido pelo professor)

> "Modifique para que as tarefas sejam listadas, com um checkbox definindo se está ativa ou concluída (check marcado).  
> Também modifique para que sejam verificadas as datas de término da tarefa. Se a data for menor que a data atual do sistema, coloque a tarefa em vermelho."

100% atendido:
- Checkbox funcional (círculo vazio → círculo verde com check)
- Verificação automática de prazo vencido usando `timezone.now()`
- Apenas tarefas não concluídas com prazo vencido ficam vermelhas

## Capturas de Tela

<img src="screenshots/tela_principal.png" alt="Tela principal" width="100%"/>
<br><br>
<img src="screenshots/tarefa_vencida.png" alt="Tarefa com prazo vencido em vermelho" width="100%"/>
<br><br>
<img src="screenshots/tarefa_concluida.png" alt="Tarefa concluída (riscada e sem vermelho)" width="100%"/>

## Como Rodar o Projeto

1. Certifique-se de ter Python 3.9+ e Poetry instalados
2. Clone ou copie o projeto
3. Entre na pasta:
   ```bash
   cd tarefas

Ative o ambiente e instale dependências:Bashpoetry install
poetry shell
Configure o banco MySQL (ou use SQLite para teste rápido):SQLCREATE DATABASE db_tarefas CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
Aplique as migrações:Bashpython manage.py makemigrations
python manage.py migrate
Crie um superusuário (opcional, para acessar /admin):Bashpython manage.py createsuperuser
Inicie o servidor:Bashpython manage.py runserver
Acesse: http://127.0.0.1:8000

Tecnologias Utilizadas

Django 4.1+
Bootstrap 5.3 + Bootstrap Icons
MySQL (configurável via .env)
Poetry para gerenciamento de dependências
Python-dotenv para variáveis de ambiente

Estrutura do Projeto
texttarefas/
├── config/              # Configurações do Django
├── tarefas_app/         # App principal
│   ├── models.py        # Modelo Tarefa com prazo_vencido()
│   ├── views.py         # Lógica de toggle e exclusão
│   └── templates/       # HTML com Bootstrap
├── templates/           # base.html e lista_tarefas.html
├── .env                 # Configurações do banco
└── README.md            # Este arquivo
Autor
Seu Nome Aqui
Disciplina: Desenvolvimento Web com Python/Django
Data: Dezembro 2025
