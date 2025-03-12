# 📌 Projeto: Sistema de Veículos - Desenvolvimento Colaborativo com GitHub

Este repositório contém um projeto simples de **herança em Java**, desenvolvido por uma equipe utilizando **Git e GitHub** com um fluxo estruturado de branches (`main` e `dev`).

---

## 🚀 Objetivo
- Implementar um **sistema de veículos usando herança** em Java.
- Trabalhar em equipe utilizando **GitHub Flow**.
- Utilizar **branches, pull requests e merges** corretamente.

---
## 📕 Instruções Gerais
- Formem um grupo de **três alunos**.
- Criem um repositório no GitHub e cada membro deve **clonar** o projeto.
Cada aluno será responsável por uma classe específica no projeto.
- Devem criar **branches individuais** para suas implementações e usar **pull requests ** para mesclar o código na branch principal (main).
- No final, um dos membros deve rodar o código principal para validar se tudo está funcionando corretamente.

---

## 🔧 Configuração do Repositório

### 1️⃣ Criar o Repositório no GitHub
1. Um dos alunos deve criar um repositório no **GitHub**:
   - Vá para [GitHub](https://github.com).
   - Clique em **New repository**.
   - Escolha um nome (exemplo: `sistema-veiculos`).
   - Selecione **Public** ou **Private**.
   - Marque **Add a README file**.
   - Clique em **Create repository**.

2. O dono do repositório deve ir até **Settings > Collaborators** e adicionar os colegas como **colaboradores**. Os alunos convidados receberão um e-mail e devem aceitar o convite.

---
### 2️⃣ Criar a Branch dev

1. No repositório, vá até a aba **Code**.
2. Clique no botão **Main** (onde está a branch atual).
3. Digite dev e clique em **Create branch: dev from main**.
4. Agora os alunos vão trabalhar na branch dev antes de integrar à main.
   
---
## 🛠️ Implementação do Código

Cada aluno criará uma **branch individual ** para sua feature e abrir um pull request para dev.

### 1️⃣ Criar a Classe Veiculo (Aluno 1)

1. No GitHub, vá até a aba **Code**.
2. No repositório, clique em **Add file > Create new file**.
3. Nomeie o arquivo como **Veiculo.java**.
4. Cole o seguinte código:

   ```java
   public class Veiculo {
       protected String marca;
       protected String modelo;
       protected int ano;
   
       public Veiculo(String marca, String modelo, int ano) {
           this.marca = marca;
           this.modelo = modelo;
           this.ano = ano;
       }
   
       public void exibirInfo() {
           System.out.println("Marca: " + marca + ", Modelo: " + modelo + ", Ano: " + ano);
       }
   }
   ```
5. **Antes de salvar**, clique em ** Create a new branch**.
    - Nomeie a branch como **feature/veiculo**.
    - Clique em **Propose new file**.
6. Clique em **Create pull request** e direcione-o para a branch dev.
7. Aguarde os colegas revisarem e aprovarem.

### 2️⃣ Criar a Classe Carro (Aluno 2)

1. No GitHub, vá até a aba **Code>dev**.
2. No repositório, clique em **Add file > Create new file**.
3. Nomeie o arquivo como **Carro.java**.
4. Cole o seguinte código:
   ```java  
   public class Carro extends Veiculo {
       private int portas;
   
       public Carro(String marca, String modelo, int ano, int portas) {
           super(marca, modelo, ano);
           this.portas = portas;
       }
   
       @Override
       public void exibirInfo() {
           super.exibirInfo();
           System.out.println("Número de portas: " + portas);
       }
   }
   ```

5. **Antes de salvar**, clique em **Create a new branch**.
   - Nomeie a branch como **feature/carro**.
   - Clique em **Propose new file**.
6. Clique em **Create pull request** e direcione-o para a branch dev.
7. Aguarde a revisão dos colegas.

### 3️⃣ Criar a Classe Moto (Aluno 3)

1. No GitHub, vá até a aba **Code>dev**.
2. No repositório, clique em **Add file > Create new file**.
3. Nomeie o arquivo como **Moto.java**.
4. Cole o seguinte código:

   ```java
   public class Moto extends Veiculo {
       private boolean partidaEletrica;
   
       public Moto(String marca, String modelo, int ano, boolean partidaEletrica) {
           super(marca, modelo, ano);
           this.partidaEletrica = partidaEletrica;
       }
   
       @Override
       public void exibirInfo() {
           super.exibirInfo();
           System.out.println("Possui partida elétrica: " + (partidaEletrica ? "Sim" : "Não"));
       }
   }
   ```

5. **Antes de salvar**, clique em **Create a new branch**.
   - Nomeie a branch como **feature/moto**.
   - Clique em **Propose new file**.
6. Clique em **Create pull request** e direcione-o para a branch dev.
7. Aguarde a revisão dos colegas.


## ✅ Revisão e Aprovação

Cada membro do grupo deve:

1. Ir até a aba **Pull requests**.
2. Revisar os códigos dos colegas.
3. Se estiver correto, clicar em **Merge pull request** para mesclar na dev.
4. **Após todos os merges em dev, um dos alunos deve abrir um pull request de dev para main**.
5. A equipe revisa o código antes de aprovar o merge final.

## 🚀 Criar a Classe Main e Testar

1. No GitHub, vá até a branch dev.
2. No repositório, clique em **Add file > Create new file**.
3. Nomeie o arquivo como **Main.java**.
4. Cole o seguinte código:
   ```java
   public class Main {
       public static void main(String[] args) {
           Carro carro = new Carro("Toyota", "Corolla", 2022, 4);
           Moto moto = new Moto("Honda", "CB 500", 2023, true);
   
           carro.exibirInfo();
           System.out.println();
           moto.exibirInfo();
       }
   }
   ```
5. Faça o **commit na branch dev**.
6. Abra um **pull request para main** e, após revisão, faça o merge.

## 🏁 Rodar o Código usando GitHub Codespaces

### Passo 1: Ativar Codespaces
1. Vá até seu repositório no GitHub.
2. Clique no botão **Code**.
3. Vá até a aba **Codespaces** e clique em **Create codespace on main**.

### Passo 2: Executar Código Java
No terminal do Codespaces, use os seguintes comandos:

1. Compilar o código:
   ```bash
   javac Main.java

2. Executar o código:
   ```bash
   java Main

