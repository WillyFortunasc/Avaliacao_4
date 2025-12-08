# Sistema de Tarefas com Prazo - Django

Atividade de Django que atende 100% aos requisitos do professor.

## Requisitos Atendidos

- Tarefas listadas com checkbox para marcar como ativa ou concluída (check marcado = concluída)  
- Verificação automática da data de término (prazo)  
- Tarefas com prazo vencido ficam em vermelho (somente se não estiverem concluídas)  
- Tarefas concluídas ficam riscadas e não aparecem em vermelho mesmo com prazo vencido  
- Adicionar, marcar/desmarcar e excluir tarefas  
- Design moderno, responsivo e com ícones profissionais

## Funcionalidades Extras (Bônus)

- Checkbox com animação bonita (círculo vazio → círculo verde com check)  
- Confirmação antes de excluir  
- Mensagem amigável quando não há tarefas  
- Total de tarefas exibido no cabeçalho  
- Exibe a data de hoje no rodapé  
- Totalmente responsivo (funciona no celular)

## Capturas de Tela

![Tela principal](screenshots/tela_principal.png)
![Tarefa vencida em vermelho](screenshots/tarefa_vencida.png)
![Tarefa concluída](screenshots/tarefa_concluida.png)

## Como Executar o Projeto

```bash
# 1. Entre na pasta do projeto
cd tarefas

# 2. Ative o ambiente Poetry
poetry shell

# 3. Instale as dependências (caso ainda não tenha feito)
poetry install

# 4. Crie o banco de dados (MySQL)
CREATE DATABASE db_tarefas CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

# 5. Aplique as migrações
python manage.py makemigrations
python manage.py migrate

# 6. (Opcional) Crie um superusuário para acessar o admin
python manage.py createsuperuser

# 7. Inicie o servidor
python manage.py runserver
Acesse: http://127.0.0.1:8000
Tecnologias Utilizadas

Python 3.9+
Django ~= 4.1.0
Bootstrap 5.3 + Bootstrap Icons
MySQL
Poetry
python-dotenv

Estrutura Principal
texttarefas/
├── config/                  
├── tarefas_app/             
├── templates/               
├── .env                     
├── manage.py
└── README.md                
Autor
[Seu Nome Completo Aqui]
Disciplina: Desenvolvimento Web com Django
Data: Dezembro 2025