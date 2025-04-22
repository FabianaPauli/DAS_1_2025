# Design e Arquitetura de Software

## Aula 26/02/25
[Livro Engenharia de Software Moderna - Capítulo 7](https://engsoftmoderna.info/cap7.html)

### Arquitetura de Software
Normalmente, o software possui a seguinte estrutura:
- **Frontend**
- **Backend**
- **Banco de Dados**

No **Java**, pacotes (*packages*) são pastas e são extremamente necessários para a organização de um projeto.

### Conceitos
- **Componente** → Uma função pronta utilizada para facilitar o trabalho, como `@GetMapping`, `@Controller`, `@Entity` no Java.
- **Módulos** → Representam como o software é dividido e como essas áreas/funções se comunicam por meio de interfaces, como chamadas de API REST.
- **Serviços** → Representam os casos de uso do sistema.

---

## Aula 27/06/25

### Model-View-Controller (MVC)
Arquitetura de software composta por:
- **Model** → Representa os dados que serão exibidos na tela.
- **View** → Responsável pela interface/tela do usuário.
- **Controller** → Controla e intermedia o fluxo de dados entre a interface e a lógica de negócios.

### Conceitos Relacionados
- **Entidade** → Classe que representa os dados processados e armazenados no banco.
- **Model** → Classe que representa os dados que chegam do banco e são apresentados na tela.
- **Selenium** → Ferramenta para testes de interface gráfica.

### Tipos de Arquitetura
- **Microsserviços** → Arquitetura baseada na divisão do software em módulos independentes.
- **Monolito** → Repositório único de código onde:
  - Todo o sistema está em um único lugar.
  - Utiliza uma única tecnologia.
  - É compilado e testado gerando um único pacote.
  - Executado como um único processo no sistema operacional.
  - Possui um único banco de dados.

---

## Aula 05/03/25

### **Big Ball of Mud**
Quando não há uma definição de arquitetura, sem padrão, resultando em um sistema desorganizado e difícil de manter.

### **Padrão Arquitetural**
Uma solução para um problema específico. Exemplo: **MVC** (*Model-View-Controller*), que separa as responsabilidades:
- **Model** → Dados
- **View** → Tela
- **Controller** → Comportamento

### **Estilo de Arquitetura**
Organização do projeto baseada em camadas:
- **Divisão de Responsabilidade**
- **Performance**
- **Segurança**
- **Manutenibilidade**
- **Camada de Apresentação**
  - Define requisitos visuais e de interação
- **Camada de Lógica de Negócios (Aplicação)**
  - Centraliza a definição e atualização das regras de negócio
  - Escala o backend para suportar requisições
- **Camada de Persistência (Banco de Dados)**
  - Utiliza banco de dados relacional, uma solução consolidada
  - Resolve problemas de concorrência
  - Permite compartilhamento de dados

### **Curiosidade**
O Linux e o Windows possuem uma arquitetura **monolítica**.

### **Gerenciamento de Memória em Linguagens de Programação**
- **C/C++** → Gerenciamento de memória manual (*full control*).
- **Rust** → Gerenciamento de memória mais seguro e automatizado.

### **Passagem de Parâmetros**
- **Passagem por Referência** → Envia a referência do valor, permitindo alteração direta.
- **Passagem por Valor** → Copia o valor para uma nova variável, sem alterar o original.

## Aula 06/03

[Leitura "Who Needs an Architect?" ](https://martinfowler.com/ieeeSoftware/whoNeedsArchitect.pdf)

## Aula 19/03/25

 - **Trade-off** → A mais escolhas, o famoso "Depende"
 - Obs: Protocolo OSI

 ## Aula 09/04 - Resumo – Capítulo: Características Arquiteturais

## 📌 O que são Características Arquiteturais?
São as qualidades ou atributos que um sistema de software precisa apresentar para atender às necessidades dos stakeholders, como desempenho, segurança e escalabilidade. Elas descrevem **"como"** o sistema se comporta, além de suas funcionalidades.

---

## 🧩 Categorias Principais de Características

1. **Características Funcionais**: Relacionadas ao que o sistema faz (exemplo: funcionalidade de login).
2. **Características Não Funcionais (Qualidade)**: Relacionadas ao comportamento do sistema, como:
   - **Desempenho**: Tempo de resposta, throughput.
   - **Segurança**: Proteção contra ataques, integridade dos dados.
   - **Escalabilidade**: Capacidade de aumentar recursos sem perder desempenho.
   - **Manutenibilidade**: Facilidade de alteração do sistema.

---

## 🛠️ Como Trabalhar com Características Arquiteturais?

### ✔️ **Cenários de Qualidade**:
Descrever as características com base em cenários que identificam as condições, ações e resultados esperados para medir o comportamento de uma característica.
- **Exemplo**: “Em um pico de 1000 usuários simultâneos, o sistema deve responder em menos de 2 segundos.”

### ✔️ **Táticas Arquiteturais**:
São soluções ou estratégias para alcançar características de qualidade.
- **Desempenho**: Usar cache, balanceamento de carga.
- **Segurança**: Implementar criptografia, autenticação.
- **Escalabilidade**: Usar microserviços, replicação.

---

## 📌 Importância das Características Arquiteturais
- Elas orientam as **decisões de arquitetura**, como escolhas de padrões e tecnologias.
- Ajudam a garantir que as **expectativas de qualidade** sejam atendidas ao longo do ciclo de vida do sistema.

## Aula 16/04 - Resumo – Fundamentos da Arquitetura de Software

## 📌 O que é Arquitetura de Software?
Arquitetura de software é a **estrutura organizacional** do sistema, definindo como os componentes interagem e quais decisões importantes são tomadas sobre a construção e evolução do sistema.

---

## 🧩 Objetivos da Arquitetura de Software
- Atender aos **requisitos** do sistema, equilibrando qualidades como desempenho, segurança e escalabilidade.
- **Facilitar mudanças** no sistema, garantindo que ele seja flexível e sustentável.
- **Gerenciar complexidade**, criando soluções que mantenham a clareza e o controle sobre as partes do sistema.

---

## 🛠️ Funções da Arquitetura de Software
1. **Documentação**: A arquitetura deve ser documentada para guiar a equipe de desenvolvimento.
2. **Decisões de Design**: Define como os componentes principais interagem.
3. **Avaliação**: A arquitetura serve para avaliar como o sistema pode evoluir, levando em consideração as qualidades não funcionais.

---

## 🧠 Importância da Arquitetura
- A arquitetura afeta diretamente **custo**, **desempenho**, **segurança**, **manutenção** e **escalabilidade**.
- Influi na **comunicação entre equipes** e pode afetar o **tempo de entrega** do projeto.

---

## 🔄 Processo Arquitetural
- **Definir requisitos**: Estabelecer as necessidades do sistema (funcionais e não funcionais).
- **Desenhar a arquitetura**: Escolher estilos e padrões que atendem aos requisitos.
- **Avaliar a arquitetura**: Verificar se ela atende aos objetivos através de métodos como o **ATAM** (Architecture Tradeoff Analysis Method).

---

## ⚙️ Estilos Arquiteturais
- **Camadas**: Divide a arquitetura em camadas de abstração.
- **Microserviços**: Divide o sistema em pequenos serviços independentes.
- **Cliente-Servidor**: Modelo tradicional de comunicação entre clientes e servidores.
