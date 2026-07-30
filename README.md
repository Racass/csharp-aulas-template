# Curso de C#

Repositório-modelo do curso de **C#** ministrado pelo **Prof. Cassiolato**.

Cada aula tem uma atividade prática. Este repositório mantém uma pasta
por aula em `sources/`. O objetivo é você acumular um portfólio de
exercícios versionado no seu GitHub ao longo das aulas.

---

## 🚀 Como começar

1. Clique em **"Use this template"** no topo do repositório (não use fork).
2. Dê um nome ao seu novo repositório (sugestão: `fiap-csharp`).
3. Clone localmente:
   ```
   git clone https://github.com/SEU-USUARIO/fiap-csharp
   cd fiap-csharp
   ```
4. Verifique o .NET SDK instalado:
   ```
   dotnet --version
   ```
   Se o comando não for reconhecido, instale o .NET SDK a partir de
   https://dot.net/download (qualquer versão suportada).

---

## 📁 Estrutura do repositório

```
/
├── .editorconfig            → regras de estilo do C# (aplicadas pela IDE)
├── .gitattributes           → fixa quebras de linha em LF
├── .gitignore               → padrão .NET
├── Directory.Build.props    → configurações aplicadas a todos os projetos
├── .github/workflows/       → CI (GitHub Actions)
└── sources/
    └── aula-NN/             → uma pasta por aula
```

---

## ✏️ Como adicionar a atividade de uma nova aula

No terminal, na raiz do repositório:

```
dotnet new console -o sources/aula-01
cd sources/aula-01
dotnet run
```

Isso cria um novo projeto de console dentro de `sources/aula-01/`.
Repita com `aula-02`, `aula-03`, etc.

---

## ✅ Verificação automática (CI)

Toda vez que você fizer `push`, o **GitHub Actions** roda:

1. **Build** de todos os projetos em `sources/`
2. **Verificação de formatação** (`dotnet format --verify-no-changes`)

Se o build ou a formatação falharem, você verá um ❌ nos seus commits.
Um ✅ verde significa que o código está limpo e compilando.

Isso simula um pipeline real de integração contínua usado em empresas —
tê-lo funcionando no seu GitHub é ótimo para o portfólio.

---

## 🔧 IDE

O curso utiliza o **Visual Studio 2022 ou 2026**.

- O `.editorconfig` deste repositório é aplicado automaticamente pelo Visual Studio ao salvar.

---

## 📚 Guia rápido de estilo (aplicado pelo `.editorconfig`)

- `PascalCase` — classes, métodos, propriedades, enums
- `camelCase` — variáveis locais e parâmetros
- `_camelCase` — campos privados
- `IPascalCase` — interfaces sempre começam com `I`
- 4 espaços de indentação
- Chaves sempre em nova linha em métodos e classes
- `using` fora do `namespace`, ordenados com `System` primeiro
- Valores monetários usam `decimal` (nunca `double`)

Sua IDE aplica essas regras automaticamente ao salvar.

---

## 🆘 Problemas comuns

**"`dotnet` não é reconhecido"**
→ Instale o .NET SDK (qualquer versão suportada): https://dot.net/download

**"Erro de encoding" ao clonar**
→ Configure git para usar LF:
```
git config --global core.autocrlf input
```

**"Meu commit apareceu com nome errado"**
→ Configure git com seu email do GitHub:
```
git config --global user.name "Seu Nome"
git config --global user.email "voce@exemplo.com"
```

---

*Bom código.*
