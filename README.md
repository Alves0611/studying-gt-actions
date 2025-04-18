# 📦 GitHub Actions – Workflow com Inputs para Release e Deploy

Este repositório contém um exemplo prático de um workflow GitHub Actions que utiliza **inputs personalizados** via `workflow_dispatch`, ideal para realizar deploys controlados e criar versões customizadas de uma aplicação.

---

## 🚀 O que este workflow faz?

Este workflow permite que você inicie manualmente uma execução e forneça os seguintes **inputs**:

| Input         | Tipo     | Obrigatório | Descrição                          |
|---------------|----------|-------------|------------------------------------|
| `versao`      | string   | ✅ Sim       | Versão da nova release             |
| `fazer_deploy`| boolean  | ✅ Sim       | Se deve ou não executar o deploy   |
| `ambiente`    | escolha  | ✅ Sim       | Ambiente de destino (`dev` ou `prod`) |

---

## 🧠 Como funciona

1. Os inputs são definidos no `workflow_dispatch`, permitindo execução manual via GitHub.
2. Os valores são extraídos e convertidos em variáveis de ambiente.
3. Os valores são impressos no log para conferência.
4. O deploy é executado **apenas se** `fazer_deploy` for `true`.

---

## 📂 Estrutura do repositório

```bash
.github/
└── workflows/
    └── estudando-input.yml
README.md
