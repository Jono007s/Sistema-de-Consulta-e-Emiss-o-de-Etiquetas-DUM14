# Sistema-de-Consulta-e-Emiss-o-de-Etiquetas-DUM14
Aplicação web em Flask para consulta e emissão de etiquetas DUM14, integrada ao ERP CIGAM e compatível com qualquer sistema baseado em SQL Server.

📘 Descrição detalhada (para o README.md)
🧩 Sobre o projeto

O Sistema de Consulta e Emissão de Etiquetas DUM14 foi desenvolvido para otimizar o processo de identificação e rotulagem de produtos em ambientes industriais e logísticos.
A aplicação realiza a consulta de informações de produtos diretamente do banco de dados SQL Server e gera etiquetas no formato DUM14, prontas para impressão em impressoras térmicas compatíveis com o padrão ZPL.

Embora o foco inicial tenha sido a integração com o ERP CIGAM, o sistema é totalmente adaptável para qualquer ERP ou base de dados SQL que possua estrutura semelhante.

⚙️ Principais funcionalidades

🔍 Consulta automática de informações de produtos por código DUM14

🏷️ Geração de etiquetas personalizadas com dados do produto e código de barras (EAN/DUN)

🖨️ Impressão direta em impressoras industriais (Zebra, Argox, Datamax, entre outras)

💾 Integração com bancos de dados SQL Server

🧠 Conversão automática para ZPL (Zebra Programming Language)

🎨 Layout configurável conforme modelo de etiqueta utilizado

🌐 Interface web leve e responsiva desenvolvida em Flask

🧱 Tecnologias utilizadas

Python (Flask)

SQL Server (PyODBC)

ZPL / PDF (ReportLab)

HTML, CSS e JavaScript

Windows (ambiente de execução local)

📂 Estrutura geral
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

💡 Observações

Este projeto foi projetado para uso interno, priorizando desempenho, estabilidade e compatibilidade com diferentes infraestruturas de ERP baseadas em SQL Server.
O código é modular, permitindo a personalização do layout de etiquetas, conexões e fluxos de impressão conforme a necessidade de cada empresa.
