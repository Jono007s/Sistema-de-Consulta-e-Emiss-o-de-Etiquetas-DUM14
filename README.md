# 🏷️ Sistema de Consulta e Emissão de Etiquetas DUM14

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-lightgrey)
![SQL%20Server](https://img.shields.io/badge/Database-SQL%20Server-red)
![ZPL](https://img.shields.io/badge/Printer-ZPL%20Compatible-green)

---

## 🧩 Sobre o projeto

O **Sistema de Consulta e Emissão de Etiquetas DUM14** foi desenvolvido para otimizar o processo de **identificação e rotulagem de produtos** em ambientes industriais e logísticos.

A aplicação realiza **consultas diretas no banco de dados SQL Server** e gera etiquetas personalizadas no formato **DUM14**, prontas para impressão em impressoras térmicas compatíveis com o padrão **ZPL**.

Embora o foco inicial de desenvolvimento tenha sido a integração com o **ERP CIGAM**, o sistema é **totalmente compatível com qualquer ERP baseado em SQL Server**.

---

## ⚙️ Funcionalidades principais

- 🔍 **Consulta automática** de informações de produtos por código DUM14  
- 🏷️ **Geração de etiquetas personalizadas** com dados do produto e código de barras (EAN/DUN)  
- 🖨️ **Impressão direta** em impressoras industriais (Zebra, Argox, Datamax etc.)  
- 💾 **Integração com bancos de dados SQL Server**  
- 🧠 **Conversão automática para ZPL** (Zebra Programming Language)  
- 🎨 **Layout configurável** conforme o modelo de etiqueta utilizado  
- 🌐 **Interface web responsiva** desenvolvida em Flask  

---

## 🧱 Tecnologias utilizadas

| Categoria | Tecnologia |
|------------|-------------|
| Backend | [Python 3.10+](https://www.python.org/) |
| Framework Web | [Flask](https://flask.palletsprojects.com/) |
| Banco de Dados | [Microsoft SQL Server](https://www.microsoft.com/sql-server) |
| Driver SQL | [PyODBC](https://pypi.org/project/pyodbc/) |
| Geração de PDF | [ReportLab](https://pypi.org/project/reportlab/) |
| Impressão | ZPL (Zebra Programming Language) |
| Frontend | HTML • CSS • JavaScript |

---

## 📂 Estrutura de diretórios

```
/static/
  ├─ css/
  ├─ js/
  └─ img/

/templates/
  ├─ index.html
  └─ layout.html

/app/
  ├─ dum14.py
  ├─ utils.py
  └─ config.py

/logs/
  └─ system.log
```

---

## 🚀 Instalação e configuração

### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/usuario/sistema-dum14.git
cd sistema-dum14
```

### 2️⃣ Criar e ativar o ambiente virtual
```bash
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # Linux / Mac
```

### 3️⃣ Instalar as dependências
```bash
pip install -r requirements.txt
```

### 4️⃣ Configurar o banco de dados
Edite o arquivo `config.py` e adicione suas credenciais:
```python
DB_CONFIG = {
    "server": "SEU_SERVIDOR_SQL",
    "database": "NOME_DO_BANCO",
    "username": "USUARIO",
    "password": "SENHA"
}
```

### 5️⃣ Executar o servidor
```bash
python app/dum14.py
```

Acesse no navegador:
```
http://localhost:5000
```

---

## 🖨️ Exemplo de uso

1. Digite o **código DUM14** do produto.  
2. O sistema consulta automaticamente os dados no banco.  
3. Clique em **Gerar Etiqueta** para visualizar e imprimir.  
4. A etiqueta é convertida para **ZPL** e enviada à impressora configurada.

---

## 🧾 Layout da etiqueta

As etiquetas seguem o modelo padrão industrial, com:
- Código DUM14
- Descrição do produto
- EAN / DUN (código de barras)
- Lote, linha e informações adicionais
- Identificação do operador e data de emissão  

O layout é configurável e pode ser ajustado conforme o padrão da empresa (85x50 mm, 100x75 mm, etc).

---

## 🧠 Arquitetura simplificada

```
[Usuário Web]
     │
     ▼
[Flask App] → [SQL Server]
     │
     ▼
[ZPL / PDF Gerado]
     │
     ▼
[Impressora Industrial]
```

---

## 🪶 Objetivo

Este sistema foi criado para:
- Reduzir o tempo de emissão de etiquetas;
- Padronizar informações de produto;
- Integrar diretamente com o banco de dados corporativo;
- Garantir compatibilidade com impressoras industriais baseadas em ZPL.

---

## 💡 Autor

**Desenvolvido por João Pedro Cardoso**  
💼 Consultor e desenvolvedor de soluções em automação industrial e ERP  
📧 joaopedro.vieiracardoso6@gmail.com
🌎 https://www.linkedin.com/in/joa0o/
