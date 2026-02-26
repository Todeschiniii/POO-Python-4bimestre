# 📊 Sistema de Geração de Boletins Escolares em HTML

> Automação completa para leitura de notas em Excel e geração de páginas HTML individuais por aluno, com formatação visual inteligente e exportação para PDF.

---

# 📑 Sumário

- [📌 Sobre o Projeto](#-sobre-o-projeto)
- [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [⚙️ Funcionalidades Principais](#️-funcionalidades-principais)
- [🧠 Lógica e Arquitetura](#-lógica-e-arquitetura)
- [📂 Estrutura do Projeto](#-estrutura-do-projeto)
- [📈 Exemplo de Dados](#-exemplo-de-dados)
- [🖥️ Exemplo de Saída HTML](#️-exemplo-de-saída-html)
- [⚙️ Como Executar](#️-como-executar)
- [📊 Diferenciais Técnicos](#-diferenciais-técnicos)
- [🚀 Melhorias Futuras](#-melhorias-futuras)
- [👨‍💻 Autor](#-autor)
- [📄 Licença](#-licença)

---

# 📌 Sobre o Projeto

Este projeto automatiza o processo de geração de boletins escolares a partir de uma planilha Excel.

O sistema:

- 📥 Lê dados diretamente de um arquivo `.xlsx`
- 📊 Organiza e exibe notas no terminal com PrettyTable
- 🌐 Gera uma página HTML individual para cada aluno
- 🎨 Aplica formatação visual automática baseada na nota
- 🖨️ Permite exportação para PDF via navegador

Cada aluno recebe um arquivo HTML personalizado contendo:

- Código
- Nome
- Turma
- Notas por disciplina
- Média final formatada com destaque visual

---

# 🚀 Tecnologias Utilizadas

- Python 3
- Pandas
- PrettyTable
- HTML5
- CSS3
- Manipulação de arquivos (os)

Instalação das dependências:

```bash
pip install pandas prettytable openpyxl
```

---

# ⚙️ Funcionalidades Principais

## 📥 Leitura Inteligente do Excel

- Padronização automática de nomes de colunas
- Identificação dinâmica da coluna de MÉDIA
- Detecção automática das disciplinas

---

## 🎨 Formatação Visual Automática

As notas recebem cores automaticamente:

| Condição | Cor |
|----------|------|
| Nota < 6.0 | 🔴 Vermelho |
| Nota ≥ 6.0 | 🔵 Azul |
| Não informada | ⚪ Cinza |

---

## 📄 Geração de HTML Individual

Para cada aluno é criado:

```
paginas_alunos/
    504207.html
    5040401.html
    5040710.html
```

Cada página contém:

- Layout centralizado
- Tabela estilizada
- Destaque nas notas
- Botão para gerar PDF
- Design responsivo simples e limpo

---

## 🖨️ Exportação para PDF

O botão:

```
Gerar PDF
```

Utiliza:

```javascript
window.print()
```

Permitindo salvar diretamente como PDF pelo navegador.

---

# 🧠 Lógica e Arquitetura

Fluxo do sistema:

```
Excel (.xlsx)
      ↓
Pandas DataFrame
      ↓
Identificação de disciplinas
      ↓
Exibição no terminal (PrettyTable)
      ↓
Geração de HTML personalizado
      ↓
Exportação opcional para PDF
```

---

# 📂 Estrutura do Projeto

```
📁 projeto/
│
├── alberson.xlsx
├── script.py
└── 📁 paginas_alunos/
      ├── 504207.html
      ├── 5040401.html
      └── 5040710.html
```

---

# 📈 Exemplo de Dados

Planilha de entrada:

| Código | Aluno | TURMA | IPC | LE | REDES | JOGOS | SC | MÉDIA AT FINAL |
|--------|-------|-------|-----|----|-------|-------|----|----------------|
| 504207 | Davi  | 2IID  | 7   | 8  | 0     | 10    | 6  | 6.2 |
| 5040401| Nicolas| 2IID | 1   | 1.5| 0.5   | 2     | 2  | 1.4 |
| 5040710| Kaique | 2IID | 1   | 2  | 3     | 2     | 4  | 2.4 |

---

# 🖥️ Exemplo de Saída HTML

Cada página gerada contém:

- Cabeçalho com nome e código
- Tabela estilizada
- Notas coloridas dinamicamente
- Média final destacada
- Botão para exportação

Estrutura visual:

```
Aluno: Nome (Código: XXXX) - Turma: 2IID

-----------------------------------
| Disciplina | Nota              |
-----------------------------------
| IPC        | 🔵 7.0            |
| LE         | 🔵 8.0            |
| REDES      | 🔴 0.0            |
| ...        | ...               |
-----------------------------------
| MÉDIA AT FINAL | 🔵 6.2        |
-----------------------------------
```

---

# ⚙️ Como Executar

1️⃣ Coloque seu arquivo Excel na raiz do projeto  
2️⃣ Ajuste o nome do arquivo na variável:

```python
arquivo_excel = "alberson.xlsx"
```

3️⃣ Execute:

```bash
python script.py
```

4️⃣ Os arquivos HTML serão gerados automaticamente na pasta:

```
paginas_alunos/
```

---

# 📊 Diferenciais Técnicos

- Identificação dinâmica da coluna de média
- Sistema flexível para qualquer número de disciplinas
- Separação clara de responsabilidades
- Código organizado e legível
- Geração automatizada de múltiplos arquivos
- Aplicação prática de Pandas para automação real
- Integração entre Python e frontend (HTML/CSS)

---

# 🚀 Melhorias Futuras

- Envio automático por e-mail
- Dashboard web com Flask ou FastAPI
- Autenticação por login
- Upload de Excel via interface
- Geração automática de PDF via backend
- Hospedagem em servidor cloud

---

# 👨‍💻 Autor

**Seu Nome Aqui**

Desenvolvedor focado em:

- Automação com Python
- Manipulação de dados
- Integração backend + frontend
- Geração dinâmica de relatórios
- Estruturação de sistemas escaláveis

---

# 📄 Licença

Projeto desenvolvido para fins educacionais.

---

# # 👥 Créditos & contatos

1. <b>Mateus Todeschini</b> - GitHub: https://github.com/Todeschiniii<br>
2. <b>Heitor Pinheiro</b> - GitHub: https://github.com/HeitorPinheiro11<br>
3. <b>Davi Dancuart<b> - GitHub: https://github.com/DaviDancuart<br>

Repositório: https://github.com/AEV-autoescola-Virtual/Simulador-de-Carro-teste
