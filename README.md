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