# 💻 Sistema de Gerenciamento de Dispositivos

Aplicação em console Java desenvolvida para realizar o cadastro, listagem, busca e alteração de estado (ligar/desligar) de dispositivos de hardware e rede (Computadores, Impressoras e Roteadores), além de gerar um relatório estatístico de encerramento.

---

## 🚀 Funcionalidades

- **Cadastro de Dispositivos:**
  - **Computador:** Nome, código, fabricante, quantidade de RAM e sistema operacional.
  - **Impressora:** Nome, código, fabricante, tipo de tinta e velocidade de impressão.
  - **Roteador:** Nome, código, fabricante, quantidade de portas e velocidade de rede.
- **Gerenciamento:**
  - Listagem geral de todos os dispositivos cadastrados.
  - Consulta detalhada de um dispositivo por código.
  - Alteração do status de funcionamento (*Ligar* / *Desligar*).
- **Relatório de Encerramento:**
  - Exibição do total de equipamentos e percentual por tipo de dispositivo.

---

## 🛠️ Tecnologias e Conceitos

- **Linguagem:** Java (JDK 17 ou superior)
- **Orientação a Objetos:** Herança, Polimorfismo, Encapsulamento e Abstração
- **Estruturas de Dados:** `ArrayList<Dispositivo>` para manipulação em memória
- **Entrada e Saída:** `Scanner` centralizado e com tratamento de validação de dados

---

## 📂 Estrutura do Projeto

```text
src/
 ├── App.java           # Classe principal (Menu, controle de fluxo e I/O)
 ├── Dispositivo.java   # Classe base (Superclasse)
 ├── Computador.java    # Subclasse de Dispositivo
 ├── Impressora.java    # Subclasse de Dispositivo
 └── Roteador.java      # Subclasse de Dispositivo
```
## 🧠 Princípios de Clean Code Aplicados

1. **Nomes Significativos e Intuitivos (*Meaningful Names*):**
   - Nomes autodescritivos para variáveis (`quantidadeRAM`, `sistemaOperacional`) e métodos (`cadastrarComputador()`, `listarDispositivos()`).
   
2. **Princípio da Responsabilidade Única (*Single Responsibility Principle - SRP*):**
   - Métodos pequenos e focados em apenas uma tarefa específica (ex: `exibirMenu()`, `cadastrarRoteador()`, `lerInteiro()`).

3. **Evitação de Duplicação (*DRY - Don't Repeat Yourself*):**
   - Funções utilitárias de leitura (`lerTexto()` e `lerInteiro()`) que encapsulam a validação e limpeza de buffer do `Scanner`, prevenindo repetição de código ao longo do projeto.

4. **Polimorfismo e Abstração:**
   - Uso de uma coleção genérica `ArrayList<Dispositivo>` para gerenciar objetos derivados (`Computador`, `Impressora`, `Roteador`) de forma unificada.

5. **Código Autoexplicativo (*Self-Documenting Code*):**
   - A estrutura e a clareza dos nomes reduzem a necessidade de comentários explicativos, mantendo a leitura limpa e direta.
