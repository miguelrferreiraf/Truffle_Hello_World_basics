# Truffle_Hello_World

Este repositório contém um projeto simples de **contrato inteligente em Solidity**, com ambiente de testes e deploy utilizando **Truffle**.  
Ele é baseado no livro *Hands-On Smart Contract Development with Solidity and OpenZeppelin*, mas com ajustes para funcionar em versões mais recentes das ferramentas.

---

## 📌 Objetivo do Projeto

O projeto demonstra o ciclo completo de desenvolvimento de um contrato inteligente:

- Criação de um contrato Solidity básico (`Greeter`).
- Implementação de funcionalidades com **TDD (Test-Driven Development)**.
- Escrita de testes automatizados em **JavaScript**.
- Deploy do contrato via **Truffle**.
- Base para futura integração com uma **interface web (UI)**.

---

## ⚙️ Funcionalidades

O contrato `Greeter` possui:

- Uma mensagem inicial de saudação (`"Hello, World!"`).
- Getter `greet()` para retornar a mensagem.
- Setter `setGreeting(string)` para atualizar a saudação.
- Controle de acesso via `onlyOwner`, garantindo que apenas o criador do contrato possa atualizar a saudação.
- Função `owner()` que retorna o endereço da conta que realizou o deploy.

Os testes (`test/greeter_test.js`) validam:

1. Se o contrato é deployado corretamente.  
2. Se a função `greet()` retorna `"Hello, World!"`.  
3. Se a função `owner()` retorna o endereço do deployer.  
4. Se apenas o `owner` pode atualizar a saudação.  

---
## 📂 Estrutura do Projeto

greeter/
├─ contracts/
│ └─ Greeter.sol # Contrato principal
├─ migrations/
│ └─ 2_deploy_greeter.js # Script de deploy do contrato
├─ test/
│ └─ greeter_test.js # Testes em JavaScript
└─ README.md # Este arquivo


---

## 🚀 Como Executar

### 1. Clone o repositório
```
git clone https://github.com/<seu-usuario>/Truffle_Hello_World.git
cd Truffle_Hello_World
```

### 2. Instale as dependências

Certifique-se de ter o Node.js (>= 18.x) e o Truffle instalados:
```
npm install -g truffle
```

### 3. Compile os contratos
```
truffle compile
```
### 4. Rode os testes
```
truffle test
```
📖 Referência

Projeto inspirado no livro:
Hands-On Smart Contract Development with Solidity and OpenZeppelin (Kevin Solorio, Randall Kanna, David H. Hoover).

