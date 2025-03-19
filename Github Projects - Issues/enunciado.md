# 🎮 Desenvolvimento Colaborativo: Personagens de um Jogo

## 📌 Objetivo

Esse projeto consiste em desenvolver um **sistema de personagens para um jogo**, utilizando **herança** e organizando o trabalho em equipe com **GitHub Issues e GitHub Projects**.  

A equipe deverá:
- Criar um **GitHub Project Board** para gerenciar as tarefas.
- Criar **Issues** para cada funcionalidade do projeto.
- Trabalhar em **branches individuais** e utilizar **Pull Requests**.
- Implementar um **sistema de personagens usando herança** em Java.

---

## 🎯 **Passo 1 – Criar o Repositório e Configurar GitHub Projects**

### 1️⃣ Criar o Repositório
- Um dos alunos cria um **novo repositório** no GitHub.
- Adiciona os colegas como **colaboradores**.

### 2️⃣ Criar um GitHub Project
- Vá até a aba **Projects** do repositório e clique em **"New Project"**.
- Escolha **"Board" (Kanban)** e nomeie como **"Desenvolvimento dos Personagens"**.
- Adicione **três colunas**:
  - **To Do** → Tarefas a serem iniciadas
  - **In Progress** → Tarefas em andamento
  - **Done** → Tarefas concluídas

---

## 📌 **Passo 2 – Criar Issues para Cada Parte do Código**

Cada aluno será responsável por uma parte do código e deverá criar uma **Issue** correspondente no GitHub.

### 📌 **Lista de Issues**
1️⃣ **Criar a superclasse `Personagem`**  
   - **Título:** Criar a classe base `Personagem`  
   - **Descrição:** Implementar a classe base com atributos comuns como `nome`, `vida` e `forca`.  
   - **Labels:** `feature`, `back-end`  
   - **Atribuído a:** Aluno 1  

2️⃣ **Criar a subclasse `Guerreiro`**  
   - **Título:** Criar a classe `Guerreiro`  
   - **Descrição:** Implementar a classe `Guerreiro`, herdando de `Personagem` e adicionando o atributo `espada`.  
   - **Labels:** `feature`, `back-end`  
   - **Atribuído a:** Aluno 2  

3️⃣ **Criar a subclasse `Mago`**  
   - **Título:** Criar a classe `Mago`  
   - **Descrição:** Implementar a classe `Mago`, herdando de `Personagem` e adicionando o atributo `mana`.  
   - **Labels:** `feature`, `back-end`  
   - **Atribuído a:** Aluno 3  

4️⃣ **Criar a classe `Main` para testes**  
   - **Título:** Criar a classe `Main.java`  
   - **Descrição:** Criar um programa principal para instanciar e testar `Guerreiro` e `Mago`.  
   - **Labels:** `test`, `back-end`  
   - **Atribuído a:** Qualquer aluno  

Cada Issue deve ser **movida para a coluna "To Do" no GitHub Project**.

---

## 🏗️ **Passo 3 – Implementação no GitHub com Issues e Branches**

Cada aluno seguirá este fluxo:

1. **Criar uma branch para sua tarefa**
   ```sh
   git checkout -b feature/nome-da-classe
2. **Implementar sua parte do código**
3. **Enviar as alterações**
    ```sh
    git add .
    git commit -m "Adiciona a classe NomeDaClasse"
    git push origin feature/nome-da-classe
    ```
4. **Criar um Pull Request para a branch dev**
No GitHub, abrir um Pull Request e vincular à Issue correspondente.
5. **Mover a Issue para "In Progress" no GitHub Project**
6. **Após aprovação, fazer merge na branch dev**
7. **Mover a Issue para "Done" no GitHub Project**


## 🏗️ **Passo 4 – Revisão e Merge para main**
- Quando todas as Issues forem concluídas e mescladas na dev, um dos alunos cria um Pull Request de dev para main.
- O grupo revisa o código antes do merge final.

## 🏗️ **Passo 5 – Criar a Classe Main e Testar**

1. Criar uma nova branch:

    ```sh
    git checkout -b feature/main
    ```
2. Criar o arquivo Main.java e adicionar o código:
    
    ```java
    public class Main {
        public static void main(String[] args) {
            Guerreiro guerreiro = new Guerreiro("Arthur", 100, 20, "Espada Longa");
            Mago mago = new Mago("Merlin", 80, 10, 100);

            guerreiro.atacar();
            mago.atacar();
        }
    }
    ```

3. Adicionar, commitar e enviar para o GitHub:

    ```sh
    git add Main.java
    git commit -m "Adiciona classe Main para testes"
    git push origin feature/main
    ```
4. Criar um **pull request para dev**, revisar e mesclar.

5. Criar **um pull request de dev para main** e mesclar.

