# 📌 Projeto: Sistema de Veículos - Desenvolvimento Colaborativo com GitHub

Este repositório contém um projeto simples de **herança em Java**, desenvolvido por uma equipe utilizando **Git e GitHub** com um fluxo estruturado de branches (`main` e `dev`).

---

## 🚀 Objetivo
- Implementar um **sistema de veículos usando herança** em Java.
- Trabalhar em equipe utilizando **GitHub Flow** (3 alunos).
- Utilizar **branches, pull requests e merges** corretamente.

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

2. O dono do repositório deve ir até **Settings > Collaborators** e adicionar os colegas como **colaboradores**.

---

### 2️⃣ Clonar o Repositório e Criar a Branch `dev`
1. Todos os alunos devem clonar o repositório:

   ```sh
   git clone <URL_DO_REPOSITORIO>
   cd sistema-veiculos
   
2. O aluno responsável pelo repositório cria a branch dev e a envia para o GitHub:

   ```sh
   git checkout -b dev
   git push origin dev
   
3. Todos os membros devem atualizar o repositório local para incluir a nova branch:

   ```sh
   git pull origin dev

Todos devem trabalhar na branch dev.

---

## 🛠️ Implementação do Código

Cada aluno criará uma **branch individual ** para sua feature e fará um pull request para dev.
### 1️⃣ Criar a Classe Veiculo (Aluno 1)

1. Criar uma nova branch:

   ```sh
   checkout -b feature/veiculo

2. Criar o arquivo **Veiculo.java** com o seguinte código:

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
3. Enviar para o GitHub:

   ```sh
   
   git add Veiculo.java
   git commit -m "Adiciona classe base Veiculo"
   git push origin feature/veiculo

4. Criar um **pull request para dev** no GitHub.

### 2️⃣ Criar a Classe Carro (Aluno 2)

1. Criar uma nova branch:

   ```sh
   git checkout -b feature/carro

2. Criar o arquivo **Carro.java** com o seguinte código:

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

3. Enviar para o GitHub:

   ```sh
   git add Carro.java
   git commit -m "Adiciona classe Carro"
   git push origin feature/carro

4. Criar um **pull request para dev** no GitHub.


### 3️⃣ Criar a Classe Moto (Aluno 3)

1. Criar uma nova branch:

   ```sh
   git checkout -b feature/moto

2. Criar o arquivo Moto.java com o seguinte código:

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

3. Enviar para o GitHub:

   ```sh
   git add Moto.java
   git commit -m "Adiciona classe Moto"
   git push origin feature/moto

4. Criar um **pull request para dev** no GitHub.
